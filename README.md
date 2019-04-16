# MNIST_Fashion

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>mnist</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># from __future__ import absolute_import, division, print_function</span>
<span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="kn">from</span> <span class="nn">tensorflow</span> <span class="k">import</span> <span class="n">keras</span>

<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="k">import</span> <span class="n">confusion_matrix</span>
<span class="nb">print</span><span class="p">(</span><span class="n">tf</span><span class="o">.</span><span class="n">__version__</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>1.12.0
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fashion_mnist</span> <span class="o">=</span> <span class="n">keras</span><span class="o">.</span><span class="n">datasets</span><span class="o">.</span><span class="n">fashion_mnist</span>
<span class="p">(</span><span class="n">train_images</span><span class="p">,</span> <span class="n">train_labels</span><span class="p">),</span> <span class="p">(</span><span class="n">test_images</span><span class="p">,</span> <span class="n">test_labels</span><span class="p">)</span> <span class="o">=</span> <span class="n">fashion_mnist</span><span class="o">.</span><span class="n">load_data</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[121]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train_images</span><span class="o">.</span><span class="n">shape</span>
<span class="c1">#60000 examples with 28x28 NumPy arrays (each example has 28 cols and 28 rows)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[121]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(60000, 28, 28)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#an observation looks like this</span>
<span class="n">train_images</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[18]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   1,
          0,   0,  13,  73,   0,   0,   1,   4,   0,   0,   0,   0,   1,
          1,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   3,
          0,  36, 136, 127,  62,  54,   0,   0,   0,   1,   3,   4,   0,
          0,   3],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   6,
          0, 102, 204, 176, 134, 144, 123,  23,   0,   0,   0,   0,  12,
         10,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0, 155, 236, 207, 178, 107, 156, 161, 109,  64,  23,  77, 130,
         72,  15],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   1,   0,
         69, 207, 223, 218, 216, 216, 163, 127, 121, 122, 146, 141,  88,
        172,  66],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   1,   1,   1,   0,
        200, 232, 232, 233, 229, 223, 223, 215, 213, 164, 127, 123, 196,
        229,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
        183, 225, 216, 223, 228, 235, 227, 224, 222, 224, 221, 223, 245,
        173,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
        193, 228, 218, 213, 198, 180, 212, 210, 211, 213, 223, 220, 243,
        202,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   1,   3,   0,  12,
        219, 220, 212, 218, 192, 169, 227, 208, 218, 224, 212, 226, 197,
        209,  52],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   6,   0,  99,
        244, 222, 220, 218, 203, 198, 221, 215, 213, 222, 220, 245, 119,
        167,  56],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   4,   0,   0,  55,
        236, 228, 230, 228, 240, 232, 213, 218, 223, 234, 217, 217, 209,
         92,   0],
       [  0,   0,   1,   4,   6,   7,   2,   0,   0,   0,   0,   0, 237,
        226, 217, 223, 222, 219, 222, 221, 216, 223, 229, 215, 218, 255,
         77,   0],
       [  0,   3,   0,   0,   0,   0,   0,   0,   0,  62, 145, 204, 228,
        207, 213, 221, 218, 208, 211, 218, 224, 223, 219, 215, 224, 244,
        159,   0],
       [  0,   0,   0,   0,  18,  44,  82, 107, 189, 228, 220, 222, 217,
        226, 200, 205, 211, 230, 224, 234, 176, 188, 250, 248, 233, 238,
        215,   0],
       [  0,  57, 187, 208, 224, 221, 224, 208, 204, 214, 208, 209, 200,
        159, 245, 193, 206, 223, 255, 255, 221, 234, 221, 211, 220, 232,
        246,   0],
       [  3, 202, 228, 224, 221, 211, 211, 214, 205, 205, 205, 220, 240,
         80, 150, 255, 229, 221, 188, 154, 191, 210, 204, 209, 222, 228,
        225,   0],
       [ 98, 233, 198, 210, 222, 229, 229, 234, 249, 220, 194, 215, 217,
        241,  65,  73, 106, 117, 168, 219, 221, 215, 217, 223, 223, 224,
        229,  29],
       [ 75, 204, 212, 204, 193, 205, 211, 225, 216, 185, 197, 206, 198,
        213, 240, 195, 227, 245, 239, 223, 218, 212, 209, 222, 220, 221,
        230,  67],
       [ 48, 203, 183, 194, 213, 197, 185, 190, 194, 192, 202, 214, 219,
        221, 220, 236, 225, 216, 199, 206, 186, 181, 177, 172, 181, 205,
        206, 115],
       [  0, 122, 219, 193, 179, 171, 183, 196, 204, 210, 213, 207, 211,
        210, 200, 196, 194, 191, 195, 191, 198, 192, 176, 156, 167, 177,
        210,  92],
       [  0,   0,  74, 189, 212, 191, 175, 172, 175, 181, 185, 188, 189,
        188, 193, 198, 204, 209, 210, 210, 211, 188, 188, 194, 192, 216,
        170,   0],
       [  2,   0,   0,   0,  66, 200, 222, 237, 239, 242, 246, 243, 244,
        221, 220, 193, 191, 179, 182, 182, 181, 176, 166, 168,  99,  58,
          0,   0],
       [  0,   0,   0,   0,   0,   0,   0,  40,  61,  44,  72,  41,  35,
          0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0],
       [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
          0,   0]], dtype=uint8)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train_labels</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[19]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>9</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#6000 counts for each number from 0-9</span>
<span class="n">np</span><span class="o">.</span><span class="n">bincount</span><span class="p">(</span><span class="n">train_labels</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[20]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([6000, 6000, 6000, 6000, 6000, 6000, 6000, 6000, 6000, 6000])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">class_names</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;T-shirt/top&#39;</span><span class="p">,</span> <span class="s1">&#39;Trouser&#39;</span><span class="p">,</span> <span class="s1">&#39;Pullover&#39;</span><span class="p">,</span> <span class="s1">&#39;Dress&#39;</span><span class="p">,</span> <span class="s1">&#39;Coat&#39;</span><span class="p">,</span> 
               <span class="s1">&#39;Sandal&#39;</span><span class="p">,</span> <span class="s1">&#39;Shirt&#39;</span><span class="p">,</span> <span class="s1">&#39;Sneaker&#39;</span><span class="p">,</span> <span class="s1">&#39;Bag&#39;</span><span class="p">,</span> <span class="s1">&#39;Ankle boot&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">train_images</span><span class="p">[</span><span class="mi">12</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">colorbar</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">False</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[7]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;function matplotlib.pyplot.show(*args, **kw)&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#scaling image</span>
<span class="n">train_image</span> <span class="o">=</span> <span class="n">train_images</span> <span class="o">/</span> <span class="mf">255.0</span>
<span class="n">test_image</span> <span class="o">=</span> <span class="n">test_images</span> <span class="o">/</span> <span class="mf">255.0</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#quick look at the observations</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">10</span><span class="p">))</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">35</span><span class="p">):</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">5</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span> <span class="c1">#5x5 grid, i+1 = index position of each photo</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">([])</span> <span class="c1">#remove x ticks</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">yticks</span><span class="p">([])</span> <span class="c1">#remove y ticks</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">False</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">train_images</span><span class="p">[</span><span class="n">i</span><span class="p">],</span> <span class="n">cmap</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">cm</span><span class="o">.</span><span class="n">binary</span><span class="p">)</span> <span class="c1">#plt.cm = colormap (show image color)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="n">class_names</span><span class="p">[</span><span class="n">train_labels</span><span class="p">[</span><span class="n">i</span><span class="p">]])</span> <span class="c1">#label on x bar</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span> <span class="c1">#show image</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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4YcfXvO3uufU/VYyduzYbt9bd3U4r9MTHYLrsZKB0OMhhxwCwE033RRliy++OACrr756lD3wwAMADB48OMpGjRoFwKqrrgrAYostFve98sorANx+++1R9v777wP5QAdg5ZVXBoodL53nrLPOirKVVlqp4Wdq9TqdZVncDqHYvm+77bZxe+bMmQB8+OGHUWYHjOLrX/86AP/5z3+iTDr+zGc+E2Vql+07/Oijj4Bihwu8TjcL12NzaFSP7iZzHMdxHKej8c6Q4ziO4zgdTbfcZI1Sy9W03nrrxe1HH30UKJpvF154YQCWWmqpKJMvXDFAMsUDPPfccwC88847USZTrvWhf+973wPgF7/4RZRtt912AEycODHKdM/1XHzthszrqXdTaW63x1tSx6WQe2OzzTaLsocffhiA1VZbrdvna0V6o59a7L333nH7O9/5DgDrr79+lKmuKI6uv7nxxhvj9pNPPgkU67Tc27b+fPrTnwbgpZdeirLHH38cyF1c1pR9//33AzD//HnzNGzYsKprvfjiiwCsuOKKUfbaa68B8N3vfjfKLr300kYfr+Wp5SZ7/vnn47baSrkXIY+5lI4Azj33XKDYViqOSO5NyN/Fb37zmyjTua3rzHHalfb/yjuO4ziO4/SCplmG7IglZUnZdNNNAZg+fXqUaeaHHb1otGNlGpVo5CNrEOSjEjvTTKOchRZaKMq0bQMKzz//fKAYlPmPf/yj6hn0bO1syaik3rM0+qyTJ08GYNq0aVEmi98Pf/jDKJMOr7322igbKOtGilrvODUa11+7r9Y5Pvjgg7itkbfV2fjx4wF45JFHomzu3LlAXia7Ond/ct1118VtzVixll09m31eWXWspUe6UhCutUKoTttZT4sssghQnBQhK7J9B8sttxxQnIBx6623ArDFFls08ogtTcpirbby6aefjvs++clPAsX2TlY4q1dZkGTlg7wttXr99re/XXUv84LF3HGEl2bHcRzHcToa7ww5juM4jtPRNM1NljLf28DFO++8E8jzi0Bu8rUm9Uo3hN1WcjVrvtU5Um46GxSoc9gkY8svvzwA11xzTZRdffXVAOy00041n63VqBVYaWWVOUEsf/nLX+L2JptsAsAtt9wSZQqeXGaZZaJM+UlsYLQCfk855ZQoGzNmTANPMXCk3F6V+yB36wjrtpBLwgaUar8tdzff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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#setting layers</span>
<span class="n">model</span> <span class="o">=</span> <span class="n">keras</span><span class="o">.</span><span class="n">Sequential</span><span class="p">([</span>
    <span class="n">keras</span><span class="o">.</span><span class="n">layers</span><span class="o">.</span><span class="n">Flatten</span><span class="p">(</span><span class="n">input_shape</span><span class="o">=</span><span class="p">(</span><span class="mi">28</span><span class="p">,</span><span class="mi">28</span><span class="p">)),</span> <span class="c1">#convert 2d images to 1d images by 28*28=784 pixels</span>
    <span class="n">keras</span><span class="o">.</span><span class="n">layers</span><span class="o">.</span><span class="n">Dense</span><span class="p">(</span><span class="mi">128</span><span class="p">,</span> <span class="n">activation</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">nn</span><span class="o">.</span><span class="n">relu</span><span class="p">),</span> <span class="c1">#128 nodes</span>
    <span class="n">keras</span><span class="o">.</span><span class="n">layers</span><span class="o">.</span><span class="n">Dense</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="n">activation</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">nn</span><span class="o">.</span><span class="n">softmax</span><span class="p">)</span> <span class="c1">#10 nodes, each node contains a score that indicates the prob. that the current image belongs to one of the 10 classes</span>
<span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">compile</span><span class="p">(</span><span class="n">optimizer</span><span class="o">=</span><span class="s1">&#39;adam&#39;</span><span class="p">,</span> 
              <span class="n">loss</span><span class="o">=</span><span class="s1">&#39;sparse_categorical_crossentropy&#39;</span><span class="p">,</span>
              <span class="n">metrics</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;accuracy&#39;</span><span class="p">])</span>
<span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">train_image</span><span class="p">,</span> <span class="n">train_labels</span><span class="p">,</span> <span class="n">epochs</span><span class="o">=</span><span class="mi">5</span><span class="p">)</span> <span class="c1">#use normalized data to train</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Epoch 1/5
60000/60000 [==============================] - 5s 85us/step - loss: 0.4992 - acc: 0.8249
Epoch 2/5
60000/60000 [==============================] - 5s 80us/step - loss: 0.3747 - acc: 0.8634
Epoch 3/5
60000/60000 [==============================] - 5s 86us/step - loss: 0.3354 - acc: 0.8776
Epoch 4/5
60000/60000 [==============================] - 5s 85us/step - loss: 0.3098 - acc: 0.8858
Epoch 5/5
60000/60000 [==============================] - 5s 82us/step - loss: 0.2961 - acc: 0.8913
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt output_prompt">Out[12]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;tensorflow.python.keras.callbacks.History at 0x1a4d5c7f60&gt;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test_loss</span><span class="p">,</span> <span class="n">test_acc</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">evaluate</span><span class="p">(</span><span class="n">test_image</span><span class="p">,</span> <span class="n">test_labels</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Test accuracy:&#39;</span><span class="p">,</span> <span class="n">test_acc</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>10000/10000 [==============================] - 0s 45us/step
Test accuracy: 0.8728
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">predictions</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">predict_classes</span><span class="p">(</span><span class="n">test_images</span><span class="p">)</span>
<span class="c1">#predictions = model.predict(test_images) #this returns an array of probabilities for each example</span>
<span class="c1">#confusion_matrix(test_label, np.argmax(predictions, axis=1))</span>
<span class="c1">#np.argmax(predictions, axis=1) #returns an array of predicted classes of length 10000</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Confusion matrix in array</span>
<span class="n">confusion</span> <span class="o">=</span> <span class="n">confusion_matrix</span><span class="p">(</span><span class="n">test_labels</span><span class="p">,</span> <span class="n">predictions</span><span class="p">)</span>
<span class="n">confusion</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[15]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[870,  13,  32,  19,   4,   0,  52,   0,  10,   0],
       [  1, 978,   0,  15,   3,   0,   1,   0,   2,   0],
       [ 13,   3, 827,   4, 130,   0,  21,   0,   1,   1],
       [ 24,  37,  26, 826,  64,   1,  17,   0,   4,   1],
       [  1,   2, 127,  17, 841,   0,  10,   0,   2,   0],
       [  0,   0,   0,   0,   0, 919,   0,  30,   1,  50],
       [185,  12, 174,  21, 155,   0, 438,   0,  15,   0],
       [  0,   0,   0,   0,   0,  15,   0, 916,   2,  67],
       [  4,   0,   6,   3,   4,   3,   0,   3, 976,   1],
       [  0,   0,   0,   0,   0,   3,   1,  18,   0, 978]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Create a nice table of confusion matrix</span>
<span class="n">y_actu</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">Series</span><span class="p">(</span><span class="n">test_labels</span><span class="p">,</span> <span class="n">name</span> <span class="o">=</span> <span class="s1">&#39;Actual&#39;</span><span class="p">)</span>
<span class="n">y_pred</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">Series</span><span class="p">(</span><span class="n">predictions</span><span class="p">,</span> <span class="n">name</span> <span class="o">=</span> <span class="s1">&#39;Pred&#39;</span><span class="p">)</span>
<span class="n">df_confusion</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">crosstab</span><span class="p">(</span><span class="n">y_actu</span><span class="p">,</span> <span class="n">y_pred</span><span class="p">,</span> <span class="n">margins</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df_confusion</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[16]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>Pred</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
      <th>8</th>
      <th>9</th>
      <th>All</th>
    </tr>
    <tr>
      <th>Actual</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>870</td>
      <td>13</td>
      <td>32</td>
      <td>19</td>
      <td>4</td>
      <td>0</td>
      <td>52</td>
      <td>0</td>
      <td>10</td>
      <td>0</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>978</td>
      <td>0</td>
      <td>15</td>
      <td>3</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>13</td>
      <td>3</td>
      <td>827</td>
      <td>4</td>
      <td>130</td>
      <td>0</td>
      <td>21</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>24</td>
      <td>37</td>
      <td>26</td>
      <td>826</td>
      <td>64</td>
      <td>1</td>
      <td>17</td>
      <td>0</td>
      <td>4</td>
      <td>1</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>2</td>
      <td>127</td>
      <td>17</td>
      <td>841</td>
      <td>0</td>
      <td>10</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>919</td>
      <td>0</td>
      <td>30</td>
      <td>1</td>
      <td>50</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>185</td>
      <td>12</td>
      <td>174</td>
      <td>21</td>
      <td>155</td>
      <td>0</td>
      <td>438</td>
      <td>0</td>
      <td>15</td>
      <td>0</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>15</td>
      <td>0</td>
      <td>916</td>
      <td>2</td>
      <td>67</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>4</td>
      <td>0</td>
      <td>6</td>
      <td>3</td>
      <td>4</td>
      <td>3</td>
      <td>0</td>
      <td>3</td>
      <td>976</td>
      <td>1</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>18</td>
      <td>0</td>
      <td>978</td>
      <td>1000</td>
    </tr>
    <tr>
      <th>All</th>
      <td>1098</td>
      <td>1045</td>
      <td>1192</td>
      <td>905</td>
      <td>1201</td>
      <td>941</td>
      <td>540</td>
      <td>967</td>
      <td>1013</td>
      <td>1098</td>
      <td>10000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
