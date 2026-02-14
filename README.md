<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To My One & Only ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        /* CUSTOM COLORS - EDIT THESE TO MATCH THEIR FAVORITES! */
        :root {
            --main-color: #d6336c; /* Pink-red (default) - change me! */
            --bg-color: #ffe6ea; /* Light pink (default) - change me! */
            --accent-color: #ffffff; /* White (default) - change me! */
            --text-color: #333333; /* Dark gray (default) - change me! */
        }
        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        .hero {
            background: url('YOUR-COUPLE-PHOTO-URL-HERE') center/cover no-repeat;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
        }
        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(214, 51, 108, 0.5);
            /* Match overlay to main color: use rgba(RED, GREEN, BLUE, OPACITY) */
        }
        .hero-content {
            position: relative;
            color: var(--accent-color);
            padding: 0 20px;
        }
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }
        .btn {
            background: var(--accent-color);
            color: var(--main-color);
            padding: 12px 24px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            border: 2px solid var(--main-color);
        }
        .btn:hover {
            background: var(--main-color);
            color: var(--accent-color);
            transform: scale(1.05);
        }
        /* Music Player Style */
        .music-player {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--main-color);
            color: var(--accent-color);
            padding: 10px 15px;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }
        .music-player:hover {
            transform: scale(1.1);
        }
        /* Message Section */
        .message-section {
            padding: 60px 20px;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }
        .message-section h2 {
            font-size: 2rem;
            margin-bottom: 2rem;
            color: var(--main-color);
        }
        .message-section p {
            font-size: 1.2rem;
            margin-bottom: 3rem;
        }
        /* Hidden Surprise Message */
        .surprise-box {
            background: var(--accent-color);
            border: 3px dashed var(--main-color);
            padding: 20px;
            border-radius: 15px;
            margin: 30px 0;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .surprise-box:hover {
            background: rgba(var(--main-color), 0.1);
        }
        .surprise-hidden {
            display: none;
            margin-top: 15px;
            font-size: 1.1rem;
            color: var(--main-color);
            font-weight: bold;
        }
        /* Gallery */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        .gallery img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .closing {
            font-size: 1.3rem;
            font-weight: bold;
            margin-top: 2rem;
            color: var(--main-color);
        }
        footer {
            background: var(--main-color);
            color: var(--accent-color);
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>To My Love, [PARTNER'S NAME]</h1>
            <p>Every moment with you is a gift ❤️</p>
            <a href="#our-message" class="btn">See What I Wrote For You</a>
        </div>
    </section>

    <!-- Music Player -->
    <div class="music-player" id="musicBtn">
        🎵 Play Our Song
    </div>
    <audio id="loveSong" loop>
        <source src="YOUR-SONG-URL-HERE" type="audio/mp3">
        Your browser doesn't support audio playback.
    

    <!-- Message & Gallery Section -->
    <section id="our-message" class="message-section">
        <h2>You Mean Everything To Me</h2>
        <p>[WRITE YOUR PERSONAL MESSAGE HERE – share what you love about them, your favorite memories, or your hopes for the future!]</p>
        
        <!-- Hidden Surprise Message -->
        <div class="surprise-box" onclick="showSurprise()">
            👉 Click Here For A Little Secret! 👈
            <div class="surprise-hidden" id="surpriseText">
                [YOUR HIDDEN MESSAGE HERE – e.g., "I've been planning a surprise dinner for us at our favorite restaurant!", or "You're the first person I think about every morning and the last at night!"]
            </div>
        </div>

        <h3>Our Favorite Moments</h3>
        <div class="gallery">
            <img src="PHOTO-1-URL-HERE" alt="Memory 1">
            <img src="PHOTO-2-URL-HERE" alt="Memory 2">
            <img src="PHOTO-3-URL-HERE" alt="Memory 3">
            <img src="PHOTO-4-URL-HERE" alt="Memory 4">
        </div>

        <p class="closing">Happy Valentine's Day, my love. I can't wait to spend forever with you.<br>With all my heart, [YOUR NAME]</p>
    </section>

    <footer>
        Made with ❤️ on February 14, 2026
    </footer>

    <script>
        // Music Player Function
        const musicBtn = document.getElementById('musicBtn');
        const loveSong = document.getElementById('loveSong');
        let isPlaying = false;

        musicBtn.addEventListener('click', () => {
            if (isPlaying) {
                loveSong.pause();
                musicBtn.textContent = "🎵 Play Our Song";
            } else {
                loveSong.play();
                musicBtn.textContent = "⏸️ Pause Our Song";
            }
            isPlaying = !isPlaying;
        });

        // Hidden Surprise Message Function
        function showSurprise() {
            const surpriseText = document.getElementById('surpriseText');
            surpriseText.style.display = surpriseText.style.display === 'block' ? 'none' : 'block';
        }
    </script>
</body>
</html>
![IMG_20250817_144823_237](https://github.com/user-attachments/assets/b2affca5-2cea-4ff3-a9b3-17b69f01db19)
![Messenger_creation_D87F02F5-D086-4063-BC89-00CD947B1967](https://github.com/user-attachments/assets/c7d25d88-dce4-4885-9e5f-cc12448ba2e5)
