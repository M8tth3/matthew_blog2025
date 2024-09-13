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
           - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>
{% include nav/home.html %}
<div></div>

<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "I am in California", "description": "California"},
        {"flag": "5/54/Flag_of_Washington.svg", "greeting": "I was in Washington", "description": "Washington"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### If you could have one super power... what would it be?
**I would personally like the ability to fly. While there are some disadvantages, the advantages outweigh in my humble opinion. You can check out some advantages and disadvantages [here](https://www.quora.com/What-would-be-the-advantages-and-disadvantages-of-everyone-in-the-world-having-the-ability-to-fly)**
<br>

<img id='me' src="{{site.baseurl}}//images/Subject.png" width="60px" height=auto>

<br>


<button onclick='fly()' class='button-30' id="fly">I also would like the ability to fly</button>

### Hobbies
    I enjoy swimming. I'm on the Del Norte Swim Team and I swim for a club team called Pacific Swim as well.

    In my free time I like to play video games.

    Recently I've been playing chess puzzles which I've been having a lot of fun with. They are very helpful for destressing(sometimes)


<p>&#128512;</p>


<img class='images' src='https://github.com/user-attachments/assets/ca8a7a23-8bb7-4390-85ef-b7b493d71470'>

    I like to hang out with my friends, sometimes we'll go on runs or just chill out. 

<img class='images' src='https://github.com/user-attachments/assets/0395f9f2-48ab-47bd-b785-c5f638384299'>

    I enjoy baking every now and then. I've made a few desserts and am planning on making many more in my free time.

<img class='images' src='https://github.com/user-attachments/assets/f82db223-fb56-4d20-951e-bcdd78c8be0b'>

### Family
    This is my family. I am the middle child of three children. I am 5.5 years younger than my older sister and 5.5 years older than my younger sister. My older sister just 
<p>&#128585;</p>

<img class='images' src='https://github.com/user-attachments/assets/c2c54cb7-b3ad-49fa-a45f-da19da544fae'>

![image](https://github.com/user-attachments/assets/dc616681-2eb5-4430-af7b-6bdab74fdddb)


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