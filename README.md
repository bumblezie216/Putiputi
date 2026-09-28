<!DOCTYPE html>
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
            color: #ffffff;
            overflow-x: hidden;
            min-height: 100vh;

            background:
                radial-gradient(
                    circle at 50% 10%,
                    rgba(180, 225, 245, 0.30),
                    transparent 35%
                ),
                radial-gradient(
                    circle at 15% 50%,
                    rgba(135, 206, 235, 0.12),
                    transparent 30%
                ),
                linear-gradient(
                    180deg,
                    #183d55 0%,
                    #285a73 40%,
                    #477f97 70%,
                    #1e4359 100%
                );
        }

        /* -------------------------
           SUBTLE STARS
        ------------------------- */

        .star {
            position: fixed;
            width: 2px;
            height: 2px;
            background: rgba(255, 255, 255, 0.75);
            border-radius: 50%;
            pointer-events: none;
            z-index: -1;
            animation: twinkle 5s ease-in-out infinite;
        }

        @keyframes twinkle {
            0%, 100% {
                opacity: 0.2;
            }

            50% {
                opacity: 0.75;
            }
        }

        /* -------------------------
           SHOOTING STARS
        ------------------------- */

        .shooting-star {
            position: fixed;
            width: 70px;
            height: 1px;

            background: linear-gradient(
                90deg,
                transparent,
                rgba(225, 247, 255, 0.65)
            );

            transform: rotate(-30deg);
            opacity: 0;
            pointer-events: none;
            z-index: -1;

            animation: shooting 13s linear infinite;
        }

        .shooting-star.one {
            top: 23%;
            left: -100px;
        }

        .shooting-star.two {
            top: 67%;
            left: -100px;
            animation-delay: 7s;
        }

        @keyframes shooting {
            0% {
                left: -100px;
                opacity: 0;
            }

            8% {
                opacity: 0.6;
            }

            20% {
                left: 105%;
                opacity: 0;
            }

            100% {
                left: 105%;
                opacity: 0;
            }
        }

        /* -------------------------
           FLOATING PEONIES
        ------------------------- */

        .peony {
            position: fixed;
            font-size: 25px;
            opacity: 0.13;
            pointer-events: none;
            z-index: -1;

            animation: floatPeony 16s ease-in-out infinite;
        }

        .peony.one {
            left: 7%;
            top: 32%;
        }

        .peony.two {
            right: 8%;
            top: 60%;
            animation-delay: 5s;
        }

        .peony.three {
            left: 16%;
            bottom: 12%;
            animation-delay: 9s;
        }

        @keyframes floatPeony {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }

            50% {
                transform: translateY(-22px) rotate(7deg);
            }
        }

        /* -------------------------
           STINGRAYS
        ------------------------- */

        .stingray {
            position: fixed;
            font-size: 34px;
            opacity: 0.12;
            pointer-events: none;
            z-index: -1;

            animation: swim 30s linear infinite;
        }

        .ray-one {
            top: 28%;
            left: -80px;
        }

        .ray-two {
            top: 70%;
            left: -80px;
            animation-delay: 15s;
        }

        @keyframes swim {
            0% {
                transform: translateX(-100px) translateY(0);
            }

            25% {
                transform: translateX(25vw) translateY(-12px);
            }

            50% {
                transform: translateX(55vw) translateY(10px);
            }

            75% {
                transform: translateX(85vw) translateY(-8px);
            }

            100% {
                transform: translateX(115vw) translateY(0);
            }
        }

        /* -------------------------
           SECTIONS
        ------------------------- */

        section {
            min-height: 100vh;
            padding: 80px 20px;

            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            position: relative;
        }

        .container {
            width: min(100%, 950px);
            margin: auto;
        }

        /* -------------------------
           TEXT
        ------------------------- */

        h1 {
            font-size: clamp(3rem, 10vw, 7rem);
            line-height: 0.95;
            text-align: center;

            color: #f0fbff;

            text-shadow:
                0 0 20px rgba(190, 230, 245, 0.25);
        }

        h2 {
            font-size: clamp(2rem, 6vw, 4rem);
            text-align: center;
            margin-bottom: 20px;

            color: #e5f8ff;

            text-shadow:
                0 0 18px rgba(190, 230, 245, 0.25);
        }

        h3 {
            margin-bottom: 12px;
        }

        p {
            line-height: 1.8;
        }

        .subtitle {
            text-align: center;
            max-width: 700px;
            margin: 20px auto;

            font-size: 1.15rem;
            color: #e0f4fa;
        }

        /* -------------------------
           BUTTONS
        ------------------------- */

        .glow-button {
            margin-top: 25px;

            padding: 14px 27px;

            border-radius: 999px;

            background: rgba(190, 230, 245, 0.13);

            border: 1px solid rgba(220, 245, 255, 0.45);

            color: white;

            font-family: inherit;
            font-size: 1rem;

            cursor: pointer;

            box-shadow:
                0 0 25px rgba(190, 230, 245, 0.10);

            transition: 0.3s;
        }

        .glow-button:hover {
            transform: translateY(-3px);

            background: rgba(190, 230, 245, 0.22);

            box-shadow:
                0 0 30px rgba(190, 230, 245, 0.20);
        }

        /* -------------------------
           DECORATION
        ------------------------- */

        .soft-decoration {
            text-align: center;
            font-size: 2.2rem;
            letter-spacing: 12px;
            margin-bottom: 25px;

            opacity: 0.75;
        }

        /* -------------------------
           CARDS
        ------------------------- */

        .card-grid {
            display: grid;

            grid-template-columns:
                repeat(auto-fit, minmax(230px, 1fr));

            gap: 18px;

            width: 100%;

            margin-top: 30px;
        }

        .card {
            background:
                rgba(15, 50, 68, 0.42);

            border:
                1px solid rgba(220, 245, 255, 0.15);

            border-radius: 22px;

            padding: 24px;

            backdrop-filter: blur(8px);

            box-shadow:
                0 15px 40px rgba(0, 0, 0, 0.14);
        }

        /* -------------------------
           FAVOURITES
        ------------------------- */

        .favourite {
            text-align: center;
            font-size: 2rem;
            color: #e4f8ff;
        }

        .favourite span {
            display: block;

            font-size: 1rem;

            margin-top: 8px;

            color: #d9eef5;
        }

        /* -------------------------
           27 REASONS
        ------------------------- */

        .reason {
            cursor: pointer;
            transition: 0.3s;
        }

        .reason:hover {
            transform: translateY(-4px);
        }

        .reason .secret {
            display: none;

            margin-top: 15px;

            color: #d6edf4;

            font-style: italic;
        }

        .reason.open .secret {
            display: block;
        }

        /* -------------------------
           OPEN WHEN
        ------------------------- */

        .open-card {
            text-align: center;
            cursor: pointer;
        }

        .open-message {
            display: none;

            margin-top: 18px;

            color: #d7eef5;
        }

        .open-card.open .open-message {
            display: block;
        }

        /* -------------------------
           CONSTELLATION
        ------------------------- */

        .constellation {
            position: relative;

            width: min(90vw, 700px);

            height: 450px;

            margin: 30px auto;

            border-radius: 30px;

            background:
                radial-gradient(
                    circle at center,
                    rgba(190, 230, 245, 0.12),
                    transparent 65%
                ),
                rgba(10, 35, 50, 0.25);

            border:
                1px solid rgba(220, 245, 255, 0.14);

            overflow: hidden;
        }

        .constellation-star {
            position: absolute;

            width: 11px;
            height: 11px;

            background: #e8faff;

            border-radius: 50%;

            box-shadow:
                0 0 13px 3px rgba(210, 240, 250, 0.5);

            cursor: pointer;

            transition: 0.25s;
        }

        .constellation-star:hover {
            transform: scale(1.5);
        }

        .star-line {
            position: absolute;

            height: 1px;

            background:
                rgba(220, 245, 255, 0.25);

            transform-origin: left center;
        }

        .constellation-message {
            text-align: center;

            min-height: 60px;

            max-width: 650px;

            margin: 20px auto;

            color: #d8f3fa;

            font-style: italic;
        }

        /* -------------------------
           TREASURE HUNT
        ------------------------- */

        .treasure-box {
            text-align: center;

            padding: 35px;

            border-radius: 28px;

            background:
                rgba(15, 50, 68, 0.45);

            border:
                1px solid rgba(220, 245, 255, 0.18);
        }

        .clue {
            display: none;
        }

        .clue.active {
            display: block;
        }

        /* -------------------------
           WORD FIND
        ------------------------- */

        .word-find {
            max-width: 500px;
            margin: 30px auto;
        }

        .word-list {
            display: flex;

            flex-wrap: wrap;

            justify-content: center;

            gap: 8px;

            margin-bottom: 20px;
        }

        .word {
            padding: 7px 12px;

            border-radius: 999px;

            background:
                rgba(190, 230, 245, 0.08);

            border:
                1px solid rgba(220, 245, 255, 0.18);
        }

        .word.found {
            text-decoration: line-through;
            opacity: 0.45;
        }

        .grid {
            display: grid;

            grid-template-columns:
                repeat(10, 1fr);

            gap: 4px;

            user-select: none;
        }

        .cell {
            aspect-ratio: 1;

            display: flex;

            align-items: center;
            justify-content: center;

            background:
                rgba(220, 245, 255, 0.06);

            border:
                1px solid rgba(220, 245, 255, 0.1);

            border-radius: 5px;

            font-size:
                clamp(0.7rem, 2.5vw, 1rem);

            cursor: pointer;
        }

        .cell.selected {
            background:
                rgba(180, 225, 245, 0.3);
        }

        .cell.correct {
            background:
                rgba(130, 205, 195, 0.3);
        }

        /* -------------------------
           COLOURING
        ------------------------- */

        .colour-wrap {
            width: min(100%, 800px);

            background:
                rgba(15, 50, 68, 0.45);

            border:
                1px solid rgba(220, 245, 255, 0.18);

            padding: 20px;

            border-radius: 28px;
        }

        .colour-canvas {
            width: 100%;

            display: block;

            background: white;

            border-radius: 18px;

            cursor: crosshair;

            touch-action: none;
        }

        .palette {
            display: flex;

            flex-wrap: wrap;

            gap: 10px;

            justify-content: center;

            margin: 20px 0 5px;
        }

        .colour {
            width: 38px;
            height: 38px;

            border-radius: 50%;

            border: 3px solid white;

            cursor: pointer;
        }

        .colour.active {
            transform: scale(1.15);

            box-shadow:
                0 0 12px white;
        }

        /* -------------------------
           LOVE LETTER
        ------------------------- */

        .letter {
            max-width: 750px;

            background:
                rgba(15, 50, 68, 0.48);

            border:
                1px solid rgba(220, 245, 255, 0.18);

            padding:
                clamp(25px, 6vw, 55px);

            border-radius: 30px;

            box-shadow:
                0 25px 70px rgba(0, 0, 0, 0.18);
        }

        .letter p {
            margin-bottom: 18px;
        }

        /* -------------------------
           FUTURE
        ------------------------- */

        .future-list {
            display: grid;

            gap: 12px;

            width: 100%;
        }

        .future-item {
            padding: 18px 20px;

            background:
                rgba(15, 50, 68, 0.42);

            border-radius: 16px;

            border-left:
                3px solid rgba(190, 230, 245, 0.5);
        }

        /* -------------------------
           FINAL
        ------------------------- */

        .final {
            text-align: center;

            background:
                radial-gradient(
                    circle at center,
                    rgba(190, 230, 245, 0.15),
                    transparent 55%
                );
        }

        .final-message {
            max-width: 750px;

            font-size:
                clamp(1.1rem, 3vw, 1.5rem);

            line-height: 2;

            color: #e1f6fb;
        }

        .signature {
            margin-top: 30px;

            font-size: 1.4rem;
        }

        /* -------------------------
           MOBILE
        ------------------------- */

        @media (max-width: 600px) {

            section {
                padding: 65px 15px;
            }

            .soft-decoration {
                font-size: 1.8rem;
                letter-spacing: 7px;
            }

            .card {
                padding: 20px;
            }

            .constellation {
                height: 350px;
            }

            .letter {
                padding: 25px 20px;
            }

            .stingray {
                font-size: 28px;
            }
        }
    </style>
</head>

<body>

    <!-- SUBTLE BACKGROUND DECORATION -->

    <div class="shooting-star one"></div>
    <div class="shooting-star two"></div>

    <div class="peony one">🌸</div>
    <div class="peony two">🌸</div>
    <div class="peony three">🌸</div>

    <div class="stingray ray-one">🪽</div>
    <div class="stingray ray-two">🪽</div>


    <!-- HERO -->

    <section id="birthday">

        <div class="container">

            <div class="soft-decoration">
                🌸 🩵 🌊
            </div>

            <h1>
                A little universe<br>
                made for Lola ♡
            </h1>

            <p class="subtitle">
                Twenty-seven years of you.
            </p>

            <p class="subtitle">
                So I made you a tiny universe.
                Every little corner is here because it reminds me of you.
            </p>

            <div style="text-align:center;">

                <button
                    class="glow-button"
                    onclick="enterUniverse()">

                    Enter my little universe ↓

                </button>

            </div>

        </div>

    </section>


    <!-- INTRO -->

    <section>

        <div class="container">

            <h2>
                Happy 27th Birthday, Lola 🩵
            </h2>

            <p class="subtitle">

                Today isn't just about another year passing.
                It's about celebrating the person who makes my world softer
                simply by existing in it.

            </p>

            <p class="subtitle">

                I wish I could be beside you today.
                So instead, I built you somewhere you can come back to
                whenever you need a reminder of how loved you are.

            </p>

            <div class="soft-decoration">
                🩵 ⭐ 🌊 🌸
            </div>

        </div>

    </section>


    <!-- FAVOURITES -->

    <section>

        <div class="container">

            <h2>
                Your little universe
            </h2>

            <p class="subtitle">
                A few of the things that make me think of you.
            </p>

            <div class="card-grid">

                <div class="card favourite">
                    🩵
                    <span>Baby blue</span>
                </div>

                <div class="card favourite">
                    🦦
                    <span>Otters</span>
                </div>

                <div class="card favourite">
                    ☕
                    <span>Black coffee</span>
                </div>

                <div class="card favourite">
                    🍣
                    <span>Sushi</span>
                </div>

                <div class="card favourite">
                    🌊
                    <span>The ocean</span>
                </div>

                <div class="card favourite">
                    ⭐
                    <span>Stars</span>
                </div>

                <div class="card favourite">
                    🤎
                    <span>Hazel eyes</span>
                </div>

                <div class="card favourite">
                    🎂
                    <span>Twenty-seven</span>
                </div>

                <div class="card favourite">
                    🌸
                    <span>Peonies</span>
                </div>

                <div class="card favourite">
                    🌅
                    <span>Sunrises</span>
                </div>

            </div>

        </div>

    </section>


    <!-- 27 REASONS -->

    <section>

        <div class="container">

            <h2>
                27 reasons I love you
            </h2>

            <p class="subtitle">
                Tap each one.
                There is a little message hidden underneath every reason.
            </p>

            <div class="card-grid">

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>1. Your hazel eyes.</h3>
                    <p class="secret">
                        There is something about looking into your eyes that makes everything else disappear for a moment.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>2. Your voice.</h3>
                    <p class="secret">
                        Even when you don't realise it, hearing you can turn an ordinary moment into one I want to remember.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>3. The way you make me feel at home.</h3>
                    <p class="secret">
                        Home stopped being somewhere I needed to go when I realised how safe my heart feels with you.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>4. Your little laugh.</h3>
                    <p class="secret">
                        I would happily do ridiculous things just to hear that laugh one more time.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>5. Your beautiful heart.</h3>
                    <p class="secret">
                        You care more deeply than you sometimes realise, and that tenderness is one of the things I treasure most.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>6. Your softness.</h3>
                    <p class="secret">
                        The softness you carry isn't weakness. It is one of the most beautiful things about you.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>7. Your strength.</h3>
                    <p class="secret">
                        I admire every quiet moment where you kept going even when nobody else could see how hard it was.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>8. Your love for otters.</h3>
                    <p class="secret">
                        Somehow the fact that you love these adorable little creatures makes me love your heart even more.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>9. Your baby blue world.</h3>
                    <p class="secret">
                        Whenever I see that colour, a tiny part of my brain immediately thinks of you.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>10. Your black coffee.</h3>
                    <p class="secret">
                        I don't even have to like the coffee. I just love imagining you holding your little cup of it.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>11. The way you make me smile.</h3>
                    <p class="secret">
                        Sometimes I'll be completely fine and then I'll remember something about you and suddenly I'm smiling at my phone.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>12. The way you listen.</h3>
                    <p class="secret">
                        Being heard by someone you love is a kind of comfort that words don't really know how to explain.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>13. Your little habits.</h3>
                    <p class="secret">
                        The tiny things you probably don't think anyone notices are often the things I secretly adore most.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>14. Your beautiful soul.</h3>
                    <p class="secret">
                        I don't just love the person I can see. I love the person underneath everything too.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>15. The way you calm me.</h3>
                    <p class="secret">
                        There are moments when the world feels loud, and somehow your presence makes it quieter.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>16. The way you make ordinary moments special.</h3>
                    <p class="secret">
                        With you, even doing absolutely nothing can become something I want to keep forever.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>17. Your kindness.</h3>
                    <p class="secret">
                        Kindness leaves fingerprints on the world, and yours are everywhere.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>18. Your patience.</h3>
                    <p class="secret">
                        You remind me that love doesn't always need grand gestures. Sometimes it is simply staying and understanding.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>19. Your silly side.</h3>
                    <p class="secret">
                        I never want you to feel like you have to hide the weird, goofy and ridiculous parts of yourself from me.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>20. Your beautiful mind.</h3>
                    <p class="secret">
                        I love learning the way you think, the things you notice and the little worlds that exist inside your head.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>21. The way you make distance feel smaller.</h3>
                    <p class="secret">
                        Miles can separate two people physically, but you've never felt far away from my heart.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>22. The way you became my home.</h3>
                    <p class="secret">
                        I never planned on finding home in another person. Then you came along and completely changed that.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>23. The way you make me feel understood.</h3>
                    <p class="secret">
                        Being understood without having to explain every little piece of yourself is a rare kind of magic.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>24. Your dreams.</h3>
                    <p class="secret">
                        I want to know every dream you have, even the tiny ones, because I want to know the future you're imagining.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>25. Your courage.</h3>
                    <p class="secret">
                        Courage isn't always loud. Sometimes it is simply waking up and choosing to keep moving forward.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>26. The person you are becoming.</h3>
                    <p class="secret">
                        I don't only love who you are today. I love getting to watch all the beautiful versions of you that are still waiting to unfold.
                    </p>
                </div>

                <div class="card reason" onclick="this.classList.toggle('open')">
                    <h3>27. Simply because you're Lola.</h3>
                    <p class="secret">
                        After all the lists, explanations and words, it really comes down to this: I love you because you are you. And there is nobody else in the universe I'd rather find.
                    </p>
                </div>

            </div>

        </div>

    </section>


    <!-- CONSTELLATION -->

    <section>

        <div class="container">

            <h2>
                Our constellation ⭐
            </h2>

            <p class="subtitle">
                Tap the stars and let them tell you something.
            </p>

            <div class="constellation">

                <div
                    class="constellation-star"
                    style="left:15%;top:35%;"
                    onclick="constellationMessage(0)">
                </div>

                <div
                    class="constellation-star"
                    style="left:29%;top:20%;"
                    onclick="constellationMessage(1)">
                </div>

                <div
                    class="constellation-star"
                    style="left:43%;top:38%;"
                    onclick="constellationMessage(2)">
                </div>

                <div
                    class="constellation-star"
                    style="left:57%;top:23%;"
                    onclick="constellationMessage(3)">
                </div>

                <div
                    class="constellation-star"
                    style="left:73%;top:40%;"
                    onclick="constellationMessage(4)">
                </div>

                <div
                    class="constellation-star"
                    style="left:61%;top:65%;"
                    onclick="constellationMessage(0)">
                </div>

                <div
                    class="constellation-star"
                    style="left:35%;top:68%;"
                    onclick="constellationMessage(1)">
                </div>

                <div
                    class="star-line"
                    style="left:17%;top:37%;width:15%;transform:rotate(-28deg);">
                </div>

                <div
                    class="star-line"
                    style="left:31%;top:23%;width:17%;transform:rotate(30deg);">
                </div>

                <div
                    class="star-line"
                    style="left:45%;top:39%;width:16%;transform:rotate(-25deg);">
                </div>

                <div
                    class="star-line"
                    style="left:59%;top:25%;width:17%;transform:rotate(28deg);">
                </div>

            </div>

            <p
                class="constellation-message"
                id="constellationMessage">

                The stars are waiting for you. ✨

            </p>

        </div>

    </section>


    <!-- OPEN WHEN -->

    <section>

        <div class="container">

            <h2>
                Open when... 💌
            </h2>

            <p class="subtitle">
                Little pieces of me for the moments when you need them.
            </p>

            <div class="card-grid">

                <div
                    class="card open-card"
                    onclick="this.classList.toggle('open')">

                    <h3>
                        💭 Open when you miss me
                    </h3>

                    <p class="open-message">
                        If you miss me, look at the sky.
                        Somewhere beneath that same sky is a girl who is
                        missing you too.
                        Distance doesn't change where my heart belongs. 🩵
                    </p>

                </div>

                <div
                    class="card open-card"
                    onclick="this.classList.toggle('open')">

                    <h3>
                        🌧️ Open when you're sad
                    </h3>

                    <p class="open-message">
                        If you're sad, you don't have to pretend to be okay.
                        Come exactly as you are.
                        You can be messy, tired, quiet or broken.
                        I'll still love you through every version of you.
                    </p>

                </div>

                <div
                    class="card open-card"
                    onclick="this.classList.toggle('open')">

                    <h3>
                        🌙 Open when you can't sleep
                    </h3>

                    <p class="open-message">
                        If you can't sleep, imagine me beside you.
                        No distance. No screens.
                        Just quiet, warm and safe.
                        Close your eyes and imagine my hand in yours.
                    </p>

                </div>

                <div
                    class="card open-card"
                    onclick="this.classList.toggle('open')">

                    <h3>
                        🩵 Open when you need to feel loved
                    </h3>

                    <p class="open-message">
                        If you need to feel loved, remember this:
                        you are loved beyond the kilometres between us,
                        beyond the days we spend apart and beyond anything
                        words could ever properly explain.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- FUTURE -->

    <section>

        <div class="container">

            <h2>
                Things I want with you 🌅
            </h2>

            <p class="subtitle">
                Because twenty-seven isn't the end of a story.
                It's another page.
            </p>

            <div class="future-list">

                <div class="future-item">
                    🌸 The day I finally get to hold you.
                </div>

                <div class="future-item">
                    🌊 Seeing the ocean together.
                </div>

                <div class="future-item">
                    🌅 A sunrise where neither of us has to say goodbye afterwards.
                </div>

                <div class="future-item">
                    🗺️ Exploring somewhere neither of us has ever been.
                </div>

                <div class="future-item">
                    🏡 A little place that feels like ours.
                </div>

                <div class="future-item">
                    ⭐ Looking at the stars beside you instead of through a screen.
                </div>

                <div class="future-item">
                    🍣 Sharing a ridiculous amount of sushi even though I don't like sushi.
                </div>

                <div class="future-item">
                    🎵 Finding somewhere beautiful to sit and listen to music together.
                </div>

                <div class="future-item">
                    😂 Watching you laugh while we make memories that don't have to fit inside a screen.
                </div>

                <div class="future-item">
                    🤍 Growing older together.
                </div>

            </div>

        </div>

    </section>


    <!-- TREASURE HUNT -->

    <section>

        <div class="container">

            <h2>
                Our little treasure hunt 🗝️
            </h2>

            <p class="subtitle">
                Follow the clues. Don't skip ahead. ♡
            </p>

            <div class="treasure-box">

                <div class="clue active" id="clue1">

                    <h3>
                        Clue One ⭐
                    </h3>

                    <p>
                        I shine above you, but I'm not the sun.
                        Find me where our little universe keeps its secrets.
                    </p>

                    <p style="margin-top:10px;">
                        Hint: ⭐
                    </p>

                    <button
                        class="glow-button"
                        onclick="nextClue(2)">

                        I found it →

                    </button>

                </div>


                <div class="clue" id="clue2">

                    <h3>
                        Clue Two 💌
                    </h3>

                    <p>
                        You've found the stars.
                        Now find the place where twenty-seven little reasons
                        are waiting to tell you why you're loved.
                    </p>

                    <button
                        class="glow-button"
                        onclick="nextClue(3)">

                        Next clue →

                    </button>

                </div>


                <div class="clue" id="clue3">

                    <h3>
                        Clue Three 💭
                    </h3>

                    <p>
                        Twenty-seven reasons, but one person behind them all.
                        Now find the place where you can open little messages
                        whenever you need them.
                    </p>

                    <button
                        class="glow-button"
                        onclick="nextClue(4)">

                        Next clue →

                    </button>

                </div>


                <div class="clue" id="clue4">

                    <h3>
                        Clue Four 🌅
                    </h3>

                    <p>
                        Now find the place where tomorrow lives.
                        Look for the little list of things I want with you.
                    </p>

                    <button
                        class="glow-button"
                        onclick="nextClue(5)">

                        Next clue →

                    </button>

                </div>


                <div class="clue" id="clue5">

                    <h3>
                        Clue Five 🎨
                    </h3>

                    <p>
                        Almost there, my love.
                        Find the sunrise.
                        It is waiting for you to give it some colour.
                    </p>

                    <button
                        class="glow-button"
                        onclick="nextClue(6)">

                        I found the sunrise →

                    </button>

                </div>


                <div class="clue" id="clue6">

                    <h3>
                        Your treasure 🩵
                    </h3>

                    <p>
                        Your treasure was never something I could put inside a box.
                        It was you.
                    </p>

                    <p style="margin-top:18px;">
                        Happy 27th birthday, Lola.
                        You are my favourite treasure in every universe.
                        ⭐ 🩵 🌌
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- WORD FIND -->

    <section>

        <div class="container">

            <h2>
                Find our words 🔎
            </h2>

            <p class="subtitle">
                Find the hidden words in the grid.
                Tap letters in order.
            </p>

            <div class="word-find">

                <div
                    class="word-list"
                    id="wordList">
                </div>

                <div
                    class="grid"
                    id="wordGrid">
                </div>

                <p
                    id="wordMessage"
                    class="subtitle"
                    style="min-height:35px;">

                    Find your first word. 🩵

                </p>

            </div>

        </div>

    </section>


    <!-- COLOURING -->

    <section>

        <div class="container">

            <h2>
                Colour our sunrise 🌅
            </h2>

            <p class="subtitle">
                A little colouring page for you.
                Make the sunrise whatever colours you want.
            </p>

            <div class="colour-wrap">

                <canvas
                    id="colourCanvas"
                    class="colour-canvas"
                    width="800"
                    height="500">
                </canvas>

                <div class="palette">

                    <button
                        class="colour active"
                        style="background:#ffb6c1;"
                        data-colour="#ffb6c1">
                    </button>

                    <button
                        class="colour"
                        style="background:#ffd166;"
                        data-colour="#ffd166">
                    </button>

                    <button
                        class="colour"
                        style="background:#ff8c69;"
                        data-colour="#ff8c69">
                    </button>

                    <button
                        class="colour"
                        style="background:#87ceeb;"
                        data-colour="#87ceeb">
                    </button>

                    <button
                        class="colour"
                        style="background:#8ecae6;"
                        data-colour="#8ecae6">
                    </button>

                    <button
                        class="colour"
                        style="background:#b19cd9;"
                        data-colour="#b19cd9">
                    </button>

                    <button
                        class="colour"
                        style="background:#90be6d;"
                        data-colour="#90be6d">
                    </button>

                    <button
                        class="colour"
                        style="background:#ffffff;"
                        data-colour="#ffffff">
                    </button>

                    <button
                        class="colour"
                        style="background:#111827;"
                        data-colour="#111827">
                    </button>

                </div>

                <div style="text-align:center;">

                    <button
                        class="glow-button"
                        onclick="clearCanvas()">

                        Start again

                    </button>

                </div>

            </div>

        </div>

    </section>


    <!-- LOVE LETTER -->

    <section>

        <div class="container">

            <h2>
                A letter for you 💌
            </h2>

            <div class="letter">

                <p>My love,</p>

                <p>
                    I wish I could be there beside you today.
                    I wish I could watch your face when you wake up,
                    give you something wrapped in far too much ribbon,
                    and steal the first birthday hug before anyone else could.
                </p>

                <p>
                    But even though there are kilometres between us,
                    there is something distance has never managed to touch.
                    The way I love you.
                </p>

                <p>
                    You became home to me in a way I never expected.
                    Not because of a place. Not because of a house.
                    But because somehow, when I'm talking to you,
                    the world becomes a little quieter.
                </p>

                <p>
                    So on your twenty-seventh birthday,
                    I hope you remember something.
                    You are so deeply loved.
                    Not because you're perfect.
                    Not because you always have everything figured out.
                    But because you're you.
                </p>

                <p>
                    I hope you know how beautiful it is that you are still here,
                    still dreaming, still becoming, still finding little reasons to smile.
                </p>

                <p>
                    I hope this next year gives you moments that make your heart feel light.
                    Places you've never seen.
                    Things you've always wanted to try.
                    Quiet mornings.
                    Beautiful sunsets.
                    And eventually, an ocean that we can stand beside together.
                </p>

                <p>
                    And if I had to find you again through every lifetime,
                    every universe, every galaxy, every version of this world...
                    I'd still look for you.
                </p>

                <p>
                    I'd recognise your heart.
                    I'd recognise your laugh.
                    I'd recognise the way you make home feel less like a place
                    and more like a person.
                </p>

                <p>
                    Happy birthday, my love.
                </p>

                <p>
                    I'll find you beneath every sky.
                </p>

                <p class="signature">
                    Bree / Putiputi ♡
                </p>

            </div>

        </div>

    </section>


    <!-- FINAL -->

    <section class="final">

        <div class="container">

            <div class="soft-decoration">
                ⭐ 🩵 🌸
            </div>

            <h2>
                One last thing...
            </h2>

            <p class="final-message">

                If I could give you anything for your birthday,
                it would be the ability to see yourself through my eyes.

                Maybe then you'd finally understand why I love you so much.

                You are my favourite person,
                my soft place to land,
                my little piece of home.

                Happy 27th birthday, my love.

                I love you across every kilometre,
                every timezone,
                every ocean,
                every sky,
                and every universe.

                🩵 🌌 🦦 ⭐ 🌸

            </p>

            <p class="signature">
                Forever yours,<br>
                Bree ♡
            </p>

        </div>

    </section>


    <footer style="
        text-align:center;
        padding:40px 20px;
        opacity:.65;
        background:rgba(0,0,0,.15);
    ">

        Made with an unreasonable amount of love for Lola ♡
        🩵 🦦 🌊 ⭐ 🌸

    </footer>


    <script>

        /* -------------------------
           ENTER UNIVERSE
        ------------------------- */

        function enterUniverse() {

            window.scrollTo({
                top: window.innerHeight,
                behavior: "smooth"
            });

        }


        /* -------------------------
           SUBTLE STARS
        ------------------------- */

        for (let i = 0; i < 28; i++) {

            const star =
                document.createElement("div");

            star.className = "star";

            star.style.left =
                Math.random() * 100 + "vw";

            star.style.top =
                Math.random() * 100 + "vh";

            star.style.animationDelay =
                Math.random() * 5 + "s";

            document.body.appendChild(star);

        }


        /* -------------------------
           CONSTELLATION
        ------------------------- */

        const constellationMessages = [

            "You are the star I would choose in every universe. 🩵",

            "Somewhere between all these stars, I found you.",

            "Distance is only geography. My heart has never been far from yours.",

            "If the universe had a favourite love story, I hope it would be ours.",

            "Look up at the night sky. Somewhere beneath it, I'm loving you too."

        ];


        function constellationMessage(index) {

            document
                .getElementById("constellationMessage")
                .textContent =
                constellationMessages[index];

        }


        /* -------------------------
           TREASURE HUNT
        ------------------------- */

        function nextClue(number) {

            document
                .querySelectorAll(".clue")
                .forEach(clue =>
                    clue.classList.remove("active")
                );

            const next =
                document.getElementById("clue" + number);

            if (next) {

                next.classList.add("active");

            }

        }


        /* -------------------------
           WORD FIND
        ------------------------- */

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


        const gridLetters = [

            ["X","L","O","L","A","Q","W","E","R","T"],

            ["F","O","R","E","V","E","R","X","Y","Z"],

            ["Q","S","T","A","R","S","A","B","C","D"],

            ["X","O","X","O","C","E","A","N","X","X"],

            ["X","X","O","T","T","E","R","X","X","X"],

            ["H","E","A","R","T","X","X","X","X","X"],

            ["B","A","B","Y","B","L","U","E","X","X"],

            ["X","X","S","U","N","R","I","S","E","Q"],

            ["L","O","V","E","H","O","M","E","X","X"],

            ["Q","W","E","R","T","Y","U","I","O","P"]

        ];


        const grid =
            document.getElementById("wordGrid");

        const wordList =
            document.getElementById("wordList");

        const wordMessage =
            document.getElementById("wordMessage");

        let selectedCells = [];

        let foundWords = [];


        words.forEach(word => {

            const el =
                document.createElement("div");

            el.className = "word";

            el.id = "word-" + word;

            el.textContent = word;

            wordList.appendChild(el);

        });


        for (let row = 0; row < 10; row++) {

            for (let col = 0; col < 10; col++) {

                const cell =
                    document.createElement("div");

                cell.className = "cell";

                cell.textContent =
                    gridLetters[row][col];

                cell.dataset.row = row;

                cell.dataset.col = col;

                cell.addEventListener(
                    "click",
                    () => selectCell(cell)
                );

                grid.appendChild(cell);

            }

        }


        function selectCell(cell) {

            if (
                cell.classList.contains("correct")
            ) {
                return;
            }

            if (selectedCells.includes(cell)) {
                return;
            }

            selectedCells.push(cell);

            cell.classList.add("selected");

            const currentWord =
                selectedCells
                    .map(c => c.textContent)
                    .join("");

            const possible =
                words.some(word =>
                    word.startsWith(currentWord) &&
                    !foundWords.includes(word)
                );

            if (!possible) {

                selectedCells.forEach(c =>
                    c.classList.remove("selected")
                );

                selectedCells = [];

                wordMessage.textContent =
                    "That wasn't one of our words. Try again. 🩵";

                return;

            }

            if (
                words.includes(currentWord) &&
                !foundWords.includes(currentWord)
            ) {

                foundWords.push(currentWord);

                selectedCells.forEach(c => {

                    c.classList.remove("selected");

                    c.classList.add("correct");

                });

                document
                    .getElementById("word-" + currentWord)
                    .classList.add("found");

                wordMessage.textContent =
                    "You found " + currentWord + "! ⭐";

                selectedCells = [];

                if (
                    foundWords.length === words.length
                ) {

                    wordMessage.textContent =
                        "You found every word! 🩵🌊⭐ I love you, Lola.";

                }

            }

        }


        /* -------------------------
           COLOURING
        ------------------------- */

        const canvas =
            document.getElementById("colourCanvas");

        const ctx =
            canvas.getContext("2d");

        let drawing = false;

        let currentColour = "#ffb6c1";


        function drawScene() {

            ctx.clearRect(
                0,
                0,
                canvas.width,
                canvas.height
            );

            ctx.fillStyle = "#f7fbff";

            ctx.fillRect(
                0,
                0,
                canvas.width,
                canvas.height
            );

            ctx.lineWidth = 5;

            ctx.lineCap = "round";

            ctx.lineJoin = "round";

            ctx.strokeStyle = "#20263a";


            /* SUN */

            ctx.beginPath();

            ctx.arc(
                400,
                210,
                70,
                0,
                Math.PI * 2
            );

            ctx.stroke();


            /* SUN RAYS */

            for (let i = 0; i < 12; i++) {

                const angle =
                    i * Math.PI / 6;

                const x1 =
                    400 + Math.cos(angle) * 90;

                const y1 =
                    210 + Math.sin(angle) * 90;

                const x2 =
                    400 + Math.cos(angle) * 120;

                const y2 =
                    210 + Math.sin(angle) * 120;

                ctx.beginPath();

                ctx.moveTo(x1, y1);

                ctx.lineTo(x2, y2);

                ctx.stroke();

            }


            /* HORIZON */

            ctx.beginPath();

            ctx.moveTo(0, 300);

            ctx.lineTo(800, 300);

            ctx.stroke();


            /* OCEAN */

            ctx.beginPath();

            ctx.moveTo(0, 300);

            ctx.lineTo(800, 300);

            ctx.lineTo(800, 500);

            ctx.lineTo(0, 500);

            ctx.closePath();

            ctx.stroke();


            /* BEACH */

            ctx.beginPath();

            ctx.moveTo(0, 400);

            ctx.quadraticCurveTo(
                200,
                350,
                400,
                410
            );

            ctx.quadraticCurveTo(
                600,
                470,
                800,
                390
            );

            ctx.stroke();


            /* LITTLE HEART */

            ctx.beginPath();

            ctx.moveTo(400, 150);

            ctx.bezierCurveTo(
                365, 115,
                320, 160,
                400, 215
            );

            ctx.bezierCurveTo(
                480, 160,
                435, 115,
                400, 150
            );

            ctx.stroke();


            /* FLOWERS */

            for (let x = 90; x < 760; x += 110) {

                ctx.beginPath();

                ctx.moveTo(x, 430);

                ctx.lineTo(x, 390);

                ctx.stroke();

                ctx.beginPath();

                ctx.arc(
                    x,
                    385,
                    12,
                    0,
                    Math.PI * 2
                );

                ctx.stroke();

            }

        }


        drawScene();


        function getPosition(event) {

            const rect =
                canvas.getBoundingClientRect();

            let clientX;
            let clientY;

            if (event.touches) {

                clientX =
                    event.touches[0].clientX;

                clientY =
                    event.touches[0].clientY;

            } else {

                clientX =
                    event.clientX;

                clientY =
                    event.clientY;

            }

            return {

                x:
                    (clientX - rect.left)
                    * canvas.width
                    / rect.width,

                y:
                    (clientY - rect.top)
                    * canvas.height
                    / rect.height

            };

        }


        function draw(event) {

            if (!drawing) {
                return;
            }

            event.preventDefault();

            const pos =
                getPosition(event);

            ctx.fillStyle =
                currentColour;

            ctx.beginPath();

            ctx.arc(
                pos.x,
                pos.y,
                12,
                0,
                Math.PI * 2
            );

            ctx.fill();

        }


        canvas.addEventListener(
            "pointerdown",
            event => {

                drawing = true;

                draw(event);

            }
        );


        canvas.addEventListener(
            "pointermove",
            draw
        );


        canvas.addEventListener(
            "pointerup",
            () => {
                drawing = false;
            }
        );


        canvas.addEventListener(
            "pointerleave",
            () => {
                drawing = false;
            }
        );


        document
            .querySelectorAll(".colour")
            .forEach(button => {

                button.addEventListener(
                    "click",
                    () => {

                        currentColour =
                            button.dataset.colour;

                        document
                            .querySelectorAll(".colour")
                            .forEach(b =>
                                b.classList.remove("active")
                            );

                        button.classList.add("active");

                    }
                );

            });


        function clearCanvas() {

            drawScene();

        }

    </script>

</body>
</html>
