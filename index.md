---
layout: base
title: Student Home 
description: Home Page
hide: true
---

{%include nav/home.html %}
<style>
</style>
<body>
  <div id="typedtext"></div>
</body>

{%include homepage.html %}
<!-- My journey starts here. -->
<!-- <script>
    window.onload = setInterval(musicLoop, 1000/10);
    let myAudio = new Audio();
    myAudio.src = 'ff7.wav';
    function musicLoop()
    {
        myAudio.play()
        if (myAudio.paused == true)
        {
            myAudio.play()
        }
    }
</script> -->
<script>
    var aText = new Array(
"Hi there! Welcome to my blog!"
)
var iSpeed = 100; // time delay of print out
var iIndex = 0; // start printing array at this posision
var iArrLength = aText[0].length; // the length of the text array
var iScrollAt = 20; // start scrolling up at this many lines
 
var iTextPos = 0; // initialise text position
var sContents = ''; // initialise contents variable
var iRow; // initialise current row
 
function typewriter()
{
 sContents =  ' ';
 iRow = Math.max(0, iIndex-iScrollAt);
 var destination = document.getElementById("typedtext");
 
 while ( iRow < iIndex ) {
  sContents += aText[iRow++] + '<br />';
 }
 destination.innerHTML = sContents + aText[iIndex].substring(0, iTextPos) + "_";
 if ( iTextPos++ == iArrLength ) {
  iTextPos = 0;
  iIndex++;
  if ( iIndex != aText.length ) {
   iArrLength = aText[iIndex].length;
   setTimeout("typewriter()", 500);
  }
 } else {
  setTimeout("typewriter()", iSpeed);
 }
}


typewriter();
</script>