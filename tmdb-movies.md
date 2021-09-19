<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>tmdb-movies</title>

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
    body[data-notebook-name] > #header #header-container:not(.show-panel), /* body has data-notebook-name attribute when 
a notebook is open. this rule won't be applied when the notebook is not open (in 404 view for example) */
body[data-notebook-name] #menubar-container #maintoolbar:not(.show-panel),
body[data-notebook-name] #menubar-container ul.navbar-nav:not(.show-panel) {
  display: none;
}

#menubar.only-panel #menus.navbar-default {
    background: #fff;
    border-color: #fff;
}

.toolbar.with-statusbar{
    margin-top: 3px;
    margin-bottom: 0;
}

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

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Project:-tmdb-movies-Data-Analysis">Project: tmdb-movies Data Analysis<a class="anchor-link" href="#Project:-tmdb-movies-Data-Analysis">&#182;</a></h1><h2 id="Table-of-Contents">Table of Contents<a class="anchor-link" href="#Table-of-Contents">&#182;</a></h2><ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#wrangling">Data Wrangling</a></li>
<li><a href="#eda">Exploratory Data Analysis</a></li>
<li><a href="#conclusions">Conclusions</a></li>
</ul>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='intro'></a></p>
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><h3 id="Dataset-Description">Dataset Description<a class="anchor-link" href="#Dataset-Description">&#182;</a></h3><p>In this project, I will analysis the data associated with number of different movies over the years.</p>
<h3 id="Question(s)-for-Analysis">Question(s) for Analysis<a class="anchor-link" href="#Question(s)-for-Analysis">&#182;</a></h3><p>I will try to find the common properties between high revenue movies and what is the difference between them and low revenue movies!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="import-statements">import statements<a class="anchor-link" href="#import-statements">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="o">%</span> <span class="n">matplotlib</span> <span class="n">inline</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='wrangling'></a></p>
<h2 id="Data-Wrangling">Data Wrangling<a class="anchor-link" href="#Data-Wrangling">&#182;</a></h2><h3 id="General-Properties">General Properties<a class="anchor-link" href="#General-Properties">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Loading-the-data:">Loading the data:<a class="anchor-link" href="#Loading-the-data:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">&quot;tmdb-movies.csv&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Discover-the-dimensions-of-the-dataset:">Discover the dimensions of the dataset:<a class="anchor-link" href="#Discover-the-dimensions-of-the-dataset:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[3]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(10866, 21)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>It's so big dataset enough to train strong models</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Discover-the-first-rows-in-the-dataset:">Discover the first rows in the dataset:<a class="anchor-link" href="#Discover-the-first-rows-in-the-dataset:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[4]:</div>



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
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>homepage</th>
      <th>director</th>
      <th>tagline</th>
      <th>...</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Chris Pratt|Bryce Dallas Howard|Irrfan Khan|Vi...</td>
      <td>http://www.jurassicworld.com/</td>
      <td>Colin Trevorrow</td>
      <td>The park is open.</td>
      <td>...</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>Action|Adventure|Science Fiction|Thriller</td>
      <td>Universal Studios|Amblin Entertainment|Legenda...</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Tom Hardy|Charlize Theron|Hugh Keays-Byrne|Nic...</td>
      <td>http://www.madmaxmovie.com/</td>
      <td>George Miller</td>
      <td>What a Lovely Day.</td>
      <td>...</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>Action|Adventure|Science Fiction|Thriller</td>
      <td>Village Roadshow Pictures|Kennedy Miller Produ...</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>262500</td>
      <td>tt2908446</td>
      <td>13.112507</td>
      <td>110000000</td>
      <td>295238201</td>
      <td>Insurgent</td>
      <td>Shailene Woodley|Theo James|Kate Winslet|Ansel...</td>
      <td>http://www.thedivergentseries.movie/#insurgent</td>
      <td>Robert Schwentke</td>
      <td>One Choice Can Destroy You</td>
      <td>...</td>
      <td>Beatrice Prior must confront her inner demons ...</td>
      <td>119</td>
      <td>Adventure|Science Fiction|Thriller</td>
      <td>Summit Entertainment|Mandeville Films|Red Wago...</td>
      <td>3/18/15</td>
      <td>2480</td>
      <td>6.3</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>2.716190e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>140607</td>
      <td>tt2488496</td>
      <td>11.173104</td>
      <td>200000000</td>
      <td>2068178225</td>
      <td>Star Wars: The Force Awakens</td>
      <td>Harrison Ford|Mark Hamill|Carrie Fisher|Adam D...</td>
      <td>http://www.starwars.com/films/star-wars-episod...</td>
      <td>J.J. Abrams</td>
      <td>Every generation has a story.</td>
      <td>...</td>
      <td>Thirty years after defeating the Galactic Empi...</td>
      <td>136</td>
      <td>Action|Adventure|Science Fiction|Fantasy</td>
      <td>Lucasfilm|Truenorth Productions|Bad Robot</td>
      <td>12/15/15</td>
      <td>5292</td>
      <td>7.5</td>
      <td>2015</td>
      <td>1.839999e+08</td>
      <td>1.902723e+09</td>
    </tr>
    <tr>
      <th>4</th>
      <td>168259</td>
      <td>tt2820852</td>
      <td>9.335014</td>
      <td>190000000</td>
      <td>1506249360</td>
      <td>Furious 7</td>
      <td>Vin Diesel|Paul Walker|Jason Statham|Michelle ...</td>
      <td>http://www.furious7.com/</td>
      <td>James Wan</td>
      <td>Vengeance Hits Home</td>
      <td>...</td>
      <td>Deckard Shaw seeks revenge against Dominic Tor...</td>
      <td>137</td>
      <td>Action|Crime|Thriller</td>
      <td>Universal Pictures|Original Film|Media Rights ...</td>
      <td>4/1/15</td>
      <td>2947</td>
      <td>7.3</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.385749e+09</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 21 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li><strong>production company, genres and cast columns</strong> contain multiple values separated by pipe so we need to separate this values into different rows.</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Discover-the-data-types-of-the-dataset-columns:">Discover the data types of the dataset columns:<a class="anchor-link" href="#Discover-the-data-types-of-the-dataset-columns:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">dtypes</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[5]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>id                        int64
imdb_id                  object
popularity              float64
budget                    int64
revenue                   int64
original_title           object
cast                     object
homepage                 object
director                 object
tagline                  object
keywords                 object
overview                 object
runtime                   int64
genres                   object
production_companies     object
release_date             object
vote_count                int64
vote_average            float64
release_year              int64
budget_adj              float64
revenue_adj             float64
dtype: object</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Find-statistics-information-about-the-dataset:">Find statistics information about the dataset:<a class="anchor-link" href="#Find-statistics-information-about-the-dataset:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[6]:</div>



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
      <th></th>
      <th>id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>10866.000000</td>
      <td>10866.000000</td>
      <td>1.086600e+04</td>
      <td>1.086600e+04</td>
      <td>10866.000000</td>
      <td>10866.000000</td>
      <td>10866.000000</td>
      <td>10866.000000</td>
      <td>1.086600e+04</td>
      <td>1.086600e+04</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>66064.177434</td>
      <td>0.646441</td>
      <td>1.462570e+07</td>
      <td>3.982332e+07</td>
      <td>102.070863</td>
      <td>217.389748</td>
      <td>5.974922</td>
      <td>2001.322658</td>
      <td>1.755104e+07</td>
      <td>5.136436e+07</td>
    </tr>
    <tr>
      <th>std</th>
      <td>92130.136561</td>
      <td>1.000185</td>
      <td>3.091321e+07</td>
      <td>1.170035e+08</td>
      <td>31.381405</td>
      <td>575.619058</td>
      <td>0.935142</td>
      <td>12.812941</td>
      <td>3.430616e+07</td>
      <td>1.446325e+08</td>
    </tr>
    <tr>
      <th>min</th>
      <td>5.000000</td>
      <td>0.000065</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>10.000000</td>
      <td>1.500000</td>
      <td>1960.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>10596.250000</td>
      <td>0.207583</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
      <td>90.000000</td>
      <td>17.000000</td>
      <td>5.400000</td>
      <td>1995.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>20669.000000</td>
      <td>0.383856</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
      <td>99.000000</td>
      <td>38.000000</td>
      <td>6.000000</td>
      <td>2006.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>75610.000000</td>
      <td>0.713817</td>
      <td>1.500000e+07</td>
      <td>2.400000e+07</td>
      <td>111.000000</td>
      <td>145.750000</td>
      <td>6.600000</td>
      <td>2011.000000</td>
      <td>2.085325e+07</td>
      <td>3.369710e+07</td>
    </tr>
    <tr>
      <th>max</th>
      <td>417859.000000</td>
      <td>32.985763</td>
      <td>4.250000e+08</td>
      <td>2.781506e+09</td>
      <td>900.000000</td>
      <td>9767.000000</td>
      <td>9.200000</td>
      <td>2015.000000</td>
      <td>4.250000e+08</td>
      <td>2.827124e+09</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="plotting-histogram-for-each-variable-in-the-data-set:">plotting histogram for each variable in the data set:<a class="anchor-link" href="#plotting-histogram-for-each-variable-in-the-data-set:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span><span class="mi">15</span><span class="p">));</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-duplicated-rows:">Check for duplicated rows:<a class="anchor-link" href="#Check-for-duplicated-rows:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">duplicated</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[8]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>1</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>so we need to remove this duplicate</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-missing-values:">Check for missing values:<a class="anchor-link" href="#Check-for-missing-values:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[9]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>id                         0
imdb_id                   10
popularity                 0
budget                     0
revenue                    0
original_title             0
cast                      76
homepage                7930
director                  44
tagline                 2824
keywords                1493
overview                   4
runtime                    0
genres                    23
production_companies    1030
release_date               0
vote_count                 0
vote_average               0
release_year               0
budget_adj                 0
revenue_adj                0
dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>we need to remove those missing values to remain the accuracy of our analysis and any future training models, but in some columns we couldn't remove the whole rows which contain nulls in order not underestimate our dataset.</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Data-Cleaning">Data Cleaning<a class="anchor-link" href="#Data-Cleaning">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="We-will-drop-the-redundant-rows-here:">We will drop the redundant rows here:<a class="anchor-link" href="#We-will-drop-the-redundant-rows-here:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">drop_duplicates</span><span class="p">(</span><span class="n">inplace</span> <span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-duplicates:">Check for duplicates:<a class="anchor-link" href="#Check-for-duplicates:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">duplicated</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[11]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><p><strong>Homepage, tagline and keywords columns</strong> have many missing values and if we drop all these rows we will lose a big part of our dataset so we will drop this column as we don't need it to answer our questions.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Dropping-these-columns:">Dropping these columns:<a class="anchor-link" href="#Dropping-these-columns:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s2">&quot;homepage&quot;</span><span class="p">,</span><span class="s2">&quot;tagline&quot;</span><span class="p">,</span><span class="s2">&quot;keywords&quot;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-dropped-columns-existance:">Check for dropped columns existance:<a class="anchor-link" href="#Check-for-dropped-columns-existance:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">columns</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[13]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index([&#39;id&#39;, &#39;imdb_id&#39;, &#39;popularity&#39;, &#39;budget&#39;, &#39;revenue&#39;, &#39;original_title&#39;,
       &#39;cast&#39;, &#39;director&#39;, &#39;overview&#39;, &#39;runtime&#39;, &#39;genres&#39;,
       &#39;production_companies&#39;, &#39;release_date&#39;, &#39;vote_count&#39;, &#39;vote_average&#39;,
       &#39;release_year&#39;, &#39;budget_adj&#39;, &#39;revenue_adj&#39;],
      dtype=&#39;object&#39;)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Drop-all-rows-which-have-missing-values:">Drop all rows which have missing values:<a class="anchor-link" href="#Drop-all-rows-which-have-missing-values:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-missing-values:">Check for missing values:<a class="anchor-link" href="#Check-for-missing-values:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[15]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>id                      0
imdb_id                 0
popularity              0
budget                  0
revenue                 0
original_title          0
cast                    0
director                0
overview                0
runtime                 0
genres                  0
production_companies    0
release_date            0
vote_count              0
vote_average            0
release_year            0
budget_adj              0
revenue_adj             0
dtype: int64</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[16]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(9770, 18)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="After-drop-missing-values-we-should-get-back-the-default-indexes:">After drop missing values we should get back the default indexes:<a class="anchor-link" href="#After-drop-missing-values-we-should-get-back-the-default-indexes:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Separate-multiple-values-in-production_companies,-genres-and-cast-columns:">Separate multiple values in production_companies, genres and cast columns:<a class="anchor-link" href="#Separate-multiple-values-in-production_companies,-genres-and-cast-columns:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#get five copies of the dataset to separate multi values in it</span>
<span class="n">df1</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df2</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df3</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df4</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
<span class="n">df5</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#separate original dataset into two datasets but with single values in those columns</span>
<span class="n">split_columns</span> <span class="o">=</span> <span class="p">[</span><span class="s2">&quot;production_companies&quot;</span><span class="p">,</span><span class="s2">&quot;cast&quot;</span><span class="p">,</span><span class="s2">&quot;genres&quot;</span><span class="p">]</span>
<span class="k">for</span> <span class="n">col</span> <span class="ow">in</span> <span class="n">split_columns</span><span class="p">:</span>
    <span class="n">df1</span><span class="p">[</span><span class="n">col</span><span class="p">]</span> <span class="o">=</span> <span class="n">df1</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span><span class="n">x</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">,</span><span class="n">maxsplit</span><span class="o">=</span><span class="mi">4</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span> <span class="k">if</span> <span class="n">x</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">)</span> <span class="o">&gt;=</span> <span class="mi">1</span> <span class="k">else</span> <span class="n">x</span><span class="p">)</span>
    <span class="n">df2</span><span class="p">[</span><span class="n">col</span><span class="p">]</span> <span class="o">=</span> <span class="n">df2</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span><span class="n">x</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">,</span><span class="n">maxsplit</span><span class="o">=</span><span class="mi">4</span><span class="p">)[</span><span class="mi">1</span><span class="p">]</span> <span class="k">if</span> <span class="n">x</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">)</span> <span class="o">&gt;=</span> <span class="mi">1</span> <span class="k">else</span> <span class="kc">None</span><span class="p">)</span>
    <span class="n">df3</span><span class="p">[</span><span class="n">col</span><span class="p">]</span> <span class="o">=</span> <span class="n">df3</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span><span class="n">x</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">,</span><span class="n">maxsplit</span><span class="o">=</span><span class="mi">4</span><span class="p">)[</span><span class="mi">2</span><span class="p">]</span> <span class="k">if</span> <span class="n">x</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">)</span> <span class="o">&gt;=</span> <span class="mi">2</span> <span class="k">else</span> <span class="kc">None</span><span class="p">)</span>
    <span class="n">df4</span><span class="p">[</span><span class="n">col</span><span class="p">]</span> <span class="o">=</span> <span class="n">df4</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span><span class="n">x</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">,</span><span class="n">maxsplit</span><span class="o">=</span><span class="mi">4</span><span class="p">)[</span><span class="mi">3</span><span class="p">]</span> <span class="k">if</span> <span class="n">x</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">)</span> <span class="o">&gt;=</span> <span class="mi">3</span> <span class="k">else</span> <span class="kc">None</span><span class="p">)</span>
    <span class="n">df5</span><span class="p">[</span><span class="n">col</span><span class="p">]</span> <span class="o">=</span> <span class="n">df5</span><span class="p">[</span><span class="n">col</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span><span class="n">x</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">,</span><span class="n">maxsplit</span><span class="o">=</span><span class="mi">4</span><span class="p">)[</span><span class="mi">4</span><span class="p">]</span> <span class="k">if</span> <span class="n">x</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">)</span> <span class="o">&gt;=</span> <span class="mi">4</span> <span class="k">else</span> <span class="kc">None</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-the-separation-in-the-five-dataset:">Check for the separation in the five dataset:<a class="anchor-link" href="#Check-for-the-separation-in-the-five-dataset:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[20]:</div>



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
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>director</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Chris Pratt</td>
      <td>Colin Trevorrow</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>Action</td>
      <td>Universal Studios</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Tom Hardy</td>
      <td>George Miller</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>Action</td>
      <td>Village Roadshow Pictures</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>262500</td>
      <td>tt2908446</td>
      <td>13.112507</td>
      <td>110000000</td>
      <td>295238201</td>
      <td>Insurgent</td>
      <td>Shailene Woodley</td>
      <td>Robert Schwentke</td>
      <td>Beatrice Prior must confront her inner demons ...</td>
      <td>119</td>
      <td>Adventure</td>
      <td>Summit Entertainment</td>
      <td>3/18/15</td>
      <td>2480</td>
      <td>6.3</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>2.716190e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>140607</td>
      <td>tt2488496</td>
      <td>11.173104</td>
      <td>200000000</td>
      <td>2068178225</td>
      <td>Star Wars: The Force Awakens</td>
      <td>Harrison Ford</td>
      <td>J.J. Abrams</td>
      <td>Thirty years after defeating the Galactic Empi...</td>
      <td>136</td>
      <td>Action</td>
      <td>Lucasfilm</td>
      <td>12/15/15</td>
      <td>5292</td>
      <td>7.5</td>
      <td>2015</td>
      <td>1.839999e+08</td>
      <td>1.902723e+09</td>
    </tr>
    <tr>
      <th>4</th>
      <td>168259</td>
      <td>tt2820852</td>
      <td>9.335014</td>
      <td>190000000</td>
      <td>1506249360</td>
      <td>Furious 7</td>
      <td>Vin Diesel</td>
      <td>James Wan</td>
      <td>Deckard Shaw seeks revenge against Dominic Tor...</td>
      <td>137</td>
      <td>Action</td>
      <td>Universal Pictures</td>
      <td>4/1/15</td>
      <td>2947</td>
      <td>7.3</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.385749e+09</td>
    </tr>
    <tr>
      <th>5</th>
      <td>281957</td>
      <td>tt1663202</td>
      <td>9.110700</td>
      <td>135000000</td>
      <td>532950503</td>
      <td>The Revenant</td>
      <td>Leonardo DiCaprio</td>
      <td>Alejandro GonzÃ¡lez IÃ±Ã¡rritu</td>
      <td>In the 1820s, a frontiersman, Hugh Glass, sets...</td>
      <td>156</td>
      <td>Western</td>
      <td>Regency Enterprises</td>
      <td>12/25/15</td>
      <td>3929</td>
      <td>7.2</td>
      <td>2015</td>
      <td>1.241999e+08</td>
      <td>4.903142e+08</td>
    </tr>
    <tr>
      <th>6</th>
      <td>87101</td>
      <td>tt1340138</td>
      <td>8.654359</td>
      <td>155000000</td>
      <td>440603537</td>
      <td>Terminator Genisys</td>
      <td>Arnold Schwarzenegger</td>
      <td>Alan Taylor</td>
      <td>The year is 2029. John Connor, leader of the r...</td>
      <td>125</td>
      <td>Science Fiction</td>
      <td>Paramount Pictures</td>
      <td>6/23/15</td>
      <td>2598</td>
      <td>5.8</td>
      <td>2015</td>
      <td>1.425999e+08</td>
      <td>4.053551e+08</td>
    </tr>
    <tr>
      <th>7</th>
      <td>286217</td>
      <td>tt3659388</td>
      <td>7.667400</td>
      <td>108000000</td>
      <td>595380321</td>
      <td>The Martian</td>
      <td>Matt Damon</td>
      <td>Ridley Scott</td>
      <td>During a manned mission to Mars, Astronaut Mar...</td>
      <td>141</td>
      <td>Drama</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>9/30/15</td>
      <td>4572</td>
      <td>7.6</td>
      <td>2015</td>
      <td>9.935996e+07</td>
      <td>5.477497e+08</td>
    </tr>
    <tr>
      <th>8</th>
      <td>211672</td>
      <td>tt2293640</td>
      <td>7.404165</td>
      <td>74000000</td>
      <td>1156730962</td>
      <td>Minions</td>
      <td>Sandra Bullock</td>
      <td>Kyle Balda|Pierre Coffin</td>
      <td>Minions Stuart, Kevin and Bob are recruited by...</td>
      <td>91</td>
      <td>Family</td>
      <td>Universal Pictures</td>
      <td>6/17/15</td>
      <td>2893</td>
      <td>6.5</td>
      <td>2015</td>
      <td>6.807997e+07</td>
      <td>1.064192e+09</td>
    </tr>
    <tr>
      <th>9</th>
      <td>150540</td>
      <td>tt2096673</td>
      <td>6.326804</td>
      <td>175000000</td>
      <td>853708609</td>
      <td>Inside Out</td>
      <td>Amy Poehler</td>
      <td>Pete Docter</td>
      <td>Growing up can be a bumpy road, and it's no ex...</td>
      <td>94</td>
      <td>Comedy</td>
      <td>Walt Disney Pictures</td>
      <td>6/9/15</td>
      <td>3935</td>
      <td>8.0</td>
      <td>2015</td>
      <td>1.609999e+08</td>
      <td>7.854116e+08</td>
    </tr>
    <tr>
      <th>10</th>
      <td>206647</td>
      <td>tt2379713</td>
      <td>6.200282</td>
      <td>245000000</td>
      <td>880674609</td>
      <td>Spectre</td>
      <td>Daniel Craig</td>
      <td>Sam Mendes</td>
      <td>A cryptic message from Bondâ€™s past sends him...</td>
      <td>148</td>
      <td>Action</td>
      <td>Columbia Pictures</td>
      <td>10/26/15</td>
      <td>3254</td>
      <td>6.2</td>
      <td>2015</td>
      <td>2.253999e+08</td>
      <td>8.102203e+08</td>
    </tr>
    <tr>
      <th>11</th>
      <td>76757</td>
      <td>tt1617661</td>
      <td>6.189369</td>
      <td>176000003</td>
      <td>183987723</td>
      <td>Jupiter Ascending</td>
      <td>Mila Kunis</td>
      <td>Lana Wachowski|Lilly Wachowski</td>
      <td>In a universe where human genetic material is ...</td>
      <td>124</td>
      <td>Science Fiction</td>
      <td>Village Roadshow Pictures</td>
      <td>2/4/15</td>
      <td>1937</td>
      <td>5.2</td>
      <td>2015</td>
      <td>1.619199e+08</td>
      <td>1.692686e+08</td>
    </tr>
    <tr>
      <th>12</th>
      <td>264660</td>
      <td>tt0470752</td>
      <td>6.118847</td>
      <td>15000000</td>
      <td>36869414</td>
      <td>Ex Machina</td>
      <td>Domhnall Gleeson</td>
      <td>Alex Garland</td>
      <td>Caleb, a 26 year old coder at the world's larg...</td>
      <td>108</td>
      <td>Drama</td>
      <td>DNA Films</td>
      <td>1/21/15</td>
      <td>2854</td>
      <td>7.6</td>
      <td>2015</td>
      <td>1.379999e+07</td>
      <td>3.391985e+07</td>
    </tr>
    <tr>
      <th>13</th>
      <td>257344</td>
      <td>tt2120120</td>
      <td>5.984995</td>
      <td>88000000</td>
      <td>243637091</td>
      <td>Pixels</td>
      <td>Adam Sandler</td>
      <td>Chris Columbus</td>
      <td>Video game experts are recruited by the milita...</td>
      <td>105</td>
      <td>Action</td>
      <td>Columbia Pictures</td>
      <td>7/16/15</td>
      <td>1575</td>
      <td>5.8</td>
      <td>2015</td>
      <td>8.095996e+07</td>
      <td>2.241460e+08</td>
    </tr>
    <tr>
      <th>14</th>
      <td>99861</td>
      <td>tt2395427</td>
      <td>5.944927</td>
      <td>280000000</td>
      <td>1405035767</td>
      <td>Avengers: Age of Ultron</td>
      <td>Robert Downey Jr.</td>
      <td>Joss Whedon</td>
      <td>When Tony Stark tries to jumpstart a dormant p...</td>
      <td>141</td>
      <td>Action</td>
      <td>Marvel Studios</td>
      <td>4/22/15</td>
      <td>4304</td>
      <td>7.4</td>
      <td>2015</td>
      <td>2.575999e+08</td>
      <td>1.292632e+09</td>
    </tr>
    <tr>
      <th>15</th>
      <td>273248</td>
      <td>tt3460252</td>
      <td>5.898400</td>
      <td>44000000</td>
      <td>155760117</td>
      <td>The Hateful Eight</td>
      <td>Samuel L. Jackson</td>
      <td>Quentin Tarantino</td>
      <td>Bounty hunters seek shelter from a raging bliz...</td>
      <td>167</td>
      <td>Crime</td>
      <td>Double Feature Films</td>
      <td>12/25/15</td>
      <td>2389</td>
      <td>7.4</td>
      <td>2015</td>
      <td>4.047998e+07</td>
      <td>1.432992e+08</td>
    </tr>
    <tr>
      <th>16</th>
      <td>260346</td>
      <td>tt2446042</td>
      <td>5.749758</td>
      <td>48000000</td>
      <td>325771424</td>
      <td>Taken 3</td>
      <td>Liam Neeson</td>
      <td>Olivier Megaton</td>
      <td>Ex-government operative Bryan Mills finds his ...</td>
      <td>109</td>
      <td>Crime</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>1/1/15</td>
      <td>1578</td>
      <td>6.1</td>
      <td>2015</td>
      <td>4.415998e+07</td>
      <td>2.997096e+08</td>
    </tr>
    <tr>
      <th>17</th>
      <td>102899</td>
      <td>tt0478970</td>
      <td>5.573184</td>
      <td>130000000</td>
      <td>518602163</td>
      <td>Ant-Man</td>
      <td>Paul Rudd</td>
      <td>Peyton Reed</td>
      <td>Armed with the astonishing ability to shrink i...</td>
      <td>115</td>
      <td>Science Fiction</td>
      <td>Marvel Studios</td>
      <td>7/14/15</td>
      <td>3779</td>
      <td>7.0</td>
      <td>2015</td>
      <td>1.195999e+08</td>
      <td>4.771138e+08</td>
    </tr>
    <tr>
      <th>18</th>
      <td>150689</td>
      <td>tt1661199</td>
      <td>5.556818</td>
      <td>95000000</td>
      <td>542351353</td>
      <td>Cinderella</td>
      <td>Lily James</td>
      <td>Kenneth Branagh</td>
      <td>When her father unexpectedly passes away, youn...</td>
      <td>112</td>
      <td>Romance</td>
      <td>Walt Disney Pictures</td>
      <td>3/12/15</td>
      <td>1495</td>
      <td>6.8</td>
      <td>2015</td>
      <td>8.739996e+07</td>
      <td>4.989630e+08</td>
    </tr>
    <tr>
      <th>19</th>
      <td>131634</td>
      <td>tt1951266</td>
      <td>5.476958</td>
      <td>160000000</td>
      <td>650523427</td>
      <td>The Hunger Games: Mockingjay - Part 2</td>
      <td>Jennifer Lawrence</td>
      <td>Francis Lawrence</td>
      <td>With the nation of Panem in a full scale war, ...</td>
      <td>136</td>
      <td>War</td>
      <td>Studio Babelsberg</td>
      <td>11/18/15</td>
      <td>2380</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.471999e+08</td>
      <td>5.984813e+08</td>
    </tr>
    <tr>
      <th>20</th>
      <td>158852</td>
      <td>tt1964418</td>
      <td>5.462138</td>
      <td>190000000</td>
      <td>209035668</td>
      <td>Tomorrowland</td>
      <td>Britt Robertson</td>
      <td>Brad Bird</td>
      <td>Bound by a shared destiny, a bright, optimisti...</td>
      <td>130</td>
      <td>Action</td>
      <td>Walt Disney Pictures</td>
      <td>5/19/15</td>
      <td>1899</td>
      <td>6.2</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.923127e+08</td>
    </tr>
    <tr>
      <th>21</th>
      <td>307081</td>
      <td>tt1798684</td>
      <td>5.337064</td>
      <td>30000000</td>
      <td>91709827</td>
      <td>Southpaw</td>
      <td>Jake Gyllenhaal</td>
      <td>Antoine Fuqua</td>
      <td>Billy "The Great" Hope, the reigning junior mi...</td>
      <td>123</td>
      <td>Action</td>
      <td>Escape Artists</td>
      <td>6/15/15</td>
      <td>1386</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.759999e+07</td>
      <td>8.437300e+07</td>
    </tr>
    <tr>
      <th>22</th>
      <td>254128</td>
      <td>tt2126355</td>
      <td>4.907832</td>
      <td>110000000</td>
      <td>470490832</td>
      <td>San Andreas</td>
      <td>Dwayne Johnson</td>
      <td>Brad Peyton</td>
      <td>In the aftermath of a massive earthquake in Ca...</td>
      <td>114</td>
      <td>Action</td>
      <td>New Line Cinema</td>
      <td>5/27/15</td>
      <td>2060</td>
      <td>6.1</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>4.328514e+08</td>
    </tr>
    <tr>
      <th>23</th>
      <td>216015</td>
      <td>tt2322441</td>
      <td>4.710402</td>
      <td>40000000</td>
      <td>569651467</td>
      <td>Fifty Shades of Grey</td>
      <td>Dakota Johnson</td>
      <td>Sam Taylor-Johnson</td>
      <td>When college senior Anastasia Steele steps in ...</td>
      <td>125</td>
      <td>Drama</td>
      <td>Focus Features</td>
      <td>2/11/15</td>
      <td>1865</td>
      <td>5.3</td>
      <td>2015</td>
      <td>3.679998e+07</td>
      <td>5.240791e+08</td>
    </tr>
    <tr>
      <th>24</th>
      <td>318846</td>
      <td>tt1596363</td>
      <td>4.648046</td>
      <td>28000000</td>
      <td>133346506</td>
      <td>The Big Short</td>
      <td>Christian Bale</td>
      <td>Adam McKay</td>
      <td>The men who made millions from a global econom...</td>
      <td>130</td>
      <td>Comedy</td>
      <td>Paramount Pictures</td>
      <td>12/11/15</td>
      <td>1545</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.575999e+07</td>
      <td>1.226787e+08</td>
    </tr>
    <tr>
      <th>25</th>
      <td>177677</td>
      <td>tt2381249</td>
      <td>4.566713</td>
      <td>150000000</td>
      <td>682330139</td>
      <td>Mission: Impossible - Rogue Nation</td>
      <td>Tom Cruise</td>
      <td>Christopher McQuarrie</td>
      <td>Ethan and team take on their most impossible m...</td>
      <td>131</td>
      <td>Action</td>
      <td>Paramount Pictures</td>
      <td>7/23/15</td>
      <td>2349</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>6.277435e+08</td>
    </tr>
    <tr>
      <th>26</th>
      <td>214756</td>
      <td>tt2637276</td>
      <td>4.564549</td>
      <td>68000000</td>
      <td>215863606</td>
      <td>Ted 2</td>
      <td>Mark Wahlberg</td>
      <td>Seth MacFarlane</td>
      <td>Newlywed couple Ted and Tami-Lynn want to have...</td>
      <td>115</td>
      <td>Comedy</td>
      <td>Universal Pictures</td>
      <td>6/25/15</td>
      <td>1666</td>
      <td>6.3</td>
      <td>2015</td>
      <td>6.255997e+07</td>
      <td>1.985944e+08</td>
    </tr>
    <tr>
      <th>27</th>
      <td>207703</td>
      <td>tt2802144</td>
      <td>4.503789</td>
      <td>81000000</td>
      <td>403802136</td>
      <td>Kingsman: The Secret Service</td>
      <td>Taron Egerton</td>
      <td>Matthew Vaughn</td>
      <td>The story of a super-secret spy organization t...</td>
      <td>130</td>
      <td>Crime</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>1/24/15</td>
      <td>3833</td>
      <td>7.6</td>
      <td>2015</td>
      <td>7.451997e+07</td>
      <td>3.714978e+08</td>
    </tr>
    <tr>
      <th>28</th>
      <td>314365</td>
      <td>tt1895587</td>
      <td>4.062293</td>
      <td>20000000</td>
      <td>88346473</td>
      <td>Spotlight</td>
      <td>Mark Ruffalo</td>
      <td>Tom McCarthy</td>
      <td>The true story of how The Boston Globe uncover...</td>
      <td>128</td>
      <td>Drama</td>
      <td>Participant Media</td>
      <td>11/6/15</td>
      <td>1559</td>
      <td>7.8</td>
      <td>2015</td>
      <td>1.839999e+07</td>
      <td>8.127872e+07</td>
    </tr>
    <tr>
      <th>29</th>
      <td>294254</td>
      <td>tt4046784</td>
      <td>3.968891</td>
      <td>61000000</td>
      <td>311256926</td>
      <td>Maze Runner: The Scorch Trials</td>
      <td>Dylan O'Brien</td>
      <td>Wes Ball</td>
      <td>Thomas and his fellow Gladers face their great...</td>
      <td>132</td>
      <td>Action</td>
      <td>Gotham Group</td>
      <td>9/9/15</td>
      <td>1849</td>
      <td>6.4</td>
      <td>2015</td>
      <td>5.611998e+07</td>
      <td>2.863562e+08</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9740</th>
      <td>12639</td>
      <td>tt0060897</td>
      <td>0.310688</td>
      <td>0</td>
      <td>0</td>
      <td>Return of the Seven</td>
      <td>Yul Brynner</td>
      <td>Burt Kennedy</td>
      <td>Chico one of the remaining members of The Magn...</td>
      <td>95</td>
      <td>Action</td>
      <td>C.B. Films S.A.</td>
      <td>10/19/66</td>
      <td>14</td>
      <td>5.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9741</th>
      <td>5923</td>
      <td>tt0060934</td>
      <td>0.299911</td>
      <td>12000000</td>
      <td>20000000</td>
      <td>The Sand Pebbles</td>
      <td>Steve McQueen</td>
      <td>Robert Wise</td>
      <td>Engineer Jake Holman arrives aboard the gunboa...</td>
      <td>182</td>
      <td>Action</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>12/20/66</td>
      <td>28</td>
      <td>7.0</td>
      <td>1966</td>
      <td>8.061618e+07</td>
      <td>1.343603e+08</td>
    </tr>
    <tr>
      <th>9742</th>
      <td>38720</td>
      <td>tt0061170</td>
      <td>0.239435</td>
      <td>0</td>
      <td>0</td>
      <td>Walk Don't Run</td>
      <td>Cary Grant</td>
      <td>Charles Walters</td>
      <td>British industrialist Sir William Rutland - "B...</td>
      <td>114</td>
      <td>Comedy</td>
      <td>Columbia Pictures Corporation</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9743</th>
      <td>19728</td>
      <td>tt0060177</td>
      <td>0.291704</td>
      <td>0</td>
      <td>0</td>
      <td>The Blue Max</td>
      <td>George Peppard</td>
      <td>John Guillermin</td>
      <td>A young pilot in the German air force of 1918,...</td>
      <td>156</td>
      <td>War</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>6/21/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9744</th>
      <td>22383</td>
      <td>tt0060862</td>
      <td>0.151845</td>
      <td>0</td>
      <td>0</td>
      <td>The Professionals</td>
      <td>Burt Lancaster</td>
      <td>Richard Brooks</td>
      <td>The Professionals is a 1966 American Western f...</td>
      <td>117</td>
      <td>Action</td>
      <td>Columbia Pictures</td>
      <td>11/1/66</td>
      <td>21</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9745</th>
      <td>13353</td>
      <td>tt0060550</td>
      <td>0.276133</td>
      <td>0</td>
      <td>0</td>
      <td>It's the Great Pumpkin, Charlie Brown</td>
      <td>Christopher Shea</td>
      <td>Bill Melendez</td>
      <td>This classic "Peanuts" tale focuses on the thu...</td>
      <td>25</td>
      <td>Family</td>
      <td>Warner Bros. Home Video</td>
      <td>10/27/66</td>
      <td>49</td>
      <td>7.2</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9746</th>
      <td>34388</td>
      <td>tt0060437</td>
      <td>0.102530</td>
      <td>0</td>
      <td>0</td>
      <td>Funeral in Berlin</td>
      <td>Michael Caine</td>
      <td>Guy Hamilton</td>
      <td>Colonel Stok, a Soviet intelligence officer re...</td>
      <td>102</td>
      <td>Thriller</td>
      <td>Lowndes Productions Limited</td>
      <td>12/22/66</td>
      <td>13</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9747</th>
      <td>42701</td>
      <td>tt0062262</td>
      <td>0.264925</td>
      <td>75000</td>
      <td>0</td>
      <td>The Shooting</td>
      <td>Will Hutchins</td>
      <td>Monte Hellman</td>
      <td>A hired gun seeks to enact revenge on a group ...</td>
      <td>82</td>
      <td>Western</td>
      <td>Proteus Films</td>
      <td>10/23/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>5.038511e+05</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9748</th>
      <td>29710</td>
      <td>tt0060588</td>
      <td>0.252399</td>
      <td>0</td>
      <td>0</td>
      <td>Khartoum</td>
      <td>Charlton Heston</td>
      <td>Basil Dearden|Eliot Elisofon</td>
      <td>English General Charles George Gordon, a devou...</td>
      <td>134</td>
      <td>Adventure</td>
      <td>Julian Blaustein Productions Ltd.</td>
      <td>6/9/66</td>
      <td>12</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9749</th>
      <td>23728</td>
      <td>tt0059557</td>
      <td>0.236098</td>
      <td>0</td>
      <td>0</td>
      <td>Our Man Flint</td>
      <td>James Coburn</td>
      <td>Daniel Mann</td>
      <td>When scientists use eco-terrorism to impose th...</td>
      <td>108</td>
      <td>Adventure</td>
      <td>20th Century Fox</td>
      <td>1/16/66</td>
      <td>13</td>
      <td>5.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9750</th>
      <td>5065</td>
      <td>tt0059014</td>
      <td>0.230873</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Cowboy</td>
      <td>Sid James</td>
      <td>Gerald Thomas</td>
      <td>Stodge City is in the grip of the Rumpo Kid an...</td>
      <td>93</td>
      <td>Comedy</td>
      <td>Peter Rogers Productions</td>
      <td>3/1/66</td>
      <td>15</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9751</th>
      <td>17102</td>
      <td>tt0059127</td>
      <td>0.212716</td>
      <td>0</td>
      <td>0</td>
      <td>Dracula: Prince of Darkness</td>
      <td>Christopher Lee</td>
      <td>Terence Fisher</td>
      <td>Whilst vacationing in the Carpathian Mountain,...</td>
      <td>90</td>
      <td>Horror</td>
      <td>Seven Arts Productions</td>
      <td>1/9/66</td>
      <td>16</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9752</th>
      <td>28763</td>
      <td>tt0060548</td>
      <td>0.034555</td>
      <td>0</td>
      <td>0</td>
      <td>Island of Terror</td>
      <td>Peter Cushing</td>
      <td>Terence Fisher</td>
      <td>A small island community is overrun with creep...</td>
      <td>89</td>
      <td>Science Fiction</td>
      <td>Planet Film Productions</td>
      <td>6/20/66</td>
      <td>13</td>
      <td>5.3</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9753</th>
      <td>2161</td>
      <td>tt0060397</td>
      <td>0.207257</td>
      <td>5115000</td>
      <td>12000000</td>
      <td>Fantastic Voyage</td>
      <td>Stephen Boyd</td>
      <td>Richard Fleischer</td>
      <td>The science of miniaturization has been unlock...</td>
      <td>100</td>
      <td>Adventure</td>
      <td>Twentieth Century Fox Film Corporation</td>
      <td>8/24/66</td>
      <td>42</td>
      <td>6.7</td>
      <td>1966</td>
      <td>3.436265e+07</td>
      <td>8.061618e+07</td>
    </tr>
    <tr>
      <th>9754</th>
      <td>28270</td>
      <td>tt0060445</td>
      <td>0.206537</td>
      <td>0</td>
      <td>0</td>
      <td>Gambit</td>
      <td>Michael Caine</td>
      <td>Ronald Neame</td>
      <td>Harry Dean (Michael Caine) has a perfect plan ...</td>
      <td>109</td>
      <td>Action</td>
      <td>Universal Pictures</td>
      <td>12/16/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9755</th>
      <td>26268</td>
      <td>tt0060490</td>
      <td>0.202473</td>
      <td>0</td>
      <td>0</td>
      <td>Harper</td>
      <td>Paul Newman</td>
      <td>Jack Smight</td>
      <td>Harper is a cynical private eye in the best tr...</td>
      <td>121</td>
      <td>Action</td>
      <td>Warner Bros.</td>
      <td>2/23/66</td>
      <td>14</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9756</th>
      <td>15347</td>
      <td>tt0060182</td>
      <td>0.342791</td>
      <td>0</td>
      <td>0</td>
      <td>Born Free</td>
      <td>Virginia McKenna</td>
      <td>James Hill</td>
      <td>Born Free (1966) is an Open Road Films Ltd./Co...</td>
      <td>95</td>
      <td>Adventure</td>
      <td>High Road</td>
      <td>6/22/66</td>
      <td>15</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9757</th>
      <td>37301</td>
      <td>tt0060165</td>
      <td>0.227220</td>
      <td>0</td>
      <td>0</td>
      <td>A Big Hand for the Little Lady</td>
      <td>Henry Fonda</td>
      <td>Fielder Cook</td>
      <td>A naive traveler in Laredo gets involved in a ...</td>
      <td>95</td>
      <td>Western</td>
      <td>Eden Productions Inc.</td>
      <td>5/31/66</td>
      <td>11</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9758</th>
      <td>31602</td>
      <td>tt0060232</td>
      <td>0.146402</td>
      <td>0</td>
      <td>0</td>
      <td>The Chase</td>
      <td>Marlon Brando</td>
      <td>Arthur Penn</td>
      <td>Most everyone in town thinks that Sheriff Cald...</td>
      <td>135</td>
      <td>Thriller</td>
      <td>Horizon Pictures</td>
      <td>2/17/66</td>
      <td>17</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9759</th>
      <td>13343</td>
      <td>tt0059221</td>
      <td>0.141026</td>
      <td>700000</td>
      <td>0</td>
      <td>The Ghost &amp; Mr. Chicken</td>
      <td>Don Knotts</td>
      <td>Alan Rafkin</td>
      <td>Luther Heggs aspires to being a reporter for h...</td>
      <td>90</td>
      <td>Comedy</td>
      <td>Universal Pictures</td>
      <td>1/20/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>4.702610e+06</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9760</th>
      <td>20277</td>
      <td>tt0061135</td>
      <td>0.140934</td>
      <td>0</td>
      <td>0</td>
      <td>The Ugly Dachshund</td>
      <td>Dean Jones</td>
      <td>Norman Tokar</td>
      <td>The Garrisons (Dean Jones and Suzanne Pleshett...</td>
      <td>93</td>
      <td>Comedy</td>
      <td>Walt Disney Pictures</td>
      <td>2/16/66</td>
      <td>14</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9761</th>
      <td>5921</td>
      <td>tt0060748</td>
      <td>0.131378</td>
      <td>0</td>
      <td>0</td>
      <td>Nevada Smith</td>
      <td>Steve McQueen</td>
      <td>Henry Hathaway</td>
      <td>Nevada Smith is the young son of an Indian mot...</td>
      <td>128</td>
      <td>Action</td>
      <td>Paramount Pictures</td>
      <td>6/10/66</td>
      <td>10</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9762</th>
      <td>31918</td>
      <td>tt0060921</td>
      <td>0.317824</td>
      <td>0</td>
      <td>0</td>
      <td>The Russians Are Coming, The Russians Are Coming</td>
      <td>Carl Reiner</td>
      <td>Norman Jewison</td>
      <td>Without hostile intent, a Soviet sub runs agro...</td>
      <td>126</td>
      <td>Comedy</td>
      <td>The Mirisch Corporation</td>
      <td>5/25/66</td>
      <td>11</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9763</th>
      <td>20620</td>
      <td>tt0060955</td>
      <td>0.089072</td>
      <td>0</td>
      <td>0</td>
      <td>Seconds</td>
      <td>Rock Hudson</td>
      <td>John Frankenheimer</td>
      <td>A secret organisation offers wealthy people a ...</td>
      <td>100</td>
      <td>Mystery</td>
      <td>Gibraltar Productions</td>
      <td>10/5/66</td>
      <td>22</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9764</th>
      <td>5060</td>
      <td>tt0060214</td>
      <td>0.087034</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Screaming!</td>
      <td>Kenneth Williams</td>
      <td>Gerald Thomas</td>
      <td>The sinister Dr Watt has an evil scheme going....</td>
      <td>87</td>
      <td>Comedy</td>
      <td>Peter Rogers Productions</td>
      <td>5/20/66</td>
      <td>13</td>
      <td>7.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9765</th>
      <td>21</td>
      <td>tt0060371</td>
      <td>0.080598</td>
      <td>0</td>
      <td>0</td>
      <td>The Endless Summer</td>
      <td>Michael Hynson</td>
      <td>Bruce Brown</td>
      <td>The Endless Summer, by Bruce Brown, is one of ...</td>
      <td>95</td>
      <td>Documentary</td>
      <td>Bruce Brown Films</td>
      <td>6/15/66</td>
      <td>11</td>
      <td>7.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9766</th>
      <td>20379</td>
      <td>tt0060472</td>
      <td>0.065543</td>
      <td>0</td>
      <td>0</td>
      <td>Grand Prix</td>
      <td>James Garner</td>
      <td>John Frankenheimer</td>
      <td>Grand Prix driver Pete Aron is fired by his te...</td>
      <td>176</td>
      <td>Action</td>
      <td>Cherokee Productions</td>
      <td>12/21/66</td>
      <td>20</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9767</th>
      <td>39768</td>
      <td>tt0060161</td>
      <td>0.065141</td>
      <td>0</td>
      <td>0</td>
      <td>Beregis Avtomobilya</td>
      <td>Innokentiy Smoktunovskiy</td>
      <td>Eldar Ryazanov</td>
      <td>An insurance agent who moonlights as a carthie...</td>
      <td>94</td>
      <td>Mystery</td>
      <td>Mosfilm</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>6.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9768</th>
      <td>21449</td>
      <td>tt0061177</td>
      <td>0.064317</td>
      <td>0</td>
      <td>0</td>
      <td>What's Up, Tiger Lily?</td>
      <td>Tatsuya Mihashi</td>
      <td>Woody Allen</td>
      <td>In comic Woody Allen's film debut, he took the...</td>
      <td>80</td>
      <td>Action</td>
      <td>Benedict Pictures Corp.</td>
      <td>11/2/66</td>
      <td>22</td>
      <td>5.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9769</th>
      <td>22293</td>
      <td>tt0060666</td>
      <td>0.035919</td>
      <td>19000</td>
      <td>0</td>
      <td>Manos: The Hands of Fate</td>
      <td>Harold P. Warren</td>
      <td>Harold P. Warren</td>
      <td>A family gets lost on the road and stumbles up...</td>
      <td>74</td>
      <td>Horror</td>
      <td>Norm-Iris</td>
      <td>11/15/66</td>
      <td>15</td>
      <td>1.5</td>
      <td>1966</td>
      <td>1.276423e+05</td>
      <td>0.000000e+00</td>
    </tr>
  </tbody>
</table>
<p>9770 rows × 18 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df2</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[21]:</div>



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
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>director</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Bryce Dallas Howard</td>
      <td>Colin Trevorrow</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>Adventure</td>
      <td>Amblin Entertainment</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Charlize Theron</td>
      <td>George Miller</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>Adventure</td>
      <td>Kennedy Miller Productions</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>262500</td>
      <td>tt2908446</td>
      <td>13.112507</td>
      <td>110000000</td>
      <td>295238201</td>
      <td>Insurgent</td>
      <td>Theo James</td>
      <td>Robert Schwentke</td>
      <td>Beatrice Prior must confront her inner demons ...</td>
      <td>119</td>
      <td>Science Fiction</td>
      <td>Mandeville Films</td>
      <td>3/18/15</td>
      <td>2480</td>
      <td>6.3</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>2.716190e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>140607</td>
      <td>tt2488496</td>
      <td>11.173104</td>
      <td>200000000</td>
      <td>2068178225</td>
      <td>Star Wars: The Force Awakens</td>
      <td>Mark Hamill</td>
      <td>J.J. Abrams</td>
      <td>Thirty years after defeating the Galactic Empi...</td>
      <td>136</td>
      <td>Adventure</td>
      <td>Truenorth Productions</td>
      <td>12/15/15</td>
      <td>5292</td>
      <td>7.5</td>
      <td>2015</td>
      <td>1.839999e+08</td>
      <td>1.902723e+09</td>
    </tr>
    <tr>
      <th>4</th>
      <td>168259</td>
      <td>tt2820852</td>
      <td>9.335014</td>
      <td>190000000</td>
      <td>1506249360</td>
      <td>Furious 7</td>
      <td>Paul Walker</td>
      <td>James Wan</td>
      <td>Deckard Shaw seeks revenge against Dominic Tor...</td>
      <td>137</td>
      <td>Crime</td>
      <td>Original Film</td>
      <td>4/1/15</td>
      <td>2947</td>
      <td>7.3</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.385749e+09</td>
    </tr>
    <tr>
      <th>5</th>
      <td>281957</td>
      <td>tt1663202</td>
      <td>9.110700</td>
      <td>135000000</td>
      <td>532950503</td>
      <td>The Revenant</td>
      <td>Tom Hardy</td>
      <td>Alejandro GonzÃ¡lez IÃ±Ã¡rritu</td>
      <td>In the 1820s, a frontiersman, Hugh Glass, sets...</td>
      <td>156</td>
      <td>Drama</td>
      <td>Appian Way</td>
      <td>12/25/15</td>
      <td>3929</td>
      <td>7.2</td>
      <td>2015</td>
      <td>1.241999e+08</td>
      <td>4.903142e+08</td>
    </tr>
    <tr>
      <th>6</th>
      <td>87101</td>
      <td>tt1340138</td>
      <td>8.654359</td>
      <td>155000000</td>
      <td>440603537</td>
      <td>Terminator Genisys</td>
      <td>Jason Clarke</td>
      <td>Alan Taylor</td>
      <td>The year is 2029. John Connor, leader of the r...</td>
      <td>125</td>
      <td>Action</td>
      <td>Skydance Productions</td>
      <td>6/23/15</td>
      <td>2598</td>
      <td>5.8</td>
      <td>2015</td>
      <td>1.425999e+08</td>
      <td>4.053551e+08</td>
    </tr>
    <tr>
      <th>7</th>
      <td>286217</td>
      <td>tt3659388</td>
      <td>7.667400</td>
      <td>108000000</td>
      <td>595380321</td>
      <td>The Martian</td>
      <td>Jessica Chastain</td>
      <td>Ridley Scott</td>
      <td>During a manned mission to Mars, Astronaut Mar...</td>
      <td>141</td>
      <td>Adventure</td>
      <td>Scott Free Productions</td>
      <td>9/30/15</td>
      <td>4572</td>
      <td>7.6</td>
      <td>2015</td>
      <td>9.935996e+07</td>
      <td>5.477497e+08</td>
    </tr>
    <tr>
      <th>8</th>
      <td>211672</td>
      <td>tt2293640</td>
      <td>7.404165</td>
      <td>74000000</td>
      <td>1156730962</td>
      <td>Minions</td>
      <td>Jon Hamm</td>
      <td>Kyle Balda|Pierre Coffin</td>
      <td>Minions Stuart, Kevin and Bob are recruited by...</td>
      <td>91</td>
      <td>Animation</td>
      <td>Illumination Entertainment</td>
      <td>6/17/15</td>
      <td>2893</td>
      <td>6.5</td>
      <td>2015</td>
      <td>6.807997e+07</td>
      <td>1.064192e+09</td>
    </tr>
    <tr>
      <th>9</th>
      <td>150540</td>
      <td>tt2096673</td>
      <td>6.326804</td>
      <td>175000000</td>
      <td>853708609</td>
      <td>Inside Out</td>
      <td>Phyllis Smith</td>
      <td>Pete Docter</td>
      <td>Growing up can be a bumpy road, and it's no ex...</td>
      <td>94</td>
      <td>Animation</td>
      <td>Pixar Animation Studios</td>
      <td>6/9/15</td>
      <td>3935</td>
      <td>8.0</td>
      <td>2015</td>
      <td>1.609999e+08</td>
      <td>7.854116e+08</td>
    </tr>
    <tr>
      <th>10</th>
      <td>206647</td>
      <td>tt2379713</td>
      <td>6.200282</td>
      <td>245000000</td>
      <td>880674609</td>
      <td>Spectre</td>
      <td>Christoph Waltz</td>
      <td>Sam Mendes</td>
      <td>A cryptic message from Bondâ€™s past sends him...</td>
      <td>148</td>
      <td>Adventure</td>
      <td>Danjaq</td>
      <td>10/26/15</td>
      <td>3254</td>
      <td>6.2</td>
      <td>2015</td>
      <td>2.253999e+08</td>
      <td>8.102203e+08</td>
    </tr>
    <tr>
      <th>11</th>
      <td>76757</td>
      <td>tt1617661</td>
      <td>6.189369</td>
      <td>176000003</td>
      <td>183987723</td>
      <td>Jupiter Ascending</td>
      <td>Channing Tatum</td>
      <td>Lana Wachowski|Lilly Wachowski</td>
      <td>In a universe where human genetic material is ...</td>
      <td>124</td>
      <td>Fantasy</td>
      <td>Dune Entertainment</td>
      <td>2/4/15</td>
      <td>1937</td>
      <td>5.2</td>
      <td>2015</td>
      <td>1.619199e+08</td>
      <td>1.692686e+08</td>
    </tr>
    <tr>
      <th>12</th>
      <td>264660</td>
      <td>tt0470752</td>
      <td>6.118847</td>
      <td>15000000</td>
      <td>36869414</td>
      <td>Ex Machina</td>
      <td>Alicia Vikander</td>
      <td>Alex Garland</td>
      <td>Caleb, a 26 year old coder at the world's larg...</td>
      <td>108</td>
      <td>Science Fiction</td>
      <td>Universal Pictures International (UPI)</td>
      <td>1/21/15</td>
      <td>2854</td>
      <td>7.6</td>
      <td>2015</td>
      <td>1.379999e+07</td>
      <td>3.391985e+07</td>
    </tr>
    <tr>
      <th>13</th>
      <td>257344</td>
      <td>tt2120120</td>
      <td>5.984995</td>
      <td>88000000</td>
      <td>243637091</td>
      <td>Pixels</td>
      <td>Michelle Monaghan</td>
      <td>Chris Columbus</td>
      <td>Video game experts are recruited by the milita...</td>
      <td>105</td>
      <td>Comedy</td>
      <td>Happy Madison Productions</td>
      <td>7/16/15</td>
      <td>1575</td>
      <td>5.8</td>
      <td>2015</td>
      <td>8.095996e+07</td>
      <td>2.241460e+08</td>
    </tr>
    <tr>
      <th>14</th>
      <td>99861</td>
      <td>tt2395427</td>
      <td>5.944927</td>
      <td>280000000</td>
      <td>1405035767</td>
      <td>Avengers: Age of Ultron</td>
      <td>Chris Hemsworth</td>
      <td>Joss Whedon</td>
      <td>When Tony Stark tries to jumpstart a dormant p...</td>
      <td>141</td>
      <td>Adventure</td>
      <td>Prime Focus</td>
      <td>4/22/15</td>
      <td>4304</td>
      <td>7.4</td>
      <td>2015</td>
      <td>2.575999e+08</td>
      <td>1.292632e+09</td>
    </tr>
    <tr>
      <th>15</th>
      <td>273248</td>
      <td>tt3460252</td>
      <td>5.898400</td>
      <td>44000000</td>
      <td>155760117</td>
      <td>The Hateful Eight</td>
      <td>Kurt Russell</td>
      <td>Quentin Tarantino</td>
      <td>Bounty hunters seek shelter from a raging bliz...</td>
      <td>167</td>
      <td>Drama</td>
      <td>The Weinstein Company</td>
      <td>12/25/15</td>
      <td>2389</td>
      <td>7.4</td>
      <td>2015</td>
      <td>4.047998e+07</td>
      <td>1.432992e+08</td>
    </tr>
    <tr>
      <th>16</th>
      <td>260346</td>
      <td>tt2446042</td>
      <td>5.749758</td>
      <td>48000000</td>
      <td>325771424</td>
      <td>Taken 3</td>
      <td>Forest Whitaker</td>
      <td>Olivier Megaton</td>
      <td>Ex-government operative Bryan Mills finds his ...</td>
      <td>109</td>
      <td>Action</td>
      <td>M6 Films</td>
      <td>1/1/15</td>
      <td>1578</td>
      <td>6.1</td>
      <td>2015</td>
      <td>4.415998e+07</td>
      <td>2.997096e+08</td>
    </tr>
    <tr>
      <th>17</th>
      <td>102899</td>
      <td>tt0478970</td>
      <td>5.573184</td>
      <td>130000000</td>
      <td>518602163</td>
      <td>Ant-Man</td>
      <td>Michael Douglas</td>
      <td>Peyton Reed</td>
      <td>Armed with the astonishing ability to shrink i...</td>
      <td>115</td>
      <td>Action</td>
      <td>None</td>
      <td>7/14/15</td>
      <td>3779</td>
      <td>7.0</td>
      <td>2015</td>
      <td>1.195999e+08</td>
      <td>4.771138e+08</td>
    </tr>
    <tr>
      <th>18</th>
      <td>150689</td>
      <td>tt1661199</td>
      <td>5.556818</td>
      <td>95000000</td>
      <td>542351353</td>
      <td>Cinderella</td>
      <td>Cate Blanchett</td>
      <td>Kenneth Branagh</td>
      <td>When her father unexpectedly passes away, youn...</td>
      <td>112</td>
      <td>Fantasy</td>
      <td>Genre Films</td>
      <td>3/12/15</td>
      <td>1495</td>
      <td>6.8</td>
      <td>2015</td>
      <td>8.739996e+07</td>
      <td>4.989630e+08</td>
    </tr>
    <tr>
      <th>19</th>
      <td>131634</td>
      <td>tt1951266</td>
      <td>5.476958</td>
      <td>160000000</td>
      <td>650523427</td>
      <td>The Hunger Games: Mockingjay - Part 2</td>
      <td>Josh Hutcherson</td>
      <td>Francis Lawrence</td>
      <td>With the nation of Panem in a full scale war, ...</td>
      <td>136</td>
      <td>Adventure</td>
      <td>StudioCanal</td>
      <td>11/18/15</td>
      <td>2380</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.471999e+08</td>
      <td>5.984813e+08</td>
    </tr>
    <tr>
      <th>20</th>
      <td>158852</td>
      <td>tt1964418</td>
      <td>5.462138</td>
      <td>190000000</td>
      <td>209035668</td>
      <td>Tomorrowland</td>
      <td>George Clooney</td>
      <td>Brad Bird</td>
      <td>Bound by a shared destiny, a bright, optimisti...</td>
      <td>130</td>
      <td>Family</td>
      <td>Babieka</td>
      <td>5/19/15</td>
      <td>1899</td>
      <td>6.2</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.923127e+08</td>
    </tr>
    <tr>
      <th>21</th>
      <td>307081</td>
      <td>tt1798684</td>
      <td>5.337064</td>
      <td>30000000</td>
      <td>91709827</td>
      <td>Southpaw</td>
      <td>Rachel McAdams</td>
      <td>Antoine Fuqua</td>
      <td>Billy "The Great" Hope, the reigning junior mi...</td>
      <td>123</td>
      <td>Drama</td>
      <td>Riche-Ludwig Productions</td>
      <td>6/15/15</td>
      <td>1386</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.759999e+07</td>
      <td>8.437300e+07</td>
    </tr>
    <tr>
      <th>22</th>
      <td>254128</td>
      <td>tt2126355</td>
      <td>4.907832</td>
      <td>110000000</td>
      <td>470490832</td>
      <td>San Andreas</td>
      <td>Alexandra Daddario</td>
      <td>Brad Peyton</td>
      <td>In the aftermath of a massive earthquake in Ca...</td>
      <td>114</td>
      <td>Drama</td>
      <td>Village Roadshow Pictures</td>
      <td>5/27/15</td>
      <td>2060</td>
      <td>6.1</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>4.328514e+08</td>
    </tr>
    <tr>
      <th>23</th>
      <td>216015</td>
      <td>tt2322441</td>
      <td>4.710402</td>
      <td>40000000</td>
      <td>569651467</td>
      <td>Fifty Shades of Grey</td>
      <td>Jamie Dornan</td>
      <td>Sam Taylor-Johnson</td>
      <td>When college senior Anastasia Steele steps in ...</td>
      <td>125</td>
      <td>Romance</td>
      <td>Trigger Street Productions</td>
      <td>2/11/15</td>
      <td>1865</td>
      <td>5.3</td>
      <td>2015</td>
      <td>3.679998e+07</td>
      <td>5.240791e+08</td>
    </tr>
    <tr>
      <th>24</th>
      <td>318846</td>
      <td>tt1596363</td>
      <td>4.648046</td>
      <td>28000000</td>
      <td>133346506</td>
      <td>The Big Short</td>
      <td>Steve Carell</td>
      <td>Adam McKay</td>
      <td>The men who made millions from a global econom...</td>
      <td>130</td>
      <td>Drama</td>
      <td>Plan B Entertainment</td>
      <td>12/11/15</td>
      <td>1545</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.575999e+07</td>
      <td>1.226787e+08</td>
    </tr>
    <tr>
      <th>25</th>
      <td>177677</td>
      <td>tt2381249</td>
      <td>4.566713</td>
      <td>150000000</td>
      <td>682330139</td>
      <td>Mission: Impossible - Rogue Nation</td>
      <td>Jeremy Renner</td>
      <td>Christopher McQuarrie</td>
      <td>Ethan and team take on their most impossible m...</td>
      <td>131</td>
      <td>None</td>
      <td>Skydance Productions</td>
      <td>7/23/15</td>
      <td>2349</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>6.277435e+08</td>
    </tr>
    <tr>
      <th>26</th>
      <td>214756</td>
      <td>tt2637276</td>
      <td>4.564549</td>
      <td>68000000</td>
      <td>215863606</td>
      <td>Ted 2</td>
      <td>Seth MacFarlane</td>
      <td>Seth MacFarlane</td>
      <td>Newlywed couple Ted and Tami-Lynn want to have...</td>
      <td>115</td>
      <td>None</td>
      <td>Media Rights Capital</td>
      <td>6/25/15</td>
      <td>1666</td>
      <td>6.3</td>
      <td>2015</td>
      <td>6.255997e+07</td>
      <td>1.985944e+08</td>
    </tr>
    <tr>
      <th>27</th>
      <td>207703</td>
      <td>tt2802144</td>
      <td>4.503789</td>
      <td>81000000</td>
      <td>403802136</td>
      <td>Kingsman: The Secret Service</td>
      <td>Colin Firth</td>
      <td>Matthew Vaughn</td>
      <td>The story of a super-secret spy organization t...</td>
      <td>130</td>
      <td>Comedy</td>
      <td>Marv Films</td>
      <td>1/24/15</td>
      <td>3833</td>
      <td>7.6</td>
      <td>2015</td>
      <td>7.451997e+07</td>
      <td>3.714978e+08</td>
    </tr>
    <tr>
      <th>28</th>
      <td>314365</td>
      <td>tt1895587</td>
      <td>4.062293</td>
      <td>20000000</td>
      <td>88346473</td>
      <td>Spotlight</td>
      <td>Michael Keaton</td>
      <td>Tom McCarthy</td>
      <td>The true story of how The Boston Globe uncover...</td>
      <td>128</td>
      <td>Thriller</td>
      <td>Open Road Films</td>
      <td>11/6/15</td>
      <td>1559</td>
      <td>7.8</td>
      <td>2015</td>
      <td>1.839999e+07</td>
      <td>8.127872e+07</td>
    </tr>
    <tr>
      <th>29</th>
      <td>294254</td>
      <td>tt4046784</td>
      <td>3.968891</td>
      <td>61000000</td>
      <td>311256926</td>
      <td>Maze Runner: The Scorch Trials</td>
      <td>Kaya Scodelario</td>
      <td>Wes Ball</td>
      <td>Thomas and his fellow Gladers face their great...</td>
      <td>132</td>
      <td>Science Fiction</td>
      <td>Temple Hill Entertainment</td>
      <td>9/9/15</td>
      <td>1849</td>
      <td>6.4</td>
      <td>2015</td>
      <td>5.611998e+07</td>
      <td>2.863562e+08</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9740</th>
      <td>12639</td>
      <td>tt0060897</td>
      <td>0.310688</td>
      <td>0</td>
      <td>0</td>
      <td>Return of the Seven</td>
      <td>Robert Fuller</td>
      <td>Burt Kennedy</td>
      <td>Chico one of the remaining members of The Magn...</td>
      <td>95</td>
      <td>Western</td>
      <td>The Mirisch Production Company</td>
      <td>10/19/66</td>
      <td>14</td>
      <td>5.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9741</th>
      <td>5923</td>
      <td>tt0060934</td>
      <td>0.299911</td>
      <td>12000000</td>
      <td>20000000</td>
      <td>The Sand Pebbles</td>
      <td>Richard Attenborough</td>
      <td>Robert Wise</td>
      <td>Engineer Jake Holman arrives aboard the gunboa...</td>
      <td>182</td>
      <td>Adventure</td>
      <td>Solar Productions</td>
      <td>12/20/66</td>
      <td>28</td>
      <td>7.0</td>
      <td>1966</td>
      <td>8.061618e+07</td>
      <td>1.343603e+08</td>
    </tr>
    <tr>
      <th>9742</th>
      <td>38720</td>
      <td>tt0061170</td>
      <td>0.239435</td>
      <td>0</td>
      <td>0</td>
      <td>Walk Don't Run</td>
      <td>Samantha Eggar</td>
      <td>Charles Walters</td>
      <td>British industrialist Sir William Rutland - "B...</td>
      <td>114</td>
      <td>Romance</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9743</th>
      <td>19728</td>
      <td>tt0060177</td>
      <td>0.291704</td>
      <td>0</td>
      <td>0</td>
      <td>The Blue Max</td>
      <td>James Mason</td>
      <td>John Guillermin</td>
      <td>A young pilot in the German air force of 1918,...</td>
      <td>156</td>
      <td>Action</td>
      <td>None</td>
      <td>6/21/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9744</th>
      <td>22383</td>
      <td>tt0060862</td>
      <td>0.151845</td>
      <td>0</td>
      <td>0</td>
      <td>The Professionals</td>
      <td>Lee Marvin</td>
      <td>Richard Brooks</td>
      <td>The Professionals is a 1966 American Western f...</td>
      <td>117</td>
      <td>Adventure</td>
      <td>None</td>
      <td>11/1/66</td>
      <td>21</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9745</th>
      <td>13353</td>
      <td>tt0060550</td>
      <td>0.276133</td>
      <td>0</td>
      <td>0</td>
      <td>It's the Great Pumpkin, Charlie Brown</td>
      <td>Sally Dryer</td>
      <td>Bill Melendez</td>
      <td>This classic "Peanuts" tale focuses on the thu...</td>
      <td>25</td>
      <td>Animation</td>
      <td>None</td>
      <td>10/27/66</td>
      <td>49</td>
      <td>7.2</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9746</th>
      <td>34388</td>
      <td>tt0060437</td>
      <td>0.102530</td>
      <td>0</td>
      <td>0</td>
      <td>Funeral in Berlin</td>
      <td>Paul Hubschmid</td>
      <td>Guy Hamilton</td>
      <td>Colonel Stok, a Soviet intelligence officer re...</td>
      <td>102</td>
      <td>None</td>
      <td>None</td>
      <td>12/22/66</td>
      <td>13</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9747</th>
      <td>42701</td>
      <td>tt0062262</td>
      <td>0.264925</td>
      <td>75000</td>
      <td>0</td>
      <td>The Shooting</td>
      <td>Millie Perkins</td>
      <td>Monte Hellman</td>
      <td>A hired gun seeks to enact revenge on a group ...</td>
      <td>82</td>
      <td>None</td>
      <td>None</td>
      <td>10/23/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>5.038511e+05</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9748</th>
      <td>29710</td>
      <td>tt0060588</td>
      <td>0.252399</td>
      <td>0</td>
      <td>0</td>
      <td>Khartoum</td>
      <td>Laurence Olivier</td>
      <td>Basil Dearden|Eliot Elisofon</td>
      <td>English General Charles George Gordon, a devou...</td>
      <td>134</td>
      <td>Drama</td>
      <td>None</td>
      <td>6/9/66</td>
      <td>12</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9749</th>
      <td>23728</td>
      <td>tt0059557</td>
      <td>0.236098</td>
      <td>0</td>
      <td>0</td>
      <td>Our Man Flint</td>
      <td>Lee J. Cobb</td>
      <td>Daniel Mann</td>
      <td>When scientists use eco-terrorism to impose th...</td>
      <td>108</td>
      <td>Comedy</td>
      <td>None</td>
      <td>1/16/66</td>
      <td>13</td>
      <td>5.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9750</th>
      <td>5065</td>
      <td>tt0059014</td>
      <td>0.230873</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Cowboy</td>
      <td>Jim Dale</td>
      <td>Gerald Thomas</td>
      <td>Stodge City is in the grip of the Rumpo Kid an...</td>
      <td>93</td>
      <td>Western</td>
      <td>None</td>
      <td>3/1/66</td>
      <td>15</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9751</th>
      <td>17102</td>
      <td>tt0059127</td>
      <td>0.212716</td>
      <td>0</td>
      <td>0</td>
      <td>Dracula: Prince of Darkness</td>
      <td>Barbara Shelley</td>
      <td>Terence Fisher</td>
      <td>Whilst vacationing in the Carpathian Mountain,...</td>
      <td>90</td>
      <td>None</td>
      <td>Hammer Film Productions</td>
      <td>1/9/66</td>
      <td>16</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9752</th>
      <td>28763</td>
      <td>tt0060548</td>
      <td>0.034555</td>
      <td>0</td>
      <td>0</td>
      <td>Island of Terror</td>
      <td>Edward Judd</td>
      <td>Terence Fisher</td>
      <td>A small island community is overrun with creep...</td>
      <td>89</td>
      <td>Horror</td>
      <td>Protelco</td>
      <td>6/20/66</td>
      <td>13</td>
      <td>5.3</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9753</th>
      <td>2161</td>
      <td>tt0060397</td>
      <td>0.207257</td>
      <td>5115000</td>
      <td>12000000</td>
      <td>Fantastic Voyage</td>
      <td>Raquel Welch</td>
      <td>Richard Fleischer</td>
      <td>The science of miniaturization has been unlock...</td>
      <td>100</td>
      <td>Science Fiction</td>
      <td>None</td>
      <td>8/24/66</td>
      <td>42</td>
      <td>6.7</td>
      <td>1966</td>
      <td>3.436265e+07</td>
      <td>8.061618e+07</td>
    </tr>
    <tr>
      <th>9754</th>
      <td>28270</td>
      <td>tt0060445</td>
      <td>0.206537</td>
      <td>0</td>
      <td>0</td>
      <td>Gambit</td>
      <td>Shirley MacLaine</td>
      <td>Ronald Neame</td>
      <td>Harry Dean (Michael Caine) has a perfect plan ...</td>
      <td>109</td>
      <td>Comedy</td>
      <td>None</td>
      <td>12/16/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9755</th>
      <td>26268</td>
      <td>tt0060490</td>
      <td>0.202473</td>
      <td>0</td>
      <td>0</td>
      <td>Harper</td>
      <td>Lauren Bacall</td>
      <td>Jack Smight</td>
      <td>Harper is a cynical private eye in the best tr...</td>
      <td>121</td>
      <td>Drama</td>
      <td>None</td>
      <td>2/23/66</td>
      <td>14</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9756</th>
      <td>15347</td>
      <td>tt0060182</td>
      <td>0.342791</td>
      <td>0</td>
      <td>0</td>
      <td>Born Free</td>
      <td>Bill Travers</td>
      <td>James Hill</td>
      <td>Born Free (1966) is an Open Road Films Ltd./Co...</td>
      <td>95</td>
      <td>Drama</td>
      <td>None</td>
      <td>6/22/66</td>
      <td>15</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9757</th>
      <td>37301</td>
      <td>tt0060165</td>
      <td>0.227220</td>
      <td>0</td>
      <td>0</td>
      <td>A Big Hand for the Little Lady</td>
      <td>Joanne Woodward</td>
      <td>Fielder Cook</td>
      <td>A naive traveler in Laredo gets involved in a ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>5/31/66</td>
      <td>11</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9758</th>
      <td>31602</td>
      <td>tt0060232</td>
      <td>0.146402</td>
      <td>0</td>
      <td>0</td>
      <td>The Chase</td>
      <td>Jane Fonda</td>
      <td>Arthur Penn</td>
      <td>Most everyone in town thinks that Sheriff Cald...</td>
      <td>135</td>
      <td>Drama</td>
      <td>Columbia Pictures Corporation</td>
      <td>2/17/66</td>
      <td>17</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9759</th>
      <td>13343</td>
      <td>tt0059221</td>
      <td>0.141026</td>
      <td>700000</td>
      <td>0</td>
      <td>The Ghost &amp; Mr. Chicken</td>
      <td>Joan Staley</td>
      <td>Alan Rafkin</td>
      <td>Luther Heggs aspires to being a reporter for h...</td>
      <td>90</td>
      <td>Family</td>
      <td>None</td>
      <td>1/20/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>4.702610e+06</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9760</th>
      <td>20277</td>
      <td>tt0061135</td>
      <td>0.140934</td>
      <td>0</td>
      <td>0</td>
      <td>The Ugly Dachshund</td>
      <td>Suzanne Pleshette</td>
      <td>Norman Tokar</td>
      <td>The Garrisons (Dean Jones and Suzanne Pleshett...</td>
      <td>93</td>
      <td>Drama</td>
      <td>None</td>
      <td>2/16/66</td>
      <td>14</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9761</th>
      <td>5921</td>
      <td>tt0060748</td>
      <td>0.131378</td>
      <td>0</td>
      <td>0</td>
      <td>Nevada Smith</td>
      <td>Karl Malden</td>
      <td>Henry Hathaway</td>
      <td>Nevada Smith is the young son of an Indian mot...</td>
      <td>128</td>
      <td>Western</td>
      <td>Solar Productions</td>
      <td>6/10/66</td>
      <td>10</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9762</th>
      <td>31918</td>
      <td>tt0060921</td>
      <td>0.317824</td>
      <td>0</td>
      <td>0</td>
      <td>The Russians Are Coming, The Russians Are Coming</td>
      <td>Eva Marie Saint</td>
      <td>Norman Jewison</td>
      <td>Without hostile intent, a Soviet sub runs agro...</td>
      <td>126</td>
      <td>War</td>
      <td>None</td>
      <td>5/25/66</td>
      <td>11</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9763</th>
      <td>20620</td>
      <td>tt0060955</td>
      <td>0.089072</td>
      <td>0</td>
      <td>0</td>
      <td>Seconds</td>
      <td>Salome Jens</td>
      <td>John Frankenheimer</td>
      <td>A secret organisation offers wealthy people a ...</td>
      <td>100</td>
      <td>Science Fiction</td>
      <td>Joel Productions</td>
      <td>10/5/66</td>
      <td>22</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9764</th>
      <td>5060</td>
      <td>tt0060214</td>
      <td>0.087034</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Screaming!</td>
      <td>Jim Dale</td>
      <td>Gerald Thomas</td>
      <td>The sinister Dr Watt has an evil scheme going....</td>
      <td>87</td>
      <td>None</td>
      <td>Anglo-Amalgamated Film Distributors</td>
      <td>5/20/66</td>
      <td>13</td>
      <td>7.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9765</th>
      <td>21</td>
      <td>tt0060371</td>
      <td>0.080598</td>
      <td>0</td>
      <td>0</td>
      <td>The Endless Summer</td>
      <td>Robert August</td>
      <td>Bruce Brown</td>
      <td>The Endless Summer, by Bruce Brown, is one of ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/66</td>
      <td>11</td>
      <td>7.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9766</th>
      <td>20379</td>
      <td>tt0060472</td>
      <td>0.065543</td>
      <td>0</td>
      <td>0</td>
      <td>Grand Prix</td>
      <td>Eva Marie Saint</td>
      <td>John Frankenheimer</td>
      <td>Grand Prix driver Pete Aron is fired by his te...</td>
      <td>176</td>
      <td>Adventure</td>
      <td>Joel Productions</td>
      <td>12/21/66</td>
      <td>20</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9767</th>
      <td>39768</td>
      <td>tt0060161</td>
      <td>0.065141</td>
      <td>0</td>
      <td>0</td>
      <td>Beregis Avtomobilya</td>
      <td>Oleg Efremov</td>
      <td>Eldar Ryazanov</td>
      <td>An insurance agent who moonlights as a carthie...</td>
      <td>94</td>
      <td>Comedy</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>6.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9768</th>
      <td>21449</td>
      <td>tt0061177</td>
      <td>0.064317</td>
      <td>0</td>
      <td>0</td>
      <td>What's Up, Tiger Lily?</td>
      <td>Akiko Wakabayashi</td>
      <td>Woody Allen</td>
      <td>In comic Woody Allen's film debut, he took the...</td>
      <td>80</td>
      <td>Comedy</td>
      <td>None</td>
      <td>11/2/66</td>
      <td>22</td>
      <td>5.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9769</th>
      <td>22293</td>
      <td>tt0060666</td>
      <td>0.035919</td>
      <td>19000</td>
      <td>0</td>
      <td>Manos: The Hands of Fate</td>
      <td>Tom Neyman</td>
      <td>Harold P. Warren</td>
      <td>A family gets lost on the road and stumbles up...</td>
      <td>74</td>
      <td>None</td>
      <td>None</td>
      <td>11/15/66</td>
      <td>15</td>
      <td>1.5</td>
      <td>1966</td>
      <td>1.276423e+05</td>
      <td>0.000000e+00</td>
    </tr>
  </tbody>
</table>
<p>9770 rows × 18 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df3</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[22]:</div>



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
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>director</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Irrfan Khan</td>
      <td>Colin Trevorrow</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>Science Fiction</td>
      <td>Legendary Pictures</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Hugh Keays-Byrne</td>
      <td>George Miller</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>Science Fiction</td>
      <td>None</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>262500</td>
      <td>tt2908446</td>
      <td>13.112507</td>
      <td>110000000</td>
      <td>295238201</td>
      <td>Insurgent</td>
      <td>Kate Winslet</td>
      <td>Robert Schwentke</td>
      <td>Beatrice Prior must confront her inner demons ...</td>
      <td>119</td>
      <td>Thriller</td>
      <td>Red Wagon Entertainment</td>
      <td>3/18/15</td>
      <td>2480</td>
      <td>6.3</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>2.716190e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>140607</td>
      <td>tt2488496</td>
      <td>11.173104</td>
      <td>200000000</td>
      <td>2068178225</td>
      <td>Star Wars: The Force Awakens</td>
      <td>Carrie Fisher</td>
      <td>J.J. Abrams</td>
      <td>Thirty years after defeating the Galactic Empi...</td>
      <td>136</td>
      <td>Science Fiction</td>
      <td>Bad Robot</td>
      <td>12/15/15</td>
      <td>5292</td>
      <td>7.5</td>
      <td>2015</td>
      <td>1.839999e+08</td>
      <td>1.902723e+09</td>
    </tr>
    <tr>
      <th>4</th>
      <td>168259</td>
      <td>tt2820852</td>
      <td>9.335014</td>
      <td>190000000</td>
      <td>1506249360</td>
      <td>Furious 7</td>
      <td>Jason Statham</td>
      <td>James Wan</td>
      <td>Deckard Shaw seeks revenge against Dominic Tor...</td>
      <td>137</td>
      <td>Thriller</td>
      <td>Media Rights Capital</td>
      <td>4/1/15</td>
      <td>2947</td>
      <td>7.3</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.385749e+09</td>
    </tr>
    <tr>
      <th>5</th>
      <td>281957</td>
      <td>tt1663202</td>
      <td>9.110700</td>
      <td>135000000</td>
      <td>532950503</td>
      <td>The Revenant</td>
      <td>Will Poulter</td>
      <td>Alejandro GonzÃ¡lez IÃ±Ã¡rritu</td>
      <td>In the 1820s, a frontiersman, Hugh Glass, sets...</td>
      <td>156</td>
      <td>Adventure</td>
      <td>CatchPlay</td>
      <td>12/25/15</td>
      <td>3929</td>
      <td>7.2</td>
      <td>2015</td>
      <td>1.241999e+08</td>
      <td>4.903142e+08</td>
    </tr>
    <tr>
      <th>6</th>
      <td>87101</td>
      <td>tt1340138</td>
      <td>8.654359</td>
      <td>155000000</td>
      <td>440603537</td>
      <td>Terminator Genisys</td>
      <td>Emilia Clarke</td>
      <td>Alan Taylor</td>
      <td>The year is 2029. John Connor, leader of the r...</td>
      <td>125</td>
      <td>Thriller</td>
      <td>None</td>
      <td>6/23/15</td>
      <td>2598</td>
      <td>5.8</td>
      <td>2015</td>
      <td>1.425999e+08</td>
      <td>4.053551e+08</td>
    </tr>
    <tr>
      <th>7</th>
      <td>286217</td>
      <td>tt3659388</td>
      <td>7.667400</td>
      <td>108000000</td>
      <td>595380321</td>
      <td>The Martian</td>
      <td>Kristen Wiig</td>
      <td>Ridley Scott</td>
      <td>During a manned mission to Mars, Astronaut Mar...</td>
      <td>141</td>
      <td>Science Fiction</td>
      <td>Mid Atlantic Films</td>
      <td>9/30/15</td>
      <td>4572</td>
      <td>7.6</td>
      <td>2015</td>
      <td>9.935996e+07</td>
      <td>5.477497e+08</td>
    </tr>
    <tr>
      <th>8</th>
      <td>211672</td>
      <td>tt2293640</td>
      <td>7.404165</td>
      <td>74000000</td>
      <td>1156730962</td>
      <td>Minions</td>
      <td>Michael Keaton</td>
      <td>Kyle Balda|Pierre Coffin</td>
      <td>Minions Stuart, Kevin and Bob are recruited by...</td>
      <td>91</td>
      <td>Adventure</td>
      <td>None</td>
      <td>6/17/15</td>
      <td>2893</td>
      <td>6.5</td>
      <td>2015</td>
      <td>6.807997e+07</td>
      <td>1.064192e+09</td>
    </tr>
    <tr>
      <th>9</th>
      <td>150540</td>
      <td>tt2096673</td>
      <td>6.326804</td>
      <td>175000000</td>
      <td>853708609</td>
      <td>Inside Out</td>
      <td>Richard Kind</td>
      <td>Pete Docter</td>
      <td>Growing up can be a bumpy road, and it's no ex...</td>
      <td>94</td>
      <td>Family</td>
      <td>Walt Disney Studios Motion Pictures</td>
      <td>6/9/15</td>
      <td>3935</td>
      <td>8.0</td>
      <td>2015</td>
      <td>1.609999e+08</td>
      <td>7.854116e+08</td>
    </tr>
    <tr>
      <th>10</th>
      <td>206647</td>
      <td>tt2379713</td>
      <td>6.200282</td>
      <td>245000000</td>
      <td>880674609</td>
      <td>Spectre</td>
      <td>LÃ©a Seydoux</td>
      <td>Sam Mendes</td>
      <td>A cryptic message from Bondâ€™s past sends him...</td>
      <td>148</td>
      <td>Crime</td>
      <td>B24</td>
      <td>10/26/15</td>
      <td>3254</td>
      <td>6.2</td>
      <td>2015</td>
      <td>2.253999e+08</td>
      <td>8.102203e+08</td>
    </tr>
    <tr>
      <th>11</th>
      <td>76757</td>
      <td>tt1617661</td>
      <td>6.189369</td>
      <td>176000003</td>
      <td>183987723</td>
      <td>Jupiter Ascending</td>
      <td>Sean Bean</td>
      <td>Lana Wachowski|Lilly Wachowski</td>
      <td>In a universe where human genetic material is ...</td>
      <td>124</td>
      <td>Action</td>
      <td>Anarchos Productions</td>
      <td>2/4/15</td>
      <td>1937</td>
      <td>5.2</td>
      <td>2015</td>
      <td>1.619199e+08</td>
      <td>1.692686e+08</td>
    </tr>
    <tr>
      <th>12</th>
      <td>264660</td>
      <td>tt0470752</td>
      <td>6.118847</td>
      <td>15000000</td>
      <td>36869414</td>
      <td>Ex Machina</td>
      <td>Oscar Isaac</td>
      <td>Alex Garland</td>
      <td>Caleb, a 26 year old coder at the world's larg...</td>
      <td>108</td>
      <td>None</td>
      <td>Film4</td>
      <td>1/21/15</td>
      <td>2854</td>
      <td>7.6</td>
      <td>2015</td>
      <td>1.379999e+07</td>
      <td>3.391985e+07</td>
    </tr>
    <tr>
      <th>13</th>
      <td>257344</td>
      <td>tt2120120</td>
      <td>5.984995</td>
      <td>88000000</td>
      <td>243637091</td>
      <td>Pixels</td>
      <td>Peter Dinklage</td>
      <td>Chris Columbus</td>
      <td>Video game experts are recruited by the milita...</td>
      <td>105</td>
      <td>Science Fiction</td>
      <td>None</td>
      <td>7/16/15</td>
      <td>1575</td>
      <td>5.8</td>
      <td>2015</td>
      <td>8.095996e+07</td>
      <td>2.241460e+08</td>
    </tr>
    <tr>
      <th>14</th>
      <td>99861</td>
      <td>tt2395427</td>
      <td>5.944927</td>
      <td>280000000</td>
      <td>1405035767</td>
      <td>Avengers: Age of Ultron</td>
      <td>Mark Ruffalo</td>
      <td>Joss Whedon</td>
      <td>When Tony Stark tries to jumpstart a dormant p...</td>
      <td>141</td>
      <td>Science Fiction</td>
      <td>Revolution Sun Studios</td>
      <td>4/22/15</td>
      <td>4304</td>
      <td>7.4</td>
      <td>2015</td>
      <td>2.575999e+08</td>
      <td>1.292632e+09</td>
    </tr>
    <tr>
      <th>15</th>
      <td>273248</td>
      <td>tt3460252</td>
      <td>5.898400</td>
      <td>44000000</td>
      <td>155760117</td>
      <td>The Hateful Eight</td>
      <td>Jennifer Jason Leigh</td>
      <td>Quentin Tarantino</td>
      <td>Bounty hunters seek shelter from a raging bliz...</td>
      <td>167</td>
      <td>Mystery</td>
      <td>FilmColony</td>
      <td>12/25/15</td>
      <td>2389</td>
      <td>7.4</td>
      <td>2015</td>
      <td>4.047998e+07</td>
      <td>1.432992e+08</td>
    </tr>
    <tr>
      <th>16</th>
      <td>260346</td>
      <td>tt2446042</td>
      <td>5.749758</td>
      <td>48000000</td>
      <td>325771424</td>
      <td>Taken 3</td>
      <td>Maggie Grace</td>
      <td>Olivier Megaton</td>
      <td>Ex-government operative Bryan Mills finds his ...</td>
      <td>109</td>
      <td>Thriller</td>
      <td>Canal+</td>
      <td>1/1/15</td>
      <td>1578</td>
      <td>6.1</td>
      <td>2015</td>
      <td>4.415998e+07</td>
      <td>2.997096e+08</td>
    </tr>
    <tr>
      <th>17</th>
      <td>102899</td>
      <td>tt0478970</td>
      <td>5.573184</td>
      <td>130000000</td>
      <td>518602163</td>
      <td>Ant-Man</td>
      <td>Evangeline Lilly</td>
      <td>Peyton Reed</td>
      <td>Armed with the astonishing ability to shrink i...</td>
      <td>115</td>
      <td>Adventure</td>
      <td>None</td>
      <td>7/14/15</td>
      <td>3779</td>
      <td>7.0</td>
      <td>2015</td>
      <td>1.195999e+08</td>
      <td>4.771138e+08</td>
    </tr>
    <tr>
      <th>18</th>
      <td>150689</td>
      <td>tt1661199</td>
      <td>5.556818</td>
      <td>95000000</td>
      <td>542351353</td>
      <td>Cinderella</td>
      <td>Richard Madden</td>
      <td>Kenneth Branagh</td>
      <td>When her father unexpectedly passes away, youn...</td>
      <td>112</td>
      <td>Family</td>
      <td>Beagle Pug Films</td>
      <td>3/12/15</td>
      <td>1495</td>
      <td>6.8</td>
      <td>2015</td>
      <td>8.739996e+07</td>
      <td>4.989630e+08</td>
    </tr>
    <tr>
      <th>19</th>
      <td>131634</td>
      <td>tt1951266</td>
      <td>5.476958</td>
      <td>160000000</td>
      <td>650523427</td>
      <td>The Hunger Games: Mockingjay - Part 2</td>
      <td>Liam Hemsworth</td>
      <td>Francis Lawrence</td>
      <td>With the nation of Panem in a full scale war, ...</td>
      <td>136</td>
      <td>Science Fiction</td>
      <td>Lionsgate</td>
      <td>11/18/15</td>
      <td>2380</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.471999e+08</td>
      <td>5.984813e+08</td>
    </tr>
    <tr>
      <th>20</th>
      <td>158852</td>
      <td>tt1964418</td>
      <td>5.462138</td>
      <td>190000000</td>
      <td>209035668</td>
      <td>Tomorrowland</td>
      <td>Raffey Cassidy</td>
      <td>Brad Bird</td>
      <td>Bound by a shared destiny, a bright, optimisti...</td>
      <td>130</td>
      <td>Science Fiction</td>
      <td>A113</td>
      <td>5/19/15</td>
      <td>1899</td>
      <td>6.2</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.923127e+08</td>
    </tr>
    <tr>
      <th>21</th>
      <td>307081</td>
      <td>tt1798684</td>
      <td>5.337064</td>
      <td>30000000</td>
      <td>91709827</td>
      <td>Southpaw</td>
      <td>Forest Whitaker</td>
      <td>Antoine Fuqua</td>
      <td>Billy "The Great" Hope, the reigning junior mi...</td>
      <td>123</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/15</td>
      <td>1386</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.759999e+07</td>
      <td>8.437300e+07</td>
    </tr>
    <tr>
      <th>22</th>
      <td>254128</td>
      <td>tt2126355</td>
      <td>4.907832</td>
      <td>110000000</td>
      <td>470490832</td>
      <td>San Andreas</td>
      <td>Carla Gugino</td>
      <td>Brad Peyton</td>
      <td>In the aftermath of a massive earthquake in Ca...</td>
      <td>114</td>
      <td>Thriller</td>
      <td>Warner Bros.</td>
      <td>5/27/15</td>
      <td>2060</td>
      <td>6.1</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>4.328514e+08</td>
    </tr>
    <tr>
      <th>23</th>
      <td>216015</td>
      <td>tt2322441</td>
      <td>4.710402</td>
      <td>40000000</td>
      <td>569651467</td>
      <td>Fifty Shades of Grey</td>
      <td>Jennifer Ehle</td>
      <td>Sam Taylor-Johnson</td>
      <td>When college senior Anastasia Steele steps in ...</td>
      <td>125</td>
      <td>None</td>
      <td>Michael De Luca Productions</td>
      <td>2/11/15</td>
      <td>1865</td>
      <td>5.3</td>
      <td>2015</td>
      <td>3.679998e+07</td>
      <td>5.240791e+08</td>
    </tr>
    <tr>
      <th>24</th>
      <td>318846</td>
      <td>tt1596363</td>
      <td>4.648046</td>
      <td>28000000</td>
      <td>133346506</td>
      <td>The Big Short</td>
      <td>Ryan Gosling</td>
      <td>Adam McKay</td>
      <td>The men who made millions from a global econom...</td>
      <td>130</td>
      <td>None</td>
      <td>Regency Enterprises</td>
      <td>12/11/15</td>
      <td>1545</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.575999e+07</td>
      <td>1.226787e+08</td>
    </tr>
    <tr>
      <th>25</th>
      <td>177677</td>
      <td>tt2381249</td>
      <td>4.566713</td>
      <td>150000000</td>
      <td>682330139</td>
      <td>Mission: Impossible - Rogue Nation</td>
      <td>Simon Pegg</td>
      <td>Christopher McQuarrie</td>
      <td>Ethan and team take on their most impossible m...</td>
      <td>131</td>
      <td>None</td>
      <td>China Movie Channel</td>
      <td>7/23/15</td>
      <td>2349</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>6.277435e+08</td>
    </tr>
    <tr>
      <th>26</th>
      <td>214756</td>
      <td>tt2637276</td>
      <td>4.564549</td>
      <td>68000000</td>
      <td>215863606</td>
      <td>Ted 2</td>
      <td>Amanda Seyfried</td>
      <td>Seth MacFarlane</td>
      <td>Newlywed couple Ted and Tami-Lynn want to have...</td>
      <td>115</td>
      <td>None</td>
      <td>Fuzzy Door Productions</td>
      <td>6/25/15</td>
      <td>1666</td>
      <td>6.3</td>
      <td>2015</td>
      <td>6.255997e+07</td>
      <td>1.985944e+08</td>
    </tr>
    <tr>
      <th>27</th>
      <td>207703</td>
      <td>tt2802144</td>
      <td>4.503789</td>
      <td>81000000</td>
      <td>403802136</td>
      <td>Kingsman: The Secret Service</td>
      <td>Samuel L. Jackson</td>
      <td>Matthew Vaughn</td>
      <td>The story of a super-secret spy organization t...</td>
      <td>130</td>
      <td>Action</td>
      <td>TSG Entertainment</td>
      <td>1/24/15</td>
      <td>3833</td>
      <td>7.6</td>
      <td>2015</td>
      <td>7.451997e+07</td>
      <td>3.714978e+08</td>
    </tr>
    <tr>
      <th>28</th>
      <td>314365</td>
      <td>tt1895587</td>
      <td>4.062293</td>
      <td>20000000</td>
      <td>88346473</td>
      <td>Spotlight</td>
      <td>Rachel McAdams</td>
      <td>Tom McCarthy</td>
      <td>The true story of how The Boston Globe uncover...</td>
      <td>128</td>
      <td>History</td>
      <td>Anonymous Content</td>
      <td>11/6/15</td>
      <td>1559</td>
      <td>7.8</td>
      <td>2015</td>
      <td>1.839999e+07</td>
      <td>8.127872e+07</td>
    </tr>
    <tr>
      <th>29</th>
      <td>294254</td>
      <td>tt4046784</td>
      <td>3.968891</td>
      <td>61000000</td>
      <td>311256926</td>
      <td>Maze Runner: The Scorch Trials</td>
      <td>Thomas Brodie-Sangster</td>
      <td>Wes Ball</td>
      <td>Thomas and his fellow Gladers face their great...</td>
      <td>132</td>
      <td>Thriller</td>
      <td>TSG Entertainment</td>
      <td>9/9/15</td>
      <td>1849</td>
      <td>6.4</td>
      <td>2015</td>
      <td>5.611998e+07</td>
      <td>2.863562e+08</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9740</th>
      <td>12639</td>
      <td>tt0060897</td>
      <td>0.310688</td>
      <td>0</td>
      <td>0</td>
      <td>Return of the Seven</td>
      <td>JuliÃ¡n Mateos</td>
      <td>Burt Kennedy</td>
      <td>Chico one of the remaining members of The Magn...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>10/19/66</td>
      <td>14</td>
      <td>5.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9741</th>
      <td>5923</td>
      <td>tt0060934</td>
      <td>0.299911</td>
      <td>12000000</td>
      <td>20000000</td>
      <td>The Sand Pebbles</td>
      <td>Richard Crenna</td>
      <td>Robert Wise</td>
      <td>Engineer Jake Holman arrives aboard the gunboa...</td>
      <td>182</td>
      <td>Drama</td>
      <td>Robert Wise Productions</td>
      <td>12/20/66</td>
      <td>28</td>
      <td>7.0</td>
      <td>1966</td>
      <td>8.061618e+07</td>
      <td>1.343603e+08</td>
    </tr>
    <tr>
      <th>9742</th>
      <td>38720</td>
      <td>tt0061170</td>
      <td>0.239435</td>
      <td>0</td>
      <td>0</td>
      <td>Walk Don't Run</td>
      <td>Jim Hutton</td>
      <td>Charles Walters</td>
      <td>British industrialist Sir William Rutland - "B...</td>
      <td>114</td>
      <td>None</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9743</th>
      <td>19728</td>
      <td>tt0060177</td>
      <td>0.291704</td>
      <td>0</td>
      <td>0</td>
      <td>The Blue Max</td>
      <td>Ursula Andress</td>
      <td>John Guillermin</td>
      <td>A young pilot in the German air force of 1918,...</td>
      <td>156</td>
      <td>Adventure</td>
      <td>None</td>
      <td>6/21/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9744</th>
      <td>22383</td>
      <td>tt0060862</td>
      <td>0.151845</td>
      <td>0</td>
      <td>0</td>
      <td>The Professionals</td>
      <td>Robert Ryan</td>
      <td>Richard Brooks</td>
      <td>The Professionals is a 1966 American Western f...</td>
      <td>117</td>
      <td>Western</td>
      <td>None</td>
      <td>11/1/66</td>
      <td>21</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9745</th>
      <td>13353</td>
      <td>tt0060550</td>
      <td>0.276133</td>
      <td>0</td>
      <td>0</td>
      <td>It's the Great Pumpkin, Charlie Brown</td>
      <td>Kathy Steinberg</td>
      <td>Bill Melendez</td>
      <td>This classic "Peanuts" tale focuses on the thu...</td>
      <td>25</td>
      <td>None</td>
      <td>None</td>
      <td>10/27/66</td>
      <td>49</td>
      <td>7.2</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9746</th>
      <td>34388</td>
      <td>tt0060437</td>
      <td>0.102530</td>
      <td>0</td>
      <td>0</td>
      <td>Funeral in Berlin</td>
      <td>Oskar Homolka</td>
      <td>Guy Hamilton</td>
      <td>Colonel Stok, a Soviet intelligence officer re...</td>
      <td>102</td>
      <td>None</td>
      <td>None</td>
      <td>12/22/66</td>
      <td>13</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9747</th>
      <td>42701</td>
      <td>tt0062262</td>
      <td>0.264925</td>
      <td>75000</td>
      <td>0</td>
      <td>The Shooting</td>
      <td>Jack Nicholson</td>
      <td>Monte Hellman</td>
      <td>A hired gun seeks to enact revenge on a group ...</td>
      <td>82</td>
      <td>None</td>
      <td>None</td>
      <td>10/23/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>5.038511e+05</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9748</th>
      <td>29710</td>
      <td>tt0060588</td>
      <td>0.252399</td>
      <td>0</td>
      <td>0</td>
      <td>Khartoum</td>
      <td>Richard Johnson</td>
      <td>Basil Dearden|Eliot Elisofon</td>
      <td>English General Charles George Gordon, a devou...</td>
      <td>134</td>
      <td>War</td>
      <td>None</td>
      <td>6/9/66</td>
      <td>12</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9749</th>
      <td>23728</td>
      <td>tt0059557</td>
      <td>0.236098</td>
      <td>0</td>
      <td>0</td>
      <td>Our Man Flint</td>
      <td>Gila Golan</td>
      <td>Daniel Mann</td>
      <td>When scientists use eco-terrorism to impose th...</td>
      <td>108</td>
      <td>Fantasy</td>
      <td>None</td>
      <td>1/16/66</td>
      <td>13</td>
      <td>5.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9750</th>
      <td>5065</td>
      <td>tt0059014</td>
      <td>0.230873</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Cowboy</td>
      <td>Angela Douglas</td>
      <td>Gerald Thomas</td>
      <td>Stodge City is in the grip of the Rumpo Kid an...</td>
      <td>93</td>
      <td>None</td>
      <td>None</td>
      <td>3/1/66</td>
      <td>15</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9751</th>
      <td>17102</td>
      <td>tt0059127</td>
      <td>0.212716</td>
      <td>0</td>
      <td>0</td>
      <td>Dracula: Prince of Darkness</td>
      <td>Andrew Keir</td>
      <td>Terence Fisher</td>
      <td>Whilst vacationing in the Carpathian Mountain,...</td>
      <td>90</td>
      <td>None</td>
      <td>None</td>
      <td>1/9/66</td>
      <td>16</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9752</th>
      <td>28763</td>
      <td>tt0060548</td>
      <td>0.034555</td>
      <td>0</td>
      <td>0</td>
      <td>Island of Terror</td>
      <td>Carole Gray</td>
      <td>Terence Fisher</td>
      <td>A small island community is overrun with creep...</td>
      <td>89</td>
      <td>None</td>
      <td>None</td>
      <td>6/20/66</td>
      <td>13</td>
      <td>5.3</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9753</th>
      <td>2161</td>
      <td>tt0060397</td>
      <td>0.207257</td>
      <td>5115000</td>
      <td>12000000</td>
      <td>Fantastic Voyage</td>
      <td>Edmond O'Brien</td>
      <td>Richard Fleischer</td>
      <td>The science of miniaturization has been unlock...</td>
      <td>100</td>
      <td>None</td>
      <td>None</td>
      <td>8/24/66</td>
      <td>42</td>
      <td>6.7</td>
      <td>1966</td>
      <td>3.436265e+07</td>
      <td>8.061618e+07</td>
    </tr>
    <tr>
      <th>9754</th>
      <td>28270</td>
      <td>tt0060445</td>
      <td>0.206537</td>
      <td>0</td>
      <td>0</td>
      <td>Gambit</td>
      <td>Herbert Lom</td>
      <td>Ronald Neame</td>
      <td>Harry Dean (Michael Caine) has a perfect plan ...</td>
      <td>109</td>
      <td>Crime</td>
      <td>None</td>
      <td>12/16/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9755</th>
      <td>26268</td>
      <td>tt0060490</td>
      <td>0.202473</td>
      <td>0</td>
      <td>0</td>
      <td>Harper</td>
      <td>Julie Harris</td>
      <td>Jack Smight</td>
      <td>Harper is a cynical private eye in the best tr...</td>
      <td>121</td>
      <td>Thriller</td>
      <td>None</td>
      <td>2/23/66</td>
      <td>14</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9756</th>
      <td>15347</td>
      <td>tt0060182</td>
      <td>0.342791</td>
      <td>0</td>
      <td>0</td>
      <td>Born Free</td>
      <td>Geoffrey Keen</td>
      <td>James Hill</td>
      <td>Born Free (1966) is an Open Road Films Ltd./Co...</td>
      <td>95</td>
      <td>Action</td>
      <td>None</td>
      <td>6/22/66</td>
      <td>15</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9757</th>
      <td>37301</td>
      <td>tt0060165</td>
      <td>0.227220</td>
      <td>0</td>
      <td>0</td>
      <td>A Big Hand for the Little Lady</td>
      <td>Jason Robards</td>
      <td>Fielder Cook</td>
      <td>A naive traveler in Laredo gets involved in a ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>5/31/66</td>
      <td>11</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9758</th>
      <td>31602</td>
      <td>tt0060232</td>
      <td>0.146402</td>
      <td>0</td>
      <td>0</td>
      <td>The Chase</td>
      <td>Robert Redford</td>
      <td>Arthur Penn</td>
      <td>Most everyone in town thinks that Sheriff Cald...</td>
      <td>135</td>
      <td>Crime</td>
      <td>None</td>
      <td>2/17/66</td>
      <td>17</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9759</th>
      <td>13343</td>
      <td>tt0059221</td>
      <td>0.141026</td>
      <td>700000</td>
      <td>0</td>
      <td>The Ghost &amp; Mr. Chicken</td>
      <td>Liam Redmond</td>
      <td>Alan Rafkin</td>
      <td>Luther Heggs aspires to being a reporter for h...</td>
      <td>90</td>
      <td>Mystery</td>
      <td>None</td>
      <td>1/20/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>4.702610e+06</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9760</th>
      <td>20277</td>
      <td>tt0061135</td>
      <td>0.140934</td>
      <td>0</td>
      <td>0</td>
      <td>The Ugly Dachshund</td>
      <td>Charles Ruggles</td>
      <td>Norman Tokar</td>
      <td>The Garrisons (Dean Jones and Suzanne Pleshett...</td>
      <td>93</td>
      <td>Family</td>
      <td>None</td>
      <td>2/16/66</td>
      <td>14</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9761</th>
      <td>5921</td>
      <td>tt0060748</td>
      <td>0.131378</td>
      <td>0</td>
      <td>0</td>
      <td>Nevada Smith</td>
      <td>Brian Keith</td>
      <td>Henry Hathaway</td>
      <td>Nevada Smith is the young son of an Indian mot...</td>
      <td>128</td>
      <td>None</td>
      <td>Embassy Pictures</td>
      <td>6/10/66</td>
      <td>10</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9762</th>
      <td>31918</td>
      <td>tt0060921</td>
      <td>0.317824</td>
      <td>0</td>
      <td>0</td>
      <td>The Russians Are Coming, The Russians Are Coming</td>
      <td>Alan Arkin</td>
      <td>Norman Jewison</td>
      <td>Without hostile intent, a Soviet sub runs agro...</td>
      <td>126</td>
      <td>None</td>
      <td>None</td>
      <td>5/25/66</td>
      <td>11</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9763</th>
      <td>20620</td>
      <td>tt0060955</td>
      <td>0.089072</td>
      <td>0</td>
      <td>0</td>
      <td>Seconds</td>
      <td>John Randolph</td>
      <td>John Frankenheimer</td>
      <td>A secret organisation offers wealthy people a ...</td>
      <td>100</td>
      <td>Thriller</td>
      <td>John Frankenheimer Productions Inc.</td>
      <td>10/5/66</td>
      <td>22</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9764</th>
      <td>5060</td>
      <td>tt0060214</td>
      <td>0.087034</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Screaming!</td>
      <td>Harry H. Corbett</td>
      <td>Gerald Thomas</td>
      <td>The sinister Dr Watt has an evil scheme going....</td>
      <td>87</td>
      <td>None</td>
      <td>None</td>
      <td>5/20/66</td>
      <td>13</td>
      <td>7.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9765</th>
      <td>21</td>
      <td>tt0060371</td>
      <td>0.080598</td>
      <td>0</td>
      <td>0</td>
      <td>The Endless Summer</td>
      <td>Lord 'Tally Ho' Blears</td>
      <td>Bruce Brown</td>
      <td>The Endless Summer, by Bruce Brown, is one of ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/66</td>
      <td>11</td>
      <td>7.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9766</th>
      <td>20379</td>
      <td>tt0060472</td>
      <td>0.065543</td>
      <td>0</td>
      <td>0</td>
      <td>Grand Prix</td>
      <td>Yves Montand</td>
      <td>John Frankenheimer</td>
      <td>Grand Prix driver Pete Aron is fired by his te...</td>
      <td>176</td>
      <td>Drama</td>
      <td>Douglas &amp; Lewis Productions</td>
      <td>12/21/66</td>
      <td>20</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9767</th>
      <td>39768</td>
      <td>tt0060161</td>
      <td>0.065141</td>
      <td>0</td>
      <td>0</td>
      <td>Beregis Avtomobilya</td>
      <td>Georgi Zhzhyonov</td>
      <td>Eldar Ryazanov</td>
      <td>An insurance agent who moonlights as a carthie...</td>
      <td>94</td>
      <td>None</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>6.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9768</th>
      <td>21449</td>
      <td>tt0061177</td>
      <td>0.064317</td>
      <td>0</td>
      <td>0</td>
      <td>What's Up, Tiger Lily?</td>
      <td>Mie Hama</td>
      <td>Woody Allen</td>
      <td>In comic Woody Allen's film debut, he took the...</td>
      <td>80</td>
      <td>None</td>
      <td>None</td>
      <td>11/2/66</td>
      <td>22</td>
      <td>5.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9769</th>
      <td>22293</td>
      <td>tt0060666</td>
      <td>0.035919</td>
      <td>19000</td>
      <td>0</td>
      <td>Manos: The Hands of Fate</td>
      <td>John Reynolds</td>
      <td>Harold P. Warren</td>
      <td>A family gets lost on the road and stumbles up...</td>
      <td>74</td>
      <td>None</td>
      <td>None</td>
      <td>11/15/66</td>
      <td>15</td>
      <td>1.5</td>
      <td>1966</td>
      <td>1.276423e+05</td>
      <td>0.000000e+00</td>
    </tr>
  </tbody>
</table>
<p>9770 rows × 18 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df4</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[24]:</div>



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
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>director</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Vincent D'Onofrio</td>
      <td>Colin Trevorrow</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>Thriller</td>
      <td>Fuji Television Network</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Nicholas Hoult</td>
      <td>George Miller</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>Thriller</td>
      <td>None</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>262500</td>
      <td>tt2908446</td>
      <td>13.112507</td>
      <td>110000000</td>
      <td>295238201</td>
      <td>Insurgent</td>
      <td>Ansel Elgort</td>
      <td>Robert Schwentke</td>
      <td>Beatrice Prior must confront her inner demons ...</td>
      <td>119</td>
      <td>None</td>
      <td>NeoReel</td>
      <td>3/18/15</td>
      <td>2480</td>
      <td>6.3</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>2.716190e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>140607</td>
      <td>tt2488496</td>
      <td>11.173104</td>
      <td>200000000</td>
      <td>2068178225</td>
      <td>Star Wars: The Force Awakens</td>
      <td>Adam Driver</td>
      <td>J.J. Abrams</td>
      <td>Thirty years after defeating the Galactic Empi...</td>
      <td>136</td>
      <td>Fantasy</td>
      <td>None</td>
      <td>12/15/15</td>
      <td>5292</td>
      <td>7.5</td>
      <td>2015</td>
      <td>1.839999e+08</td>
      <td>1.902723e+09</td>
    </tr>
    <tr>
      <th>4</th>
      <td>168259</td>
      <td>tt2820852</td>
      <td>9.335014</td>
      <td>190000000</td>
      <td>1506249360</td>
      <td>Furious 7</td>
      <td>Michelle Rodriguez</td>
      <td>James Wan</td>
      <td>Deckard Shaw seeks revenge against Dominic Tor...</td>
      <td>137</td>
      <td>None</td>
      <td>Dentsu</td>
      <td>4/1/15</td>
      <td>2947</td>
      <td>7.3</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.385749e+09</td>
    </tr>
    <tr>
      <th>5</th>
      <td>281957</td>
      <td>tt1663202</td>
      <td>9.110700</td>
      <td>135000000</td>
      <td>532950503</td>
      <td>The Revenant</td>
      <td>Domhnall Gleeson</td>
      <td>Alejandro GonzÃ¡lez IÃ±Ã¡rritu</td>
      <td>In the 1820s, a frontiersman, Hugh Glass, sets...</td>
      <td>156</td>
      <td>Thriller</td>
      <td>Anonymous Content</td>
      <td>12/25/15</td>
      <td>3929</td>
      <td>7.2</td>
      <td>2015</td>
      <td>1.241999e+08</td>
      <td>4.903142e+08</td>
    </tr>
    <tr>
      <th>6</th>
      <td>87101</td>
      <td>tt1340138</td>
      <td>8.654359</td>
      <td>155000000</td>
      <td>440603537</td>
      <td>Terminator Genisys</td>
      <td>Jai Courtney</td>
      <td>Alan Taylor</td>
      <td>The year is 2029. John Connor, leader of the r...</td>
      <td>125</td>
      <td>Adventure</td>
      <td>None</td>
      <td>6/23/15</td>
      <td>2598</td>
      <td>5.8</td>
      <td>2015</td>
      <td>1.425999e+08</td>
      <td>4.053551e+08</td>
    </tr>
    <tr>
      <th>7</th>
      <td>286217</td>
      <td>tt3659388</td>
      <td>7.667400</td>
      <td>108000000</td>
      <td>595380321</td>
      <td>The Martian</td>
      <td>Jeff Daniels</td>
      <td>Ridley Scott</td>
      <td>During a manned mission to Mars, Astronaut Mar...</td>
      <td>141</td>
      <td>None</td>
      <td>International Traders</td>
      <td>9/30/15</td>
      <td>4572</td>
      <td>7.6</td>
      <td>2015</td>
      <td>9.935996e+07</td>
      <td>5.477497e+08</td>
    </tr>
    <tr>
      <th>8</th>
      <td>211672</td>
      <td>tt2293640</td>
      <td>7.404165</td>
      <td>74000000</td>
      <td>1156730962</td>
      <td>Minions</td>
      <td>Allison Janney</td>
      <td>Kyle Balda|Pierre Coffin</td>
      <td>Minions Stuart, Kevin and Bob are recruited by...</td>
      <td>91</td>
      <td>Comedy</td>
      <td>None</td>
      <td>6/17/15</td>
      <td>2893</td>
      <td>6.5</td>
      <td>2015</td>
      <td>6.807997e+07</td>
      <td>1.064192e+09</td>
    </tr>
    <tr>
      <th>9</th>
      <td>150540</td>
      <td>tt2096673</td>
      <td>6.326804</td>
      <td>175000000</td>
      <td>853708609</td>
      <td>Inside Out</td>
      <td>Bill Hader</td>
      <td>Pete Docter</td>
      <td>Growing up can be a bumpy road, and it's no ex...</td>
      <td>94</td>
      <td>None</td>
      <td>None</td>
      <td>6/9/15</td>
      <td>3935</td>
      <td>8.0</td>
      <td>2015</td>
      <td>1.609999e+08</td>
      <td>7.854116e+08</td>
    </tr>
    <tr>
      <th>10</th>
      <td>206647</td>
      <td>tt2379713</td>
      <td>6.200282</td>
      <td>245000000</td>
      <td>880674609</td>
      <td>Spectre</td>
      <td>Ralph Fiennes</td>
      <td>Sam Mendes</td>
      <td>A cryptic message from Bondâ€™s past sends him...</td>
      <td>148</td>
      <td>None</td>
      <td>None</td>
      <td>10/26/15</td>
      <td>3254</td>
      <td>6.2</td>
      <td>2015</td>
      <td>2.253999e+08</td>
      <td>8.102203e+08</td>
    </tr>
    <tr>
      <th>11</th>
      <td>76757</td>
      <td>tt1617661</td>
      <td>6.189369</td>
      <td>176000003</td>
      <td>183987723</td>
      <td>Jupiter Ascending</td>
      <td>Eddie Redmayne</td>
      <td>Lana Wachowski|Lilly Wachowski</td>
      <td>In a universe where human genetic material is ...</td>
      <td>124</td>
      <td>Adventure</td>
      <td>Warner Bros.</td>
      <td>2/4/15</td>
      <td>1937</td>
      <td>5.2</td>
      <td>2015</td>
      <td>1.619199e+08</td>
      <td>1.692686e+08</td>
    </tr>
    <tr>
      <th>12</th>
      <td>264660</td>
      <td>tt0470752</td>
      <td>6.118847</td>
      <td>15000000</td>
      <td>36869414</td>
      <td>Ex Machina</td>
      <td>Sonoya Mizuno</td>
      <td>Alex Garland</td>
      <td>Caleb, a 26 year old coder at the world's larg...</td>
      <td>108</td>
      <td>None</td>
      <td>None</td>
      <td>1/21/15</td>
      <td>2854</td>
      <td>7.6</td>
      <td>2015</td>
      <td>1.379999e+07</td>
      <td>3.391985e+07</td>
    </tr>
    <tr>
      <th>13</th>
      <td>257344</td>
      <td>tt2120120</td>
      <td>5.984995</td>
      <td>88000000</td>
      <td>243637091</td>
      <td>Pixels</td>
      <td>Josh Gad</td>
      <td>Chris Columbus</td>
      <td>Video game experts are recruited by the milita...</td>
      <td>105</td>
      <td>None</td>
      <td>None</td>
      <td>7/16/15</td>
      <td>1575</td>
      <td>5.8</td>
      <td>2015</td>
      <td>8.095996e+07</td>
      <td>2.241460e+08</td>
    </tr>
    <tr>
      <th>14</th>
      <td>99861</td>
      <td>tt2395427</td>
      <td>5.944927</td>
      <td>280000000</td>
      <td>1405035767</td>
      <td>Avengers: Age of Ultron</td>
      <td>Chris Evans</td>
      <td>Joss Whedon</td>
      <td>When Tony Stark tries to jumpstart a dormant p...</td>
      <td>141</td>
      <td>None</td>
      <td>None</td>
      <td>4/22/15</td>
      <td>4304</td>
      <td>7.4</td>
      <td>2015</td>
      <td>2.575999e+08</td>
      <td>1.292632e+09</td>
    </tr>
    <tr>
      <th>15</th>
      <td>273248</td>
      <td>tt3460252</td>
      <td>5.898400</td>
      <td>44000000</td>
      <td>155760117</td>
      <td>The Hateful Eight</td>
      <td>Walton Goggins</td>
      <td>Quentin Tarantino</td>
      <td>Bounty hunters seek shelter from a raging bliz...</td>
      <td>167</td>
      <td>Western</td>
      <td>None</td>
      <td>12/25/15</td>
      <td>2389</td>
      <td>7.4</td>
      <td>2015</td>
      <td>4.047998e+07</td>
      <td>1.432992e+08</td>
    </tr>
    <tr>
      <th>16</th>
      <td>260346</td>
      <td>tt2446042</td>
      <td>5.749758</td>
      <td>48000000</td>
      <td>325771424</td>
      <td>Taken 3</td>
      <td>Famke Janssen</td>
      <td>Olivier Megaton</td>
      <td>Ex-government operative Bryan Mills finds his ...</td>
      <td>109</td>
      <td>None</td>
      <td>EuropaCorp</td>
      <td>1/1/15</td>
      <td>1578</td>
      <td>6.1</td>
      <td>2015</td>
      <td>4.415998e+07</td>
      <td>2.997096e+08</td>
    </tr>
    <tr>
      <th>17</th>
      <td>102899</td>
      <td>tt0478970</td>
      <td>5.573184</td>
      <td>130000000</td>
      <td>518602163</td>
      <td>Ant-Man</td>
      <td>Corey Stoll</td>
      <td>Peyton Reed</td>
      <td>Armed with the astonishing ability to shrink i...</td>
      <td>115</td>
      <td>None</td>
      <td>None</td>
      <td>7/14/15</td>
      <td>3779</td>
      <td>7.0</td>
      <td>2015</td>
      <td>1.195999e+08</td>
      <td>4.771138e+08</td>
    </tr>
    <tr>
      <th>18</th>
      <td>150689</td>
      <td>tt1661199</td>
      <td>5.556818</td>
      <td>95000000</td>
      <td>542351353</td>
      <td>Cinderella</td>
      <td>Helena Bonham Carter</td>
      <td>Kenneth Branagh</td>
      <td>When her father unexpectedly passes away, youn...</td>
      <td>112</td>
      <td>Drama</td>
      <td>Allison Shearmur Productions</td>
      <td>3/12/15</td>
      <td>1495</td>
      <td>6.8</td>
      <td>2015</td>
      <td>8.739996e+07</td>
      <td>4.989630e+08</td>
    </tr>
    <tr>
      <th>19</th>
      <td>131634</td>
      <td>tt1951266</td>
      <td>5.476958</td>
      <td>160000000</td>
      <td>650523427</td>
      <td>The Hunger Games: Mockingjay - Part 2</td>
      <td>Woody Harrelson</td>
      <td>Francis Lawrence</td>
      <td>With the nation of Panem in a full scale war, ...</td>
      <td>136</td>
      <td>None</td>
      <td>Walt Disney Studios Motion Pictures</td>
      <td>11/18/15</td>
      <td>2380</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.471999e+08</td>
      <td>5.984813e+08</td>
    </tr>
    <tr>
      <th>20</th>
      <td>158852</td>
      <td>tt1964418</td>
      <td>5.462138</td>
      <td>190000000</td>
      <td>209035668</td>
      <td>Tomorrowland</td>
      <td>Thomas Robinson</td>
      <td>Brad Bird</td>
      <td>Bound by a shared destiny, a bright, optimisti...</td>
      <td>130</td>
      <td>Adventure</td>
      <td>None</td>
      <td>5/19/15</td>
      <td>1899</td>
      <td>6.2</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.923127e+08</td>
    </tr>
    <tr>
      <th>21</th>
      <td>307081</td>
      <td>tt1798684</td>
      <td>5.337064</td>
      <td>30000000</td>
      <td>91709827</td>
      <td>Southpaw</td>
      <td>Oona Laurence</td>
      <td>Antoine Fuqua</td>
      <td>Billy "The Great" Hope, the reigning junior mi...</td>
      <td>123</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/15</td>
      <td>1386</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.759999e+07</td>
      <td>8.437300e+07</td>
    </tr>
    <tr>
      <th>22</th>
      <td>254128</td>
      <td>tt2126355</td>
      <td>4.907832</td>
      <td>110000000</td>
      <td>470490832</td>
      <td>San Andreas</td>
      <td>Ioan Gruffudd</td>
      <td>Brad Peyton</td>
      <td>In the aftermath of a massive earthquake in Ca...</td>
      <td>114</td>
      <td>None</td>
      <td>Flynn Picture Company</td>
      <td>5/27/15</td>
      <td>2060</td>
      <td>6.1</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>4.328514e+08</td>
    </tr>
    <tr>
      <th>23</th>
      <td>216015</td>
      <td>tt2322441</td>
      <td>4.710402</td>
      <td>40000000</td>
      <td>569651467</td>
      <td>Fifty Shades of Grey</td>
      <td>Eloise Mumford</td>
      <td>Sam Taylor-Johnson</td>
      <td>When college senior Anastasia Steele steps in ...</td>
      <td>125</td>
      <td>None</td>
      <td>None</td>
      <td>2/11/15</td>
      <td>1865</td>
      <td>5.3</td>
      <td>2015</td>
      <td>3.679998e+07</td>
      <td>5.240791e+08</td>
    </tr>
    <tr>
      <th>24</th>
      <td>318846</td>
      <td>tt1596363</td>
      <td>4.648046</td>
      <td>28000000</td>
      <td>133346506</td>
      <td>The Big Short</td>
      <td>Brad Pitt</td>
      <td>Adam McKay</td>
      <td>The men who made millions from a global econom...</td>
      <td>130</td>
      <td>None</td>
      <td>None</td>
      <td>12/11/15</td>
      <td>1545</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.575999e+07</td>
      <td>1.226787e+08</td>
    </tr>
    <tr>
      <th>25</th>
      <td>177677</td>
      <td>tt2381249</td>
      <td>4.566713</td>
      <td>150000000</td>
      <td>682330139</td>
      <td>Mission: Impossible - Rogue Nation</td>
      <td>Rebecca Ferguson</td>
      <td>Christopher McQuarrie</td>
      <td>Ethan and team take on their most impossible m...</td>
      <td>131</td>
      <td>None</td>
      <td>Bad Robot</td>
      <td>7/23/15</td>
      <td>2349</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>6.277435e+08</td>
    </tr>
    <tr>
      <th>26</th>
      <td>214756</td>
      <td>tt2637276</td>
      <td>4.564549</td>
      <td>68000000</td>
      <td>215863606</td>
      <td>Ted 2</td>
      <td>Jessica Barth</td>
      <td>Seth MacFarlane</td>
      <td>Newlywed couple Ted and Tami-Lynn want to have...</td>
      <td>115</td>
      <td>None</td>
      <td>None</td>
      <td>6/25/15</td>
      <td>1666</td>
      <td>6.3</td>
      <td>2015</td>
      <td>6.255997e+07</td>
      <td>1.985944e+08</td>
    </tr>
    <tr>
      <th>27</th>
      <td>207703</td>
      <td>tt2802144</td>
      <td>4.503789</td>
      <td>81000000</td>
      <td>403802136</td>
      <td>Kingsman: The Secret Service</td>
      <td>Michael Caine</td>
      <td>Matthew Vaughn</td>
      <td>The story of a super-secret spy organization t...</td>
      <td>130</td>
      <td>Adventure</td>
      <td>Cloudy Productions</td>
      <td>1/24/15</td>
      <td>3833</td>
      <td>7.6</td>
      <td>2015</td>
      <td>7.451997e+07</td>
      <td>3.714978e+08</td>
    </tr>
    <tr>
      <th>28</th>
      <td>314365</td>
      <td>tt1895587</td>
      <td>4.062293</td>
      <td>20000000</td>
      <td>88346473</td>
      <td>Spotlight</td>
      <td>Liev Schreiber</td>
      <td>Tom McCarthy</td>
      <td>The true story of how The Boston Globe uncover...</td>
      <td>128</td>
      <td>None</td>
      <td>Rocklin / Faust</td>
      <td>11/6/15</td>
      <td>1559</td>
      <td>7.8</td>
      <td>2015</td>
      <td>1.839999e+07</td>
      <td>8.127872e+07</td>
    </tr>
    <tr>
      <th>29</th>
      <td>294254</td>
      <td>tt4046784</td>
      <td>3.968891</td>
      <td>61000000</td>
      <td>311256926</td>
      <td>Maze Runner: The Scorch Trials</td>
      <td>Giancarlo Esposito</td>
      <td>Wes Ball</td>
      <td>Thomas and his fellow Gladers face their great...</td>
      <td>132</td>
      <td>None</td>
      <td>None</td>
      <td>9/9/15</td>
      <td>1849</td>
      <td>6.4</td>
      <td>2015</td>
      <td>5.611998e+07</td>
      <td>2.863562e+08</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9740</th>
      <td>12639</td>
      <td>tt0060897</td>
      <td>0.310688</td>
      <td>0</td>
      <td>0</td>
      <td>Return of the Seven</td>
      <td>Warren Oates</td>
      <td>Burt Kennedy</td>
      <td>Chico one of the remaining members of The Magn...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>10/19/66</td>
      <td>14</td>
      <td>5.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9741</th>
      <td>5923</td>
      <td>tt0060934</td>
      <td>0.299911</td>
      <td>12000000</td>
      <td>20000000</td>
      <td>The Sand Pebbles</td>
      <td>Candice Bergen</td>
      <td>Robert Wise</td>
      <td>Engineer Jake Holman arrives aboard the gunboa...</td>
      <td>182</td>
      <td>War</td>
      <td>None</td>
      <td>12/20/66</td>
      <td>28</td>
      <td>7.0</td>
      <td>1966</td>
      <td>8.061618e+07</td>
      <td>1.343603e+08</td>
    </tr>
    <tr>
      <th>9742</th>
      <td>38720</td>
      <td>tt0061170</td>
      <td>0.239435</td>
      <td>0</td>
      <td>0</td>
      <td>Walk Don't Run</td>
      <td>John Standing</td>
      <td>Charles Walters</td>
      <td>British industrialist Sir William Rutland - "B...</td>
      <td>114</td>
      <td>None</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9743</th>
      <td>19728</td>
      <td>tt0060177</td>
      <td>0.291704</td>
      <td>0</td>
      <td>0</td>
      <td>The Blue Max</td>
      <td>Jeremy Kemp</td>
      <td>John Guillermin</td>
      <td>A young pilot in the German air force of 1918,...</td>
      <td>156</td>
      <td>Drama</td>
      <td>None</td>
      <td>6/21/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9744</th>
      <td>22383</td>
      <td>tt0060862</td>
      <td>0.151845</td>
      <td>0</td>
      <td>0</td>
      <td>The Professionals</td>
      <td>Woody Strode</td>
      <td>Richard Brooks</td>
      <td>The Professionals is a 1966 American Western f...</td>
      <td>117</td>
      <td>None</td>
      <td>None</td>
      <td>11/1/66</td>
      <td>21</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9745</th>
      <td>13353</td>
      <td>tt0060550</td>
      <td>0.276133</td>
      <td>0</td>
      <td>0</td>
      <td>It's the Great Pumpkin, Charlie Brown</td>
      <td>Ann Altieri</td>
      <td>Bill Melendez</td>
      <td>This classic "Peanuts" tale focuses on the thu...</td>
      <td>25</td>
      <td>None</td>
      <td>None</td>
      <td>10/27/66</td>
      <td>49</td>
      <td>7.2</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9746</th>
      <td>34388</td>
      <td>tt0060437</td>
      <td>0.102530</td>
      <td>0</td>
      <td>0</td>
      <td>Funeral in Berlin</td>
      <td>Eva Renzi</td>
      <td>Guy Hamilton</td>
      <td>Colonel Stok, a Soviet intelligence officer re...</td>
      <td>102</td>
      <td>None</td>
      <td>None</td>
      <td>12/22/66</td>
      <td>13</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9747</th>
      <td>42701</td>
      <td>tt0062262</td>
      <td>0.264925</td>
      <td>75000</td>
      <td>0</td>
      <td>The Shooting</td>
      <td>Warren Oates</td>
      <td>Monte Hellman</td>
      <td>A hired gun seeks to enact revenge on a group ...</td>
      <td>82</td>
      <td>None</td>
      <td>None</td>
      <td>10/23/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>5.038511e+05</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9748</th>
      <td>29710</td>
      <td>tt0060588</td>
      <td>0.252399</td>
      <td>0</td>
      <td>0</td>
      <td>Khartoum</td>
      <td>Ralph Richardson</td>
      <td>Basil Dearden|Eliot Elisofon</td>
      <td>English General Charles George Gordon, a devou...</td>
      <td>134</td>
      <td>History</td>
      <td>None</td>
      <td>6/9/66</td>
      <td>12</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9749</th>
      <td>23728</td>
      <td>tt0059557</td>
      <td>0.236098</td>
      <td>0</td>
      <td>0</td>
      <td>Our Man Flint</td>
      <td>Edward Mulhare</td>
      <td>Daniel Mann</td>
      <td>When scientists use eco-terrorism to impose th...</td>
      <td>108</td>
      <td>Science Fiction</td>
      <td>None</td>
      <td>1/16/66</td>
      <td>13</td>
      <td>5.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9750</th>
      <td>5065</td>
      <td>tt0059014</td>
      <td>0.230873</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Cowboy</td>
      <td>Kenneth Williams</td>
      <td>Gerald Thomas</td>
      <td>Stodge City is in the grip of the Rumpo Kid an...</td>
      <td>93</td>
      <td>None</td>
      <td>None</td>
      <td>3/1/66</td>
      <td>15</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9751</th>
      <td>17102</td>
      <td>tt0059127</td>
      <td>0.212716</td>
      <td>0</td>
      <td>0</td>
      <td>Dracula: Prince of Darkness</td>
      <td>Francis Matthews</td>
      <td>Terence Fisher</td>
      <td>Whilst vacationing in the Carpathian Mountain,...</td>
      <td>90</td>
      <td>None</td>
      <td>None</td>
      <td>1/9/66</td>
      <td>16</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9752</th>
      <td>28763</td>
      <td>tt0060548</td>
      <td>0.034555</td>
      <td>0</td>
      <td>0</td>
      <td>Island of Terror</td>
      <td>Eddie Byrne</td>
      <td>Terence Fisher</td>
      <td>A small island community is overrun with creep...</td>
      <td>89</td>
      <td>None</td>
      <td>None</td>
      <td>6/20/66</td>
      <td>13</td>
      <td>5.3</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9753</th>
      <td>2161</td>
      <td>tt0060397</td>
      <td>0.207257</td>
      <td>5115000</td>
      <td>12000000</td>
      <td>Fantastic Voyage</td>
      <td>Donald Pleasence</td>
      <td>Richard Fleischer</td>
      <td>The science of miniaturization has been unlock...</td>
      <td>100</td>
      <td>None</td>
      <td>None</td>
      <td>8/24/66</td>
      <td>42</td>
      <td>6.7</td>
      <td>1966</td>
      <td>3.436265e+07</td>
      <td>8.061618e+07</td>
    </tr>
    <tr>
      <th>9754</th>
      <td>28270</td>
      <td>tt0060445</td>
      <td>0.206537</td>
      <td>0</td>
      <td>0</td>
      <td>Gambit</td>
      <td>John Abbott</td>
      <td>Ronald Neame</td>
      <td>Harry Dean (Michael Caine) has a perfect plan ...</td>
      <td>109</td>
      <td>None</td>
      <td>None</td>
      <td>12/16/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9755</th>
      <td>26268</td>
      <td>tt0060490</td>
      <td>0.202473</td>
      <td>0</td>
      <td>0</td>
      <td>Harper</td>
      <td>Arthur Hill</td>
      <td>Jack Smight</td>
      <td>Harper is a cynical private eye in the best tr...</td>
      <td>121</td>
      <td>Crime</td>
      <td>None</td>
      <td>2/23/66</td>
      <td>14</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9756</th>
      <td>15347</td>
      <td>tt0060182</td>
      <td>0.342791</td>
      <td>0</td>
      <td>0</td>
      <td>Born Free</td>
      <td>Peter Lukoye</td>
      <td>James Hill</td>
      <td>Born Free (1966) is an Open Road Films Ltd./Co...</td>
      <td>95</td>
      <td>Family</td>
      <td>None</td>
      <td>6/22/66</td>
      <td>15</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9757</th>
      <td>37301</td>
      <td>tt0060165</td>
      <td>0.227220</td>
      <td>0</td>
      <td>0</td>
      <td>A Big Hand for the Little Lady</td>
      <td>Paul Ford</td>
      <td>Fielder Cook</td>
      <td>A naive traveler in Laredo gets involved in a ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>5/31/66</td>
      <td>11</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9758</th>
      <td>31602</td>
      <td>tt0060232</td>
      <td>0.146402</td>
      <td>0</td>
      <td>0</td>
      <td>The Chase</td>
      <td>E.G. Marshall</td>
      <td>Arthur Penn</td>
      <td>Most everyone in town thinks that Sheriff Cald...</td>
      <td>135</td>
      <td>None</td>
      <td>None</td>
      <td>2/17/66</td>
      <td>17</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9759</th>
      <td>13343</td>
      <td>tt0059221</td>
      <td>0.141026</td>
      <td>700000</td>
      <td>0</td>
      <td>The Ghost &amp; Mr. Chicken</td>
      <td>Dick Sargent</td>
      <td>Alan Rafkin</td>
      <td>Luther Heggs aspires to being a reporter for h...</td>
      <td>90</td>
      <td>Romance</td>
      <td>None</td>
      <td>1/20/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>4.702610e+06</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9760</th>
      <td>20277</td>
      <td>tt0061135</td>
      <td>0.140934</td>
      <td>0</td>
      <td>0</td>
      <td>The Ugly Dachshund</td>
      <td>Kelly Thordsen</td>
      <td>Norman Tokar</td>
      <td>The Garrisons (Dean Jones and Suzanne Pleshett...</td>
      <td>93</td>
      <td>None</td>
      <td>None</td>
      <td>2/16/66</td>
      <td>14</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9761</th>
      <td>5921</td>
      <td>tt0060748</td>
      <td>0.131378</td>
      <td>0</td>
      <td>0</td>
      <td>Nevada Smith</td>
      <td>Arthur Kennedy</td>
      <td>Henry Hathaway</td>
      <td>Nevada Smith is the young son of an Indian mot...</td>
      <td>128</td>
      <td>None</td>
      <td>None</td>
      <td>6/10/66</td>
      <td>10</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9762</th>
      <td>31918</td>
      <td>tt0060921</td>
      <td>0.317824</td>
      <td>0</td>
      <td>0</td>
      <td>The Russians Are Coming, The Russians Are Coming</td>
      <td>Brian Keith</td>
      <td>Norman Jewison</td>
      <td>Without hostile intent, a Soviet sub runs agro...</td>
      <td>126</td>
      <td>None</td>
      <td>None</td>
      <td>5/25/66</td>
      <td>11</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9763</th>
      <td>20620</td>
      <td>tt0060955</td>
      <td>0.089072</td>
      <td>0</td>
      <td>0</td>
      <td>Seconds</td>
      <td>Will Geer</td>
      <td>John Frankenheimer</td>
      <td>A secret organisation offers wealthy people a ...</td>
      <td>100</td>
      <td>Drama</td>
      <td>None</td>
      <td>10/5/66</td>
      <td>22</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9764</th>
      <td>5060</td>
      <td>tt0060214</td>
      <td>0.087034</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Screaming!</td>
      <td>Joan Sims</td>
      <td>Gerald Thomas</td>
      <td>The sinister Dr Watt has an evil scheme going....</td>
      <td>87</td>
      <td>None</td>
      <td>None</td>
      <td>5/20/66</td>
      <td>13</td>
      <td>7.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9765</th>
      <td>21</td>
      <td>tt0060371</td>
      <td>0.080598</td>
      <td>0</td>
      <td>0</td>
      <td>The Endless Summer</td>
      <td>Bruce Brown</td>
      <td>Bruce Brown</td>
      <td>The Endless Summer, by Bruce Brown, is one of ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/66</td>
      <td>11</td>
      <td>7.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9766</th>
      <td>20379</td>
      <td>tt0060472</td>
      <td>0.065543</td>
      <td>0</td>
      <td>0</td>
      <td>Grand Prix</td>
      <td>ToshirÅ Mifune</td>
      <td>John Frankenheimer</td>
      <td>Grand Prix driver Pete Aron is fired by his te...</td>
      <td>176</td>
      <td>None</td>
      <td>None</td>
      <td>12/21/66</td>
      <td>20</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9767</th>
      <td>39768</td>
      <td>tt0060161</td>
      <td>0.065141</td>
      <td>0</td>
      <td>0</td>
      <td>Beregis Avtomobilya</td>
      <td>Olga Aroseva</td>
      <td>Eldar Ryazanov</td>
      <td>An insurance agent who moonlights as a carthie...</td>
      <td>94</td>
      <td>None</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>6.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9768</th>
      <td>21449</td>
      <td>tt0061177</td>
      <td>0.064317</td>
      <td>0</td>
      <td>0</td>
      <td>What's Up, Tiger Lily?</td>
      <td>John Sebastian</td>
      <td>Woody Allen</td>
      <td>In comic Woody Allen's film debut, he took the...</td>
      <td>80</td>
      <td>None</td>
      <td>None</td>
      <td>11/2/66</td>
      <td>22</td>
      <td>5.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9769</th>
      <td>22293</td>
      <td>tt0060666</td>
      <td>0.035919</td>
      <td>19000</td>
      <td>0</td>
      <td>Manos: The Hands of Fate</td>
      <td>Diane Mahree</td>
      <td>Harold P. Warren</td>
      <td>A family gets lost on the road and stumbles up...</td>
      <td>74</td>
      <td>None</td>
      <td>None</td>
      <td>11/15/66</td>
      <td>15</td>
      <td>1.5</td>
      <td>1966</td>
      <td>1.276423e+05</td>
      <td>0.000000e+00</td>
    </tr>
  </tbody>
</table>
<p>9770 rows × 18 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df5</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[25]:</div>



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
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>director</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Nick Robinson</td>
      <td>Colin Trevorrow</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>None</td>
      <td>Dentsu</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Josh Helman</td>
      <td>George Miller</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>None</td>
      <td>None</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
    <tr>
      <th>2</th>
      <td>262500</td>
      <td>tt2908446</td>
      <td>13.112507</td>
      <td>110000000</td>
      <td>295238201</td>
      <td>Insurgent</td>
      <td>Miles Teller</td>
      <td>Robert Schwentke</td>
      <td>Beatrice Prior must confront her inner demons ...</td>
      <td>119</td>
      <td>None</td>
      <td>None</td>
      <td>3/18/15</td>
      <td>2480</td>
      <td>6.3</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>2.716190e+08</td>
    </tr>
    <tr>
      <th>3</th>
      <td>140607</td>
      <td>tt2488496</td>
      <td>11.173104</td>
      <td>200000000</td>
      <td>2068178225</td>
      <td>Star Wars: The Force Awakens</td>
      <td>Daisy Ridley</td>
      <td>J.J. Abrams</td>
      <td>Thirty years after defeating the Galactic Empi...</td>
      <td>136</td>
      <td>None</td>
      <td>None</td>
      <td>12/15/15</td>
      <td>5292</td>
      <td>7.5</td>
      <td>2015</td>
      <td>1.839999e+08</td>
      <td>1.902723e+09</td>
    </tr>
    <tr>
      <th>4</th>
      <td>168259</td>
      <td>tt2820852</td>
      <td>9.335014</td>
      <td>190000000</td>
      <td>1506249360</td>
      <td>Furious 7</td>
      <td>Dwayne Johnson</td>
      <td>James Wan</td>
      <td>Deckard Shaw seeks revenge against Dominic Tor...</td>
      <td>137</td>
      <td>None</td>
      <td>One Race Films</td>
      <td>4/1/15</td>
      <td>2947</td>
      <td>7.3</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.385749e+09</td>
    </tr>
    <tr>
      <th>5</th>
      <td>281957</td>
      <td>tt1663202</td>
      <td>9.110700</td>
      <td>135000000</td>
      <td>532950503</td>
      <td>The Revenant</td>
      <td>Paul Anderson</td>
      <td>Alejandro GonzÃ¡lez IÃ±Ã¡rritu</td>
      <td>In the 1820s, a frontiersman, Hugh Glass, sets...</td>
      <td>156</td>
      <td>None</td>
      <td>New Regency Pictures</td>
      <td>12/25/15</td>
      <td>3929</td>
      <td>7.2</td>
      <td>2015</td>
      <td>1.241999e+08</td>
      <td>4.903142e+08</td>
    </tr>
    <tr>
      <th>6</th>
      <td>87101</td>
      <td>tt1340138</td>
      <td>8.654359</td>
      <td>155000000</td>
      <td>440603537</td>
      <td>Terminator Genisys</td>
      <td>J.K. Simmons</td>
      <td>Alan Taylor</td>
      <td>The year is 2029. John Connor, leader of the r...</td>
      <td>125</td>
      <td>None</td>
      <td>None</td>
      <td>6/23/15</td>
      <td>2598</td>
      <td>5.8</td>
      <td>2015</td>
      <td>1.425999e+08</td>
      <td>4.053551e+08</td>
    </tr>
    <tr>
      <th>7</th>
      <td>286217</td>
      <td>tt3659388</td>
      <td>7.667400</td>
      <td>108000000</td>
      <td>595380321</td>
      <td>The Martian</td>
      <td>Michael PeÃ±a</td>
      <td>Ridley Scott</td>
      <td>During a manned mission to Mars, Astronaut Mar...</td>
      <td>141</td>
      <td>None</td>
      <td>TSG Entertainment</td>
      <td>9/30/15</td>
      <td>4572</td>
      <td>7.6</td>
      <td>2015</td>
      <td>9.935996e+07</td>
      <td>5.477497e+08</td>
    </tr>
    <tr>
      <th>8</th>
      <td>211672</td>
      <td>tt2293640</td>
      <td>7.404165</td>
      <td>74000000</td>
      <td>1156730962</td>
      <td>Minions</td>
      <td>Steve Coogan</td>
      <td>Kyle Balda|Pierre Coffin</td>
      <td>Minions Stuart, Kevin and Bob are recruited by...</td>
      <td>91</td>
      <td>None</td>
      <td>None</td>
      <td>6/17/15</td>
      <td>2893</td>
      <td>6.5</td>
      <td>2015</td>
      <td>6.807997e+07</td>
      <td>1.064192e+09</td>
    </tr>
    <tr>
      <th>9</th>
      <td>150540</td>
      <td>tt2096673</td>
      <td>6.326804</td>
      <td>175000000</td>
      <td>853708609</td>
      <td>Inside Out</td>
      <td>Lewis Black</td>
      <td>Pete Docter</td>
      <td>Growing up can be a bumpy road, and it's no ex...</td>
      <td>94</td>
      <td>None</td>
      <td>None</td>
      <td>6/9/15</td>
      <td>3935</td>
      <td>8.0</td>
      <td>2015</td>
      <td>1.609999e+08</td>
      <td>7.854116e+08</td>
    </tr>
    <tr>
      <th>10</th>
      <td>206647</td>
      <td>tt2379713</td>
      <td>6.200282</td>
      <td>245000000</td>
      <td>880674609</td>
      <td>Spectre</td>
      <td>Monica Bellucci</td>
      <td>Sam Mendes</td>
      <td>A cryptic message from Bondâ€™s past sends him...</td>
      <td>148</td>
      <td>None</td>
      <td>None</td>
      <td>10/26/15</td>
      <td>3254</td>
      <td>6.2</td>
      <td>2015</td>
      <td>2.253999e+08</td>
      <td>8.102203e+08</td>
    </tr>
    <tr>
      <th>11</th>
      <td>76757</td>
      <td>tt1617661</td>
      <td>6.189369</td>
      <td>176000003</td>
      <td>183987723</td>
      <td>Jupiter Ascending</td>
      <td>Douglas Booth</td>
      <td>Lana Wachowski|Lilly Wachowski</td>
      <td>In a universe where human genetic material is ...</td>
      <td>124</td>
      <td>None</td>
      <td>None</td>
      <td>2/4/15</td>
      <td>1937</td>
      <td>5.2</td>
      <td>2015</td>
      <td>1.619199e+08</td>
      <td>1.692686e+08</td>
    </tr>
    <tr>
      <th>12</th>
      <td>264660</td>
      <td>tt0470752</td>
      <td>6.118847</td>
      <td>15000000</td>
      <td>36869414</td>
      <td>Ex Machina</td>
      <td>Corey Johnson</td>
      <td>Alex Garland</td>
      <td>Caleb, a 26 year old coder at the world's larg...</td>
      <td>108</td>
      <td>None</td>
      <td>None</td>
      <td>1/21/15</td>
      <td>2854</td>
      <td>7.6</td>
      <td>2015</td>
      <td>1.379999e+07</td>
      <td>3.391985e+07</td>
    </tr>
    <tr>
      <th>13</th>
      <td>257344</td>
      <td>tt2120120</td>
      <td>5.984995</td>
      <td>88000000</td>
      <td>243637091</td>
      <td>Pixels</td>
      <td>Kevin James</td>
      <td>Chris Columbus</td>
      <td>Video game experts are recruited by the milita...</td>
      <td>105</td>
      <td>None</td>
      <td>None</td>
      <td>7/16/15</td>
      <td>1575</td>
      <td>5.8</td>
      <td>2015</td>
      <td>8.095996e+07</td>
      <td>2.241460e+08</td>
    </tr>
    <tr>
      <th>14</th>
      <td>99861</td>
      <td>tt2395427</td>
      <td>5.944927</td>
      <td>280000000</td>
      <td>1405035767</td>
      <td>Avengers: Age of Ultron</td>
      <td>Scarlett Johansson</td>
      <td>Joss Whedon</td>
      <td>When Tony Stark tries to jumpstart a dormant p...</td>
      <td>141</td>
      <td>None</td>
      <td>None</td>
      <td>4/22/15</td>
      <td>4304</td>
      <td>7.4</td>
      <td>2015</td>
      <td>2.575999e+08</td>
      <td>1.292632e+09</td>
    </tr>
    <tr>
      <th>15</th>
      <td>273248</td>
      <td>tt3460252</td>
      <td>5.898400</td>
      <td>44000000</td>
      <td>155760117</td>
      <td>The Hateful Eight</td>
      <td>DemiÃ¡n Bichir</td>
      <td>Quentin Tarantino</td>
      <td>Bounty hunters seek shelter from a raging bliz...</td>
      <td>167</td>
      <td>None</td>
      <td>None</td>
      <td>12/25/15</td>
      <td>2389</td>
      <td>7.4</td>
      <td>2015</td>
      <td>4.047998e+07</td>
      <td>1.432992e+08</td>
    </tr>
    <tr>
      <th>16</th>
      <td>260346</td>
      <td>tt2446042</td>
      <td>5.749758</td>
      <td>48000000</td>
      <td>325771424</td>
      <td>Taken 3</td>
      <td>Dougray Scott</td>
      <td>Olivier Megaton</td>
      <td>Ex-government operative Bryan Mills finds his ...</td>
      <td>109</td>
      <td>None</td>
      <td>CinÃ©+</td>
      <td>1/1/15</td>
      <td>1578</td>
      <td>6.1</td>
      <td>2015</td>
      <td>4.415998e+07</td>
      <td>2.997096e+08</td>
    </tr>
    <tr>
      <th>17</th>
      <td>102899</td>
      <td>tt0478970</td>
      <td>5.573184</td>
      <td>130000000</td>
      <td>518602163</td>
      <td>Ant-Man</td>
      <td>Bobby Cannavale</td>
      <td>Peyton Reed</td>
      <td>Armed with the astonishing ability to shrink i...</td>
      <td>115</td>
      <td>None</td>
      <td>None</td>
      <td>7/14/15</td>
      <td>3779</td>
      <td>7.0</td>
      <td>2015</td>
      <td>1.195999e+08</td>
      <td>4.771138e+08</td>
    </tr>
    <tr>
      <th>18</th>
      <td>150689</td>
      <td>tt1661199</td>
      <td>5.556818</td>
      <td>95000000</td>
      <td>542351353</td>
      <td>Cinderella</td>
      <td>Holliday Grainger</td>
      <td>Kenneth Branagh</td>
      <td>When her father unexpectedly passes away, youn...</td>
      <td>112</td>
      <td>None</td>
      <td>None</td>
      <td>3/12/15</td>
      <td>1495</td>
      <td>6.8</td>
      <td>2015</td>
      <td>8.739996e+07</td>
      <td>4.989630e+08</td>
    </tr>
    <tr>
      <th>19</th>
      <td>131634</td>
      <td>tt1951266</td>
      <td>5.476958</td>
      <td>160000000</td>
      <td>650523427</td>
      <td>The Hunger Games: Mockingjay - Part 2</td>
      <td>Elizabeth Banks</td>
      <td>Francis Lawrence</td>
      <td>With the nation of Panem in a full scale war, ...</td>
      <td>136</td>
      <td>None</td>
      <td>Color Force</td>
      <td>11/18/15</td>
      <td>2380</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.471999e+08</td>
      <td>5.984813e+08</td>
    </tr>
    <tr>
      <th>20</th>
      <td>158852</td>
      <td>tt1964418</td>
      <td>5.462138</td>
      <td>190000000</td>
      <td>209035668</td>
      <td>Tomorrowland</td>
      <td>Hugh Laurie</td>
      <td>Brad Bird</td>
      <td>Bound by a shared destiny, a bright, optimisti...</td>
      <td>130</td>
      <td>Mystery</td>
      <td>None</td>
      <td>5/19/15</td>
      <td>1899</td>
      <td>6.2</td>
      <td>2015</td>
      <td>1.747999e+08</td>
      <td>1.923127e+08</td>
    </tr>
    <tr>
      <th>21</th>
      <td>307081</td>
      <td>tt1798684</td>
      <td>5.337064</td>
      <td>30000000</td>
      <td>91709827</td>
      <td>Southpaw</td>
      <td>50 Cent</td>
      <td>Antoine Fuqua</td>
      <td>Billy "The Great" Hope, the reigning junior mi...</td>
      <td>123</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/15</td>
      <td>1386</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.759999e+07</td>
      <td>8.437300e+07</td>
    </tr>
    <tr>
      <th>22</th>
      <td>254128</td>
      <td>tt2126355</td>
      <td>4.907832</td>
      <td>110000000</td>
      <td>470490832</td>
      <td>San Andreas</td>
      <td>Archie Panjabi</td>
      <td>Brad Peyton</td>
      <td>In the aftermath of a massive earthquake in Ca...</td>
      <td>114</td>
      <td>None</td>
      <td>None</td>
      <td>5/27/15</td>
      <td>2060</td>
      <td>6.1</td>
      <td>2015</td>
      <td>1.012000e+08</td>
      <td>4.328514e+08</td>
    </tr>
    <tr>
      <th>23</th>
      <td>216015</td>
      <td>tt2322441</td>
      <td>4.710402</td>
      <td>40000000</td>
      <td>569651467</td>
      <td>Fifty Shades of Grey</td>
      <td>Victor Rasuk</td>
      <td>Sam Taylor-Johnson</td>
      <td>When college senior Anastasia Steele steps in ...</td>
      <td>125</td>
      <td>None</td>
      <td>None</td>
      <td>2/11/15</td>
      <td>1865</td>
      <td>5.3</td>
      <td>2015</td>
      <td>3.679998e+07</td>
      <td>5.240791e+08</td>
    </tr>
    <tr>
      <th>24</th>
      <td>318846</td>
      <td>tt1596363</td>
      <td>4.648046</td>
      <td>28000000</td>
      <td>133346506</td>
      <td>The Big Short</td>
      <td>Melissa Leo</td>
      <td>Adam McKay</td>
      <td>The men who made millions from a global econom...</td>
      <td>130</td>
      <td>None</td>
      <td>None</td>
      <td>12/11/15</td>
      <td>1545</td>
      <td>7.3</td>
      <td>2015</td>
      <td>2.575999e+07</td>
      <td>1.226787e+08</td>
    </tr>
    <tr>
      <th>25</th>
      <td>177677</td>
      <td>tt2381249</td>
      <td>4.566713</td>
      <td>150000000</td>
      <td>682330139</td>
      <td>Mission: Impossible - Rogue Nation</td>
      <td>Ving Rhames</td>
      <td>Christopher McQuarrie</td>
      <td>Ethan and team take on their most impossible m...</td>
      <td>131</td>
      <td>None</td>
      <td>TC Productions</td>
      <td>7/23/15</td>
      <td>2349</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>6.277435e+08</td>
    </tr>
    <tr>
      <th>26</th>
      <td>214756</td>
      <td>tt2637276</td>
      <td>4.564549</td>
      <td>68000000</td>
      <td>215863606</td>
      <td>Ted 2</td>
      <td>Giovanni Ribisi</td>
      <td>Seth MacFarlane</td>
      <td>Newlywed couple Ted and Tami-Lynn want to have...</td>
      <td>115</td>
      <td>None</td>
      <td>None</td>
      <td>6/25/15</td>
      <td>1666</td>
      <td>6.3</td>
      <td>2015</td>
      <td>6.255997e+07</td>
      <td>1.985944e+08</td>
    </tr>
    <tr>
      <th>27</th>
      <td>207703</td>
      <td>tt2802144</td>
      <td>4.503789</td>
      <td>81000000</td>
      <td>403802136</td>
      <td>Kingsman: The Secret Service</td>
      <td>Mark Strong</td>
      <td>Matthew Vaughn</td>
      <td>The story of a super-secret spy organization t...</td>
      <td>130</td>
      <td>None</td>
      <td>None</td>
      <td>1/24/15</td>
      <td>3833</td>
      <td>7.6</td>
      <td>2015</td>
      <td>7.451997e+07</td>
      <td>3.714978e+08</td>
    </tr>
    <tr>
      <th>28</th>
      <td>314365</td>
      <td>tt1895587</td>
      <td>4.062293</td>
      <td>20000000</td>
      <td>88346473</td>
      <td>Spotlight</td>
      <td>John Slattery</td>
      <td>Tom McCarthy</td>
      <td>The true story of how The Boston Globe uncover...</td>
      <td>128</td>
      <td>None</td>
      <td>Entertainment One Features</td>
      <td>11/6/15</td>
      <td>1559</td>
      <td>7.8</td>
      <td>2015</td>
      <td>1.839999e+07</td>
      <td>8.127872e+07</td>
    </tr>
    <tr>
      <th>29</th>
      <td>294254</td>
      <td>tt4046784</td>
      <td>3.968891</td>
      <td>61000000</td>
      <td>311256926</td>
      <td>Maze Runner: The Scorch Trials</td>
      <td>Aidan Gillen</td>
      <td>Wes Ball</td>
      <td>Thomas and his fellow Gladers face their great...</td>
      <td>132</td>
      <td>None</td>
      <td>None</td>
      <td>9/9/15</td>
      <td>1849</td>
      <td>6.4</td>
      <td>2015</td>
      <td>5.611998e+07</td>
      <td>2.863562e+08</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9740</th>
      <td>12639</td>
      <td>tt0060897</td>
      <td>0.310688</td>
      <td>0</td>
      <td>0</td>
      <td>Return of the Seven</td>
      <td>Claude Akins</td>
      <td>Burt Kennedy</td>
      <td>Chico one of the remaining members of The Magn...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>10/19/66</td>
      <td>14</td>
      <td>5.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9741</th>
      <td>5923</td>
      <td>tt0060934</td>
      <td>0.299911</td>
      <td>12000000</td>
      <td>20000000</td>
      <td>The Sand Pebbles</td>
      <td>Emmanuelle Arsan</td>
      <td>Robert Wise</td>
      <td>Engineer Jake Holman arrives aboard the gunboa...</td>
      <td>182</td>
      <td>Romance</td>
      <td>None</td>
      <td>12/20/66</td>
      <td>28</td>
      <td>7.0</td>
      <td>1966</td>
      <td>8.061618e+07</td>
      <td>1.343603e+08</td>
    </tr>
    <tr>
      <th>9742</th>
      <td>38720</td>
      <td>tt0061170</td>
      <td>0.239435</td>
      <td>0</td>
      <td>0</td>
      <td>Walk Don't Run</td>
      <td>Miiko Taka</td>
      <td>Charles Walters</td>
      <td>British industrialist Sir William Rutland - "B...</td>
      <td>114</td>
      <td>None</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9743</th>
      <td>19728</td>
      <td>tt0060177</td>
      <td>0.291704</td>
      <td>0</td>
      <td>0</td>
      <td>The Blue Max</td>
      <td>Karl Michael Vogler</td>
      <td>John Guillermin</td>
      <td>A young pilot in the German air force of 1918,...</td>
      <td>156</td>
      <td>None</td>
      <td>None</td>
      <td>6/21/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9744</th>
      <td>22383</td>
      <td>tt0060862</td>
      <td>0.151845</td>
      <td>0</td>
      <td>0</td>
      <td>The Professionals</td>
      <td>Jack Palance</td>
      <td>Richard Brooks</td>
      <td>The Professionals is a 1966 American Western f...</td>
      <td>117</td>
      <td>None</td>
      <td>None</td>
      <td>11/1/66</td>
      <td>21</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9745</th>
      <td>13353</td>
      <td>tt0060550</td>
      <td>0.276133</td>
      <td>0</td>
      <td>0</td>
      <td>It's the Great Pumpkin, Charlie Brown</td>
      <td>Gail DeFaria</td>
      <td>Bill Melendez</td>
      <td>This classic "Peanuts" tale focuses on the thu...</td>
      <td>25</td>
      <td>None</td>
      <td>None</td>
      <td>10/27/66</td>
      <td>49</td>
      <td>7.2</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9746</th>
      <td>34388</td>
      <td>tt0060437</td>
      <td>0.102530</td>
      <td>0</td>
      <td>0</td>
      <td>Funeral in Berlin</td>
      <td>Guy Doleman</td>
      <td>Guy Hamilton</td>
      <td>Colonel Stok, a Soviet intelligence officer re...</td>
      <td>102</td>
      <td>None</td>
      <td>None</td>
      <td>12/22/66</td>
      <td>13</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9747</th>
      <td>42701</td>
      <td>tt0062262</td>
      <td>0.264925</td>
      <td>75000</td>
      <td>0</td>
      <td>The Shooting</td>
      <td>Charles Eastman</td>
      <td>Monte Hellman</td>
      <td>A hired gun seeks to enact revenge on a group ...</td>
      <td>82</td>
      <td>None</td>
      <td>None</td>
      <td>10/23/66</td>
      <td>12</td>
      <td>5.5</td>
      <td>1966</td>
      <td>5.038511e+05</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9748</th>
      <td>29710</td>
      <td>tt0060588</td>
      <td>0.252399</td>
      <td>0</td>
      <td>0</td>
      <td>Khartoum</td>
      <td>Alexander Knox</td>
      <td>Basil Dearden|Eliot Elisofon</td>
      <td>English General Charles George Gordon, a devou...</td>
      <td>134</td>
      <td>Action</td>
      <td>None</td>
      <td>6/9/66</td>
      <td>12</td>
      <td>5.8</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9749</th>
      <td>23728</td>
      <td>tt0059557</td>
      <td>0.236098</td>
      <td>0</td>
      <td>0</td>
      <td>Our Man Flint</td>
      <td>Benson Fong</td>
      <td>Daniel Mann</td>
      <td>When scientists use eco-terrorism to impose th...</td>
      <td>108</td>
      <td>None</td>
      <td>None</td>
      <td>1/16/66</td>
      <td>13</td>
      <td>5.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9750</th>
      <td>5065</td>
      <td>tt0059014</td>
      <td>0.230873</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Cowboy</td>
      <td>Charles Hawtrey</td>
      <td>Gerald Thomas</td>
      <td>Stodge City is in the grip of the Rumpo Kid an...</td>
      <td>93</td>
      <td>None</td>
      <td>None</td>
      <td>3/1/66</td>
      <td>15</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9751</th>
      <td>17102</td>
      <td>tt0059127</td>
      <td>0.212716</td>
      <td>0</td>
      <td>0</td>
      <td>Dracula: Prince of Darkness</td>
      <td>Suzan Farmer</td>
      <td>Terence Fisher</td>
      <td>Whilst vacationing in the Carpathian Mountain,...</td>
      <td>90</td>
      <td>None</td>
      <td>None</td>
      <td>1/9/66</td>
      <td>16</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9752</th>
      <td>28763</td>
      <td>tt0060548</td>
      <td>0.034555</td>
      <td>0</td>
      <td>0</td>
      <td>Island of Terror</td>
      <td>Sam Kydd</td>
      <td>Terence Fisher</td>
      <td>A small island community is overrun with creep...</td>
      <td>89</td>
      <td>None</td>
      <td>None</td>
      <td>6/20/66</td>
      <td>13</td>
      <td>5.3</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9753</th>
      <td>2161</td>
      <td>tt0060397</td>
      <td>0.207257</td>
      <td>5115000</td>
      <td>12000000</td>
      <td>Fantastic Voyage</td>
      <td>Arthur O'Connell</td>
      <td>Richard Fleischer</td>
      <td>The science of miniaturization has been unlock...</td>
      <td>100</td>
      <td>None</td>
      <td>None</td>
      <td>8/24/66</td>
      <td>42</td>
      <td>6.7</td>
      <td>1966</td>
      <td>3.436265e+07</td>
      <td>8.061618e+07</td>
    </tr>
    <tr>
      <th>9754</th>
      <td>28270</td>
      <td>tt0060445</td>
      <td>0.206537</td>
      <td>0</td>
      <td>0</td>
      <td>Gambit</td>
      <td>Roger C. Carmel</td>
      <td>Ronald Neame</td>
      <td>Harry Dean (Michael Caine) has a perfect plan ...</td>
      <td>109</td>
      <td>None</td>
      <td>None</td>
      <td>12/16/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9755</th>
      <td>26268</td>
      <td>tt0060490</td>
      <td>0.202473</td>
      <td>0</td>
      <td>0</td>
      <td>Harper</td>
      <td>Janet Leigh</td>
      <td>Jack Smight</td>
      <td>Harper is a cynical private eye in the best tr...</td>
      <td>121</td>
      <td>Mystery</td>
      <td>None</td>
      <td>2/23/66</td>
      <td>14</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9756</th>
      <td>15347</td>
      <td>tt0060182</td>
      <td>0.342791</td>
      <td>0</td>
      <td>0</td>
      <td>Born Free</td>
      <td>Omar Chambati</td>
      <td>James Hill</td>
      <td>Born Free (1966) is an Open Road Films Ltd./Co...</td>
      <td>95</td>
      <td>Foreign</td>
      <td>None</td>
      <td>6/22/66</td>
      <td>15</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9757</th>
      <td>37301</td>
      <td>tt0060165</td>
      <td>0.227220</td>
      <td>0</td>
      <td>0</td>
      <td>A Big Hand for the Little Lady</td>
      <td>Charles Bickford</td>
      <td>Fielder Cook</td>
      <td>A naive traveler in Laredo gets involved in a ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>5/31/66</td>
      <td>11</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9758</th>
      <td>31602</td>
      <td>tt0060232</td>
      <td>0.146402</td>
      <td>0</td>
      <td>0</td>
      <td>The Chase</td>
      <td>Angie Dickinson</td>
      <td>Arthur Penn</td>
      <td>Most everyone in town thinks that Sheriff Cald...</td>
      <td>135</td>
      <td>None</td>
      <td>None</td>
      <td>2/17/66</td>
      <td>17</td>
      <td>6.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9759</th>
      <td>13343</td>
      <td>tt0059221</td>
      <td>0.141026</td>
      <td>700000</td>
      <td>0</td>
      <td>The Ghost &amp; Mr. Chicken</td>
      <td>Skip Homeier</td>
      <td>Alan Rafkin</td>
      <td>Luther Heggs aspires to being a reporter for h...</td>
      <td>90</td>
      <td>None</td>
      <td>None</td>
      <td>1/20/66</td>
      <td>14</td>
      <td>6.1</td>
      <td>1966</td>
      <td>4.702610e+06</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9760</th>
      <td>20277</td>
      <td>tt0061135</td>
      <td>0.140934</td>
      <td>0</td>
      <td>0</td>
      <td>The Ugly Dachshund</td>
      <td>Parley Baer</td>
      <td>Norman Tokar</td>
      <td>The Garrisons (Dean Jones and Suzanne Pleshett...</td>
      <td>93</td>
      <td>None</td>
      <td>None</td>
      <td>2/16/66</td>
      <td>14</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9761</th>
      <td>5921</td>
      <td>tt0060748</td>
      <td>0.131378</td>
      <td>0</td>
      <td>0</td>
      <td>Nevada Smith</td>
      <td>Suzanne Pleshette</td>
      <td>Henry Hathaway</td>
      <td>Nevada Smith is the young son of an Indian mot...</td>
      <td>128</td>
      <td>None</td>
      <td>None</td>
      <td>6/10/66</td>
      <td>10</td>
      <td>5.9</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9762</th>
      <td>31918</td>
      <td>tt0060921</td>
      <td>0.317824</td>
      <td>0</td>
      <td>0</td>
      <td>The Russians Are Coming, The Russians Are Coming</td>
      <td>Paul Ford</td>
      <td>Norman Jewison</td>
      <td>Without hostile intent, a Soviet sub runs agro...</td>
      <td>126</td>
      <td>None</td>
      <td>None</td>
      <td>5/25/66</td>
      <td>11</td>
      <td>5.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9763</th>
      <td>20620</td>
      <td>tt0060955</td>
      <td>0.089072</td>
      <td>0</td>
      <td>0</td>
      <td>Seconds</td>
      <td>Jeff Corey</td>
      <td>John Frankenheimer</td>
      <td>A secret organisation offers wealthy people a ...</td>
      <td>100</td>
      <td>None</td>
      <td>None</td>
      <td>10/5/66</td>
      <td>22</td>
      <td>6.6</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9764</th>
      <td>5060</td>
      <td>tt0060214</td>
      <td>0.087034</td>
      <td>0</td>
      <td>0</td>
      <td>Carry On Screaming!</td>
      <td>Charles Hawtrey</td>
      <td>Gerald Thomas</td>
      <td>The sinister Dr Watt has an evil scheme going....</td>
      <td>87</td>
      <td>None</td>
      <td>None</td>
      <td>5/20/66</td>
      <td>13</td>
      <td>7.0</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9765</th>
      <td>21</td>
      <td>tt0060371</td>
      <td>0.080598</td>
      <td>0</td>
      <td>0</td>
      <td>The Endless Summer</td>
      <td>Chip Fitzwater</td>
      <td>Bruce Brown</td>
      <td>The Endless Summer, by Bruce Brown, is one of ...</td>
      <td>95</td>
      <td>None</td>
      <td>None</td>
      <td>6/15/66</td>
      <td>11</td>
      <td>7.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9766</th>
      <td>20379</td>
      <td>tt0060472</td>
      <td>0.065543</td>
      <td>0</td>
      <td>0</td>
      <td>Grand Prix</td>
      <td>Brian Bedford</td>
      <td>John Frankenheimer</td>
      <td>Grand Prix driver Pete Aron is fired by his te...</td>
      <td>176</td>
      <td>None</td>
      <td>None</td>
      <td>12/21/66</td>
      <td>20</td>
      <td>5.7</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9767</th>
      <td>39768</td>
      <td>tt0060161</td>
      <td>0.065141</td>
      <td>0</td>
      <td>0</td>
      <td>Beregis Avtomobilya</td>
      <td>Lyubov Dobrzhanskaya</td>
      <td>Eldar Ryazanov</td>
      <td>An insurance agent who moonlights as a carthie...</td>
      <td>94</td>
      <td>None</td>
      <td>None</td>
      <td>1/1/66</td>
      <td>11</td>
      <td>6.5</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9768</th>
      <td>21449</td>
      <td>tt0061177</td>
      <td>0.064317</td>
      <td>0</td>
      <td>0</td>
      <td>What's Up, Tiger Lily?</td>
      <td>Tadao Nakamaru</td>
      <td>Woody Allen</td>
      <td>In comic Woody Allen's film debut, he took the...</td>
      <td>80</td>
      <td>None</td>
      <td>None</td>
      <td>11/2/66</td>
      <td>22</td>
      <td>5.4</td>
      <td>1966</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>9769</th>
      <td>22293</td>
      <td>tt0060666</td>
      <td>0.035919</td>
      <td>19000</td>
      <td>0</td>
      <td>Manos: The Hands of Fate</td>
      <td>Stephanie Nielson</td>
      <td>Harold P. Warren</td>
      <td>A family gets lost on the road and stumbles up...</td>
      <td>74</td>
      <td>None</td>
      <td>None</td>
      <td>11/15/66</td>
      <td>15</td>
      <td>1.5</td>
      <td>1966</td>
      <td>1.276423e+05</td>
      <td>0.000000e+00</td>
    </tr>
  </tbody>
</table>
<p>9770 rows × 18 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="merge-all-of-these-rows-into-one:">merge all of these rows into one:<a class="anchor-link" href="#merge-all-of-these-rows-into-one:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span> <span class="o">=</span><span class="n">df1</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">df2</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">df3</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">df4</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">df5</span><span class="p">,</span><span class="n">ignore_index</span> <span class="o">=</span> <span class="kc">True</span><span class="p">),</span><span class="n">ignore_index</span> <span class="o">=</span> <span class="kc">True</span><span class="p">),</span><span class="n">ignore_index</span> <span class="o">=</span> <span class="kc">True</span><span class="p">),</span><span class="n">ignore_index</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-missing-data:">Check for missing data:<a class="anchor-link" href="#Check-for-missing-data:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[22]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>id                          0
imdb_id                     0
popularity                  0
budget                      0
revenue                     0
original_title              0
cast                      840
director                    0
overview                    0
runtime                     0
genres                  24207
production_companies    25709
release_date                0
vote_count                  0
vote_average                0
release_year                0
budget_adj                  0
revenue_adj                 0
dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Drop-missing-data:">Drop missing data:<a class="anchor-link" href="#Drop-missing-data:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-again:">Check again:<a class="anchor-link" href="#Check-again:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[24]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>id                      0
imdb_id                 0
popularity              0
budget                  0
revenue                 0
original_title          0
cast                    0
director                0
overview                0
runtime                 0
genres                  0
production_companies    0
release_date            0
vote_count              0
vote_average            0
release_year            0
budget_adj              0
revenue_adj             0
dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Check-for-duplicates:">Check for duplicates:<a class="anchor-link" href="#Check-for-duplicates:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">duplicated</span><span class="p">()</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[25]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Get-the-indexes-to-the-default-again:">Get the indexes to the default again:<a class="anchor-link" href="#Get-the-indexes-to-the-default-again:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">reset_index</span><span class="p">(</span><span class="n">drop</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Investigation-the-three-columns-in-the-new-data-set:">Investigation the three columns in the new data set:<a class="anchor-link" href="#Investigation-the-three-columns-in-the-new-data-set:">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[27]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(17310, 18)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">genres</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[28]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Drama              3463
Comedy             2772
Action             1943
Thriller           1629
Horror             1220
Adventure          1024
Crime               885
Romance             832
Science Fiction     599
Fantasy             535
Family              468
Animation           460
Mystery             452
Documentary         281
Music               199
History             198
War                 158
Western              83
TV Movie             73
Foreign              36
Name: genres, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[59]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">cast</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[59]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Robert De Niro           57
Nicolas Cage             54
Bruce Willis             50
Clint Eastwood           42
Johnny Depp              41
Robin Williams           40
John Travolta            40
Samuel L. Jackson        40
Harrison Ford            39
Tom Hanks                39
Sylvester Stallone       38
John Cusack              38
Jean-Claude Van Damme    35
Morgan Freeman           35
Meryl Streep             34
Al Pacino                33
Denzel Washington        33
Eddie Murphy             33
Liam Neeson              33
Mel Gibson               32
Steve Martin             32
Nicole Kidman            32
Richard Gere             32
Tom Cruise               32
Sean Connery             31
Kevin Costner            31
Gene Hackman             31
Michael Caine            31
Adam Sandler             30
Matt Damon               30
                         ..
Uta Hagen                 1
Jimmy Somerville          1
Jake Abel                 1
Kou Shibasaki             1
Matthew Marsden           1
Linus Roache              1
Jack MacGowran            1
Stephen Spinella          1
Kevin Durant              1
Pamela Conrad             1
Peter Robbins             1
John Boyega               1
Collin Blackard           1
John Waters               1
Ha Ji-won                 1
Scot Williams             1
Kurt Fuller               1
Marc Price                1
RÃºaidhrÃ­ Conroy         1
Paul Shaffer              1
June Diane Raphael        1
Raymond Cruz              1
Julia Winter              1
Frank Finlay              1
James Hong                1
Ahn Jae-mo                1
Grace Thorsen             1
Andrzej Chyra             1
AndrÃ¡s SÃ¼tÃ¶            1
Brent Roam                1
Name: cast, Length: 6140, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">production_companies</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[35]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Universal Pictures                        508
Paramount Pictures                        430
Warner Bros.                              392
Twentieth Century Fox Film Corporation    277
Columbia Pictures                         272
New Line Cinema                           219
Walt Disney Pictures                      213
Metro-Goldwyn-Mayer (MGM)                 176
Columbia Pictures Corporation             152
Touchstone Pictures                       146
TriStar Pictures                          144
Miramax Films                             137
20th Century Fox                           88
DreamWorks SKG                             86
Village Roadshow Pictures                  86
BBC Films                                  83
Regency Enterprises                        82
United Artists                             76
Orion Pictures                             72
Fox Searchlight Pictures                   68
Dimension Films                            67
Amblin Entertainment                       63
Castle Rock Entertainment                  60
Summit Entertainment                       59
Lions Gate Films                           56
Lionsgate                                  55
Imagine Entertainment                      54
DC Comics                                  53
Hollywood Pictures                         53
StudioCanal                                50
                                         ... 
CoPilot Pictures                            1
Snowfall Films                              1
Seven8 Media                                1
Alexander Groupe                            1
Storefront Pictures                         1
Film Direction                              1
Green Screen Productions                    1
JSM productions1                            1
International Movie Service S.r.l.          1
Rapid Film                                  1
TPW Films                                   1
Lost Witness Pictures                       1
RMB Productions                             1
AMC Pictures                                1
V/M Productions                             1
JCE Entertainment Ltd,                      1
TriStar Television                          1
E3W Productions                             1
DareDevil Films                             1
Producciones Amaranta                       1
Silverstein / Barder Company                1
G4 Pictures                                 1
Bedlam Productions                          1
Great Southern Land Entertainment           1
Blue Yonder Films                           1
Shoot Productions                           1
WhiteFlame Productions                      1
Shamley Productions                         1
IRS Media                                   1
Hernany Perla Films                         1
Name: production_companies, Length: 5601, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[66]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">runtime</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[66]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>90     763
95     550
100    541
93     510
97     500
94     474
96     471
91     454
105    439
98     427
92     424
102    414
88     410
101    409
99     378
108    377
104    364
89     358
103    353
106    352
107    349
110    341
85     330
87     314
86     272
109    263
112    257
113    247
115    244
111    229
      ... 
199      2
54       2
229      2
292      2
213      2
372      2
219      1
31       1
19       1
877      1
51       1
36       1
29       1
300      1
236      1
28       1
235      1
336      1
470      1
500      1
17       1
42       1
49       1
242      1
216      1
705      1
40       1
24       1
566      1
233      1
Name: runtime, Length: 223, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Remove-unwanted-columns-from-our-data:">Remove unwanted columns from our data:<a class="anchor-link" href="#Remove-unwanted-columns-from-our-data:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s2">&quot;id&quot;</span><span class="p">,</span><span class="s2">&quot;imdb_id&quot;</span><span class="p">,</span><span class="s2">&quot;overview&quot;</span><span class="p">,</span><span class="s2">&quot;budget&quot;</span><span class="p">,</span><span class="s2">&quot;budget_adj&quot;</span><span class="p">,],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='eda'></a></p>
<h2 id="Exploratory-Data-Analysis">Exploratory Data Analysis<a class="anchor-link" href="#Exploratory-Data-Analysis">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[30]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># make a mask for our dependent variable</span>
<span class="n">high_revenue</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">revenue</span> <span class="o">&gt;</span> <span class="n">df</span><span class="o">.</span><span class="n">revenue</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">low_revenue</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">revenue</span> <span class="o">&lt;</span> <span class="n">df</span><span class="o">.</span><span class="n">revenue</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="There-was-a-relation-between-high-revenue-movie-and-its-vote-average?">There was a relation between high revenue movie and its vote average?<a class="anchor-link" href="#There-was-a-relation-between-high-revenue-movie-and-its-vote-average?">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="find-the-mean-of-vote_average-according-to-high-revenue-:">find the mean of vote_average according to high revenue :<a class="anchor-link" href="#find-the-mean-of-vote_average-according-to-high-revenue-:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[31]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">vote_average</span><span class="p">[</span><span class="n">high_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[31]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>6.2936499872999745</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="find-the-mean-of-vote_average-according-to-high-revenue-:">find the mean of vote_average according to high revenue :<a class="anchor-link" href="#find-the-mean-of-vote_average-according-to-high-revenue-:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">vote_average</span><span class="p">[</span><span class="n">low_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[32]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>5.8762581320571297</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><ul>
<li>So high vote average movies have higher revenue</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="plot-a-multi-histogram-for-the-vote_average-of-high-and-low-revenue-movies:">plot a multi histogram for the vote_average of high and low revenue movies:<a class="anchor-link" href="#plot-a-multi-histogram-for-the-vote_average-of-high-and-low-revenue-movies:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">vote_average</span><span class="p">[</span><span class="n">high_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">alpha</span> <span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;green&quot;</span><span class="p">,</span><span class="n">bins</span><span class="o">=</span><span class="mi">25</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s1">&#39;high_revenue&#39;</span><span class="p">);</span>
<span class="n">df</span><span class="o">.</span><span class="n">vote_average</span><span class="p">[</span><span class="n">low_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">alpha</span> <span class="o">=</span><span class="mf">0.5</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;red&quot;</span><span class="p">,</span><span class="n">bins</span><span class="o">=</span><span class="mi">25</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s1">&#39;low_revenue&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Vote Average&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Frequency&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;vote average cooresponding to revenue&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">();</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><ul>
<li>There is no high colleration between the vote average and high revenue which tell us that maybe most of the votes are fake which makes the movies over rated, but in general high revenue movies have higher vote average than low revenew movies</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Test-if-vote-average-is-critic-or-audience:">Test if vote average is critic or audience:<a class="anchor-link" href="#Test-if-vote-average-is-critic-or-audience:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">,</span> <span class="n">x</span> <span class="o">=</span> <span class="s1">&#39;vote_average&#39;</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s1">&#39;popularity&#39;</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.7</span><span class="p">,</span> <span class="n">marker</span><span class="o">=</span><span class="s1">&#39;1&#39;</span><span class="p">,</span>
            <span class="n">label</span><span class="o">=</span><span class="s2">&quot;rate&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Vote Average&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Popularity&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Popularity vs Vote Average&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="s1">&#39;upper left&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">();</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><ul>
<li>Most of the vote average is critic rating not audience rating</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="There-was-a-relation-between-high-revenue-movie-and-its-duration?">There was a relation between high revenue movie and its duration?<a class="anchor-link" href="#There-was-a-relation-between-high-revenue-movie-and-its-duration?">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="find-the-mean-of-vote_average-according-to-high-revenue-:">find the mean of vote_average according to high revenue :<a class="anchor-link" href="#find-the-mean-of-vote_average-according-to-high-revenue-:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[34]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">runtime</span><span class="p">[</span><span class="n">high_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[34]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>114.12623825247651</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="find-the-mean-of-vote_average-according-to-high-revenue-:">find the mean of vote_average according to high revenue :<a class="anchor-link" href="#find-the-mean-of-vote_average-according-to-high-revenue-:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">runtime</span><span class="p">[</span><span class="n">low_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[35]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>101.60966125775816</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><ul>
<li>So small duration movies have lower revenue</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="plot-a-multi-histogram-for-the-duration-of-high-and-low-revenue-movies:">plot a multi histogram for the duration of high and low revenue movies:<a class="anchor-link" href="#plot-a-multi-histogram-for-the-duration-of-high-and-low-revenue-movies:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">runtime</span><span class="p">[</span><span class="n">high_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">alpha</span> <span class="o">=</span><span class="mf">0.8</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;green&quot;</span><span class="p">,</span><span class="n">bins</span><span class="o">=</span><span class="mi">25</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s1">&#39;high_revenue&#39;</span><span class="p">);</span>
<span class="n">df</span><span class="o">.</span><span class="n">runtime</span><span class="p">[</span><span class="n">low_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">alpha</span> <span class="o">=</span><span class="mf">0.5</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;yellow&quot;</span><span class="p">,</span><span class="n">bins</span><span class="o">=</span><span class="mi">25</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s1">&#39;low_revenue&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Runtime cooresponding to revenue&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Runtime&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Frequency&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">();</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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aAYPHsy4ceNYt24dDz30EF/84her16uoqOC0004D2Kr+WWedxbp164Ds3nuXXXYZgwcP5h/+4R948cXsicPl5eVceeWV1W0dcsghLF26FIDf/va3HHnkkQwaNIjzzz+fzZvrejrw9nHiMLM2bfHixUycOJEXXniB7t27c88991Qv27BhA+effz4PPfQQTz75JCtWrNhq3RdffJFHHnmEZ555hh/+8Ids2rSpzvd56aWXGDduHM899xy77bYbkydP5g9/+APz58/n8MMP56qrrmLkyJHMmTOH9957D4C77rqLMWPGsHLlyq3qDxkyhKuuuqq67T322IP58+fzjW98Y6tkUZtFixZx11138ac//YkFCxbQoUMHbrvttu3pujp5qMrM2rQBAwYwaNAgAI444ojq/8ohSwz77LNP9Rfhxo4dy9SpU6uXf/azn6Vz58507tyZXr168eabb9K3b99a36dfv34MGzYMgDlz5rBw4UKOOeYYIEtQxxxzDB07duTkk0/m/vvvZ/To0fz+97/nZz/7GU888cRW9Tdu3MjRRx9d3fYZZ5xRHf+9995b7/bOnj2befPmMXToUADWr19Pr169iu6vYjhxmFmb1rlz5+rpDh06sH79+ur5hp6AWnPdDz/8sM66hc/biAhGjhzJHXfcAWz9zfExY8Zw7bXX0qNHD4YOHUrXrl23qV9XHIUxdOzYkY8++qi6TtUX+iKC8ePH85Of/KTebdsRThxm1iRa4uWzBxxwAC+//DJLly6lf//+3HXXXY3S7rBhw5g4cSJLlixh33335f3332f58uXst99+DB8+nPPOO48bb7yRMWPG1Fm/srKS/fbbr8736N+/Pw888AAA8+fP55VXXgFgxIgRnH766UyaNIlevXqxevVq1q5dS79+/Rpl28DnOMysHdtll12YMmUKJ598Msceeyy9e/emW7duO9zuxz/+cW655RbGjh3LoYceyogRI6pPanfo0IFTTz2Vhx56qPpEfM36w4YNq65flzPPPJPVq1czaNAgrrvuuuokc9BBBzF58mROPPFEDj30UEaOHMny5ct3eJsKqaFDtdZoyJAh0bKfAFhe4vqNr7U8wawpuU9qV9UvixYt4sADD2zucBq0bt06ysrKiAgmTpzIwIEDmTRpUqO+R0u6yWGV2j4fSfMiosFvavqIw8zatRtvvJFBgwZx8MEH884773D++ec3d0gtns9xmFm7NmnSpKKPMFatWsWIESO2KZ89ezY9e/Zs7NBaLCcOM7Mi9ezZkwULFjR3GM3OQ1VmZpaLE4eZmeXixGFmZrmU9ByHpEnAV4EAnge+AuwJ3An0AOYDX46IjZI6A9OBI4BVwJiIWJrauRg4D9gMXBARj5QybjMrhfIW3p4Vq2RHHJL6ABcAQyLiEKADcDbwU+DqiBgIrCFLCKSfayJiX+DqVA9JB6X1DgZOBqZI6lCquM2s7SgrK2vuENqkUg9VdQR2kdQR2BVYDnwGuDstnwZ8Pk2fnuZJy0coezDu6cCdEfFBRLwCLAGOLHHcZmYNioit7hfVXpRsqCoi/i7pSuA1YD3wKDAPeDsiqu4UVgn0SdN9gGVp3Q8lvQP0TOVzCpouXKeapAnABIDevXtTUVGx3bGvW7duh9Zv2P4561eUIohcSt8nrY/7pHZV/dKtWzfWrl1bXb7zzh806vts3Li24Upk39qOCH7wgx8wa9YsJPGv//qvnHnmmUyaNImRI0cyatQovvSlL9G9e3emTJnC9OnTWbp0KZdeeuk27b366quceeaZHHfccTz77LPcfvvtLF68mCuuuIKNGzcyYMAApkyZwp///Gduu+02pk2bxubNm3nwwQf55S9/yYwZM5g9e/Y29cvKyjjkkEMYO3YsDz/8MJs2bWL69Onst99+XHHFFZSVlXHBBRcAcNRRRzFjxgz69evHnXfeyfXXX8+mTZuqb8feoUPDgzIbNmzY7v23ZIlD0u5kRwsDgLeB3wGn1FK16p4nqmNZXeVbF0RMBaZCdsuRHbkVRMu75cjYUgSRi2+vsS33Se0Kbzmy9W02Ote5zvbo3Lm4W3h07dqVe+65h4ULF/L888+zcuVKhg4dykknncQJJ5zA3LlzGTNmDG+++SYrVqyga9euzJ07l7PPPrvW24SUlZWxePFipk2bxk033cTKlSv5xje+weOPP85uu+3GT3/6U2688UYuueQSJk2aVP0kwPvvv59zzjmHDz74gKuuumqb+pdeeimS6NOnDwsWLGDKlClcd9113HTTTdW3dq+KZ6eddqKsrIzKykpmzpzJnDlz6NSpE9/85jeZOXMm48aNa7BfunTpwuGHH56jx7co5cnxE4BXImIFgKR7gX8EukvqmI46+gKvp/qVwN5AZRra6gasLiivUriOmVmDnnzyScaOHUuHDh3o3bs3n/70p3n22Wc57rjjuOaaa1i4cCEHHXQQa9asYfny5Tz11FP1PvGvvmdvVD1Lo/DZGyeddFKrffZGbUqZOF4DhknalWyoagQwF3gcGE12ZdV44L5Uf2aafyotfywiQtJM4HZJVwF7AQOBZ0oYt5m1MXXdzLVPnz6sWbOGhx9+mOOPP57Vq1czY8YMysrK6r0pYX3P3ihU9eyNLl26tNpnb9SmlOc4npZ0N9kltx8Cz5ENJf0euFPS5FR2c1rlZuBWSUvIjjTOTu28IGkGsDC1MzEiGvcBumbWBMqb7Z2PP/54brjhBsaPH8/q1av54x//yL//+78DcPTRR3PNNdfw2GOPsWrVKkaPHs3o0aOLbru+Z2lUPXsjIhg7dmyD9evSnM/eqE1Jv8cREZcBl9UofplaroqKiA3AWXW0czlweaMHaGbtwhe+8AWeeuopDjvsMCTxs5/9jE984hMAHHfccTz66KPsu+++9OvXj9WrV3PccccV3XbhszQ++CC7AGDy5Mnst99+1c/euOWWW6qf+11f/bqceeaZTJ8+nUGDBjF06NBan73x0Ucf0alTJ6699tqSJw4/j6MWLe/keN76jc8ngrflPqlda3seR1Pw8zjMzKxd823Vzcxq4Wdv1M2Jw8xKJiLIbgDR+rTlZ2/s6CkKD1WZWUl06dKFVatW7fAfKWtcEcGqVavo0qXLdrfhIw4zK4m+fftSWVnJihUrmjuUZrdhw4Yd+kPd2Lp06ULfvn23e30nDjMriU6dOjFgwIDmDqNFqKio2O7be7REHqoyM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxyceIwM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxyceIwM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy6WkiUNSd0l3S3pR0iJJR0vqIWmWpMXp5+6priT9QtISSX+RNLignfGp/mJJ40sZs5mZ1a/URxw/Bx6OiAOAw4BFwEXA7IgYCMxO8wCnAAPTawJwHYCkHsBlwFHAkcBlVcnGzMyaXskSh6SPAccDNwNExMaIeBs4HZiWqk0DPp+mTwemR2YO0F3SnsBJwKyIWB0Ra4BZwMmlitvMzOrXsYRt7wOsAH4j6TBgHvAtoHdELAeIiOWSeqX6fYBlBetXprK6yrciaQLZkQq9e/emoqJiuwNft27dDq3fsP1z1q8oRRC5lL5PWh/3Se3cL9tqa31SysTRERgM/EtEPC3p52wZlqqNaimLesq3LoiYCkwFGDJkSAwfPjx3wFUqKirYkfUbVp6z/thSBJFL6fuk9XGf1M79sq221ielPMdRCVRGxNNp/m6yRPJmGoIi/XyroP7eBev3BV6vp9zMzJpByRJHRLwBLJNUNS4zAlgIzASqrowaD9yXpmcC49LVVcOAd9KQ1iPAiZJ2TyfFT0xlZmbWDEo5VAXwL8BtknYGXga+QpasZkg6D3gNOCvVfRAYBSwB3k91iYjVkn4MPJvq/SgiVpc4bjMzq0NJE0dELACG1LJoRC11A5hYRzu/Bn7duNGZmdn28DfHzcwsFycOMzPLxYnDzMxyKSpxSDqk1IGYmVnrUOwRx/WSnpH0TUndSxqRmZm1aEUljog4FjiH7It4cyXdLmlkSSMzM7MWqehzHBGxGPg+8D3g08Av0u3SzyhVcGZm1vIUe47jUElXk90W/TPAaRFxYJq+uoTxmZlZC1PsFwB/BdwIXBIR66sKI+J1Sd8vSWRmZtYiFZs4RgHrI2IzgKSdgC4R8X5E3Fqy6MzMrMUp9hzHH4BdCuZ3TWVmZtbOFJs4ukTEuqqZNL1raUIyM7OWrNjE8Z6kwVUzko4A1tdT38zM2qhiz3F8G/idpKoHKO0JjClNSGZm1pIVlTgi4llJB5A9LFvAixGxqaSRmZlZi5TneRxDgf5pncMlERHTSxKVmZm1WEUlDkm3Ap8CFgCbU3EAThxmZu1MsUccQ4CD0lP6zMysHSv2qqq/Ap8oZSBmZtY6FHvEsQewUNIzwAdVhRHxuZJEZWZmLVaxiaO8lEGYmVnrUezluE9I6gcMjIg/SNoV6FDa0MzMrCUq9rbqXwPuBm5IRX2A/ypVUGZm1nIVe3J8InAM8C5UP9SpV6mCMjOzlqvYxPFBRGysmpHUkex7HGZm1s4UmziekHQJsEt61vjvgPtLF5aZmbVUxSaOi4AVwPPA+cCDZM8fNzOzdqbYq6o+Int07I2lDcfMzFq6Yu9V9Qq1nNOIiH0aPSIzM2vR8tyrqkoX4CygR+OHY2ZmLV1R5zgiYlXB6+8RcQ3wmRLHZmZmLVCxQ1WDC2Z3IjsC6VqSiMzMrEUrdqjqPwqmPwSWAl9s9GjMzKzFK/aqqv9T6kDMzKx1KHao6v/WtzwirmqccMzMrKXLc1XVUGBmmj8N+COwrBRBmZlZy5XnQU6DI2ItgKRy4HcR8dVSBWZmZi1Tsbcc+SSwsWB+I9C/0aMxM7MWr9jEcSvwjKRySZcBTwPTi1lRUgdJz0l6IM0PkPS0pMWS7pK0cyrvnOaXpOX9C9q4OJW/JOmkPBtoZmaNq9gvAF4OfAVYA7wNfCUirijyPb4FLCqY/ylwdUQMTO2dl8rPA9ZExL7A1akekg4CzgYOBk4Gpkjy0wfNzJpJsUccALsC70bEz4FKSQMaWkFSX+CzwE1pXmTfOL87VZkGfD5Nn57mSctHpPqnA3dGxAcR8QqwBDgyR9xmZtaIir0c9zKyK6v2B34DdAJ+S/ZUwPpcA3yXLd8y7wm8HREfpvlKssfQkn4uA4iIDyW9k+r3AeYUtFm4TmGME4AJAL1796aioqKYTavVunXrdmj9hu2fs35FKYLIpfR90vq4T2rnftlWW+uTYq+q+gJwODAfICJel1TvLUcknQq8FRHzJA2vKq6lajSwrL51thRETAWmAgwZMiSGDx9es0rRKioq2JH1G1aes/7YUgSRS+n7pPVxn9TO/bKtttYnxSaOjRERkgJA0m5FrHMM8DlJo8juqPsxsiOQ7pI6pqOOvsDrqX4lsDfZMFhHoBuwuqC8SuE6ZmbWxIo9xzFD0g1kf/S/BvyBBh7qFBEXR0TfiOhPdnL7sYg4B3gcGJ2qjQfuS9Mz0zxp+WMREan87HTV1QBgIPBMkXGbmVkjK/ZeVVemZ42/SzZAf2lEzNrO9/wecKekycBzwM2p/GbgVklLyI40zk7v/YKkGcBCshssToyIzdv53q1UeYnrm5kVr8HEkS59fSQiTgC2K1lERAXpDG9EvEwtV0VFxAayB0TVtv7lwOXb895mZta4GhyqSv/dvy+pWxPEY2ZmLVyxJ8c3AM9LmgW8V1UYEReUJCozM2uxik0cv08vMzNr5+pNHJI+GRGvRcS0+uqZmVn70dA5jv+qmpB0T4ljMTOzVqChxFH4re19ShmImZm1Dg0ljqhj2szM2qmGTo4fJuldsiOPXdI0aT4i4mMljc7MzFqcehNHRPi5F2ZmtpU8z+MwMzNz4jAzs3ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxyceIwM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxyceIwM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy8WJw8zMcilZ4pC0t6THJS2S9IKkb6XyHpJmSVqcfu6eyiXpF5KWSPqLpMEFbY1P9RdLGl+qmM3MrGGlPOL4EPhORBwIDAMmSjoIuAiYHREDgdlpHuAUYGB6TQCugyzRAJcBRwFHApdVJRszM2t6HUvVcEQsB5an6bWSFgF9gNOB4anaNKAC+F4qnx4RAcyR1F3SnqnurIhYDSBpFnAycEepYm8Jps6b2mCdCUdMaIJIzMy21iTnOCT1Bw4HngZ6p6RSlVx6pWp9gGUFq1WmsrrKzcysGZTsiKOKpDLgHuDbEfGupDqr1lIW9ZTXfJ8JZENc9O7dm4qKiu2KF2DdunU7tH7D9m+wRo/3L2qwTkXFx+taki+cIpS+T1of90nt3C/bamt9UtLEIakTWdK4LSLuTcVvStozIpanoai3UnklsHfB6n2B11P58BrlFTXfKyKmAlMBhgwZEsOHD69ZpWgVFRXsyPoNK2+wRjFDVaPrHKoamy+cIpS+T1of90nt3C/bamt9UsqrqgTcDCyKiKsKFs0Eqq6MGg/cV1A+Ll1dNQx4Jw1lPQKcKGn3dFL8xFRmZmbNoJRHHMcAXwael7QglV0C/BswQ9J5wGvAWWnZg8AoYAnwPvAVgIhYLenHwLOp3o+qTpSbmVnTK+VVVU9S+/kJgBG11A9gYh1t/Rr4deNFZ2Zm28vfHDczs1ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxyceIwM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxyceIwM7NcOjZ3ALb9ps6bWkf5A1vNz50wtynCMbN2wkccZmaWixOHmZnl4qGqZlDXEJOZWWvgIw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy8WJw8zMcnHiMDOzXJw4zMwsFycOMzPLxYnDzMxy8S1H2qAJR7xeo6S8gTUaWm5mtoWPOMzMLBcfcdRqOfn+C89Tt+k1dFPFqfMe8DM7zKxoThyNory5AzAzazKtJnFIOhn4OdABuCki/q2ZQ2ozsnMi5Q3U2r9GnYbqm1lb1SrOcUjqAFwLnAIcBIyVdFDzRmVm1j61liOOI4ElEfEygKQ7gdOBhc0aVRvS0HmQHu9fVKOkvGSxNE37Zra9Wkvi6AMsK5ivBI4qrCBpAjAhza6T9NIOvN8ewModWL8N+lYT98kPm+6ttp8Y53lBAAAFtUlEQVT3k9q5X7bVWvqkXzGVWkviUC1lsdVMxFSgUZ7JKmluRAxpjLbaCvfJttwntXO/bKut9UmrOMdBdoSxd8F8X6Dmt9zMzKwJtJbE8SwwUNIASTsDZwMzmzkmM7N2qVUMVUXEh5L+GXiE7HLcX0fECyV8y0YZ8mpj3Cfbcp/Uzv2yrTbVJ4qIhmuZmZklrWWoyszMWggnDjMzy8WJo4CkkyW9JGmJpJrfeGuzJO0t6XFJiyS9IOlbqbyHpFmSFqefu6dySfpF6qe/SBrcvFtQOpI6SHpO0gNpfoCkp1Of3JUu1kBS5zS/JC3v35xxl5Kk7pLulvRi2meObu/7iqRJ6Xfnr5LukNSlLe8rThxJO7+tyYfAdyLiQGAYMDFt+0XA7IgYCMxO85D10cD0mgBc1/QhN5lvAYsK5n8KXJ36ZA1wXio/D1gTEfsCV6d6bdXPgYcj4gDgMLL+abf7iqQ+wAXAkIg4hOwCnrNpy/tKRPiVXSBwNPBIwfzFwMXNHVcz9cV9wEjgJWDPVLYn8FKavgEYW1C/ul5bepF9X2g28BngAbIvoq4EOtbcZ8iu+Ds6TXdM9dTc21CCPvkY8ErNbWvP+wpb7mzRI332DwAnteV9xUccW9R2W5M+zRRLs0mHzYcDTwO9I2I5QPrZK1VrL311DfBd4KM03xN4OyI+TPOF213dJ2n5O6l+W7MPsAL4TRrCu0nSbrTjfSUi/g5cCbxG9jCfd4B5tOF9xYljiwZva9LWSSoD7gG+HRHv1le1lrI21VeSTgXeioh5hcW1VI0ilrUlHYHBwHURcTjwHluGpWrT5vslnc85HRgA7AXsRjZEV1Ob2VecOLZo17c1kdSJLGncFhH3puI3Je2Zlu8JvJXK20NfHQN8TtJS4E6y4aprgO6Sqr44W7jd1X2SlncDVjdlwE2kEqiMiKfT/N1kiaQ97ysnAK9ExIqI2ATcC/wjbXhfceLYot3e1kSSgJuBRRFxVcGimcD4ND2e7NxHVfm4dMXMMOCdqmGKtiIiLo6IvhHRn2xfeCwizgEeB0anajX7pKqvRqf6req/yGJExBvAMkn7p6IRZI83aLf7CtkQ1TBJu6bfpao+abv7SnOfZGlJL2AU8L/A34D/19zxNOF2H0t2qPwXYEF6jSIbd50NLE4/e6T6IrsC7W/A82RXkzT7dpSwf4YDD6TpfYBngCXA74DOqbxLml+Slu/T3HGXsD8GAXPT/vJfwO7tfV8hew7Ai8BfgVuBzm15X/EtR8zMLBcPVZmZWS5OHGZmlosTh5mZ5eLEYWZmuThxmJlZLk4cZg2QtFnSgnTn0/sldd+BtoZL+seC+a9LGtc4kZo1DV+Oa9YASesioixNTwP+NyIu3862yoF1EXFlI4Zo1qR8xGGWz1Okm9Wlo4cHqhZI+pWkc9P0Ukk/lDRf0vOSDkg3kPw6MCkdwRwnqVzShWmdCklXS/pjes7FUEn3puc5TC54n3+S9Exq44b0SACzJuPEYVak9Ad6BMXfimZlRAwmewbFhRGxFLie7BkNgyLiv2tZZ2NEHJ/q3QdMBA4BzpXUU9KBwBjgmIgYBGwGztmR7TLLq2PDVczavV0kLQD6k90ue1aR61XdLHIecEaR61QlpeeBFyLd10nSy2Q3xjsWOAJ4NrstEruw5YaCZk3CRxxmDVuf/rvvB+xMdhQA2ZMTC3+HutRY74P0czPF/5NWtc5HBdNV8x3J7v00LR2xDIqI/SOivMi2zRqFE4dZkSLiHbJHhF6YbkP/KnBQeoZ0N7JhrIasBbruQBizgdGSekH1c+H77UB7Zrk5cZjlEBHPAf8DnB0Ry4AZZHeJvQ14rogm7ge+UHVyfDvefyHwfeBRSX8hGzbbM287ZjvCl+OamVkuPuIwM7NcnDjMzCwXJw4zM8vFicPMzHJx4jAzs1ycOMzMLBcnDjMzy+X/A/yQfKDZDbSFAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><ul>
<li>Most of the low revenue movies have a smaller duration than high revenue movies</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="There-was-a-relation-between-high-revenue-movie-and-its-genre?">There was a relation between high revenue movie and its genre?<a class="anchor-link" href="#There-was-a-relation-between-high-revenue-movie-and-its-genre?">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="find-the-mode-of-genres-according-to-high-revenue-:">find the mode of genres according to high revenue :<a class="anchor-link" href="#find-the-mode-of-genres-according-to-high-revenue-:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">genres</span><span class="p">[</span><span class="n">high_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">mode</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[37]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&#39;Drama&#39;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="find-the-mode-of-genres-according-to-low-revenue-:">find the mode of genres according to low revenue :<a class="anchor-link" href="#find-the-mode-of-genres-according-to-low-revenue-:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[43]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">genres</span><span class="p">[</span><span class="n">low_revenue</span><span class="p">]</span><span class="o">.</span><span class="n">mode</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[43]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&#39;Drama&#39;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="plot-a-bar-chart-for-the-average-revenues-corresponding-to-each-genre:">plot a bar chart for the average revenues corresponding to each genre:<a class="anchor-link" href="#plot-a-bar-chart-for-the-average-revenues-corresponding-to-each-genre:">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[38]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;genres&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">revenue</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">kind</span><span class="o">=</span><span class="s1">&#39;bar&#39;</span><span class="p">,</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">5</span><span class="p">));</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Runtime cooresponding to revenue&quot;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;revenue&quot;</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


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
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><ul>
<li>fantasy, adventure ,science fiction and family movies have the highest revenues</li>
<li>Documentary, Foreign and TV movies have the lowest revenues</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Conclusions">Conclusions<a class="anchor-link" href="#Conclusions">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>There is no high colleration between the vote average and high revenue which tell us that maybe most of the votes are fake which makes the movies over rated, but in general high revenue movies have higher vote average than low revenew movies</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>additional reasearch can be done to specify the audience vote from critic vote</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>Most of the low revenue movies have a smaller duration than high revenue movies</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>fantasy, adventure ,science fiction and family movies have the highest revenues</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>Documentary, Foreign and TV movies have the lowest revenues</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Limitations">Limitations<a class="anchor-link" href="#Limitations">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>I prefered to delete rows instead of filling it with regression</li>
</ul>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>
