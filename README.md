<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Lola ♡</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Georgia, "Times New Roman", serif;
    color: #edf8ff;
    min-height: 100vh;
    overflow-x: hidden;
    background:
        radial-gradient(circle at 15% 10%, rgba(78,164,255,.24), transparent 28%),
        radial-gradient(circle at 85% 25%, rgba(116,89,255,.20), transparent 30%),
        radial-gradient(circle at 45% 75%, rgba(53,187,255,.16), transparent 32%),
        linear-gradient(
            180deg,
            #01030d 0%,
            #05091d 38%,
            #07132c 70%,
            #020510 100%
        );
    position: relative;
}

/* STARS */

body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: -10;
    background-image:
        radial-gradient(circle, rgba(255,255,255,.95) 1px, transparent 1.5px),
        radial-gradient(circle, rgba(160,215,255,.8) 1px, transparent 1.5px),
        radial-gradient(circle, rgba(255,255,255,.65) 1px, transparent 1.5px);
    background-size:
        85px 85px,
        135px 135px,
        210px 210px;
    background-position:
        10px 20px,
        50px 80px,
        120px 40px;
    animation: starsMove 40s linear infinite;
    opacity: .55;
}

@keyframes starsMove {
    from {
        transform: translateY(0);
    }

    to {
        transform: translateY(85px);
    }
}

/* GALAXY CLOUDS */

.galaxy-cloud {
    position: fixed;
    width: 500px;
    height: 500px;
    border-radius: 50%;
    filter: blur(80px);
    opacity: .13;
    pointer-events: none;
    z-index: -8;
}

.cloud-one {
    background: #42a5ff;
    top: -220px;
    left: -170px;
}

.cloud-two {
    background: #8a63ff;
    top: 35%;
    right: -240px;
}

.cloud-three {
    background: #36cfff;
    bottom: -280px;
    left: 20%;
}

/* SHOOTING STARS */

.shooting-star {
    position: fixed;
    width: 140px;
    height: 2px;
    background: linear-gradient(
        90deg,
        transparent,
        #bfeaff,
        white
    );
    transform: rotate(-35deg);
    opacity: 0;
    pointer-events: none;
    z-index: -4;
    animation: shooting 9s linear infinite;
}

.shooting-star.one {
    top: 14%;
    left: -160px;
    animation-delay: 2s;
}

.shooting-star.two {
    top: 52%;
    left: -160px;
    animation-delay: 6s;
}

@keyframes shooting {

    0% {
        transform: translate(-100px,-50px) rotate(-35deg);
        opacity: 0;
    }

    8% {
        opacity: 1;
    }

    25% {
        transform: translate(100vw,40vh) rotate(-35deg);
        opacity: 0;
    }

    100% {
        opacity: 0;
    }
}

/* STINGRAYS */

.stingray {
    position: fixed;
    width: 110px;
    height: 65px;
    z-index: -3;
    opacity: .28;
    pointer-events: none;
    animation: swimAcross 27s linear infinite;
}

.stingray::before {
    content: "";
    position: absolute;
    width: 72px;
    height: 45px;
    left: 15px;
    top: 5px;
    background:
        radial-gradient(
            ellipse at 50% 35%,
            rgba(185,235,255,.8),
            rgba(77,145,185,.75) 60%,
            rgba(40,91,130,.7)
        );
    clip-path: polygon(
        0% 38%,
        22% 0%,
        50% 25%,
        78% 0%,
        100% 38%,
        72% 70%,
        58% 100%,
        42% 100%,
        28% 70%
    );
    box-shadow: 0 0 25px rgba(110,210,255,.3);
}

.stingray::after {
    content: "";
    position: absolute;
    width: 58px;
    height: 2px;
    left: 68px;
    top: 48px;
    background: #70c9ed;
    transform: rotate(16deg);
    transform-origin: left center;
    box-shadow: 0 0 7px rgba(100,210,255,.35);
}

.stingray .tail {
    position: absolute;
    width: 8px;
    height: 8px;
    left: 70px;
    top: 42px;
    border-radius: 50%;
    background: #8bdcff;
    opacity: .7;
}

.stingray-one {
    top: 17%;
    left: -160px;
    animation-delay: 0s;
}

.stingray-two {
    top: 45%;
    left: -180px;
    animation-delay: 9s;
    transform: scale(.72);
}

.stingray-three {
    top: 72%;
    left: -160px;
    animation-delay: 16s;
    transform: scale(1.15);
}

@keyframes swimAcross {

    0% {
        left: -170px;
        transform: translateY(0) rotate(0deg);
    }

    25% {
        transform: translateY(-30px) rotate(4deg);
    }

    50% {
        transform: translateY(20px) rotate(-4deg);
    }

    75% {
        transform: translateY(-20px) rotate(4deg);
    }

    100% {
        left: 110vw;
        transform: translateY(0) rotate(0deg);
    }
}

/* PEONIES */

.peony {
    position: fixed;
    z-index: -2;
    pointer-events: none;
    font-size: 2.8rem;
    opacity: .16;
    animation: floatPeony 14s ease-in-out infinite;
}

.peony.one {
    left: 7%;
    top: 25%;
    animation-delay: 1s;
}

.peony.two {
    right: 8%;
    top: 58%;
    font-size: 3.4rem;
    animation-delay: 5s;
}

.peony.three {
    left: 13%;
    bottom: 12%;
    font-size: 2.4rem;
    animation-delay: 9s;
}

.peony.four {
    right: 15%;
    top: 10%;
    font-size: 2.2rem;
    animation-delay: 3s;
}

@keyframes floatPeony {

    0%,100% {
        transform: translateY(0) rotate(-5deg);
    }

    50% {
        transform: translateY(-22px) rotate(7deg);
    }
}

/* MAIN */

.container {
    width: min(900px,92%);
    margin: auto;
    position: relative;
    z-index: 2;
}

section {
    padding: 95px 0;
}

.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.hero-inner {
    max-width: 760px;
}

.small-title {
    color: #9ddcff;
    letter-spacing: 4px;
    text-transform: uppercase;
    font-size: .75rem;
    margin-bottom: 25px;
}

h1 {
    font-size: clamp(4rem,15vw,8rem);
    color: #c8edff;
    text-shadow:
        0 0 10px rgba(140,215,255,.5),
        0 0 35px rgba(100,180,255,.4),
        0 0 70px rgba(90,160,255,.25);
    margin-bottom: 20px;
    animation: glow 4s ease-in-out infinite;
}

@keyframes glow {

    0%,100% {
        text-shadow:
            0 0 10px rgba(140,215,255,.5),
            0 0 35px rgba(100,180,255,.4);
    }

    50% {
        text-shadow:
            0 0 20px rgba(180,230,255,.8),
            0 0 60px rgba(100,180,255,.7);
    }
}

h2 {
    font-size: clamp(2rem,7vw,3.6rem);
    color: #bde9ff;
    margin-bottom: 25px;
}

h3 {
    color: #c9edff;
    margin-bottom: 12px;
}

p {
    line-height: 1.9;
    color: #dcefff;
}

.hero p {
    font-size: 1.15rem;
    max-width: 650px;
    margin: auto;
}

.button {
    display: inline-block;
    margin-top: 35px;
    padding: 15px 28px;
    border: 1px solid rgba(180,225,255,.55);
    border-radius: 50px;
    color: #effaff;
    text-decoration: none;
    background: rgba(110,190,255,.08);
    transition: .3s;
    cursor: pointer;
    font-family: inherit;
    font-size: 1rem;
    box-shadow: 0 0 20px rgba(80,170,255,.08);
}

.button:hover {
    background: rgba(150,220,255,.2);
    transform: translateY(-4px);
    box-shadow: 0 0 35px rgba(130,210,255,.25);
}

.card {
    background: rgba(255,255,255,.055);
    border: 1px solid rgba(180,220,255,.16);
    border-radius: 28px;
    padding: 35px;
    margin: 25px 0;
    backdrop-filter: blur(15px);
    box-shadow: 0 20px 60px rgba(0,0,0,.25);
}

.center {
    text-align: center;
}

.intro {
    font-size: 1.15rem;
    max-width: 720px;
    margin: auto;
}

/* HEART */

.tap-heart {
    width: 105px;
    height: 105px;
    margin: 35px auto;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3.2rem;
    cursor: pointer;
    background: rgba(130,210,255,.08);
    border: 1px solid rgba(170,220,255,.3);
    box-shadow: 0 0 35px rgba(100,190,255,.15);
    transition: .4s;
    animation: heartPulse 2.5s ease-in-out infinite;
}

.tap-heart:hover {
    transform: scale(1.12);
}

@keyframes heartPulse {

    0%,100% {
        box-shadow: 0 0 20px rgba(100,190,255,.12);
    }

    50% {
        box-shadow: 0 0 45px rgba(100,210,255,.3);
    }
}

.heart-message {
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: max-height 1s ease,opacity 1s ease;
}

.heart-message.show {
    max-height: 500px;
    opacity: 1;
}

/* REASONS */

.reasons {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(230px,1fr));
    gap: 15px;
    margin-top: 35px;
}

.reason {
    border: 1px solid rgba(180,220,255,.14);
    border-radius: 20px;
    padding: 22px;
    background: rgba(255,255,255,.045);
    cursor: pointer;
    transition: .35s;
}

.reason:hover {
    transform: translateY(-5px);
    background: rgba(130,210,255,.1);
}

.reason-number {
    color: #83d2ff;
    font-size: .8rem;
    margin-bottom: 8px;
}

.reason .secret {
    display: block;
    margin-top: 12px;
    color: #bce8ff;
    opacity: 0;
    max-height: 0;
    overflow: hidden;
    transition: .5s;
}

.reason.revealed .secret {
    opacity: 1;
    max-height: 200px;
}

/* TIMELINE */

.timeline {
    margin-top: 40px;
}

.timeline-item {
    padding: 28px;
    margin: 20px 0;
    border-left: 2px solid #83caff;
    background: rgba(255,255,255,.04);
    border-radius: 0 20px 20px 0;
    transition: .3s;
}

.timeline-item:hover {
    transform: translateX(5px);
    background: rgba(120,200,255,.07);
}

/* FAVOURITES */

.favourites {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(170px,1fr));
    gap: 15px;
    margin-top: 30px;
}

.favourite {
    text-align: center;
    padding: 28px 15px;
    border-radius: 22px;
    background: rgba(255,255,255,.05);
    border: 1px solid rgba(180,220,255,.12);
    transition: .35s;
}

.favourite:hover {
    transform: translateY(-6px);
    box-shadow: 0 10px 35px rgba(100,190,255,.1);
}

.favourite-icon {
    font-size: 2.3rem;
    margin-bottom: 12px;
}

/* CONSTELLATION */

.constellation {
    position: relative;
    height: 280px;
    margin-top: 30px;
    border-radius: 25px;
    background:
        radial-gradient(
            circle at center,
            rgba(100,180,255,.08),
            transparent 65%
        );
    overflow: hidden;
    border: 1px solid rgba(160,220,255,.12);
}

.constellation::before {
    content: "";
    position: absolute;
    width: 65%;
    height: 1px;
    background: rgba(170,220,255,.25);
    top: 43%;
    left: 18%;
    transform: rotate(10deg);
}

.constellation::after {
    content: "";
    position: absolute;
    width: 55%;
    height: 1px;
    background: rgba(170,220,255,.2);
    top: 48%;
    left: 25%;
    transform: rotate(-18deg);
}

.star {
    position: absolute;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background: white;
    box-shadow: 0 0 18px #a9ddff;
    cursor: pointer;
    transition: .3s;
    z-index: 2;
}

.star:hover {
    transform: scale(1.8);
}

.star.one {
    left: 20%;
    top: 35%;
}

.star.two {
    left: 40%;
    top: 20%;
}

.star.three {
    left: 60%;
    top: 40%;
}

.star.four {
    left: 75%;
    top: 25%;
}

.star.five {
    left: 50%;
    top: 70%;
}

.constellation-message {
    text-align: center;
    padding-top: 25px;
    color: #aee3ff;
    min-height: 60px;
}

/* OPEN WHEN */

.open-when {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
    gap: 15px;
    margin-top: 30px;
}

.open-button {
    padding: 27px 15px;
    border: 1px solid rgba(180,220,255,.2);
    border-radius: 22px;
    background: rgba(255,255,255,.045);
    color: #dff5ff;
    font-family: inherit;
    font-size: 1rem;
    cursor: pointer;
    transition: .35s;
}

.open-button:hover {
    background: rgba(150,210,255,.12);
    transform: translateY(-5px);
}

/* FUTURE */

.future-list {
    list-style: none;
    margin-top: 30px;
}

.future-list li {
    padding: 20px;
    margin: 12px 0;
    border-radius: 18px;
    background: rgba(255,255,255,.045);
    border: 1px solid rgba(180,220,255,.1);
    transition: .3s;
}

.future-list li:hover {
    transform: translateX(8px);
}

.future-list li::before {
    content: "✦ ";
    color: #83caff;
}

/* TREASURE HUNT */

.treasure {
    text-align: center;
}

.clue {
    padding: 25px;
    border-radius: 20px;
    background: rgba(255,255,255,.045);
    border: 1px solid rgba(180,220,255,.13);
    margin-top: 25px;
    line-height: 1.9;
}

.clue-number {
    color: #83d2ff;
    letter-spacing: 2px;
    font-size: .8rem;
    margin-bottom: 12px;
}

.clue-button {
    margin-top: 20px;
}

/* WORD FIND */

.word-find {
    display: grid;
    grid-template-columns: repeat(10,1fr);
    max-width: 620px;
    margin: 30px auto;
    border: 1px solid rgba(180,220,255,.2);
    border-radius: 15px;
    overflow: hidden;
}

.letter-cell {
    aspect-ratio: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid rgba(180,220,255,.08);
    background: rgba(255,255,255,.035);
    color: #dff5ff;
    font-size: clamp(.7rem,3vw,1rem);
    cursor: pointer;
    user-select: none;
    transition: .2s;
}

.letter-cell:hover {
    background: rgba(130,210,255,.15);
}

.letter-cell.selected {
    background: rgba(110,205,255,.3);
}

.letter-cell.found {
    background: rgba(110,210,255,.22);
    color: white;
}

.word-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    margin-top: 20px;
}

.word-pill {
    padding: 8px 13px;
    border-radius: 30px;
    border: 1px solid rgba(180,220,255,.15);
    background: rgba(255,255,255,.04);
    color: #bce8ff;
    font-size: .85rem;
}

.word-pill.found {
    text-decoration: line-through;
    opacity: .55;
}

/* COLOURING */

.colouring-area {
    text-align: center;
}

canvas {
    width: 100%;
    max-width: 700px;
    height: auto;
    display: block;
    margin: 30px auto 20px;
    border-radius: 22px;
    background: #dff5ff;
    border: 2px solid rgba(180,220,255,.25);
    touch-action: none;
}

.colour-tools {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin: 20px 0;
}

.colour {
    width: 35px;
    height: 35px;
    border-radius: 50%;
    border: 2px solid rgba(255,255,255,.7);
    cursor: pointer;
}

.clear-colour {
    padding: 10px 18px;
    border-radius: 25px;
    border: 1px solid rgba(180,220,255,.25);
    background: rgba(255,255,255,.05);
    color: #dff5ff;
    cursor: pointer;
    font-family: inherit;
}

/* LETTER */

.letter {
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: max-height 1.5s ease,opacity 1s ease;
}

.letter.open {
    max-height: 1500px;
    opacity: 1;
}

.letter p {
    margin-bottom: 20px;
}

/* FINAL */

.final-card {
    text-align: center;
    padding: 55px 30px;
    background:
        radial-gradient(
            circle at center,
            rgba(120,200,255,.13),
            transparent 65%
        ),
        rgba(255,255,255,.04);
}

.hidden-message {
    display: none;
    margin-top: 30px;
    font-size: 1.2rem;
    line-height: 2;
    color: #dff5ff;
}

/* FOOTER */

footer {
    text-align: center;
    padding: 45px 20px;
    color: #7fa8c4;
    font-size: .9rem;
}

/* MOBILE */

@media (max-width:600px) {

    section {
        padding: 70px 0;
    }

    .card {
        padding: 24px;
    }

    .stingray {
        opacity: .16;
    }

    .constellation {
        height: 230px;
    }

    .word-find {
        max-width: 100%;
    }

    .letter-cell {
        font-size: .68rem;
    }
}
</style>
</head>

<body>

<div class="galaxy-cloud cloud-one"></div>
<div class="galaxy-cloud cloud-two"></div>
<div class="galaxy-cloud cloud-three"></div>

<div class="shooting-star one"></div>
<div class="shooting-star two"></div>

<div class="stingray stingray-one">
    <div class="tail"></div>
</div>

<div class="stingray stingray-two">
    <div class="tail"></div>
</div>

<div class="stingray stingray-three">
    <div class="tail"></div>
</div>

<div class="peony one">🌸</div>
<div class="peony two">🌸</div>
<div class="peony three">🌸</div>
<div class="peony four">🌸</div>


<!-- HERO -->

<section class="hero">

<div class="container hero-inner">

<div class="small-title">
A little universe made for
</div>

<h1 id="heroName"></h1>

<p>
Twenty-seven years of you.
</p>

<p style="margin-top:20px;">
And somehow, in all the billions of people in this world,
I got lucky enough to find you.
</p>

<a href="#birthday" class="button">
Enter my little universe ↓
</a>

</div>

</section>


<!-- BIRTHDAY -->

<section id="birthday">

<div class="container">

<div class="card center">

<div class="small-title">
For the girl who became my universe
</div>

<h2 id="birthdayTitle"></h2>

<p class="intro" id="birthdayMessage"></p>

<p class="intro" style="margin-top:20px;" id="birthdayIntro"></p>

<div class="tap-heart" onclick="revealHeart()">
♡
</div>

<div class="heart-message" id="heartMessage">

<p>
Tap the heart whenever you want a little piece of my heart.
</p>

<p style="margin-top:15px;">
Because if I could put every reason I love you into the stars,
there still wouldn't be enough of them.
</p>

</div>

</div>

</div>

</section>


<!-- 27 REASONS -->

<section>

<div class="container">

<div class="center">

<div class="small-title">
Twenty-seven little reasons
</div>

<h2>
Why I love you
</h2>

<p>
Tap each one. Every one is hiding something.
</p>

</div>

<div class="reasons" id="reasons"></div>

</div>

</section>


<!-- STORY -->

<section>

<div class="container">

<div class="center">

<div class="small-title">
Our little story
</div>

<h2>
Then, now, always.
</h2>

</div>

<div class="timeline">

<div class="timeline-item">

<h3>
Then there was you.
</h3>

<p>
Somewhere among all the people in this enormous world,
our paths crossed.

And somehow, I found my way to you.
</p>

</div>

<div class="timeline-item">

<h3>
The distance.
</h3>

<p>
Different countries.
Different skies.
Different time zones.

And somehow you still became one of the closest people to my heart.
</p>

</div>

<div class="timeline-item">

<h3>
All the little things.
</h3>

<p>
The conversations.
The laughter.
The sleepy nights.
The storms.
The moments when your voice made everything feel okay.
</p>

</div>

<div class="timeline-item">

<h3>
And now you're 27.
</h3>

<p>
Another year of you existing,
growing,
dreaming,
laughing,
loving,
and becoming more completely yourself.
</p>

</div>

</div>

</div>

</section>


<!-- FAVOURITES -->

<section>

<div class="container">

<div class="center">

<div class="small-title">
Things that remind me of you
</div>

<h2>
Your little universe
</h2>

</div>

<div class="favourites" id="favourites"></div>

</div>

</section>


<!-- CONSTELLATION -->

<section>

<div class="container">

<div class="card center">

<div class="small-title">
A constellation for you
</div>

<h2>
Find the stars ♡
</h2>

<p>
Tap the stars.
Something is waiting underneath them.
</p>

<div class="constellation">

<div class="star one" onclick="starMessage(1)"></div>
<div class="star two" onclick="starMessage(2)"></div>
<div class="star three" onclick="starMessage(3)"></div>
<div class="star four" onclick="starMessage(4)"></div>
<div class="star five" onclick="starMessage(5)"></div>

</div>

<div class="constellation-message" id="starMessage">
Tap a star above ✦
</div>

</div>

</div>

</section>


<!-- OPEN WHEN -->

<section>

<div class="container">

<div class="center">

<div class="small-title">
For whenever you need me
</div>

<h2>
Open when...
</h2>

<p>
Some words from me for the moments when you need them most.
</p>

</div>

<div class="open-when">

<button class="open-button" onclick="showMessage('miss')">
💌
<br><br>
You miss me
</button>

<button class="open-button" onclick="showMessage('sad')">
🩵
<br><br>
You're sad
</button>

<button class="open-button" onclick="showMessage('sleep')">
🌙
<br><br>
You can't sleep
</button>

<button class="open-button" onclick="showMessage('loved')">
⭐
<br><br>
You need to feel loved
</button>

</div>

</div>

</section>


<!-- FUTURE -->

<section>

<div class="container">

<div class="center">

<div class="small-title">
Things I want with you
</div>

<h2>
Our someday
</h2>

<p>
These are little places I hope life takes us.
</p>

</div>

<ul class="future-list" id="future"></ul>

</div>

</section>


<!-- TREASURE HUNT -->

<section>

<div class="container">

<div class="card treasure">

<div class="small-title">
A little adventure
</div>

<h2>
Find your birthday treasure ♡
</h2>

<p>
Follow the clues through your little universe.
</p>

<div class="clue">

<div class="clue-number">
CLUE ONE
</div>

<p>
I shine above you, but I'm not the sun.
Find me where our little universe keeps its secrets.
</p>

<p style="margin-top:12px;">
Hint: the stars are waiting.
</p>

<button class="button clue-button" onclick="nextClue()">
I found it ✦
</button>

</div>

<div id="treasureResult" style="margin-top:25px;"></div>

</div>

</div>

</section>


<!-- WORD FIND -->

<section>

<div class="container">

<div class="card center">

<div class="small-title">
A little game for you
</div>

<h2>
Find the words ♡
</h2>

<p>
Tap the letters of each word in order.
</p>

<div class="word-find" id="wordFind"></div>

<div class="word-list" id="wordList"></div>

<p id="wordStatus" style="margin-top:20px;">
Find all ten words ✦
</p>

</div>

</div>

</section>


<!-- COLOURING -->

<section>

<div class="container">

<div class="card colouring-area">

<div class="small-title">
Something for you to colour
</div>

<h2>
Our little sunrise 🌅
</h2>

<p>
Colour the sunrise you'd like us to see together someday.
</p>

<div class="colour-tools">

<button class="colour" style="background:#ffb6c1;" onclick="setColour('#ffb6c1')"></button>

<button class="colour" style="background:#ffd166;" onclick="setColour('#ffd166')"></button>

<button class="colour" style="background:#ff9f68;" onclick="setColour('#ff9f68')"></button>

<button class="colour" style="background:#9ddcff;" onclick="setColour('#9ddcff')"></button>

<button class="colour" style="background:#78c091;" onclick="setColour('#78c091')"></button>

<button class="colour" style="background:#b995d6;" onclick="setColour('#b995d6')"></button>

<button class="colour" style="background:#ffffff;" onclick="setColour('#ffffff')"></button>

<button class="clear-colour" onclick="clearCanvas()">
Start again
</button>

</div>

<canvas id="sunriseCanvas" width="700" height="450"></canvas>

<p>
You can colour with your finger on your phone or with your mouse.
</p>

</div>

</div>

</section>


<!-- LOVE LETTER -->

<section>

<div class="container">

<div class="card center">

<div class="small-title">
A letter from me to you
</div>

<h2>
Read this when you're ready ♡
</h2>

<button class="button" onclick="openLetter()">
Open my heart
</button>

<div class="letter" id="letter">

<br>

<p>
My love,
</p>

<p>
I wish I could be there beside you today.
</p>

<p>
I wish I could watch your face when you wake up,
give you something wrapped in far too much ribbon,
and steal the first birthday hug before anyone else could.
</p>

<p>
But even though there are kilometres between us,
there is something distance has never managed to touch.
</p>

<p>
The way I love you.
</p>

<p>
You became home to me in a way I never expected.
</p>

<p>
Not because of a place.
</p>

<p>
Not because of a house.
</p>

<p>
But because somehow,
when I'm talking to you,
the world becomes a little quieter.
</p>

<p>
So on your twenty-seventh birthday,
I hope you remember something.
</p>

<p>
You are so deeply loved.
</p>

<p>
Not because you're perfect.
</p>

<p>
Not because you always have everything figured out.
</p>

<p>
But because you're you.
</p>

<p>
I hope this next year gives you moments
that make your heart feel light.
</p>

<p>
Places you've never seen.
Things you've always wanted to try.
Quiet mornings.
Beautiful sunsets.
And eventually,
an ocean that we can stand beside together.
</p>

<p>
And if I had to find you again
through every lifetime,
every universe,
every galaxy,
every version of this world...
</p>

<p>
I'd still look for you.
</p>

<p>
I'd recognise your heart.
I'd recognise your laugh.
I'd recognise the way you make home feel
less like a place and more like a person.
</p>

<p>
Happy birthday, my love.
</p>

<p>
I'll find you beneath every sky.
</p>

<p>
<br>
Bree / Putiputi ♡
</p>

</div>

</div>

</div>

</section>


<!-- FINAL -->

<section>

<div class="container">

<div class="card final-card">

<div class="small-title">
One last thing
</div>

<h2>
Until I can give you these things in person...
</h2>

<p>
let this little universe hold them for me.
</p>

<p style="margin-top:25px;">
Love always,
<br>
<strong>Bree / Putiputi</strong>
♡
</p>

<button class="button" onclick="revealFinal()">
One last thing... 🩵
</button>

<div class="hidden-message" id="finalMessage"></div>

</div>

</div>

</section>


<footer>

Made with an unreasonable amount of love for Lola ♡

<br><br>

🌌 🩵 🦦 🌊 ⭐ 🌸

</footer>


<script>

/* BIRTHDAY INFORMATION */

const birthday = {

    name: "Lola",

    age: 27,

    from: "Bree / Putiputi",

    birthdayMessage:
        "Today isn't just about another year passing. It's about celebrating the person who makes my world softer simply by existing in it.",

    intro:
        "So I made you a tiny universe. Every little corner is here because it reminds me of you."

};


/* 27 REASONS */

const reasons = [

    "Your hazel eyes.",
    "Your voice.",
    "The way you make me feel at home.",
    "Your little laugh.",
    "Your beautiful heart.",
    "Your softness.",
    "Your strength.",
    "Your love for otters.",
    "Your baby blue world.",
    "Your black coffee.",
    "The way you make me smile.",
    "The way you listen.",
    "Your little habits.",
    "Your beautiful soul.",
    "The way you calm me.",
    "The way you make ordinary moments special.",
    "Your kindness.",
    "Your patience.",
    "Your silly side.",
    "Your beautiful mind.",
    "The way you make distance feel smaller.",
    "The way you became my home.",
    "The way you make me feel understood.",
    "Your dreams.",
    "Your courage.",
    "The person you are becoming.",
    "Simply because you're Lola."

];


const secretReasons = [

    "There is something about looking into your eyes that makes everything else disappear for a moment.",

    "Even when you don't realise it, hearing you can turn an ordinary moment into one I want to remember.",

    "Home stopped being somewhere I needed to go when I realised how safe my heart feels with you.",

    "I would happily do ridiculous things just to hear that laugh one more time.",

    "You care more deeply than you sometimes realise, and that tenderness is one of the things I treasure most.",

    "The softness you carry isn't weakness. It is one of the most beautiful things about you.",

    "I admire every quiet moment where you kept going even when nobody else could see how hard it was.",

    "Somehow the fact that you love these adorable little creatures makes me love your heart even more.",

    "Whenever I see that colour, a tiny part of my brain immediately thinks of you.",

    "I don't even have to like the coffee. I just love imagining you holding your little cup of it.",

    "Sometimes I'll be completely fine and then I'll remember something about you and suddenly I'm smiling at my phone.",

    "Being heard by someone you love is a kind of comfort that words don't really know how to explain.",

    "The tiny things you probably don't think anyone notices are often the things I secretly adore most.",

    "I don't just love the person I can see. I love the person underneath everything too.",

    "There are moments when the world feels loud, and somehow your presence makes it quieter.",

    "With you, even doing absolutely nothing can become something I want to keep forever.",

    "Kindness leaves fingerprints on the world, and yours are everywhere.",

    "You remind me that love doesn't always need grand gestures. Sometimes it is simply staying and understanding.",

    "I never want you to feel like you have to hide the weird, goofy and ridiculous parts of yourself from me.",

    "I love learning the way you think, the things you notice and the little worlds that exist inside your head.",

    "Miles can separate two people physically, but you've never felt far away from my heart.",

    "I never planned on finding home in another person. Then you came along and completely changed that.",

    "Being understood without having to explain every little piece of yourself is a rare kind of magic.",

    "I want to know every dream you have, even the tiny ones, because I want to know the future you're imagining.",

    "Courage isn't always loud. Sometimes it is simply waking up and choosing to keep moving forward.",

    "I don't only love who you are today. I love getting to watch all the beautiful versions of you that are still waiting to unfold.",

    "After all the lists, explanations and words, it really comes down to this: I love you because you are you. And there is nobody else in the universe I'd rather find."

];


/* FAVOURITES */

const favourites = [

    ["🩵","Baby blue"],
    ["🦦","Otters"],
    ["☕","Black coffee"],
    ["🍣","Sushi"],
    ["🌊","The ocean"],
    ["⭐","Stars"],
    ["🤎","Hazel eyes"],
    ["🌸","Peonies"],
    ["🌅","Sunrises"],
    ["🎂","Twenty-seven"]

];


/* OPEN WHEN */

const openWhen = {

    miss:
        "If you miss me, look at the sky. Somewhere beneath that same sky is a girl who is missing you too. Distance doesn't change where my heart belongs. 🩵",

    sad:
        "If you're sad, you don't have to pretend to be okay. Come exactly as you are. You can be messy, tired, quiet or broken. I'll still love you through every version of you.",

    sleep:
        "If you can't sleep, imagine me beside you. No distance. No screens. Just quiet, warm and safe. Close your eyes and imagine my hand in yours.",

    loved:
        "If you need to feel loved, remember this: you are loved beyond the kilometres between us, beyond the days we spend apart and beyond anything words could ever properly explain."

};


/* FUTURE */

const future = [

    "The day I finally get to hold you.",
    "Seeing the ocean together.",
    "A sunrise where neither of us has to say goodbye afterwards.",
    "Exploring somewhere neither of us has ever been.",
    "A little place that feels like ours.",
    "Looking at the stars beside you instead of through a screen.",
    "Sharing a ridiculous amount of sushi even though I don't like sushi.",
    "Finding somewhere beautiful to sit and listen to music together.",
    "Watching you laugh while we make memories that don't have to fit inside a screen.",
    "Growing older together."

];


/* BASIC TEXT */

document.getElementById("heroName").textContent =
    birthday.name + " ♡";

document.getElementById("birthdayTitle").textContent =
    "Happy " + birthday.age + "th Birthday, my love.";

document.getElementById("birthdayMessage").textContent =
    birthday.birthdayMessage;

document.getElementById("birthdayIntro").textContent =
    birthday.intro;


/* HEART */

function revealHeart() {

    document
        .getElementById("heartMessage")
        .classList.toggle("show");

}


/* REASONS */

const reasonsContainer =
    document.getElementById("reasons");

reasons.forEach((reason,index) => {

    const div =
        document.createElement("div");

    div.className =
        "reason";

    div.innerHTML = `

        <div class="reason-number">
            ${index + 1} / 27
        </div>

        <p>
            ${reason}
        </p>

        <span class="secret">
            ✦ ${secretReasons[index]}
        </span>

    `;

    div.onclick = function() {

        div.classList.toggle("revealed");

    };

    reasonsContainer.appendChild(div);

});


/* FAVOURITES */

const favouritesContainer =
    document.getElementById("favourites");

favourites.forEach(item => {

    const div =
        document.createElement("div");

    div.className =
        "favourite";

    div.innerHTML = `

        <div class="favourite-icon">
            ${item[0]}
        </div>

        <p>
            ${item[1]}
        </p>

    `;

    favouritesContainer.appendChild(div);

});


/* FUTURE */

const futureContainer =
    document.getElementById("future");

future.forEach(item => {

    const li =
        document.createElement("li");

    li.textContent =
        item;

    futureContainer.appendChild(li);

});


/* OPEN WHEN */

function showMessage(type) {

    alert(openWhen[type]);

}


/* CONSTELLATION */

const starMessages = {

    1:
        "You are the star I would choose in every universe. 🩵",

    2:
        "Somewhere between all these stars, I found you.",

    3:
        "Distance is only geography. My heart has never been far from yours.",

    4:
        "If the universe had a favourite love story, I hope it would be ours.",

    5:
        "Look up at the night sky. Somewhere beneath it, I'm loving you too."

};


function starMessage(number) {

    document
        .getElementById("starMessage")
        .textContent =
            starMessages[number];

}


/* TREASURE HUNT */

let clueNumber = 1;

const clues = [

    {
        title: "CLUE TWO",
        text:
            "You've found the stars. Now find the place where twenty-seven little reasons are waiting to tell you why you're loved."
    },

    {
        title: "CLUE THREE",
        text:
            "Twenty-seven reasons, but one person behind them all. Now find the place where you can open little messages whenever you need them."
    },

    {
        title: "CLUE FOUR",
        text:
            "Now find the place where tomorrow lives. Look for the little list of things I want with you."
    },

    {
        title: "CLUE FIVE",
        text:
            "Almost there, my love. Find the sunrise. It is waiting for you to give it some colour."
    },

    {
        title: "YOUR TREASURE 🩵",
        text:
            "Your treasure was never something I could put inside a box. It was you. Happy 27th birthday, Lola. You are my favourite treasure in every universe. ⭐ 🩵 🌌"
    }

];


function nextClue() {

    const result =
        document.getElementById("treasureResult");

    if (clueNumber <= clues.length) {

        const clue =
            clues[clueNumber - 1];

        result.innerHTML = `

            <div class="clue">

                <div class="clue-number">
                    ${clue.title}
                </div>

                <p>
                    ${clue.text}
                </p>

                ${
                    clueNumber < clues.length
                    ?
                    `<button class="button clue-button" onclick="nextClue()">I found it ✦</button>`
                    :
                    ""
                }

            </div>

        `;

        clueNumber++;

    }

}


/* WORD FIND */

const wordGrid = [

    "XLOLAQWERT",
    "FOREVERXYZ",
    "QSTARSABCD",
    "XOXOCEANXX",
    "XXOTTERXXX",
    "HEARTXXXXX",
    "BABYBLUEXX",
    "XXSUNRISEQ",
    "LOVEHOMEXX",
    "QWERTYUIOP"

];

const words = [

    "LOLA",
    "LOVE",
    "STARS",
    "OCEAN",
    "OTTER",
    "HOME",
    "HEART",
    "FOREVER",
    "SUNRISE",
    "BABYBLUE"

];

const wordFind =
    document.getElementById("wordFind");

const wordList =
    document.getElementById("wordList");

const wordStatus =
    document.getElementById("wordStatus");

let currentSelection = [];

let foundWords = [];


/* GRID */

wordGrid.forEach((row,rowIndex) => {

    row.split("").forEach((letter,colIndex) => {

        const cell =
            document.createElement("div");

        cell.className =
            "letter-cell";

        cell.textContent =
            letter;

        cell.dataset.row =
            rowIndex;

        cell.dataset.col =
            colIndex;

        cell.onclick = function() {

            selectLetter(cell);

        };

        wordFind.appendChild(cell);

    });

});


/* WORD LIST */

words.forEach(word => {

    const pill =
        document.createElement("div");

    pill.className =
        "word-pill";

    pill.id =
        "word-" + word;

    pill.textContent =
        word;

    wordList.appendChild(pill);

});


function selectLetter(cell) {

    if (cell.classList.contains("found")) {
        return;
    }

    cell.classList.add("selected");

    currentSelection.push(cell);

    let selectedWord = "";

    currentSelection.forEach(item => {

        selectedWord += item.textContent;

    });


    const matchingWord =
        words.find(word =>
            word.startsWith(selectedWord)
        );


    if (!matchingWord) {

        setTimeout(() => {

            currentSelection.forEach(item => {

                item.classList.remove("selected");

            });

            currentSelection = [];

        },250);

        return;
    }


    if (words.includes(selectedWord)) {

        currentSelection.forEach(item => {

            item.classList.remove("selected");

            item.classList.add("found");

        });

        document
            .getElementById("word-" + selectedWord)
            .classList.add("found");

        foundWords.push(selectedWord);

        currentSelection = [];

        wordStatus.textContent =
            foundWords.length +
            " / 10 words found ✦";


        if (foundWords.length === 10) {

            wordStatus.textContent =
                "You found them all! I love you, Lola. 🩵🌸⭐";

        }

    }

}


/* COLOURING */

const canvas =
    document.getElementById("sunriseCanvas");

const ctx =
    canvas.getContext("2d");

let drawing = false;

let currentColour =
    "#ffb6c1";


function drawSunrise() {

    ctx.clearRect(
        0,
        0,
        canvas.width,
        canvas.height
    );

    /* SKY */

    ctx.fillStyle =
        "#eaf8ff";

    ctx.fillRect(
        0,
        0,
        canvas.width,
        canvas.height
    );


    /* SUN */

    ctx.beginPath();

    ctx.arc(
        350,
        230,
        65,
        0,
        Math.PI * 2
    );

    ctx.strokeStyle =
        "#4b7c94";

    ctx.lineWidth =
        4;

    ctx.stroke();


    /* HORIZON */

    ctx.beginPath();

    ctx.moveTo(
        0,
        300
    );

    ctx.lineTo(
        700,
        300
    );

    ctx.stroke();


    /* OCEAN */

    ctx.beginPath();

    ctx.moveTo(
        0,
        300
    );

    ctx.lineTo(
        700,
        300
    );

    ctx.lineTo(
        700,
        450
    );

    ctx.lineTo(
        0,
        450
    );

    ctx.closePath();

    ctx.stroke();


    /* SAND */

    ctx.beginPath();

    ctx.moveTo(
        0,
        380
    );

    ctx.quadraticCurveTo(
        350,
        350,
        700,
        380
    );

    ctx.lineTo(
        700,
        450
    );

    ctx.lineTo(
        0,
        450
    );

    ctx.closePath();

    ctx.stroke();


    /* BIRDS */

    ctx.beginPath();

    ctx.arc(
        160,
        120,
        15,
        Math.PI,
        0
    );

    ctx.arc(
        190,
        120,
        15,
        Math.PI,
        0
    );

    ctx.stroke();


    ctx.beginPath();

    ctx.arc(
        520,
        145,
        15,
        Math.PI,
        0
    );

    ctx.arc(
        550,
        145,
        15,
        Math.PI,
        0
    );

    ctx.stroke();


    /* HEART */

    ctx.beginPath();

    ctx.moveTo(
        350,
        125
    );

    ctx.bezierCurveTo(
        325,
        100,
        295,
        135,
        350,
        175
    );

    ctx.bezierCurveTo(
        405,
        135,
        375,
        100,
        350,
        125
    );

    ctx.stroke();

}


drawSunrise();


function setColour(colour) {

    currentColour =
        colour;

}


function getPosition(event) {

    const rect =
        canvas.getBoundingClientRect();

    let x;
    let y;

    if (event.touches) {

        x =
            event.touches[0].clientX -
            rect.left;

        y =
            event.touches[0].clientY -
            rect.top;

    } else {

        x =
            event.clientX -
            rect.left;

        y =
            event.clientY -
            rect.top;

    }

    return {

        x:
            x * (canvas.width / rect.width),

        y:
            y * (canvas.height / rect.height)

    };

}


function startDrawing(event) {

    drawing = true;

    draw(event);

}


function stopDrawing() {

    drawing = false;

    ctx.beginPath();

}


function draw(event) {

    if (!drawing) {
        return;
    }

    event.preventDefault();

    const position =
        getPosition(event);

    ctx.lineWidth =
        10;

    ctx.lineCap =
        "round";

    ctx.strokeStyle =
        currentColour;

    ctx.lineTo(
        position.x,
        position.y
    );

    ctx.stroke();

    ctx.beginPath();

    ctx.moveTo(
        position.x,
        position.y
    );

}


canvas.addEventListener(
    "mousedown",
    startDrawing
);

canvas.addEventListener(
    "mouseup",
    stopDrawing
);

canvas.addEventListener(
    "mouseout",
    stopDrawing
);

canvas.addEventListener(
    "mousemove",
    draw
);

canvas.addEventListener(
    "touchstart",
    startDrawing,
    { passive:false }
);

canvas.addEventListener(
    "touchend",
    stopDrawing
);

canvas.addEventListener(
    "touchmove",
    draw,
    { passive:false }
);


function clearCanvas() {

    drawSunrise();

}


/* LOVE LETTER */

function openLetter() {

    document
        .getElementById("letter")
        .classList.add("open");

}


/* FINAL MESSAGE */

function revealFinal() {

    const message =
        document.getElementById("finalMessage");

    message.innerHTML = `

        If I could give you anything for your birthday,
        it would be the ability to see yourself through my eyes.

        <br><br>

        Maybe then you'd finally understand
        why I love you so much.

        <br><br>

        You are my favourite person,
        my soft place to land,
        my little piece of home.

        <br><br>

        Happy 27th birthday, my love.

        <br><br>

        I love you across every kilometre,
        every timezone,
        every ocean,
        every sky
        and every universe.

        <br><br>

        🩵 🌌 🦦 ⭐ 🌸

    `;

    message.style.display =
        "block";

}

</script>

</body>
</html>
