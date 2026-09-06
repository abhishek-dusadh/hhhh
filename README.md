[indx.html](https://github.com/user-attachments/files/31883479/indx.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manisha ❤️ Durgesh - Our Forever Story</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Poppins:wght@300;400;600&family=Great+Vibes&display=swap" rel="stylesheet">
    
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <style>
        /* ==========================================
           COLOR THEME & BASE STYLES
           ========================================== */
        :root {
            --bg-black: #0b0205;
            --deep-red: #800020;
            --bright-red: #ff2a5f;
            --soft-pink: #ffb3c6;
            --glow-pink: #ff4d6d;
            --white: #ffffff;
            --glass-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 179, 198, 0.2);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-black);
            color: var(--white);
            font-family: 'Poppins', sans-serif;
            overflow-x: hidden;
            position: relative;
        }

        /* Floating Hearts Layer */
        #heart-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            z-index: 10;
            overflow: hidden;
        }

        .floating-heart {
            position: absolute;
            bottom: -50px;
            color: var(--glow-pink);
            font-size: 1.5rem;
            animation: floatUp 8s linear infinite;
            opacity: 0.7;
            filter: drop-shadow(0 0 8px var(--bright-red));
        }

        @keyframes floatUp {
            0% { transform: translateY(0) rotate(0deg); opacity: 0.8; }
            100% { transform: translateY(-110vh) rotate(360deg); opacity: 0; }
        }

        /* Typography */
        h1, h2, h3, .cursive {
            font-family: 'Dancing Script', cursive;
        }

        .grand-title {
            font-family: 'Great Vibes', cursive;
        }

        /* Generic Section Layout */
        section {
            min-height: 100vh;
            padding: 80px 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            z-index: 2;
        }

        /* ==========================================
           1. HERO / HOMEPAGE SECTION
           ========================================== */
        #home {
            background: radial-gradient(circle, rgba(128,0,32,0.4) 0%, rgba(11,2,5,1) 80%);
        }

        .hero-title {
            font-size: clamp(3rem, 8vw, 6rem);
            color: var(--soft-pink);
            text-shadow: 0 0 20px var(--bright-red), 0 0 40px var(--deep-red);
            margin-bottom: 10px;
            animation: pulseGlow 3s ease-in-out infinite alternate;
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 3vw, 2rem);
            color: #f0f0f0;
            font-weight: 300;
            letter-spacing: 2px;
        }

        @keyframes pulseGlow {
            0% { text-shadow: 0 0 15px var(--bright-red); transform: scale(1); }
            100% { text-shadow: 0 0 30px var(--glow-pink), 0 0 50px var(--bright-red); transform: scale(1.02); }
        }

        /* Audio Control Button */
        .audio-btn {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 100;
            background: rgba(255, 42, 95, 0.2);
            border: 1px solid var(--soft-pink);
            color: var(--white);
            padding: 10px 18px;
            border-radius: 30px;
            cursor: pointer;
            backdrop-filter: blur(5px);
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .audio-btn:hover {
            background: var(--bright-red);
            box-shadow: 0 0 15px var(--bright-red);
        }

        /* ==========================================
           2. LOVE STORY SECTION
           ========================================== */
        .section-title {
            font-size: clamp(2.5rem, 6vw, 4rem);
            color: var(--soft-pink);
            margin-bottom: 30px;
            text-shadow: 0 0 10px var(--bright-red);
        }

        .story-card {
            max-width: 800px;
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(10px);
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            line-height: 1.8;
            font-size: 1.1rem;
            color: #ead6dc;
        }

        /* ==========================================
           3. MEMORIES PHOTO GALLERY
           ========================================== */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            width: 100%;
            max-width: 1000px;
            margin-top: 20px;
        }

        .photo-card {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            height: 300px;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
        }

        .photo-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 10px 25px var(--bright-red);
        }

        .photo-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* ==========================================
           4. LOVE LETTER ENVELOPE SECTION
           ========================================== */
        .envelope-wrapper {
            position: relative;
            cursor: pointer;
            margin-top: 20px;
        }

        .envelope {
            width: 280px;
            height: 180px;
            background: var(--deep-red);
            border-radius: 10px;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 0 25px rgba(255, 42, 95, 0.4);
            border: 1px solid var(--bright-red);
            transition: transform 0.3s ease;
        }

        .envelope:hover {
            transform: scale(1.05);
        }

        .envelope-text {
            font-size: 1.2rem;
            color: var(--soft-pink);
        }

        /* Modal / Letter Overlay */
        .letter-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: rgba(0,0,0,0.85);
            z-index: 200;
            justify-content: center;
            align-items: center;
            padding: 20px;
            backdrop-filter: blur(8px);
        }

        .letter-content {
            background: #fff0f3;
            color: #2b0008;
            max-width: 600px;
            width: 100%;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 0 30px var(--bright-red);
            position: relative;
            text-align: left;
            font-family: 'Dancing Script', cursive;
            font-size: 1.5rem;
            line-height: 1.6;
            animation: openLetter 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        @keyframes openLetter {
            from { transform: scale(0.5); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        .close-letter {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 2rem;
            cursor: pointer;
            color: var(--deep-red);
            font-family: sans-serif;
        }

        /* ==========================================
           5. PROPOSAL SECTION & BUTTONS
           ========================================== */
        #proposal {
            background: radial-gradient(circle, rgba(255,42,95,0.2) 0%, rgba(11,2,5,1) 90%);
        }

        .proposal-title {
            font-size: clamp(2.5rem, 6vw, 4.5rem);
            color: var(--white);
            margin-bottom: 40px;
            text-shadow: 0 0 20px var(--bright-red);
        }

        .btn-group {
            display: flex;
            gap: 20px;
            justify-content: center;
            align-items: center;
            position: relative;
            min-height: 100px;
            width: 100%;
            max-width: 500px;
        }

        .btn {
            padding: 15px 35px;
            font-size: 1.2rem;
            font-weight: 600;
            border-radius: 50px;
            border: none;
            cursor: pointer;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .btn-yes {
            background: linear-gradient(45deg, var(--deep-red), var(--bright-red));
            color: var(--white);
            box-shadow: 0 0 20px var(--bright-red);
        }

        .btn-yes:hover {
            transform: scale(1.1);
            box-shadow: 0 0 35px var(--glow-pink);
        }

        .btn-no {
            background: rgba(255,255,255,0.1);
            color: var(--soft-pink);
            border: 1px solid var(--soft-pink);
            position: relative;
        }

        .playful-hint {
            margin-top: 20px;
            font-size: 1.1rem;
            color: var(--soft-pink);
            min-height: 30px;
        }

        /* Celebration Screen Elements */
        .celebration-screen {
            display: none;
            flex-direction: column;
            align-items: center;
            animation: fadeIn 1s forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }

        /* ==========================================
           6. FINAL SECTION
           ========================================== */
        .big-heart {
            font-size: 6rem;
            color: var(--bright-red);
            animation: heartPulse 1.2s infinite;
            margin: 20px 0;
            filter: drop-shadow(0 0 20px var(--bright-red));
        }

        @keyframes heartPulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        .replay-btn {
            background: transparent;
            border: 2px solid var(--bright-red);
            color: var(--white);
            padding: 12px 30px;
            border-radius: 30px;
            font-size: 1rem;
            cursor: pointer;
            margin-top: 20px;
            transition: all 0.3s ease;
        }

        .replay-btn:hover {
            background: var(--bright-red);
            box-shadow: 0 0 20px var(--bright-red);
        }

        /* Responsive Tweaks */
        @media (max-width: 600px) {
            .story-card { padding: 25px 15px; }
            .btn-group { flex-direction: column; }
            .letter-content { font-size: 1.2rem; padding: 25px; }
        }
    </style>
</head>
<body>

    <audio id="bg-music" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=romantic-piano-112191.mp3" type="audio/mpeg">
    </audio>

    <button class="audio-btn" onclick="toggleAudio()">🎵 Play Music</button>

    <div id="heart-container"></div>

    <section id="home">
        <h1 class="hero-title grand-title">Manisha ❤️ Durgesh</h1>
        <p class="hero-subtitle">A Special Story Written With Love...</p>
    </section>

    <section id="story">
        <h2 class="section-title">Our Beautiful Journey ❤️</h2>
        <div class="story-card">
            <p>
                From the very first moment our paths crossed, my world started changing in ways I never imagined. 
                Your smile brightened my darkest days, and your laughter became my favorite melody. 
                <br><br>
                <strong>Manisha</strong>, loving you has been the most effortless and beautiful feeling of my life. 
                Every conversation, every shared quiet moment, and every single memory with you is a treasure I hold deep in my heart. 
                You aren't just a part of my life, Durgesh's world is complete only because of you.
            </p>
        </div>
    </section>

    <section id="memories">
        <h2 class="section-title">Our Memories 📸❤️</h2>
        <div class="gallery-grid">
            <div class="photo-card">
                <img src="https://picsum.photos/400/500?random=1" alt="Memory 1">
            </div>
            <div class="photo-card">
                <img src="https://picsum.photos/400/500?random=2" alt="Memory 2">
            </div>
            <div class="photo-card">
                <img src="https://picsum.photos/400/500?random=3" alt="Memory 3">
            </div>
        </div>
    </section>

    <section id="letter">
        <h2 class="section-title">A Message For You ✉️❤️</h2>
        <div class="envelope-wrapper" onclick="openLetter()">
            <div class="envelope">
                <div class="envelope-text">Click to Open 💌</div>
            </div>
        </div>
    </section>

    <div class="letter-modal" id="letterModal">
        <div class="letter-content">
            <span class="close-letter" onclick="closeLetter()">&times;</span>
            <p>Dear Manisha,</p>
            <br>
            <p>Some people come into our lives and make everything more beautiful. You are that special person for me. Every moment with you feels precious, and I want to create countless beautiful memories with you.</p>
            <br>
            <p>Manisha, I don't just want you for today. I want to walk beside you through every tomorrow.</p>
            <br>
            <p>Will you stay with me forever? ❤️</p>
            <br>
            <p style="text-align: right;">— Yours, Durgesh</p>
        </div>
    </div>

    <section id="proposal">
        <div id="proposal-default">
            <h2 class="proposal-title">Manisha, Will You Be Mine Forever? 💍❤️</h2>
            <div class="btn-group">
                <button class="btn btn-yes" onclick="acceptProposal()">💖 YES, FOREVER!</button>
                <button class="btn btn-no" id="noBtn" onmouseover="moveButton()" onclick="moveButton()">🥺 Let Me Think</button>
            </div>
            <div class="playful-hint" id="hintText"></div>
        </div>

        <div class="celebration-screen" id="celebration">
            <h1 class="hero-title grand-title">She Said YES! ❤️🥰</h1>
            <p class="hero-subtitle" style="margin-top: 20px;">Durgesh ❤️ Manisha — Together Forever</p>
        </div>
    </section>

    <section id="final">
        <h1 class="hero-title grand-title">Manisha ❤️ Durgesh</h1>
        <p class="hero-subtitle">Two Hearts. One Story. Forever Together.</p>
        <div class="big-heart">💖</div>
        <button class="replay-btn" onclick="scrollToTop()">Replay Our Story ❤️</button>
    </section>

    <script>
        /* ==========================================
           1. AUDIO CONTROLLER
           ========================================== */
        const bgMusic = document.getElementById('bg-music');
        let isPlaying = false;

        function toggleAudio() {
            const btn = document.querySelector('.audio-btn');
            if (isPlaying) {
                bgMusic.pause();
                btn.innerHTML = '🎵 Play Music';
            } else {
                bgMusic.play().catch(() => {});
                btn.innerHTML = '⏸️ Pause Music';
            }
            isPlaying = !isPlaying;
        }

        /* ==========================================
           2. GENERATE FLOATING HEARTS
           ========================================== */
        const heartContainer = document.getElementById('heart-container');
        const heartSymbols = ['❤️', '💖', '💗', '💕', '✨'];

        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('floating-heart');
            heart.innerText = heartSymbols[Math.floor(Math.random() * heartSymbols.length)];
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 5) + 's';
            heart.style.fontSize = (Math.random() * 1.5 + 1) + 'rem';
            
            heartContainer.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 8000);
        }

        setInterval(createHeart, 400);

        /* ==========================================
           3. LOVE LETTER MODAL LOGIC
           ========================================== */
        function openLetter() {
            document.getElementById('letterModal').style.display = 'flex';
        }

        function closeLetter() {
            document.getElementById('letterModal').style.display = 'none';
        }

        /* ==========================================
           4. PLAYFUL "LET ME THINK" BUTTON LOGIC
           ========================================== */
        const playfulMessages = [
            "Are you sure? 🥺❤️",
            "Think again, Manisha 😍",
            "Durgesh is waiting... ❤️",
            "You can't say no! 😉",
            "Try clicking YES instead! ✨"
        ];
        let messageIndex = 0;

        function moveButton() {
            const noBtn = document.getElementById('noBtn');
            const hintText = document.getElementById('hintText');
            
            // Generate random positions within viewport area
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth - 100) - (window.innerWidth / 4);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight - 100) - (window.innerHeight / 4);
            
            noBtn.style.position = 'absolute';
            noBtn.style.transform = `translate(${x}px, ${y}px)`;

            // Display rotating playful text
            hintText.innerText = playfulMessages[messageIndex];
            messageIndex = (messageIndex + 1) % playfulMessages.length;
        }

        /* ==========================================
           5. PROPOSAL ACCEPTANCE LOGIC
           ========================================== */
        function acceptProposal() {
            // Hide standard question layout
            document.getElementById
