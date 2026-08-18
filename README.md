<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Babyyy ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            height: 100vh;
            background: linear-gradient(135deg, #ffccd5, #ffffff, #ffe5ec);
            background-size: 200% 200%;
            animation: bgMove 10s ease infinite;
            overflow: hidden;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        @keyframes bgMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Floating Heart Balloons */
        .balloon {
            position: absolute;
            bottom: -150px;
            width: 50px;
            height: 50px;
            background-color: #ff4d6d;
            transform: rotate(45deg);
            animation: flyUp 6s linear infinite;
            z-index: 1;
            opacity: 0.8;
            box-shadow: inset -5px -5px 0px rgba(0, 0, 0, 0.1);
        }

        .balloon::before,
        .balloon::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 50px;
            background-color: #ff4d6d;
            border-radius: 50%;
        }

        .balloon::before {
            top: -25px;
            left: 0;
        }

        .balloon::after {
            left: -25px;
            top: 0;
        }

        .balloon-string {
            position: absolute;
            bottom: -60px;
            left: 24px;
            width: 2px;
            height: 60px;
            background-color: #bbb;
        }

        @keyframes flyUp {
            0% {
                bottom: -150px;
                transform: rotate(45deg) scale(1);
            }
            50% {
                transform: rotate(45deg) scale(1.1);
            }
            100% {
                bottom: 110vh;
                transform: rotate(45deg) scale(1);
            }
        }

        /* Main Container */
        .container {
            position: relative;
            z-index: 10;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        /* Cartoon Cute Cat */
        .cat-container {
            position: relative;
            margin-bottom: 20px;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .cat-avatar {
            width: 130px;
            height: 130px;
            background: #fff;
            border: 4px solid #ff4d6d;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 70px;
            box-shadow: 0 10px 25px rgba(255, 77, 109, 0.3);
            position: relative;
        }

        /* Speech Bubble */
        .speech-bubble {
            background: #fff;
            border: 3px solid #ff4d6d;
            padding: 15px 25px;
            border-radius: 20px;
            font-size: 20px;
            color: #d90429;
            font-weight: bold;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            position: relative;
            max-width: 320px;
        }

        .speech-bubble::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            border-width: 15px 15px 0;
            border-style: solid;
            border-color: #ff4d6d transparent;
            display: block;
            width: 0;
        }

        /* Options Buttons */
        .options-box {
            display: flex;
            gap: 20px;
        }

        .btn {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 18px;
            font-weight: bold;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(255, 77, 109, 0.4);
            transition: all 0.2s ease;
            font-family: 'Comic Sans MS', cursive, sans-serif;
        }

        .btn:hover {
            background-color: #d90429;
            transform: scale(1.08);
        }

        /* Doraemon & Message Card Section */
        .hidden {
            display: none !important;
        }

        .reveal-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            animation: fadeIn 1s ease forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        .doraemon-avatar {
            width: 130px;
            height: 130px;
            background: #00b4d8;
            border: 4px solid #03045e;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 70px;
            box-shadow: 0 10px 25px rgba(0, 180, 216, 0.4);
            margin-bottom: 15px;
            animation: bounce 2s ease-in-out infinite;
        }

        .love-letter {
            background: #ffffff;
            border: 4px dashed #ff4d6d;
            padding: 25px;
            border-radius: 20px;
            max-width: 420px;
            font-size: 18px;
            color: #333;
            line-height: 1.5;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            position: relative;
        }

        .love-letter p {
            color: #d90429;
            font-weight: bold;
        }

        /* Kissing Animation Popups */
        .kiss-popup {
            position: absolute;
            font-size: 35px;
            animation: floatKiss 1.5s ease-in-out infinite;
            z-index: 20;
        }

        @keyframes floatKiss {
            0% { transform: translateY(0) scale(0.8); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(-60px) scale(1.2); opacity: 0; }
        }
    </style>
</head>
<body>

    <!-- Background Balloons Generator -->
    <div id="balloon-container"></div>

    <!-- Initial Interactive Screen -->
    <div class="container" id="main-screen">
        <div class="cat-container">
            <div class="cat-avatar">🐱</div>
        </div>
        <div class="speech-bubble">
            Hey babyyy! Choose your path carefully~ ❤️
        </div>
        <div class="options-box">
            <button class="btn" onclick="triggerSurprise()">1. Click Here</button>
            <button class="btn" onclick="triggerSurprise()">2. Select One</button>
        </div>
    </div>

    <!-- Final Surprise Screen (Doraemon & Message) -->
    <div class="container hidden" id="surprise-screen">
        <div class="reveal-section">
            <div class="doraemon-avatar">🔵</div>
            <div class="love-letter">
                <p>“Thank you my one and only babyyy for choosing me over everyone and make me your partner. I promise i'll never leave you and always keep you smiling. I love youuuuuu baby.”</p>
            </div>
        </div>
    </div>

    <!-- Kissing Cats Container -->
    <div id="kiss-container"></div>

    <script>
        // Generate Floating Heart Balloons
        const balloonContainer = document.getElementById('balloon-container');
        const colors = ['#ff4d6d', '#ff758f', '#ffb3c1', '#ff8fa3', '#c9184a'];

        function createBalloon() {
            const balloon = document.createElement('div');
            balloon.classList.add('balloon');
            
            // Random styling properties
            const color = colors[Math.floor(Math.random() * colors.length)];
            balloon.style.backgroundColor = color;
            // Target pseudo elements color dynamically via inline styling hacks or simple variants
            balloon.style.left = Math.random() * 100 + 'vw';
            const duration = Math.random() * 4 + 4; // 4 to 8 seconds
            balloon.style.animationDuration = duration + 's';
            
            // String attached
            const string = document.createElement('div');
            string.classList.add('balloon-string');
            balloon.appendChild(string);

            balloonContainer.appendChild(balloon);

            // Remove balloon after animation completes
            setTimeout(() => {
                balloon.remove();
            }, duration * 1000);
        }

        // Continuously generate balloons
        let balloonInterval = setInterval(createBalloon, 400);

        function triggerSurprise() {
            // Stop balloon generation and clear existing balloons (Burst effect)
            clearInterval(balloonInterval);
            const allBalloons = document.querySelectorAll('.balloon');
            allBalloons.forEach(b => {
                b.style.transform = 'scale(1.5)';
                b.style.opacity = '0';
                b.style.transition = 'all 0.3s ease';
                setTimeout(() => b.remove(), 300);
            });

            // Switch screens
            document.getElementById('main-screen').classList.add('hidden');
            document.getElementById('surprise-screen').classList.remove('hidden');

            // Spawn Kissing Cats at the end
            startKisses();
        }

        function startKisses() {
            const kissContainer = document.getElementById('kiss-container');
            
            // Create a cute mini cat giving kisses continuously
            setInterval(() => {
                const kiss = document.createElement('div');
                kiss.classList.add('kiss-popup');
                kiss.innerHTML = '😽💋';
                
                // Random position near bottom center
                const randomX = window.innerWidth / 2 + (Math.random() * 200 - 100);
                const randomY = window.innerHeight / 2 + 120 + (Math.random() * 40 - 20);
                
                kiss.style.left = randomX + 'px';
                kiss.style.top = randomY + 'px';
                
                kissContainer.appendChild(kiss);

                setTimeout(() => {
                    kiss.remove();
                }, 1500);
            }, 400);
        }
    </script>
</body>
</html>
