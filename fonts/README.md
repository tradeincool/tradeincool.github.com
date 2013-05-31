
@font-face {
  font-family : 'DINWebPro-Condensed';
  src : url( 'http://s3.feedly.com/fonts-ttf/DINWebPro-Condensed.ttf?v1' ) format( 'truetype' ),
  url( 'http://s3.feedly.com/fonts-woff/DINWebPro-Condensed.woff?v1' ) format( 'woff' );
  font-weight : normal;
  font-style : normal;
}

@font-face {
  font-family : "HelveticaNeue-Condensed";
  src : local( "Helvetica Neue Condensed Medium" ),
  local( "HelveticaNeue-Condensed Medium" ),
  url("http://s3.feedly.com/fonts-ttf/285f76f1-9aeb-40f3-8df6-f87eb061df28.ttf") format("truetype"),
  url("http://s3.feedly.com/fonts-woff/11398868-5e58-467f-86d1-650e10dd998a.woff") format("woff"),
  url("http://s3.feedly.com/fonts/95e9b167-72f4-4e05-8337-e993a249b8b5.svg#95e9b167-72f4-4e05-8337-e993a249b8b5") format("svg");
  font-weight : 500;
  font-style : normal;
}
@font-face {
  font-family : "HelveticaNeue-Condensed";
  src : local( "Helvetica Neue Condensed" ),
  local( "HelveticaNeue-Condensed" ),
  url("http://s3.feedly.com/fonts-ttf/6fddd219-58f2-42d3-99d5-5abbfcfde1a1.ttf") format("truetype"),
  url("http://s3.feedly.com/fonts-woff/c6206d3d-1ef8-44ad-96fa-c25e22252eb0.woff") format("woff"),
  url("http://s3.feedly.com/fonts/f620604b-846b-4517-95c0-aa8a60dbb16c.svg#f620604b-846b-4517-95c0-aa8a60dbb16c") format("svg");
  font-weight : 400;
  font-style : normal;
}
@font-face {
  font-family : "HelveticaNeue-Condensed";
  src : local( "Helvetica Neue Condensed Bold" ),
  local( "HelveticaNeue-Condensed Bold" ),
  url("http://s3.feedly.com/fonts-ttf/1d146b29-55e2-485b-96aa-5cb628e7e9eb.ttf?v1") format("truetype"),
  url("http://s3.feedly.com/fonts-woff/102ab74c-0e84-4fe5-a17a-b20fb643591a.woff?v1") format("woff"),
  url("http://s3.feedly.com/fonts/d90b3358-e1e2-4abb-ba96-356983a54c22.svg#d90b3358-e1e2-4abb-ba96-356983a54c22") format("svg");
  font-weight : bold;
  font-style : normal;
}
@font-face {
  font-family : "HelveticaNeue-Condensed";
  src : local( "Helvetica Neue Condensed Light" ),
  local( "HelveticaNeue-Condensed Light" ),
  url("http://s3.feedly.com/fonts-ttf/bc71ac4a-9cc7-4120-a150-788ae80b91ec.ttf") format("truetype"),
  url("http://s3.feedly.com/fonts-woff/4d888997-2061-451b-8569-6cee195e9915.woff") format("woff"),
  url("http://s3.feedly.com/fonts/3cf3e566-7fc6-488f-8058-e5eb7ac5dc23.svg#3cf3e566-7fc6-488f-8058-e5eb7ac5dc23") format("svg");
  font-weight : 300;
  font-style : normal;
}
/* Header format */
h1 {
  color : #000;
  margin : 0px;
  padding : 0px;
  text-transform : capitalize;
  font-size : 28px;
  line-height : 24px;
  font-weight : 500;
  font-family : HelveticaNeue-condensed, sans-serif;
  text-rendering : optimizeLegibility;
}
h1 a {
  color : inherit;
}
h2 {
  font-weight : normal;
  color : #B3B3B2;
  font-size : 18px;
  line-height : 24px;
  height : 24px;
  font-family : DINWebPro-Condensed, sans-serif;
}
h2 .hhint {
  opacity : 0;
  -webkit-transition-property : opacity;
  -webkit-transition-duration : 0.15s;
  -moz-transition-property : all;
  -moz-transition-duration : 0.15s;
  transition-property : all;
  transition-duration : 0.15s;
}
h2:hover .hhint {
  opacity : 1;
}
h2 a,
.h2 a {
  color : inherit;
}
