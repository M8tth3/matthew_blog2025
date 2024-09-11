---
layout: page
title: About
permalink: /about/

---
<style>
    body{
        display: flex;
        justify-content: center; /* Center horizontally */
    }
    #me{
        transform: scaleX(-1);
        display: none;
    }
    
    @keyframes flyLinear {
            0% {
                transform: translate(0, 0) rotate(0deg);
            }
            50%
            {
                transform: rotate(45deg);
            }
            100% {
                transform: translate(400px, -400px);
            }
        }


    .flying {
        animation: flyLinear 2s ease-in-out forwards;
    }
    .images {
        width:300px;
        height:auto;
    }
</style>
{% include nav/home.html %}
<div></div>

### If you could have one super power... what would it be?
**I would personally like the ability to fly. While there are some disadvantages, the advantages outweigh in my humble opinion. You can check out some advantages and disadvantages [here](https://www.quora.com/What-would-be-the-advantages-and-disadvantages-of-everyone-in-the-world-having-the-ability-to-fly)**
<br>

<img id='me' src="{{site.baseurl}}//images/Subject.png" width="60px" height=auto>

<br>


<button onclick='fly()' class='button-30' id="fly">I also would like the ability to fly</button>

### Hobbies
    I enjoy swimming. I'm on the Del Norte Swim Team and I swim for a club team called Pacific Swim as well.


    In my free time I like to play video games.
    
<p>&#128512;</p>

<img class='images' src='https://github.com/user-attachments/assets/ca8a7a23-8bb7-4390-85ef-b7b493d71470'>

    I like to hang out with my friends

<img class='images' src='https://github.com/user-attachments/assets/0395f9f2-48ab-47bd-b785-c5f638384299'>

    I enjoy baking every now and then. I've made a few desserts and am planning on making many more in my free time.

<img class='images' src='https://github.com/user-attachments/assets/f82db223-fb56-4d20-951e-bcdd78c8be0b'>

### Family
    This is my family. I am the middle child of three children. I am 5.5 years younger than my older sister and 5.5 years older than my younger sister. My older sister just 
<p>&#128585;</p>

<img class='images' src='https://github.com/user-attachments/assets/c2c54cb7-b3ad-49fa-a45f-da19da544fae'>

<script>
    function fly()
    {
        const me = document.getElementById('me')
        me.style.display = "block"
        me.classList.add('flying')
        let myAudio = new Audio();
        myAudio.src = '{{site.baseurl}}/pew.mp3';
        setTimeout(() => {
            myAudio.play();
            if (myAudio.paused) {
                myAudio.play();
            }
        }, 1000);
    }
</script>


<script src="https://utteranc.es/client.js"
        repo="m8tth3/matthew_blog2025"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>