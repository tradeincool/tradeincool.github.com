---
published: 
  - true
  - "true"
layout: article
title: Stock Level Control
abstract: Stock Level Control on Checkout in Drupal Commerce
author_twitter: jasonruyle
author: Jason Ruyle
categories: articles
---

Our company builds and manages a lot of Drupal websites.  We use both Ubercart and Commerce.  A recent project of ours required that our stock control had to be very gith.  We found that the default settings allow multiple users to purchase the same item.

Here is the scenareio:

Three people are in a group and sitting around waiting to buy a product, they know is exclusive.  They all add the item to their shopping cart and go through the checkout process.

We don't deduct the stock till someone validates their order by paying for it.

On the final submit page, they all three hit submit at the same time.  All the orders go through and stock is taken from +1 to -2.  This is not a good thing.  Especially for shops that do a lot of orders.  Having to validate and check each order, then check timestamps, is not something people want to do.

We came up with a solution by disabling the default rules configuration for stock validation on the checkout page and adding our own module with the following function.

```
<?php
/**
 * @file
 * commerce_stock_custom.module.
 */

/**
 * Implement commerce_stock_custom_commerce_checkout_complete().
 */
function commerce_stock_custom_commerce_checkout_complete($order) {
  $line_items = array();
  foreach ($order->commerce_line_items['und'] as $val) {
    if (isset($val)) {
      $line_items[] = commerce_line_item_load($val['line_item_id']);
    }
  }
  foreach ($line_items as $product) {
    if ($product->type == 'product') {
      $pid = $product->commerce_product['und'][0]['product_id'];
      db_set_active();
      $r = db_query("begin;");
      $stock = db_query('SELECT commerce_stock_value FROM {field_data_commerce_stock} WHERE entity_id=:pid FOR UPDATE', array(':pid' => $pid))->fetchField();
      if (intval($stock) > 0) {
        $stuck = intval($stock);
        db_query("UPDATE {field_data_commerce_stock} SET commerce_stock_value=:commerce_stock_value WHERE entity_id=:pid ",
          array(':pid' => $pid, ':commerce_stock_value' => $stock - 1));
        $r = db_query("commit;");
      }
      elseif (intval($stock) <= 0) {
        $p = commerce_product_load($pid);
        $r = db_query("rollback;");
        drupal_set_message('It looks like we ran out of ' . $p->title . '.  The item will need to be removed from your cart or you can wait and try again in a few minutes.', 'error');
        drupal_goto('cart');
      }
    }
  }
}
```