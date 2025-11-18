# fati_projectt
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Love ❤️</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            padding: 40px 30px;
            text-align: center;
            max-width: 500px;
            width: 100%;
            position: relative;
            overflow: hidden;
        }
        
        h1 {
            color: #ff6b6b;
            margin-bottom: 30px;
            font-size: 2.8rem;
            font-family: 'Dancing Script', cursive;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .heart-container {
            width: 120px;
            height: 120px;
            margin: 0 auto 25px;
            position: relative;
            animation: float 3s ease-in-out infinite;
        }
        
        .heart {
            position: absolute;
            width: 120px;
            height: 120px;
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            transform: rotate(45deg);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
        }
        
        .heart:before, .heart:after {
            content: '';
            width: 120px;
            height: 120px;
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            border-radius: 50%;
            position: absolute;
        }
        
        .heart:before {
            top: -60px;
            left: 0;
        }
        
        .heart:after {
            top: 0;
            left: -60px;
        }
        
        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 15px 35px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        #yesBtn {
            background: linear-gradient(45deg, #4CAF50, #45a049);
            color: white;
        }
        
        #yesBtn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 20px rgba(76, 175, 80, 0.4);
        }
        
        #noBtn {
            background: linear-gradient(45deg, #f44336, #d32f2f);
            color: white;
        }
        
        #noBtn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(244, 67, 54, 0.4);
        }
        
        .message {
            margin-top: 25px;
            font-size: 1.4rem;
            color: #ff6b6b;
            font-weight: 600;
            min-height: 50px;
            opacity: 0;
            transition: all 0.5s ease;
            font-family: 'Dancing Script', cursive;
        }
        
        .message.show {
            opacity: 1;
            transform: translateY(0);
        }
        
        .love-letter {
            margin-top: 30px;
            padding: 25px;
            background: linear-gradient(135deg, #fff5f5, #ffecec);
            border-radius: 15px;
            border-left: 5px solid #ff6b6b;
            display: none;
            text-align: left;
            animation: fadeIn 1s ease;
        }
        
        .love-letter h2 {
            color: #ff6b6b;
            margin-bottom: 15px;
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
        }
        
        .love-letter p {
            color: #555;
            line-height: 1.6;
            margin-bottom: 10px;
        }
        
        .floating-hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .floating-heart {
            position: absolute;
            font-size: 24px;
            opacity: 0;
            animation: floatUp 5s linear forwards;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0); }
            50% { transform: translateY(-15px) rotate(5deg); }
        }
        
        @keyframes floatUp {
            0% {
                transform: translateY(100px) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            opacity: 0;
        }
        
        @media (max-width: 500px) {
            .container {
                padding: 25px 20px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            button {
                padding: 12px 25px;
                font-size: 1rem;
            }
            
            .heart-container {
                width: 100px;
                height: 100px;
            }
            
            .heart, .heart:before, .heart:after {
                width: 100px;
                height: 100px;
            }
            
            .heart:before {
                top: -50px;
            }
            
            .heart:after {
                left: -50px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="heart-container">
            <div class="heart"></div>
        </div>
        <h1>Do you love me?</h1>
        <div class="buttons">
            <button id="yesBtn">Yes, I do! 💖</button>
            <button id="noBtn">No, I don't</button>
        </div>
        <div class="message" id="message"></div>
        <div class="love-letter" id="loveLetter">
            <h2>My Dearest Love,</h2>
            <p>From the moment we met, you've filled my life with joy and meaning. Your smile is my favorite sight, your laughter my favorite sound, and your love my greatest treasure.</p>
            <p>Every day with you is a blessing I don't take for granted. You make me a better person, and I promise to always cherish and adore you.</p>
            <p>With all my heart, now and forever...</p>
            <p style="text-align: right; margin-top: 15px; font-family: 'Dancing Script', cursive; font-size: 1.5rem;">Your Love 💕</p>
        </div>
        <div class="floating-hearts" id="floatingHearts"></div>
    </div>

    <script>
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');
        const message = document.getElementById('message');
        const loveLetter = document.getElementById('loveLetter');
        const floatingHearts = document.getElementById('floatingHearts');
        
        let clickCount = 0;
        const romanticMessages = [
            "I knew it! I love you too! 💕",
            "You make me the happiest person! 🌟",
            "My heart is smiling! 😊",
            "This is the best day ever! 💖",
            "I'll love you forever! 🌹"
        ];
        
        // Yes button functionality
        yesBtn.addEventListener('click', function() {
            clickCount++;
            const randomMessage = romanticMessages[Math.floor(Math.random() * romanticMessages.length)];
            message.textContent = randomMessage;
            message.classList.add('show');
            
            // Show love letter
            loveLetter.style.display = 'block';
            
            // Create floating hearts
            createFloatingHearts(15);
            
            // Create confetti effect
            createConfetti();
            
            // Change background to more romantic gradient
            document.body.style.background = "linear-gradient(135deg, #ff6b6b 0%, #ff8e8e 100%)";
            
            // Play romantic sound
            playRomanticSound();
        });
        
        // No button functionality - with playful interaction
        noBtn.addEventListener('mouseover', function() {
            // Move the button to a random position when hovered
            const container = document.querySelector('.container');
            const containerRect = container.getBoundingClientRect();
            const buttonRect = noBtn.getBoundingClientRect();
            
            const maxX = containerRect.width - buttonRect.width - 20;
            const maxY = containerRect.height - buttonRect.height - 20;
            
            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);
            
            noBtn.style.position = 'absolute';
            noBtn.style.left = `${randomX}px`;
            noBtn.style.top = `${randomY}px`;
        });
        
        noBtn.addEventListener('click', function() {
            message.textContent = "I don't believe you! Try the other button! 😉";
            message.classList.add('show');
        });
        
        // Function to create floating hearts
        function createFloatingHearts(count) {
            for (let i = 0; i < count; i++) {
                const heart = document.createElement('div');
                heart.classList.add('floating-heart');
                heart.innerHTML = '💖';
                
                // Random position and animation
                const left = Math.random() * 100;
                const delay = Math.random() * 2;
                const duration = 3 + Math.random() * 2;
                
                heart.style.left = `${left}%`;
                heart.style.animationDelay = `${delay}s`;
                heart.style.animationDuration = `${duration}s`;
                
                floatingHearts.appendChild(heart);
                
                // Remove heart after animation
                setTimeout(() => {
                    heart.remove();
                }, (duration + delay) * 1000);
            }
        }
        
        // Function to create confetti
        function createConfetti() {
            const colors = ['#ff6b6b', '#4CAF50', '#2196F3', '#FFEB3B', '#9C27B0'];
            const container = document.querySelector('.container');
            
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('confetti');
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.left = Math.random() * 100 + '%';
                confetti.style.top = '-10px';
                confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                
                container.appendChild(confetti);
                
                // Animate confetti
                const animation = confetti.animate([
                    { transform: `translateY(0) rotate(0deg)`, opacity: 1 },
                    { transform: `translateY(${window.innerHeight}px) rotate(${Math.random() * 360}deg)`, opacity: 0 }
                ], {
                    duration: 1000 + Math.random() * 2000,
                    easing: 'cubic-bezier(0.1, 0.8, 0.2, 1)'
                });
                
                // Remove confetti after animation
                animation.onfinish = () => confetti.remove();
            }
        }
        
        // Function to play romantic sound
        function playRomanticSound() {
            // Create a simple melody using Web Audio API
            try {
                const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                const playNote = (frequency, duration, startTime, volume = 0.1) => {
                    const oscillator = audioContext.createOscillator();
                    const gainNode = audioContext.createGain();
                    
                    oscillator.connect(gainNode);
                    gainNode.connect(audioContext.destination);
                    
                    oscillator.frequency.value = frequency;
                    oscillator.type = 'sine';
                    
                    gainNode.gain.setValueAtTime(0, startTime);
                    gainNode.gain.linearRampToValueAtTime(volume, startTime + 0.01);
                    gainNode.gain.exponentialRampToValueAtTime(0.001, startTime + duration);
                    
                    oscillator.start(startTime);
                    oscillator.stop(startTime + duration);
                };
                
                // Play a simple romantic melody
                const now = audioContext.currentTime;
                playNote(523.25, 0.6, now); // C
                playNote(659.25, 0.6, now + 0.6); // E
                playNote(783.99, 0.6, now + 1.2); // G
                playNote(659.25, 0.6, now + 1.8); // E
                playNote(880.00, 0.8, now + 2.4); // A
            } catch (e) {
                console.log("Audio not supported in this browser");
            }
        }
    </script>
</body>
</html>
