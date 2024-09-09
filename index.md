---
layout: base
title: Student Home 
description: Home Page
hide: true
---


{%include homepage.html %}

<!-- My journey starts here. -->
<script>
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
</script>