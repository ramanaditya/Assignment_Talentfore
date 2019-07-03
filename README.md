<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
 <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
<style>
* {box-sizing: border-box}
body {font-family: "Lato", sans-serif;}
.sidebar {
  margin: 0;
  padding: 0;
  width: 200px;
  background-color: #f1f1f1;
  position: fixed;
  height: 100%;
  overflow: auto;
  z-index: 5;
}

.sidebar .tablinks {
  background-color: #f1f1f1;
  display: block;
  width:100%;
  color: black;
  padding: 16px;
  text-decoration: none;
  border:0px;
}
 
.sidebar .tablinks.active {
  background-color: #4CAF50;
  color: white;
  border:0px;
}

.sidebar .tablinks:hover:not(.active) {
  background-color: #555;
  color: white;
  border:0px;
}

div.content {
  margin-left: 200px;
  padding: 1px 16px;
  height: 1000px;
}

@media screen and (max-width: 700px) {
  .sidebar {
    width: 100%;
    height: auto;
    position: relative;
  }
  .sidebar a {float: left;}
  div.content {margin-left: 0;}
}

@media screen and (max-width: 400px) {
  .sidebar a {
    text-align: center;
    float: none;
  }
}
.intl-tel-input {
font-size: 100%;
font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
color: #333;
}
.intl-tel-input input {
width: 100%;
border: 1px solid #CCC;
font-family: inherit;
font-size: 100%;
color: inherit;
padding: 12px 20px;
}
.intl-tel-input { position: relative; }
.intl-tel-input .hide { display: none; }
.intl-tel-input .flag-dropdown { position: absolute; z-index: 1; cursor: pointer; }
.intl-tel-input .flag-dropdown .selected-flag { margin: 1px; padding: 6px 16px 6px 6px;background-color: rgba(0, 0, 0, 0.05); }
.intl-tel-input .flag-dropdown .selected-flag:hover { background-color: rgba(0, 0, 0, 0.05); }
.intl-tel-input .flag-dropdown .selected-flag .down-arrow { top: 6px; position: relative; left: 20px; width: 0; height: 0; border-left: 4px solid transparent; border-right: 4px solid transparent; border-top: 4px solid black; }
.intl-tel-input .flag-dropdown .country-list { list-style: none; padding: 0; margin: 0; z-index: 1; overflow-y: scroll; box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.2); background-color: white; border: 1px solid #cccccc; position: absolute; top: 29px; width: 330px; max-height: 200px; }
.intl-tel-input .flag-dropdown .country-list .divider { padding-bottom: 5px; margin-bottom: 5px; border-bottom: 1px solid #cccccc; }
.intl-tel-input .flag-dropdown .country-list .country { line-height: 16px; padding: 4px 10px; }
.intl-tel-input .flag-dropdown .country-list .country .dial-code { color: #999999; }
.intl-tel-input .flag-dropdown .country-list .country.highlight { background-color: rgba(0, 0, 0, 0.05); }
.intl-tel-input .flag-dropdown .country-list .flag { display: inline-block; vertical-align: bottom; }
.intl-tel-input .flag-dropdown .country-list .flag, .intl-tel-input .flag-dropdown .country-list .country-name { margin-right: 6px; }
.intl-tel-input input { box-sizing: border-box; -moz-box-sizing: border-box; height: 30px; padding-left: 47px; position: relative; z-index: 0; }

/* originally from https://github.com/lafeber/world-flags-sprite */
.f16 .flag { width: 16px; height: 16px; background: url("./flags16.png") no-repeat; }
.f16 ._African_Union { background-position: 0 -16px; }
.f16 ._Arab_League { background-position: 0 -32px; }
.f16 ._ASEAN { background-position: 0 -48px; }
.f16 ._CARICOM { background-position: 0 -64px; }
.f16 ._CIS { background-position: 0 -80px; }
.f16 ._Commonwealth { background-position: 0 -96px; }
.f16 ._England { background-position: 0 -112px; }
.f16 ._European_Union { background-position: 0 -128px; }
.f16 ._Islamic_Conference { background-position: 0 -144px; }
.f16 ._Kosovo { background-position: 0 -160px; }
.f16 ._NATO { background-position: 0 -176px; }
.f16 ._Northern_Cyprus { background-position: 0 -192px; }
.f16 ._Northern_Ireland { background-position: 0 -208px; }
.f16 ._Olimpic_Movement { background-position: 0 -224px; }
.f16 ._OPEC { background-position: 0 -240px; }
.f16 ._Red_Cross { background-position: 0 -256px; }
.f16 ._Scotland { background-position: 0 -272px; }
.f16 ._Somaliland { background-position: 0 -288px; }
.f16 ._Tibet { background-position: 0 -304px; }
.f16 ._United_Nations { background-position: 0 -320px; }
.f16 ._Wales { background-position: 0 -336px; }
.f16 .ad { background-position: 0 -352px; }
.f16 .ae { background-position: 0 -368px; }
.f16 .af { background-position: 0 -384px; }
.f16 .ag { background-position: 0 -400px; }
.f16 .ai { background-position: 0 -416px; }
.f16 .al { background-position: 0 -432px; }
.f16 .am { background-position: 0 -448px; }
.f16 .an { background-position: 0 -464px; }
.f16 .ao { background-position: 0 -480px; }
.f16 .aq { background-position: 0 -496px; }
.f16 .ar { background-position: 0 -512px; }
.f16 .as { background-position: 0 -528px; }
.f16 .at { background-position: 0 -544px; }
.f16 .au { background-position: 0 -560px; }
.f16 .aw { background-position: 0 -576px; }
.f16 .az { background-position: 0 -592px; }
.f16 .ba { background-position: 0 -608px; }
.f16 .bb { background-position: 0 -624px; }
.f16 .bd { background-position: 0 -640px; }
.f16 .be { background-position: 0 -656px; }
.f16 .bf { background-position: 0 -672px; }
.f16 .bg { background-position: 0 -688px; }
.f16 .bh { background-position: 0 -704px; }
.f16 .bi { background-position: 0 -720px; }
.f16 .bj { background-position: 0 -736px; }
.f16 .bm { background-position: 0 -752px; }
.f16 .bn { background-position: 0 -768px; }
.f16 .bo { background-position: 0 -784px; }
.f16 .br { background-position: 0 -800px; }
.f16 .bs { background-position: 0 -816px; }
.f16 .bt { background-position: 0 -832px; }
.f16 .bw { background-position: 0 -848px; }
.f16 .by { background-position: 0 -864px; }
.f16 .bz { background-position: 0 -880px; }
.f16 .ca { background-position: 0 -896px; }
.f16 .cg { background-position: 0 -912px; }
.f16 .cf { background-position: 0 -928px; }
.f16 .cd { background-position: 0 -944px; }
.f16 .ch { background-position: 0 -960px; }
.f16 .ci { background-position: 0 -976px; }
.f16 .ck { background-position: 0 -992px; }
.f16 .cl { background-position: 0 -1008px; }
.f16 .cm { background-position: 0 -1024px; }
.f16 .cn { background-position: 0 -1040px; }
.f16 .co { background-position: 0 -1056px; }
.f16 .cr { background-position: 0 -1072px; }
.f16 .cu { background-position: 0 -1088px; }
.f16 .cv { background-position: 0 -1104px; }
.f16 .cy { background-position: 0 -1120px; }
.f16 .cz { background-position: 0 -1136px; }
.f16 .de { background-position: 0 -1152px; }
.f16 .dj { background-position: 0 -1168px; }
.f16 .dk { background-position: 0 -1184px; }
.f16 .dm { background-position: 0 -1200px; }
.f16 .do { background-position: 0 -1216px; }
.f16 .dz { background-position: 0 -1232px; }
.f16 .ec { background-position: 0 -1248px; }
.f16 .ee { background-position: 0 -1264px; }
.f16 .eg { background-position: 0 -1280px; }
.f16 .eh { background-position: 0 -1296px; }
.f16 .er { background-position: 0 -1312px; }
.f16 .es { background-position: 0 -1328px; }
.f16 .et { background-position: 0 -1344px; }
.f16 .fi { background-position: 0 -1360px; }
.f16 .fj { background-position: 0 -1376px; }
.f16 .fm { background-position: 0 -1392px; }
.f16 .fo { background-position: 0 -1408px; }
.f16 .fr { background-position: 0 -1424px; }
.f16 .ga { background-position: 0 -1440px; }
.f16 .gb { background-position: 0 -1456px; }
.f16 .gd { background-position: 0 -1472px; }
.f16 .ge { background-position: 0 -1488px; }
.f16 .gg { background-position: 0 -1504px; }
.f16 .gh { background-position: 0 -1520px; }
.f16 .gi { background-position: 0 -1536px; }
.f16 .gl { background-position: 0 -1552px; }
.f16 .gm { background-position: 0 -1568px; }
.f16 .gn { background-position: 0 -1584px; }
.f16 .gp { background-position: 0 -1600px; }
.f16 .gq { background-position: 0 -1616px; }
.f16 .gr { background-position: 0 -1632px; }
.f16 .gt { background-position: 0 -1648px; }
.f16 .gu { background-position: 0 -1664px; }
.f16 .gw { background-position: 0 -1680px; }
.f16 .gy { background-position: 0 -1696px; }
.f16 .hk { background-position: 0 -1712px; }
.f16 .hn { background-position: 0 -1728px; }
.f16 .hr { background-position: 0 -1744px; }
.f16 .ht { background-position: 0 -1760px; }
.f16 .hu { background-position: 0 -1776px; }
.f16 .id { background-position: 0 -1792px; }
.f16 .mc { background-position: 0 -1792px; }
.f16 .ie { background-position: 0 -1808px; }
.f16 .il { background-position: 0 -1824px; }
.f16 .im { background-position: 0 -1840px; }
.f16 .in { background-position: 0 -1856px; }
.f16 .iq { background-position: 0 -1872px; }
.f16 .ir { background-position: 0 -1888px; }
.f16 .is { background-position: 0 -1904px; }
.f16 .it { background-position: 0 -1920px; }
.f16 .je { background-position: 0 -1936px; }
.f16 .jm { background-position: 0 -1952px; }
.f16 .jo { background-position: 0 -1968px; }
.f16 .jp { background-position: 0 -1984px; }
.f16 .ke { background-position: 0 -2000px; }
.f16 .kg { background-position: 0 -2016px; }
.f16 .kh { background-position: 0 -2032px; }
.f16 .ki { background-position: 0 -2048px; }
.f16 .km { background-position: 0 -2064px; }
.f16 .kn { background-position: 0 -2080px; }
.f16 .kp { background-position: 0 -2096px; }
.f16 .kr { background-position: 0 -2112px; }
.f16 .kw { background-position: 0 -2128px; }
.f16 .ky { background-position: 0 -2144px; }
.f16 .kz { background-position: 0 -2160px; }
.f16 .la { background-position: 0 -2176px; }
.f16 .lb { background-position: 0 -2192px; }
.f16 .lc { background-position: 0 -2208px; }
.f16 .li { background-position: 0 -2224px; }
.f16 .lk { background-position: 0 -2240px; }
.f16 .lr { background-position: 0 -2256px; }
.f16 .ls { background-position: 0 -2272px; }
.f16 .lt { background-position: 0 -2288px; }
.f16 .lu { background-position: 0 -2304px; }
.f16 .lv { background-position: 0 -2320px; }
.f16 .ly { background-position: 0 -2336px; }
.f16 .ma { background-position: 0 -2352px; }
.f16 .md { background-position: 0 -2368px; }
.f16 .me { background-position: 0 -2384px; }
.f16 .mg { background-position: 0 -2400px; }
.f16 .mh { background-position: 0 -2416px; }
.f16 .mk { background-position: 0 -2432px; }
.f16 .ml { background-position: 0 -2448px; }
.f16 .mm { background-position: 0 -2464px; }
.f16 .mn { background-position: 0 -2480px; }
.f16 .mo { background-position: 0 -2496px; }
.f16 .mq { background-position: 0 -2512px; }
.f16 .mr { background-position: 0 -2528px; }
.f16 .ms { background-position: 0 -2544px; }
.f16 .mt { background-position: 0 -2560px; }
.f16 .mu { background-position: 0 -2576px; }
.f16 .mv { background-position: 0 -2592px; }
.f16 .mw { background-position: 0 -2608px; }
.f16 .mx { background-position: 0 -2624px; }
.f16 .my { background-position: 0 -2640px; }
.f16 .mz { background-position: 0 -2656px; }
.f16 .na { background-position: 0 -2672px; }
.f16 .nc { background-position: 0 -2688px; }
.f16 .ne { background-position: 0 -2704px; }
.f16 .ng { background-position: 0 -2720px; }
.f16 .ni { background-position: 0 -2736px; }
.f16 .nl { background-position: 0 -2752px; }
.f16 .no { background-position: 0 -2768px; }
.f16 .np { background-position: 0 -2784px; }
.f16 .nr { background-position: 0 -2800px; }
.f16 .nz { background-position: 0 -2816px; }
.f16 .om { background-position: 0 -2832px; }
.f16 .pa { background-position: 0 -2848px; }
.f16 .pe { background-position: 0 -2864px; }
.f16 .pf { background-position: 0 -2880px; }
.f16 .pg { background-position: 0 -2896px; }
.f16 .ph { background-position: 0 -2912px; }
.f16 .pk { background-position: 0 -2928px; }
.f16 .pl { background-position: 0 -2944px; }
.f16 .pr { background-position: 0 -2960px; }
.f16 .ps { background-position: 0 -2976px; }
.f16 .pt { background-position: 0 -2992px; }
.f16 .pw { background-position: 0 -3008px; }
.f16 .py { background-position: 0 -3024px; }
.f16 .qa { background-position: 0 -3040px; }
.f16 .re { background-position: 0 -3056px; }
.f16 .ro { background-position: 0 -3072px; }
.f16 .rs { background-position: 0 -3088px; }
.f16 .ru { background-position: 0 -3104px; }
.f16 .rw { background-position: 0 -3120px; }
.f16 .sa { background-position: 0 -3136px; }
.f16 .sb { background-position: 0 -3152px; }
.f16 .sc { background-position: 0 -3168px; }
.f16 .sd { background-position: 0 -3184px; }
.f16 .se { background-position: 0 -3200px; }
.f16 .sg { background-position: 0 -3216px; }
.f16 .si { background-position: 0 -3232px; }
.f16 .sk { background-position: 0 -3248px; }
.f16 .sl { background-position: 0 -3264px; }
.f16 .sm { background-position: 0 -3280px; }
.f16 .sn { background-position: 0 -3296px; }
.f16 .so { background-position: 0 -3312px; }
.f16 .sr { background-position: 0 -3328px; }
.f16 .st { background-position: 0 -3344px; }
.f16 .sv { background-position: 0 -3360px; }
.f16 .sy { background-position: 0 -3376px; }
.f16 .sz { background-position: 0 -3392px; }
.f16 .tc { background-position: 0 -3408px; }
.f16 .td { background-position: 0 -3424px; }
.f16 .tg { background-position: 0 -3440px; }
.f16 .th { background-position: 0 -3456px; }
.f16 .tj { background-position: 0 -3472px; }
.f16 .tl { background-position: 0 -3488px; }
.f16 .tm { background-position: 0 -3504px; }
.f16 .tn { background-position: 0 -3520px; }
.f16 .to { background-position: 0 -3536px; }
.f16 .tr { background-position: 0 -3552px; }
.f16 .tt { background-position: 0 -3568px; }
.f16 .tv { background-position: 0 -3584px; }
.f16 .tw { background-position: 0 -3600px; }
.f16 .tz { background-position: 0 -3616px; }
.f16 .ua { background-position: 0 -3632px; }
.f16 .ug { background-position: 0 -3648px; }
.f16 .us { background-position: 0 -3664px; }
.f16 .uy { background-position: 0 -3680px; }
.f16 .uz { background-position: 0 -3696px; }
.f16 .va { background-position: 0 -3712px; }
.f16 .vc { background-position: 0 -3728px; }
.f16 .ve { background-position: 0 -3744px; }
.f16 .vg { background-position: 0 -3760px; }
.f16 .vi { background-position: 0 -3776px; }
.f16 .vn { background-position: 0 -3792px; }
.f16 .vu { background-position: 0 -3808px; }
.f16 .ws { background-position: 0 -3824px; }
.f16 .ye { background-position: 0 -3840px; }
.f16 .za { background-position: 0 -3856px; }
.f16 .zm { background-position: 0 -3872px; }
.f16 .zw { background-position: 0 -3888px; }

.btn {
  border: none;
  color: white;
  padding: 14px 28px;
  font-size: 16px;
  cursor: pointer;
}
input[type=text], select, textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  resize: vertical;
}
input[type=number], select, textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  resize: vertical;
}
input[type=email], select, textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  resize: vertical;
}

label {
  padding: 12px 12px 12px 0;
  display: inline-block;
}

input[type=submit] {
  background-color: #4CAF50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  float: right;
}

input[type=submit]:hover {
  background-color: #45a049;
}

.container {
  border-radius: 5px;
  padding: 20px;
}

.col-25 {
  float: left;
  text-align: right;
  width: 25%;
  margin-top: 6px;
}

.col-75 {
  float: left;
  width: 75%;
  margin-top: 6px;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

@media screen and (max-width: 600px) {
  .col-25, .col-75, input[type=submit] {
    width: 100%;
    margin-top: 0;
  }
  .col-25{
    text-align: left;
  }
}

.success {background-color: #4CAF50;} /* Green */
.success:hover {background-color: #46a049;}

.info {background-color: #2196F3;} /* Blue */
.info:hover {background: #0b7dda;}

.warning {background-color: #ff9800;} /* Orange */
.warning:hover {background: #e68a00;}

.danger {background-color: #f44336;} /* Red */ 
.danger:hover {background: #da190b;}

.default {background-color: #e7e7e7; color: black;} /* Gray */ 
.default:hover {background: #ddd;}
/* Style the tab */
.tab {
  float: left;
  border: 1px solid #ccc;
  background-color: #f1f1f1;
  width: 20%;
  height: 100%;
}

/* Style the buttons inside the tab */
.tab button {
  display: block;
  background-color: inherit;
  color: black;
  padding: 22px 16px;
  width: 100%;
  border: none;
  outline: none;
  text-align: left;
  cursor: pointer;
  transition: 0.3s;
  font-size: 17px;
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #ddd;
}

/* Create an active/current "tab button" class */
.tab button.active {
  background-color: #ccc;
}

/* Style the tab content */
.tabcontent {
  float: left;
  padding: .8em 1em;
  border: 0px solid #ccc;
  width: 90%;
  border-left: none;
  height: 100%;

  
}
.close {
  color:red;
  display: inline-block;
}
</style>
</head>
<body>

<h2 style="text-align: center;font-weight:900;letter-spacing: 5px;margin-top: 20px;">BUILD A COMPELLING RESUME<hr></h2>

<div class="row">
  <div class="col-25">
    <div class="sidebar">
      <button class="tablinks" onclick="openCity(event, 'Personal Info')" id="defaultOpen">Personal Info</button>
      <button class="tablinks" onclick="openCity(event, 'Summary')">Summary</button>
      <button class="tablinks" onclick="openCity(event, 'Work Experience')">Work Experience</button>
      <button class="tablinks" onclick="openCity(event, 'Education')">Education</button>
      <button class="tablinks" onclick="openCity(event, 'Skills')">Skills</button>

    </div>
  </div>
  <div class="col-75">


    <div id="Personal Info" class="tabcontent">
      <div class="box" style="border: solid 1px lightgrey;padding: 10px 10px;">
    <button class="btn warning" style="padding:3px 10px;">TIPS</button> Field marked with <span style="color:red">*</span> are mandatory. However, to have enough content in your resume, please fill in all the details. </div><br>
  <h3 style="text-align:center;">CONTACT DETAILS</h3><br>

  <div class="container">
  <form action="/action_page.php">
    <div class="row">
      <div class="col-25" style="">
        <label for="fname">First Name<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="fname" name="firstname" placeholder="Your first name.." required>
      </div>
    </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="lname">Last Name<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Your last name.." required>
      </div>
    </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="email">Email<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="email" id="lname" name="lastname" placeholder="Your Email.." required>
      </div>
    </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="email">Mobile<span style="color:red">*</span></label>
      </div>
      <div class="col-75" style="padding-top: 10px;">
      <input type="tel" id="mobile-number" placeholder="e.g. +1 702 123 4567" required>
    </div>
    </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="email">Alternate Mobile<span style="color:red">*</span></label>
      </div>
      <div class="col-75" style="padding-top: 10px;">
      <input type="tel" id="mobile-number1" placeholder="e.g. +1 702 123 4567" required>
    </div>
  </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="skype">Skype<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Your Skype id" required>
      </div>
    </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="LinkedIn">LinkedIn<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Your LinkedIn id" required>
      </div>
    </div>
    <div class="row">
      <div class="col-25" style="">
        <label for="Address">Address<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Your Address " required>
      </div>
    </div>
    <div class="row" style="float:right;margin-top:20px;">
      <input type="submit" value="Save">
    </div>
  </form>
</div>
</div>

<div id="Summary" class="tabcontent">

  <div class="box" style="border: solid 1px lightgrey;padding: 10px 10px;">
    <button class="btn warning" style="padding:3px 10px;">TIPS</button> Field marked with <span style="color:red">*</span> are mandatory. However, to have enough content in your resume, please fill in all the details. </div><br>
    <div class="container">
  <form action="/action_page.php">
  <div class="row">
      <div class="col-25" style="text-align: right;">
        <label for="subject">Summary<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <textarea id="subject" name="subject" placeholder="Write About Yourself..." required style="height:200px"></textarea>
      </div>
    </div>
    <div class="row" style="float:right;margin-top:20px;">
      <input type="submit" value="Save">
    </div>
  </form>
</div>

</div>

<div id="Work Experience" class="tabcontent">
  
    <div class="box" style="border: solid 1px lightgrey;padding: 10px 0px 10px 10px;">
    <button class="btn warning" style="padding:3px 10px;">TIPS</button> Field marked with <span style="color:red">*</span> are mandatory. However, to have enough content in your resume, please fill in all the details.</div><br>
    <button onclick="myFunctionwork()" >Add Work</button>
  <div id="work" class="container">
  <div class="row">

      <div class="col-25" style="text-align: right;">
        <label for="Position">Position<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Position" required>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Start Date">Start Date<span style="color:red">*</span></label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="date" id="lname" name="lastname" placeholder="Start Date" required>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="End Date">End Date</label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="date" id="lname" name="lastname" placeholder="End Date">
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Responsibility">Responsibility</label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="text" id="myInput" placeholder="Title..." style="width:90%;">
        <span onclick="newElement()" class="addBtn"><input type="submit" value="Add" style="float:right;background-color:teal;"></span>
        <br>
        <ul id="myUL">

        </ul>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Achievements">Achievements</label>
      </div>
      <div class="col-75">
        <textarea id="subject" name="Achievements" placeholder="Achievements..." style="height:200px"></textarea>
      </div>
    </div>
    
    <hr><br>
</div>
<div class="row" style="float:right;">
      <input type="submit" value="Save">
    </div>
</div>



<div id="Education" class="tabcontent">
  <div class="box" style="border: solid 1px lightgrey;padding: 10px 0px 10px 10px;">
    <button class="btn warning" style="padding:3px 10px;">TIPS</button> Field marked with <span style="color:red">*</span> are mandatory. However, to have enough content in your resume, please fill in all the details.</div><br>
<div id="edu" class="container">
      <button onclick="myFunctionedu()" >Add School</button><br>
  <div class="row">
      
 
      <div class="col-25" style="text-align: right;">
        <label for="Degree">Degree<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Degree" required>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Start Date">Start Date<span style="color:red">*</span></label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="date" id="lname" name="lastname" placeholder="Start Date" required>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="End Date">End Date</label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="date" id="lname" name="lastname" placeholder="End Date">
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Grade">Grade<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="Grade" required>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="College">College<span style="color:red">*</span></label>
      </div>
      <div class="col-75">
        <input type="text" id="lname" name="lastname" placeholder="College" required>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Responsibility">Responsibility</label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="text" id="myInputedu" placeholder="Title..." style="width:90%;">
        <span onclick="newElementedu()" class="addBtn"><input type="submit" value="Add" style="float:right;background-color:teal;"></span>
        <ul id="myULedu">

        </ul>
      </div>
      <div class="col-25" style="text-align: right;">
        <label for="Achievements">Achievements</label>
      </div>
      <div class="col-75">
        <textarea id="subject" name="Achievements" placeholder="Achievements..." style="height:200px"></textarea>
      </div>
    </div>
    <hr><br>
  
</div>
<div class="row" style="float:right;">
      <input type="submit" value="Save">
    </div>
</div>

<div id="Skills" class="tabcontent">
  <div class="box" style="border: solid 1px lightgrey;padding: 10px 0px 10px 10px;">
    <button class="btn warning" style="padding:3px 10px;">TIPS</button> Field marked with <span style="color:red">*</span> are mandatory. However, to have enough content in your resume, please fill in all the details.</div><br>
<div class="container">
  
  <div class="row">
      <div class="col-25" style="text-align: right;">
        <label for="Skills">Skills</label>
      </div>
      <div class="col-75" style="margin-top: 15px;">
        <input type="text" id="myInputskill" placeholder="Skills..." style="width:90%;">
        <span onclick="newElementskill()" class="addBtn"><input type="submit" value="Add" style="float:right;background-color:teal;"></span>
        <ul id="myULskill">

        </ul>
      
      </div>
    
  
</div>
<div class="row" style="float:right;margin-top:20px;">
    <input type="submit" value="Save">
  </div>

</div>
</div>
<script>
function myFunctionedu() {
  var para = document.createElement("DIV");
  para.innerHTML = '<div class="row"><div class="col-25" style="text-align: right;"><label for="Degree">Degree<span style="color:red">*</span></label></div><div class="col-75"><input type="text" id="lname" name="lastname" placeholder="Degree" required></div><div class="col-25" style="text-align: right;"><label for="Start Date">Start Date<span style="color:red">*</span></label></div><div class="col-75" style="margin-top: 15px;"><input type="date" id="lname" name="lastname" placeholder="Start Date" required></div><div class="col-25" style="text-align: right;"><label for="End Date">End Date</label></div><div class="col-75" style="margin-top: 15px;"><input type="date" id="lname" name="lastname" placeholder="End Date"></div><div class="col-25" style="text-align: right;"><label for="Grade">Grade<span style="color:red">*</span></label></div><div class="col-75"><input type="text" id="lname" name="lastname" placeholder="Grade" required></div><div class="col-25" style="text-align: right;"><label for="College">College<span style="color:red">*</span></label></div><div class="col-75"><input type="text" id="lname" name="lastname" placeholder="College" required></div><div class="col-25" style="text-align: right;"><label for="Responsibility">Responsibility</label></div><div class="col-75" style="margin-top: 15px;"><input type="text" id="myInput" placeholder="Title..." style="width:90%;"><span onclick="newElement()" class="addBtn"><input type="submit" value="Add" style="float:right;background-color:teal;"></span><ul id="myUL"></ul></div><div class="col-25" style="text-align: right;"><label for="Achievements">Achievements</label></div><div class="col-75"><textarea id="subject" name="Achievements" placeholder="Achievements..." style="height:200px"></textarea></div></div><hr><br>';
  document.getElementById("edu").appendChild(para);
}
</script>
<script>
function myFunctionwork() {
  var para = document.createElement("DIV");
  para.innerHTML = '<div class="row"><div class="col-25" style="text-align: right;"><label for="Position">Position<span style="color:red">*</span></label></div><div class="col-75"><input type="text" id="lname" name="lastname" placeholder="Position" required></div><div class="col-25" style="text-align: right;"><label for="Start Date">Start Date<span style="color:red">*</span></label></div><div class="col-75" style="margin-top: 15px;"><input type="date" id="lname" name="lastname" placeholder="Start Date" required></div><div class="col-25" style="text-align: right;"><label for="End Date">End Date</label></div><div class="col-75" style="margin-top: 15px;"><input type="date" id="lname" name="lastname" placeholder="End Date"></div><div class="col-25" style="text-align: right;"><label for="Responsibility">Responsibility</label></div><div class="col-75" style="margin-top: 15px;"><input type="text" id="myInput" placeholder="Title..." style="width:90%;"><span onclick="newElement()" class="addBtn"><input type="submit" value="Add" style="float:right;background-color:teal;"></span><ul id="myUL"></ul></div><div class="col-25" style="text-align: right;"><label for="Achievements">Achievements</label></div><div class="col-75"><textarea id="subject" name="Achievements" placeholder="Achievements..." style="height:200px"></textarea></div></div><hr><br>';
  document.getElementById("work").appendChild(para);
}
</script>
<script>
var myNodelist = document.getElementsByTagName("LI");
var i;
for (i = 0; i < myNodelist.length; i++) {
  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  myNodelist[i].appendChild(span);
}

var close = document.getElementsByClassName("close");
var i;
for (i = 0; i < close.length; i++) {
  close[i].onclick = function() {
    var div = this.parentElement;
    div.style.display = "none";
  }
}

var list = document.querySelector('ul');
list.addEventListener('click', function(ev) {
  if (ev.target.tagName === 'LI') {
    ev.target.classList.toggle('checked');
  }
}, false);

function newElement() {
  var li = document.createElement("li");
  var inputValue = document.getElementById("myInput").value;
  var t = document.createTextNode(inputValue);
  li.appendChild(t);
  if (inputValue === '') {
    alert("You must write something!");
  } else {
    document.getElementById("myUL").appendChild(li);
  }
  document.getElementById("myInput").value = "";

  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  li.appendChild(span);

  for (i = 0; i < close.length; i++) {
    close[i].onclick = function() {
      var div = this.parentElement;
      div.style.display = "none";
    }
  }
}
function newElementedu() {
  var li = document.createElement("li");
  var inputValue = document.getElementById("myInputedu").value;
  var t = document.createTextNode(inputValue);
  li.appendChild(t);
  if (inputValue === '') {
    alert("You must write something!");
  } else {
    document.getElementById("myULedu").appendChild(li);
  }
  document.getElementById("myInputedu").value = "";

  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  li.appendChild(span);

  for (i = 0; i < close.length; i++) {
    close[i].onclick = function() {
      var div = this.parentElement;
      div.style.display = "none";
    }
  }
}
</script>
<script>
var myNodelist = document.getElementsByTagName("LI");
var i;
for (i = 0; i < myNodelist.length; i++) {
  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  myNodelist[i].appendChild(span);
}

var close = document.getElementsByClassName("close");
var i;
for (i = 0; i < close.length; i++) {
  close[i].onclick = function() {
    var div = this.parentElement;
    div.style.display = "none";
  }
}

var list = document.querySelector('ul');
list.addEventListener('click', function(ev) {
  if (ev.target.tagName === 'LI') {
    ev.target.classList.toggle('checked');
  }
}, false);

function newElementskill() {
  var li = document.createElement("li");
  var inputValue = document.getElementById("myInputskill").value;
  var t = document.createTextNode(inputValue);
  li.appendChild(t);
  if (inputValue === '') {
    alert("You must write something!");
  } else {
    document.getElementById("myULskill").appendChild(li);
  }
  document.getElementById("myInputskill").value = "";

  var span = document.createElement("SPAN");
  var txt = document.createTextNode("\u00D7");
  span.className = "close";
  span.appendChild(txt);
  li.appendChild(span);

  for (i = 0; i < close.length; i++) {
    close[i].onclick = function() {
      var div = this.parentElement;
      div.style.display = "none";
    }
  }
}
</script>

<script>
function openCity(evt, cityName) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.className += " active";
}
document.getElementById("defaultOpen").click();
</script>


<script>
(function($, window, document, undefined) {
    var pluginName = "intlTelInput", defaults = {
        preferredCountries: [ "in", "us" ],
        
        initialDialCode: true,
        americaMode: false,
        onlyCountries: []
    };
    function Plugin(element, options) {
        this.element = element;
        this.options = $.extend({}, defaults, options);
        this._defaults = defaults;
        this._name = pluginName;
        this.init();
    }
    Plugin.prototype = {
        init: function() {
            var that = this;
            if (this.options.onlyCountries.length > 0) {
                var newCountries = [], newCountryCodes = {};
                $.each(this.options.onlyCountries, function(i, countryCode) {
                    var countryData = that._getCountryData(countryCode);
                    if (countryData) {
                        newCountries.push(countryData);
                        var callingCode = countryData["calling-code"];
                        if (newCountryCodes[callingCode]) {
                            newCountryCodes[callingCode].push(countryCode);
                        } else {
                            newCountryCodes[callingCode] = [ countryCode ];
                        }
                    }
                });
                intlTelInput.countries = newCountries;
                intlTelInput.countryCodes = newCountryCodes;
            }
            var preferredCountries = [];
            $.each(this.options.preferredCountries, function(i, countryCode) {
                var countryData = that._getCountryData(countryCode);
                if (countryData) {
                    preferredCountries.push(countryData);
                }
            });
            this.defaultCountry = preferredCountries.length ? preferredCountries[0] : intlTelInput.countries[0];
            this.telInput = $(this.element);
            if (this.options.initialDialCode && this.telInput.val() === "") {
                this.telInput.val("+" + this.defaultCountry["calling-code"] + " ");
            }
            this.telInput.wrap($("<div>", {
                "class": "intl-tel-input"
            }));
            var flagsContainer = $("<div>", {
                "class": "flag-dropdown f16"
            }).insertBefore(this.telInput);
            var selectedFlag = $("<div>", {
                "class": "selected-flag"
            }).appendTo(flagsContainer);
            var firstCountry = this.defaultCountry.cca2;
            this.selectedFlagInner = $("<div>", {
                "class": "flag " + firstCountry
            }).appendTo(selectedFlag);
            $("<div>", {
                "class": "down-arrow"
            }).appendTo(this.selectedFlagInner);
            this.countryList = $("<ul>", {
                "class": "country-list hide"
            }).appendTo(flagsContainer);
            if (preferredCountries.length) {
                this._appendListItems(preferredCountries, "preferred");
                $("<li>", {
                    "class": "divider"
                }).appendTo(this.countryList);
            }
            this._appendListItems(intlTelInput.countries, "");
            this.countryListItems = this.countryList.children(".country");
            this.countryListItems.first().addClass("active");
            this.telInput.keyup(function() {
                var countryCode, alreadySelected = false;
                var dialCode = that._getDialCode(that.telInput.val());
                if (dialCode) {
                    var countryCodes = intlTelInput.countryCodes[dialCode];
                    $.each(countryCodes, function(i, c) {
                        if (that.selectedFlagInner.hasClass(c)) {
                            alreadySelected = true;
                        }
                    });
                    countryCode = countryCodes[0];
                } else {
                    countryCode = that.defaultCountry.cca2;
                }
                if (!alreadySelected) {
                    that._selectFlag(countryCode);
                }
            });
            this.telInput.keyup();
            selectedFlag.click(function(e) {
                e.stopPropagation();
                if (that.countryList.hasClass("hide")) {
                    that.countryListItems.removeClass("highlight");
                    var activeListItem = that.countryList.children(".active").addClass("highlight");
                    that.countryList.removeClass("hide");
                    that._scrollTo(activeListItem);
                    $(document).bind("keydown.intlTelInput", function(e) {
                        if (e.which == 38 || e.which == 40) {
                            var current = that.countryList.children(".highlight").first();
                            var next = e.which == 38 ? current.prev() : current.next();
                            if (next) {
                                if (next.hasClass("divider")) {
                                    next = e.which == 38 ? next.prev() : next.next();
                                }
                                that.countryListItems.removeClass("highlight");
                                next.addClass("highlight");
                                that._scrollTo(next);
                            }
                        } else if (e.which == 13) {
                            var currentCountry = that.countryList.children(".highlight").first();
                            if (currentCountry.length) {
                                that._selectListItem(currentCountry);
                            }
                        } else if (e.which == 9 || e.which == 27) {
                            that._closeDropdown();
                        } else if (e.which >= 97 && e.which <= 122 || e.which >= 65 && e.which <= 90) {
                            var letter = String.fromCharCode(e.which);
                            var countries = that.countryListItems.filter(function() {
                                return $(this).text().charAt(0) == letter && !$(this).hasClass("preferred");
                            });
                            if (countries.length) {
                                var highlightedCountry = countries.filter(".highlight").first();
                                var listItem;
                                if (highlightedCountry && highlightedCountry.next() && highlightedCountry.next().text().charAt(0) == letter) {
                                    listItem = highlightedCountry.next();
                                } else {
                                    listItem = countries.first();
                                }
                                that.countryListItems.removeClass("highlight");
                                listItem.addClass("highlight");
                                that._scrollTo(listItem);
                            }
                        }
                    });
                } else {
                    that._closeDropdown();
                }
            });
            this.countryListItems.mouseover(function() {
                that.countryListItems.removeClass("highlight");
                $(this).addClass("highlight");
            });
            this.countryListItems.click(function(e) {
                var listItem = $(e.currentTarget);
                that._selectListItem(listItem);
            });
            $("html").click(function(e) {
                if (!$(e.target).closest(".country-list").length) {
                    // close it
                    that._closeDropdown();
                }
            });
        },
        _getCountryData: function(countryCode) {
            for (var i = 0; i < intlTelInput.countries.length; i++) {
                if (intlTelInput.countries[i].cca2 == countryCode) {
                    return intlTelInput.countries[i];
                }
            }
        },
        _selectFlag: function(countryCode) {
            this.selectedFlagInner.attr("class", "flag " + countryCode);
            this.countryListItems.removeClass("active");
            var listItem = this.countryListItems.children(".flag." + countryCode).parent();
            listItem.addClass("active");
            return listItem;
        },
        selectCountry: function(countryCode) {
            if (!this.selectedFlagInner.hasClass(countryCode)) {
                var listItem = this._selectFlag(countryCode);
                var dialCode = listItem.attr("data-dial-code");
                this.telInput.val("+" + dialCode + " ");
            }
        },
        _selectListItem: function(listItem) {
            var countryCode = listItem.attr("data-country-code");
            this.selectedFlagInner.attr("class", "flag " + countryCode);
            var newNumber = this._updateNumber(this.telInput.val(), listItem.attr("data-dial-code"));
            this.telInput.val(newNumber);
            this._closeDropdown();
            this.telInput.focus();
            this.countryListItems.removeClass("active highlight");
            listItem.addClass("active");
        },
        _closeDropdown: function() {
            this.countryList.addClass("hide");
            $(document).unbind("keydown.intlTelInput");
        },
        _scrollTo: function(element) {
            var container = this.countryList;
            var containerHeight = container.height();
            var containerTop = container.offset().top;
            var containerBottom = containerTop + containerHeight;
            var elementHeight = element.outerHeight();
            var elementTop = element.offset().top;
            var elementBottom = elementTop + elementHeight;
            var newScrollTop = elementTop - containerTop + container.scrollTop();
            if (elementTop < containerTop) {
                container.scrollTop(newScrollTop);
            } else if (elementBottom > containerBottom) {
                var heightDifference = containerHeight - elementHeight;
                container.scrollTop(newScrollTop - heightDifference);
            }
        },
        _updateNumber: function(inputVal, dialCode) {
            var prevDialCode = "+" + this._getDialCode(inputVal);
            var newDialCode = "+" + dialCode;
            var newNumber;
            if (prevDialCode.length > 1) {
                newNumber = inputVal.replace(prevDialCode, newDialCode);
                if (inputVal == prevDialCode) {
                    newNumber += " ";
                }
            } else if (inputVal.length && inputVal.substr(0, 1) != "+") {
                newNumber = newDialCode + " " + inputVal.trim();
            } else {
                newNumber = newDialCode + " ";
            }
            if (this.options.americaMode && newNumber.substring(0, 3) == "+1 ") {
                newNumber = newNumber.substring(3);
            }
            return newNumber;
        },
        _getDialCode: function(inputVal) {
            var firstPart = inputVal.trim().split(" ")[0];
            if (firstPart.substring(0, 1) == "+") {
                var dialCode = firstPart.replace(/\D/g, "").substring(0, 4);
                for (var i = dialCode.length; i > 0; i--) {
                    dialCode = dialCode.substring(0, i);
                    if (intlTelInput.countryCodes[dialCode]) {
                        return dialCode;
                    }
                }
            }
            return "";
        },
        _appendListItems: function(countries, className) {
            var tmp = "";
            $.each(countries, function(i, c) {
                tmp += "<li class='country " + className + "' data-dial-code='" + c["calling-code"] + "' data-country-code='" + c.cca2 + "'>";
                tmp += "<div class='flag " + c.cca2 + "'></div>";
                tmp += "<span class='country-name'>" + c.name + "</span>";
                tmp += "<span class='dial-code'>+" + c["calling-code"] + "</span>";
                tmp += "</li>";
            });
            this.countryList.append(tmp);
        }
    };
    $.fn[pluginName] = function(options) {
        var args = arguments;
        if (options === undefined || typeof options === "object") {
            return this.each(function() {
                if (!$.data(this, "plugin_" + pluginName)) {
                    $.data(this, "plugin_" + pluginName, new Plugin(this, options));
                }
            });
        } else if (typeof options === "string" && options[0] !== "_" && options !== "init") {
            var returns;
            this.each(function() {
                var instance = $.data(this, "plugin_" + pluginName);
                if (instance instanceof Plugin && typeof instance[options] === "function") {
                    returns = instance[options].apply(instance, Array.prototype.slice.call(args, 1));
                }
            });
            return returns !== undefined ? returns : this;
        }
    };
})(jQuery, window, document);

var intlTelInput = {
    countries: [ {
        name: "Afghanistan",
        cca2: "af",
        "calling-code": "93"
    }, {
        name: "Albania",
        cca2: "al",
        "calling-code": "355"
    }, {
        name: "Algeria",
        cca2: "dz",
        "calling-code": "213"
    }, {
        name: "American Samoa",
        cca2: "as",
        "calling-code": "1684"
    }, {
        name: "Andorra",
        cca2: "ad",
        "calling-code": "376"
    }, {
        name: "Angola",
        cca2: "ao",
        "calling-code": "244"
    }, {
        name: "Anguilla",
        cca2: "ai",
        "calling-code": "1264"
    }, {
        name: "Antigua and Barbuda",
        cca2: "ag",
        "calling-code": "1268"
    }, {
        name: "Argentina",
        cca2: "ar",
        "calling-code": "54"
    }, {
        name: "Armenia",
        cca2: "am",
        "calling-code": "374"
    }, {
        name: "Aruba",
        cca2: "aw",
        "calling-code": "297"
    }, {
        name: "Australia",
        cca2: "au",
        "calling-code": "61"
    }, {
        name: "Austria",
        cca2: "at",
        "calling-code": "43"
    }, {
        name: "Azerbaijan",
        cca2: "az",
        "calling-code": "994"
    }, {
        name: "Bahamas",
        cca2: "bs",
        "calling-code": "1242"
    }, {
        name: "Bahrain",
        cca2: "bh",
        "calling-code": "973"
    }, {
        name: "Bangladesh",
        cca2: "bd",
        "calling-code": "880"
    }, {
        name: "Barbados",
        cca2: "bb",
        "calling-code": "1246"
    }, {
        name: "Belarus",
        cca2: "by",
        "calling-code": "375"
    }, {
        name: "Belgium",
        cca2: "be",
        "calling-code": "32"
    }, {
        name: "Belize",
        cca2: "bz",
        "calling-code": "501"
    }, {
        name: "Benin",
        cca2: "bj",
        "calling-code": "229"
    }, {
        name: "Bermuda",
        cca2: "bm",
        "calling-code": "1441"
    }, {
        name: "Bhutan",
        cca2: "bt",
        "calling-code": "975"
    }, {
        name: "Bolivia",
        cca2: "bo",
        "calling-code": "591"
    }, {
        name: "Bosnia and Herzegovina",
        cca2: "ba",
        "calling-code": "387"
    }, {
        name: "Botswana",
        cca2: "bw",
        "calling-code": "267"
    }, {
        name: "Brazil",
        cca2: "br",
        "calling-code": "55"
    }, {
        name: "Brunei Darussalam",
        cca2: "bn",
        "calling-code": "673"
    }, {
        name: "Bulgaria",
        cca2: "bg",
        "calling-code": "359"
    }, {
        name: "Burkina Faso",
        cca2: "bf",
        "calling-code": "226"
    }, {
        name: "Burundi",
        cca2: "bi",
        "calling-code": "257"
    }, {
        name: "Cambodia",
        cca2: "kh",
        "calling-code": "855"
    }, {
        name: "Cameroon",
        cca2: "cm",
        "calling-code": "237"
    }, {
        name: "Canada",
        cca2: "ca",
        "calling-code": "1"
    }, {
        name: "Cape Verde",
        cca2: "cv",
        "calling-code": "238"
    }, {
        name: "Cayman Islands",
        cca2: "ky",
        "calling-code": "1345"
    }, {
        name: "Central African Republic",
        cca2: "cf",
        "calling-code": "236"
    }, {
        name: "Chad",
        cca2: "td",
        "calling-code": "235"
    }, {
        name: "Chile",
        cca2: "cl",
        "calling-code": "56"
    }, {
        name: "China",
        cca2: "cn",
        "calling-code": "86"
    }, {
        name: "Colombia",
        cca2: "co",
        "calling-code": "57"
    }, {
        name: "Comoros",
        cca2: "km",
        "calling-code": "269"
    }, {
        name: "Congo (DRC)",
        cca2: "cd",
        "calling-code": "243"
    }, {
        name: "Congo (Republic)",
        cca2: "cg",
        "calling-code": "242"
    }, {
        name: "Cook Islands",
        cca2: "ck",
        "calling-code": "682"
    }, {
        name: "Costa Rica",
        cca2: "cr",
        "calling-code": "506"
    }, {
        name: "Côte d'Ivoire",
        cca2: "ci",
        "calling-code": "225"
    }, {
        name: "Croatia",
        cca2: "hr",
        "calling-code": "385"
    }, {
        name: "Cuba",
        cca2: "cu",
        "calling-code": "53"
    }, {
        name: "Cyprus",
        cca2: "cy",
        "calling-code": "357"
    }, {
        name: "Czech Republic",
        cca2: "cz",
        "calling-code": "420"
    }, {
        name: "Denmark",
        cca2: "dk",
        "calling-code": "45"
    }, {
        name: "Djibouti",
        cca2: "dj",
        "calling-code": "253"
    }, {
        name: "Dominica",
        cca2: "dm",
        "calling-code": "1767"
    }, {
        name: "Dominican Republic",
        cca2: "do",
        "calling-code": "1809"
    }, {
        name: "Ecuador",
        cca2: "ec",
        "calling-code": "593"
    }, {
        name: "Egypt",
        cca2: "eg",
        "calling-code": "20"
    }, {
        name: "El Salvador",
        cca2: "sv",
        "calling-code": "503"
    }, {
        name: "Equatorial Guinea",
        cca2: "gq",
        "calling-code": "240"
    }, {
        name: "Eritrea",
        cca2: "er",
        "calling-code": "291"
    }, {
        name: "Estonia",
        cca2: "ee",
        "calling-code": "372"
    }, {
        name: "Ethiopia",
        cca2: "et",
        "calling-code": "251"
    }, {
        name: "Faroe Islands",
        cca2: "fo",
        "calling-code": "298"
    }, {
        name: "Fiji",
        cca2: "fj",
        "calling-code": "679"
    }, {
        name: "Finland",
        cca2: "fi",
        "calling-code": "358"
    }, {
        name: "France",
        cca2: "fr",
        "calling-code": "33"
    }, {
        name: "French Polynesia",
        cca2: "pf",
        "calling-code": "689"
    }, {
        name: "Gabon",
        cca2: "ga",
        "calling-code": "241"
    }, {
        name: "Gambia",
        cca2: "gm",
        "calling-code": "220"
    }, {
        name: "Georgia",
        cca2: "ge",
        "calling-code": "995"
    }, {
        name: "Germany",
        cca2: "de",
        "calling-code": "49"
    }, {
        name: "Ghana",
        cca2: "gh",
        "calling-code": "233"
    }, {
        name: "Gibraltar",
        cca2: "gi",
        "calling-code": "350"
    }, {
        name: "Greece",
        cca2: "gr",
        "calling-code": "30"
    }, {
        name: "Greenland",
        cca2: "gl",
        "calling-code": "299"
    }, {
        name: "Grenada",
        cca2: "gd",
        "calling-code": "1473"
    }, {
        name: "Guadeloupe",
        cca2: "gp",
        "calling-code": "590"
    }, {
        name: "Guam",
        cca2: "gu",
        "calling-code": "1671"
    }, {
        name: "Guatemala",
        cca2: "gt",
        "calling-code": "502"
    }, {
        name: "Guernsey",
        cca2: "gg",
        "calling-code": "44"
    }, {
        name: "Guinea",
        cca2: "gn",
        "calling-code": "224"
    }, {
        name: "Guinea-Bissau",
        cca2: "gw",
        "calling-code": "245"
    }, {
        name: "Guyana",
        cca2: "gy",
        "calling-code": "592"
    }, {
        name: "Haiti",
        cca2: "ht",
        "calling-code": "509"
    }, {
        name: "Honduras",
        cca2: "hn",
        "calling-code": "504"
    }, {
        name: "Hong Kong",
        cca2: "hk",
        "calling-code": "852"
    }, {
        name: "Hungary",
        cca2: "hu",
        "calling-code": "36"
    }, {
        name: "Iceland",
        cca2: "is",
        "calling-code": "354"
    }, {
        name: "India",
        cca2: "in",
        "calling-code": "91"
    }, {
        name: "Indonesia",
        cca2: "id",
        "calling-code": "62"
    }, {
        name: "Iran",
        cca2: "ir",
        "calling-code": "98"
    }, {
        name: "Iraq",
        cca2: "iq",
        "calling-code": "964"
    }, {
        name: "Ireland",
        cca2: "ie",
        "calling-code": "353"
    }, {
        name: "Isle of Man",
        cca2: "im",
        "calling-code": "44"
    }, {
        name: "Israel",
        cca2: "il",
        "calling-code": "972"
    }, {
        name: "Italy",
        cca2: "it",
        "calling-code": "39"
    }, {
        name: "Jamaica",
        cca2: "jm",
        "calling-code": "1876"
    }, {
        name: "Japan",
        cca2: "jp",
        "calling-code": "81"
    }, {
        name: "Jersey",
        cca2: "je",
        "calling-code": "44"
    }, {
        name: "Jordan",
        cca2: "jo",
        "calling-code": "962"
    }, {
        name: "Kazakhstan",
        cca2: "kz",
        "calling-code": "7"
    }, {
        name: "Kenya",
        cca2: "ke",
        "calling-code": "254"
    }, {
        name: "Kiribati",
        cca2: "ki",
        "calling-code": "686"
    }, {
        name: "Kuwait",
        cca2: "kw",
        "calling-code": "965"
    }, {
        name: "Kyrgyzstan",
        cca2: "kg",
        "calling-code": "996"
    }, {
        name: "Laos",
        cca2: "la",
        "calling-code": "856"
    }, {
        name: "Latvia",
        cca2: "lv",
        "calling-code": "371"
    }, {
        name: "Lebanon",
        cca2: "lb",
        "calling-code": "961"
    }, {
        name: "Lesotho",
        cca2: "ls",
        "calling-code": "266"
    }, {
        name: "Liberia",
        cca2: "lr",
        "calling-code": "231"
    }, {
        name: "Libya",
        cca2: "ly",
        "calling-code": "218"
    }, {
        name: "Liechtenstein",
        cca2: "li",
        "calling-code": "423"
    }, {
        name: "Lithuania",
        cca2: "lt",
        "calling-code": "370"
    }, {
        name: "Luxembourg",
        cca2: "lu",
        "calling-code": "352"
    }, {
        name: "Macao",
        cca2: "mo",
        "calling-code": "853"
    }, {
        name: "Macedonia",
        cca2: "mk",
        "calling-code": "389"
    }, {
        name: "Madagascar",
        cca2: "mg",
        "calling-code": "261"
    }, {
        name: "Malawi",
        cca2: "mw",
        "calling-code": "265"
    }, {
        name: "Malaysia",
        cca2: "my",
        "calling-code": "60"
    }, {
        name: "Maldives",
        cca2: "mv",
        "calling-code": "960"
    }, {
        name: "Mali",
        cca2: "ml",
        "calling-code": "223"
    }, {
        name: "Malta",
        cca2: "mt",
        "calling-code": "356"
    }, {
        name: "Marshall Islands",
        cca2: "mh",
        "calling-code": "692"
    }, {
        name: "Martinique",
        cca2: "mq",
        "calling-code": "596"
    }, {
        name: "Mauritania",
        cca2: "mr",
        "calling-code": "222"
    }, {
        name: "Mauritius",
        cca2: "mu",
        "calling-code": "230"
    }, {
        name: "Mexico",
        cca2: "mx",
        "calling-code": "52"
    }, {
        name: "Micronesia",
        cca2: "fm",
        "calling-code": "691"
    }, {
        name: "Moldova",
        cca2: "md",
        "calling-code": "373"
    }, {
        name: "Monaco",
        cca2: "mc",
        "calling-code": "377"
    }, {
        name: "Mongolia",
        cca2: "mn",
        "calling-code": "976"
    }, {
        name: "Montenegro",
        cca2: "me",
        "calling-code": "382"
    }, {
        name: "Montserrat",
        cca2: "ms",
        "calling-code": "1664"
    }, {
        name: "Morocco",
        cca2: "ma",
        "calling-code": "212"
    }, {
        name: "Mozambique",
        cca2: "mz",
        "calling-code": "258"
    }, {
        name: "Myanmar (Burma)",
        cca2: "mm",
        "calling-code": "95"
    }, {
        name: "Namibia",
        cca2: "na",
        "calling-code": "264"
    }, {
        name: "Nauru",
        cca2: "nr",
        "calling-code": "674"
    }, {
        name: "Nepal",
        cca2: "np",
        "calling-code": "977"
    }, {
        name: "Netherlands",
        cca2: "nl",
        "calling-code": "31"
    }, {
        name: "New Caledonia",
        cca2: "nc",
        "calling-code": "687"
    }, {
        name: "New Zealand",
        cca2: "nz",
        "calling-code": "64"
    }, {
        name: "Nicaragua",
        cca2: "ni",
        "calling-code": "505"
    }, {
        name: "Niger",
        cca2: "ne",
        "calling-code": "227"
    }, {
        name: "Nigeria",
        cca2: "ng",
        "calling-code": "234"
    }, {
        name: "North Korea",
        cca2: "kp",
        "calling-code": "850"
    }, {
        name: "Norway",
        cca2: "no",
        "calling-code": "47"
    }, {
        name: "Oman",
        cca2: "om",
        "calling-code": "968"
    }, {
        name: "Pakistan",
        cca2: "pk",
        "calling-code": "92"
    }, {
        name: "Palau",
        cca2: "pw",
        "calling-code": "680"
    }, {
        name: "Palestinian Territory",
        cca2: "ps",
        "calling-code": "970"
    }, {
        name: "Panama",
        cca2: "pa",
        "calling-code": "507"
    }, {
        name: "Papua New Guinea",
        cca2: "pg",
        "calling-code": "675"
    }, {
        name: "Paraguay",
        cca2: "py",
        "calling-code": "595"
    }, {
        name: "Peru",
        cca2: "pe",
        "calling-code": "51"
    }, {
        name: "Philippines",
        cca2: "ph",
        "calling-code": "63"
    }, {
        name: "Poland",
        cca2: "pl",
        "calling-code": "48"
    }, {
        name: "Portugal",
        cca2: "pt",
        "calling-code": "351"
    }, {
        name: "Puerto Rico",
        cca2: "pr",
        "calling-code": "1787"
    }, {
        name: "Qatar",
        cca2: "qa",
        "calling-code": "974"
    }, {
        name: "Réunion",
        cca2: "re",
        "calling-code": "262"
    }, {
        name: "Romania",
        cca2: "ro",
        "calling-code": "40"
    }, {
        name: "Russian Federation",
        cca2: "ru",
        "calling-code": "7"
    }, {
        name: "Rwanda",
        cca2: "rw",
        "calling-code": "250"
    }, {
        name: "Saint Kitts and Nevis",
        cca2: "kn",
        "calling-code": "1869"
    }, {
        name: "Saint Lucia",
        cca2: "lc",
        "calling-code": "1758"
    }, {
        name: "Saint Vincent and the Grenadines",
        cca2: "vc",
        "calling-code": "1784"
    }, {
        name: "Samoa",
        cca2: "ws",
        "calling-code": "685"
    }, {
        name: "San Marino",
        cca2: "sm",
        "calling-code": "378"
    }, {
        name: "São Tomé and Príncipe",
        cca2: "st",
        "calling-code": "239"
    }, {
        name: "Saudi Arabia",
        cca2: "sa",
        "calling-code": "966"
    }, {
        name: "Senegal",
        cca2: "sn",
        "calling-code": "221"
    }, {
        name: "Serbia",
        cca2: "rs",
        "calling-code": "381"
    }, {
        name: "Seychelles",
        cca2: "sc",
        "calling-code": "248"
    }, {
        name: "Sierra Leone",
        cca2: "sl",
        "calling-code": "232"
    }, {
        name: "Singapore",
        cca2: "sg",
        "calling-code": "65"
    }, {
        name: "Slovakia",
        cca2: "sk",
        "calling-code": "421"
    }, {
        name: "Slovenia",
        cca2: "si",
        "calling-code": "386"
    }, {
        name: "Solomon Islands",
        cca2: "sb",
        "calling-code": "677"
    }, {
        name: "Somalia",
        cca2: "so",
        "calling-code": "252"
    }, {
        name: "South Africa",
        cca2: "za",
        "calling-code": "27"
    }, {
        name: "South Korea",
        cca2: "kr",
        "calling-code": "82"
    }, {
        name: "Spain",
        cca2: "es",
        "calling-code": "34"
    }, {
        name: "Sri Lanka",
        cca2: "lk",
        "calling-code": "94"
    }, {
        name: "Sudan",
        cca2: "sd",
        "calling-code": "249"
    }, {
        name: "Suriname",
        cca2: "sr",
        "calling-code": "597"
    }, {
        name: "Swaziland",
        cca2: "sz",
        "calling-code": "268"
    }, {
        name: "Sweden",
        cca2: "se",
        "calling-code": "46"
    }, {
        name: "Switzerland",
        cca2: "ch",
        "calling-code": "41"
    }, {
        name: "Syrian Arab Republic",
        cca2: "sy",
        "calling-code": "963"
    }, {
        name: "Taiwan, Province of China",
        cca2: "tw",
        "calling-code": "886"
    }, {
        name: "Tajikistan",
        cca2: "tj",
        "calling-code": "992"
    }, {
        name: "Tanzania",
        cca2: "tz",
        "calling-code": "255"
    }, {
        name: "Thailand",
        cca2: "th",
        "calling-code": "66"
    }, {
        name: "Timor-Leste",
        cca2: "tl",
        "calling-code": "670"
    }, {
        name: "Togo",
        cca2: "tg",
        "calling-code": "228"
    }, {
        name: "Tonga",
        cca2: "to",
        "calling-code": "676"
    }, {
        name: "Trinidad and Tobago",
        cca2: "tt",
        "calling-code": "1868"
    }, {
        name: "Tunisia",
        cca2: "tn",
        "calling-code": "216"
    }, {
        name: "Turkey",
        cca2: "tr",
        "calling-code": "90"
    }, {
        name: "Turkmenistan",
        cca2: "tm",
        "calling-code": "993"
    }, {
        name: "Turks and Caicos Islands",
        cca2: "tc",
        "calling-code": "1649"
    }, {
        name: "Tuvalu",
        cca2: "tv",
        "calling-code": "688"
    }, {
        name: "Uganda",
        cca2: "ug",
        "calling-code": "256"
    }, {
        name: "Ukraine",
        cca2: "ua",
        "calling-code": "380"
    }, {
        name: "United Arab Emirates",
        cca2: "ae",
        "calling-code": "971"
    }, {
        name: "United Kingdom",
        cca2: "gb",
        "calling-code": "44"
    }, {
        name: "United States",
        cca2: "us",
        "calling-code": "1"
    }, {
        name: "Uruguay",
        cca2: "uy",
        "calling-code": "598"
    }, {
        name: "Uzbekistan",
        cca2: "uz",
        "calling-code": "998"
    }, {
        name: "Vanuatu",
        cca2: "vu",
        "calling-code": "678"
    }, {
        name: "Vatican City",
        cca2: "va",
        "calling-code": "379"
    }, {
        name: "Venezuela",
        cca2: "ve",
        "calling-code": "58"
    }, {
        name: "Viet Nam",
        cca2: "vn",
        "calling-code": "84"
    }, {
        name: "Virgin Islands (British)",
        cca2: "vg",
        "calling-code": "1284"
    }, {
        name: "Virgin Islands (U.S.)",
        cca2: "vi",
        "calling-code": "1340"
    }, {
        name: "Western Sahara",
        cca2: "eh",
        "calling-code": "212"
    }, {
        name: "Yemen",
        cca2: "ye",
        "calling-code": "967"
    }, {
        name: "Zambia",
        cca2: "zm",
        "calling-code": "260"
    }, {
        name: "Zimbabwe",
        cca2: "zw",
        "calling-code": "263"
    } ],
    countryCodes: {
        "1": [ "us", "ca" ],
        "7": [ "ru", "kz" ],
        "20": [ "eg" ],
        "27": [ "za" ],
        "30": [ "gr" ],
        "31": [ "nl" ],
        "32": [ "be" ],
        "33": [ "fr" ],
        "34": [ "es" ],
        "36": [ "hu" ],
        "39": [ "it" ],
        "40": [ "ro" ],
        "41": [ "ch" ],
        "43": [ "at" ],
        "44": [ "gb", "gg", "im", "je" ],
        "45": [ "dk" ],
        "46": [ "se" ],
        "47": [ "no", "sj" ],
        "48": [ "pl" ],
        "49": [ "de" ],
        "51": [ "pe" ],
        "52": [ "mx" ],
        "53": [ "cu" ],
        "54": [ "ar" ],
        "55": [ "br" ],
        "56": [ "cl" ],
        "57": [ "co" ],
        "58": [ "ve" ],
        "60": [ "my" ],
        "61": [ "au", "cc", "cx" ],
        "62": [ "id" ],
        "63": [ "ph" ],
        "64": [ "nz" ],
        "65": [ "sg" ],
        "66": [ "th" ],
        "81": [ "jp" ],
        "82": [ "kr" ],
        "84": [ "vn" ],
        "86": [ "cn" ],
        "90": [ "tr" ],
        "91": [ "in" ],
        "92": [ "pk" ],
        "93": [ "af" ],
        "94": [ "lk" ],
        "95": [ "mm" ],
        "98": [ "ir" ],
        "211": [ "ss" ],
        "212": [ "ma", "eh" ],
        "213": [ "dz" ],
        "216": [ "tn" ],
        "218": [ "ly" ],
        "220": [ "gm" ],
        "221": [ "sn" ],
        "222": [ "mr" ],
        "223": [ "ml" ],
        "224": [ "gn" ],
        "225": [ "ci" ],
        "226": [ "bf" ],
        "227": [ "ne" ],
        "228": [ "tg" ],
        "229": [ "bj" ],
        "230": [ "mu" ],
        "231": [ "lr" ],
        "232": [ "sl" ],
        "233": [ "gh" ],
        "234": [ "ng" ],
        "235": [ "td" ],
        "236": [ "cf" ],
        "237": [ "cm" ],
        "238": [ "cv" ],
        "239": [ "st" ],
        "240": [ "gq" ],
        "241": [ "ga" ],
        "242": [ "cg" ],
        "243": [ "cd" ],
        "244": [ "ao" ],
        "245": [ "gw" ],
        "246": [ "io" ],
        "247": [ "ac" ],
        "248": [ "sc" ],
        "249": [ "sd" ],
        "250": [ "rw" ],
        "251": [ "et" ],
        "252": [ "so" ],
        "253": [ "dj" ],
        "254": [ "ke" ],
        "255": [ "tz" ],
        "256": [ "ug" ],
        "257": [ "bi" ],
        "258": [ "mz" ],
        "260": [ "zm" ],
        "261": [ "mg" ],
        "262": [ "re", "yt" ],
        "263": [ "zw" ],
        "264": [ "na" ],
        "265": [ "mw" ],
        "266": [ "ls" ],
        "267": [ "bw" ],
        "268": [ "sz" ],
        "269": [ "km" ],
        "290": [ "sh" ],
        "291": [ "er" ],
        "297": [ "aw" ],
        "298": [ "fo" ],
        "299": [ "gl" ],
        "350": [ "gi" ],
        "351": [ "pt" ],
        "352": [ "lu" ],
        "353": [ "ie" ],
        "354": [ "is" ],
        "355": [ "al" ],
        "356": [ "mt" ],
        "357": [ "cy" ],
        "358": [ "fi", "ax" ],
        "359": [ "bg" ],
        "370": [ "lt" ],
        "371": [ "lv" ],
        "372": [ "ee" ],
        "373": [ "md" ],
        "374": [ "am" ],
        "375": [ "by" ],
        "376": [ "ad" ],
        "377": [ "mc" ],
        "378": [ "sm" ],
        "379": [ "va" ],
        "380": [ "ua" ],
        "381": [ "rs" ],
        "382": [ "me" ],
        "385": [ "hr" ],
        "386": [ "si" ],
        "387": [ "ba" ],
        "389": [ "mk" ],
        "420": [ "cz" ],
        "421": [ "sk" ],
        "423": [ "li" ],
        "500": [ "fk" ],
        "501": [ "bz" ],
        "502": [ "gt" ],
        "503": [ "sv" ],
        "504": [ "hn" ],
        "505": [ "ni" ],
        "506": [ "cr" ],
        "507": [ "pa" ],
        "508": [ "pm" ],
        "509": [ "ht" ],
        "590": [ "gp", "bl", "mf" ],
        "591": [ "bo" ],
        "592": [ "gy" ],
        "593": [ "ec" ],
        "594": [ "gf" ],
        "595": [ "py" ],
        "596": [ "mq" ],
        "597": [ "sr" ],
        "598": [ "uy" ],
        "599": [ "cw", "bq" ],
        "670": [ "tl" ],
        "672": [ "nf" ],
        "673": [ "bn" ],
        "674": [ "nr" ],
        "675": [ "pg" ],
        "676": [ "to" ],
        "677": [ "sb" ],
        "678": [ "vu" ],
        "679": [ "fj" ],
        "680": [ "pw" ],
        "681": [ "wf" ],
        "682": [ "ck" ],
        "683": [ "nu" ],
        "685": [ "ws" ],
        "686": [ "ki" ],
        "687": [ "nc" ],
        "688": [ "tv" ],
        "689": [ "pf" ],
        "690": [ "tk" ],
        "691": [ "fm" ],
        "692": [ "mh" ],
        "850": [ "kp" ],
        "852": [ "hk" ],
        "853": [ "mo" ],
        "855": [ "kh" ],
        "856": [ "la" ],
        "880": [ "bd" ],
        "886": [ "tw" ],
        "960": [ "mv" ],
        "961": [ "lb" ],
        "962": [ "jo" ],
        "963": [ "sy" ],
        "964": [ "iq" ],
        "965": [ "kw" ],
        "966": [ "sa" ],
        "967": [ "ye" ],
        "968": [ "om" ],
        "970": [ "ps" ],
        "971": [ "ae" ],
        "972": [ "il" ],
        "973": [ "bh" ],
        "974": [ "qa" ],
        "975": [ "bt" ],
        "976": [ "mn" ],
        "977": [ "np" ],
        "992": [ "tj" ],
        "993": [ "tm" ],
        "994": [ "az" ],
        "995": [ "ge" ],
        "996": [ "kg" ],
        "998": [ "uz" ],
        "1242": [ "bs" ],
        "1246": [ "bb" ],
        "1264": [ "ai" ],
        "1268": [ "ag" ],
        "1284": [ "vg" ],
        "1340": [ "vi" ],
        "1345": [ "ky" ],
        "1441": [ "bm" ],
        "1473": [ "gd" ],
        "1649": [ "tc" ],
        "1664": [ "ms" ],
        "1671": [ "gu" ],
        "1684": [ "as" ],
        "1758": [ "lc" ],
        "1767": [ "dm" ],
        "1784": [ "vc" ],
        "1787": [ "pr" ],
        "1809": [ "do" ],
        "1868": [ "tt" ],
        "1869": [ "kn" ],
        "1876": [ "jm" ]
    }
};
  </script>
  <script>
  $( document ).ready(function() {

      $("#mobile-number").intlTelInput();

      });
</script>
  <script>
  $( document ).ready(function() {

      $("#mobile-number1").intlTelInput();

      });
</script>
</div>
</body>
</html> 

