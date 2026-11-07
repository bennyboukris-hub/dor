<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>תפוס את הביצים!</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Tone.js for Sound Effects -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.49/Tone.js"></script>
    <!-- Google Fonts for Modern Typography -->
    <link href="https://fonts.googleapis.com/css2?family=Rubik:wght@400;600;800&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            font-family: 'Rubik', sans-serif;
            user-select: none;
            -webkit-user-select: none;
            touch-action: manipulation;
        }
        body {
            background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
            overflow: hidden;
        }
        #game-container {
            position: relative;
            box-shadow: 0 20px 50px rgba(0,0,0,0.5);
        }
        canvas {
            display: block;
            border-radius: 1.5rem;
            background: linear-gradient(180deg, #87CEEB 0%, #E0F6FF 70%, #7CFC00 70%, #556B2F 100%);
        }
        /* Custom Glowing & Metallic Styling */
        .glass-panel {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.25);
        }
        .btn-bounce:active {
            transform: scale(0.92);
        }
    </style>
</head>
<body class="h-screen w-screen flex flex-col items-center justify-center p-2 sm:p-4 text-white">

    <!-- Game Container Wrapper -->
    <div id="game-container" class="relative w-full max-w-lg h-[92vh] max-h-[850px] flex flex-col items-center justify-between p-3 rounded-3xl glass-panel overflow-hidden border border-white/20">

        <!-- Top HUD Panel -->
        <div class="w-full flex justify-between items-center px-4 py-2 bg-slate-900/60 rounded-2xl border border-white/10 z-10 backdrop-blur-md">
            <div class="flex items-center gap-2">
                <i class="fa-solid fa-trophy text-yellow-400 text-xl"></i>
                <div class="flex flex-col">
                    <span class="text-xs text-slate-300">שיא:</span>
                    <span id="high-score-val" class="font-extrabold text-lg leading-tight text-yellow-300">0</span>
                </div>
            </div>
            <div class="flex items-center gap-2">
                <i class="fa-solid fa-egg text-amber-200 text-2xl"></i>
                <div class="flex flex-col items-center">
                    <span class="text-xs text-slate-300">ניקוד:</span>
                    <span id="score-val" class="font-black text-2xl leading-tight text-white">0</span>
                </div>
            </div>
            <div class="flex items-center gap-2">
                <div class="flex flex-col text-left">
                    <span class="text-xs text-slate-300">פסילות:</span>
                    <div id="lives-container" class="flex gap-1 text-red-500 text-sm">
                        <i class="fa-solid fa-heart"></i>
                        <i class="fa-solid fa-heart"></i>
                        <i class="fa-solid fa-heart"></i>
                    </div>
                </div>
            </div>
        </div>

        <!-- Canvas Game Screen -->
        <div class="relative w-full flex-grow my-2 rounded-2xl overflow-hidden">
            <canvas id="gameCanvas" class="w-full h-full"></canvas>

            <!-- Start Screen Overlay -->
            <div id="start-screen" class="absolute inset-0 bg-slate-950/85 backdrop-blur-md flex flex-col items-center justify-center p-6 text-center z-20 transition-all duration-300">
                <div class="w-20 h-20 bg-amber-400/20 rounded-full flex items-center justify-center mb-4 animate-bounce border-2 border-amber-400">
                    <i class="fa-solid fa-basket-shopping text-4xl text-amber-300"></i>
                </div>
                <h1 class="text-3xl sm:text-4xl font-black mb-2 text-transparent bg-clip-text bg-gradient-to-r from-amber-200 via-yellow-400 to-amber-500">תפוס את הביצים!</h1>
                <p class="text-slate-300 text-sm mb-6 max-w-xs">אסוף ביצים רגילות ומוזהבות, והזהר מביצי בוץ ופצצות! ככל שתתפוס יותר - המהירות תעלה!</p>
                
                <div class="w-full max-w-xs bg-slate-900/80 rounded-xl p-3 mb-6 text-xs text-slate-300 space-y-2 border border-slate-700">
                    <div class="flex justify-between items-center"><span class="flex items-center gap-2">⚪ ביצה רגילה</span> <span class="text-green-400 font-bold">+10 נק'</span></div>
                    <div class="flex justify-between items-center"><span class="flex items-center gap-2">⭐ ביצת זהב</span> <span class="text-yellow-400 font-bold">+30 נק'</span></div>
                    <div class="flex justify-between items-center"><span class="flex items-center gap-2">💩 ביצת בוץ</span> <span class="text-amber-600 font-bold">-15 נק'</span></div>
                    <div class="flex justify-between items-center"><span class="flex items-center gap-2">💣 פצצה</span> <span class="text-red-400 font-bold">-פסילה</span></div>
                </div>

                <button id="start-btn" class="w-full max-w-xs py-3.5 px-6 bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-400 hover:to-teal-500 text-white font-extrabold text-lg rounded-xl shadow-lg hover:shadow-emerald-500/30 transition-all transform active:scale-95 btn-bounce">
                    התחל משחק <i class="fa-solid fa-play mr-2"></i>
                </button>
            </div>

            <!-- Game Over Screen Overlay -->
            <div id="game-over-screen" class="absolute inset-0 bg-slate-950/90 backdrop-blur-md flex flex-col items-center justify-center p-6 text-center z-20 hidden transition-all duration-300">
                <div class="w-20 h-20 bg-red-500/20 rounded-full flex items-center justify-center mb-4 border-2 border-red-500 animate-pulse">
                    <i class="fa-solid fa-skull-crossbones text-4xl text-red-400"></i>
                </div>
                <h2 class="text-3xl font-black text-red-400 mb-1">המשחק נגמר!</h2>
                <p id="game-over-reason" class="text-slate-400 text-xs mb-4">נגמרו לכם הפסילות</p>
                
                <div class="w-full max-w-xs bg-slate-900/80 rounded-2xl p-4 mb-6 border border-slate-800 space-y-3">
                    <div class="flex justify-between items-center text-slate-300 text-sm">
                        <span>ניקוד סופי:</span>
                        <span id="final-score" class="font-extrabold text-2xl text-amber-400">0</span>
                    </div>
                    <div class="flex justify-between items-center text-slate-300 text-sm border-t border-slate-800 pt-2">
                        <span>שיא אישי:</span>
                        <span id="final-high-score" class="font-bold text-lg text-yellow-300">0</span>
                    </div>
                    <div class="flex justify-between items-center text-slate-300 text-sm border-t border-slate-800 pt-2">
                        <span>רמת מהירות שהגעת:</span>
                        <span id="final-speed-level" class="font-bold text-cyan-400">1</span>
                    </div>
                </div>

                <button id="restart-btn" class="w-full max-w-xs py-3.5 px-6 bg-gradient-to-r from-amber-500 to-orange-600 hover:from-amber-400 hover:to-orange-500 text-white font-extrabold text-lg rounded-xl shadow-lg hover:shadow-orange-500/30 transition-all transform active:scale-95 btn-bounce">
                    שחק שוב <i class="fa-solid fa-rotate-right mr-2"></i>
                </button>
            </div>
        </div>

        <!-- Touch Controls for Mobile Screens -->
        <div class="w-full flex justify-between items-center gap-3 px-2 pt-1 pb-1 z-10 sm:hidden">
            <button id="btn-left" class="flex-1 py-4 bg-slate-800/80 active:bg-slate-700 text-white rounded-2xl text-2xl flex justify-center items-center border border-white/10 active:scale-95 transition-all">
                <i class="fa-solid fa-arrow-right"></i>
            </button>
            <div class="text-[10px] text-slate-400 text-center px-1">ניתן לחלופין לגרור את הסל במסך</div>
            <button id="btn-right" class="flex-1 py-4 bg-slate-800/80 active:bg-slate-700 text-white rounded-2xl text-2xl flex justify-center items-center border border-white/10 active:scale-95 transition-all">
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

    </div>

    <!-- JavaScript Logic -->
    <script>
        // --- Sound Effects Setup using Tone.js ---
        let soundsLoaded = false;
        let catchSynth, bonusSynth, hitSynth, bombSynth;

        function initAudio() {
            if (soundsLoaded) return;
            try {
                Tone.start();
                catchSynth = new Tone.Synth({ oscillator: { type: 'sine' }, envelope: { attack: 0.005, decay: 0.1, sustain: 0, release: 0.1 } }).toDestination();
                bonusSynth = new Tone.PolySynth(Tone.Synth).toDestination();
                hitSynth = new Tone.MembraneSynth({ pitchDecay: 0.05, octaves: 4, oscillator: { type: 'sine' } }).toDestination();
                bombSynth = new Tone.NoiseSynth({ noise: { type: 'brown' }, envelope: { attack: 0.005, decay: 0.3, sustain: 0 } }).toDestination();
                soundsLoaded = true;
            } catch (e) {
                console.log("Audio initialization skipped or blocked.");
            }
        }

        function playSound(type) {
            if (!soundsLoaded) return;
            try {
                if (type === 'catch') catchSynth.triggerAttackRelease("C6", "8n");
                else if (type === 'bonus') bonusSynth.triggerAttackRelease(["E5", "G5", "B5"], "16n");
                else if (type === 'mud') hitSynth.triggerAttackRelease("G2", "8n");
                else if (type === 'bomb') bombSynth.triggerAttackRelease("8n");
            } catch (e) {}
        }

        // --- Canvas Setup ---
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');

        function resizeCanvas() {
            const rect = canvas.parentElement.getBoundingClientRect();
            canvas.width = rect.width;
            canvas.height = rect.height;
        }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        // --- Game State Variables ---
        let score = 0;
        let highScore = localStorage.getItem('egg_catcher_highscore') || 0;
        let lives = 3;
        let eggsCaughtCount = 0;
        let speedMultiplier = 1;
        let isGameOver = false;
        let isGameRunning = false;
        let animationFrameId = null;

        // Display Highscore
        document.getElementById('high-score-val').innerText = highScore;

        // Player / Basket Definition
        const player = {
            x: 0,
            y: 0,
            width: 75,
            height: 45,
            speed: 8,
            dx: 0
        };

        // Falling items array
        let items = [];
        let itemSpawnTimer = 0;
        let spawnInterval = 60; // Frames between spawns

        // Key Listeners State
        const keys = {
            left: false,
            right: false
        };

        // Item Types Config
        const ITEM_TYPES = {
            NORMAL: { type: 'normal', color: '#FFFDD0', border: '#D4AF37', points: 10, radius: 14, chance: 0.60 },
            GOLDEN: { type: 'golden', color: '#FFD700', border: '#B8860B', points: 30, radius: 16, chance: 0.15 },
            MUD: { type: 'mud', color: '#654321', border: '#3B2219', points: -15, radius: 14, chance: 0.15 },
            BOMB: { type: 'bomb', color: '#2B2B2B', border: '#000000', points: 0, radius: 15, chance: 0.10 }
        };

        // --- Game Controls ---
        window.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowRight' || e.key === 'd' || e.key === 'D') keys.right = true;
            if (e.key === 'ArrowLeft' || e.key === 'a' || e.key === 'A') keys.left = true;
        });

        window.addEventListener('keyup', (e) => {
            if (e.key === 'ArrowRight' || e.key === 'd' || e.key === 'D') keys.right = false;
            if (e.key === 'ArrowLeft' || e.key === 'a' || e.key === 'A') keys.left = false;
        });

        // Touch & Drag Controls
        let isDragging = false;

        canvas.addEventListener('touchstart', (e) => {
            if (!isGameRunning) return;
            isDragging = true;
            movePlayerToTouch(e.touches[0].clientX);
        }, { passive: true });

        canvas.addEventListener('touchmove', (e) => {
            if (!isGameRunning || !isDragging) return;
            movePlayerToTouch(e.touches[0].clientX);
        }, { passive: true });

        canvas.addEventListener('touchend', () => { isDragging = false; });

        function movePlayerToTouch(clientX) {
            const rect = canvas.getBoundingClientRect();
            const touchX = clientX - rect.left;
            player.x = touchX - player.width / 2;
            clampPlayerPosition();
        }

        // On-screen Buttons for Mobile
        const btnLeft = document.getElementById('btn-left');
        const btnRight = document.getElementById('btn-right');

        // Reversed for RTL intuitive feel: Left button moves right relative to Hebrew screen layout, right button moves left.
        // We will make Left Button move character Left, Right Button move character Right logically.
        btnLeft.addEventListener('touchstart', (e) => { e.preventDefault(); keys.right = true; });
        btnLeft.addEventListener('touchend', (e) => { e.preventDefault(); keys.right = false; });
        btnLeft.addEventListener('mousedown', () => { keys.right = true; });
        btnLeft.addEventListener('mouseup', () => { keys.right = false; });

        btnRight.addEventListener('touchstart', (e) => { e.preventDefault(); keys.left = true; });
        btnRight.addEventListener('touchend', (e) => { e.preventDefault(); keys.left = false; });
        btnRight.addEventListener('mousedown', () => { keys.left = true; });
        btnRight.addEventListener('mouseup', () => { keys.left = false; });

        function clampPlayerPosition() {
            if (player.x < 0) player.x = 0;
            if (player.x + player.width > canvas.width) player.x = canvas.width - player.width;
        }

        // --- Helper: Spawn Item ---
        function spawnItem() {
            const rand = Math.random();
            let selectedType = ITEM_TYPES.NORMAL;

            if (rand < ITEM_TYPES.BOMB.chance) {
                selectedType = ITEM_TYPES.BOMB;
            } else if (rand < ITEM_TYPES.BOMB.chance + ITEM_TYPES.MUD.chance) {
                selectedType = ITEM_TYPES.MUD;
            } else if (rand < ITEM_TYPES.BOMB.chance + ITEM_TYPES.MUD.chance + ITEM_TYPES.GOLDEN.chance) {
                selectedType = ITEM_TYPES.GOLDEN;
            }

            const radius = selectedType.radius;
            const x = Math.random() * (canvas.width - radius * 2) + radius;
            const baseSpeed = 2.5 + Math.random() * 1.5;

            items.push({
                x: x,
                y: -radius,
                radius: radius,
                speed: baseSpeed * speedMultiplier,
                type: selectedType.type,
                color: selectedType.color,
                border: selectedType.border,
                points: selectedType.points,
                rotation: 0,
                rotSpeed: (Math.random() - 0.5) * 0.05
            });
        }

        // --- Game Reset / Start ---
        function resetGame() {
            score = 0;
            lives = 3;
            eggsCaughtCount = 0;
            speedMultiplier = 1;
            items = [];
            itemSpawnTimer = 0;
            spawnInterval = 55;
            isGameOver = false;

            player.width = Math.min(canvas.width * 0.2, 85);
            player.height = player.width * 0.55;
            player.x = (canvas.width - player.width) / 2;
            player.y = canvas.height - player.height - 15;

            updateHUD();
        }

        function startGame() {
            initAudio();
            resetGame();
            document.getElementById('start-screen').classList.add('hidden');
            document.getElementById('game-over-screen').classList.add('hidden');
            isGameRunning = true;
            if (animationFrameId) cancelAnimationFrame(animationFrameId);
            gameLoop();
        }

        function triggerGameOver(reason) {
            isGameOver = true;
            isGameRunning = false;
            playSound('bomb');

            if (score > highScore) {
                highScore = score;
                localStorage.setItem('egg_catcher_highscore', highScore);
                document.getElementById('high-score-val').innerText = highScore;
            }

            document.getElementById('final-score').innerText = score;
            document.getElementById('final-high-score').innerText = highScore;
            document.getElementById('final-speed-level').innerText = speedMultiplier.toFixed(1) + 'x';
            document.getElementById('game-over-reason').innerText = reason || "נגמרו לכם הפסילות";
            document.getElementById('game-over-screen').classList.remove('hidden');
        }

        function updateHUD() {
            document.getElementById('score-val').innerText = score;
            
            // Render Hearts
            const heartsContainer = document.getElementById('lives-container');
            heartsContainer.innerHTML = '';
            for (let i = 0; i < 3; i++) {
                if (i < lives) {
                    heartsContainer.innerHTML += '<i class="fa-solid fa-heart text-red-500 text-sm"></i>';
                } else {
                    heartsContainer.innerHTML += '<i class="fa-regular fa-heart text-slate-600 text-sm"></i>';
                }
            }
        }

        // --- Drawing Functions ---
        function drawPlayer() {
            ctx.save();
            ctx.translate(player.x, player.y);

            // Basket Shadow
            ctx.beginPath();
            ctx.ellipse(player.width / 2, player.height + 4, player.width / 2, 6, 0, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(0, 0, 0, 0.25)';
            ctx.fill();

            // Basket Main Body
            ctx.beginPath();
            ctx.moveTo(0, 5);
            ctx.quadraticCurveTo(player.width / 2, player.height + 12, player.width, 5);
            ctx.lineTo(player.width * 0.85, 0);
            ctx.lineTo(player.width * 0.15, 0);
            ctx.closePath();

            const gradient = ctx.createLinearGradient(0, 0, 0, player.height);
            gradient.addColorStop(0, '#d97706');
            gradient.addColorStop(1, '#78350f');
            ctx.fillStyle = gradient;
            ctx.fill();
            ctx.lineWidth = 2.5;
            ctx.strokeStyle = '#451a03';
            ctx.stroke();

            // Basket Weave Lines Effect
            ctx.beginPath();
            ctx.moveTo(player.width * 0.2, 5);
            ctx.lineTo(player.width * 0.3, player.height - 2);
            ctx.moveTo(player.width * 0.5, 5);
            ctx.lineTo(player.width * 0.5, player.height);
            ctx.moveTo(player.width * 0.8, 5);
            ctx.lineTo(player.width * 0.7, player.height - 2);
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 2;
            ctx.stroke();

            // Basket Rim
            ctx.beginPath();
            ctx.roundRect(-2, -4, player.width + 4, 8, 4);
            ctx.fillStyle = '#b45309';
            ctx.fill();
            ctx.strokeStyle = '#451a03';
            ctx.stroke();

            ctx.restore();
        }

        function drawItem(item) {
            ctx.save();
            ctx.translate(item.x, item.y);
            ctx.rotate(item.rotation);

            if (item.type === 'bomb') {
                // Draw Bomb
                ctx.beginPath();
                ctx.arc(0, 0, item.radius, 0, Math.PI * 2);
                ctx.fillStyle = item.color;
                ctx.fill();
                ctx.lineWidth = 2;
                ctx.strokeStyle = '#555';
                ctx.stroke();

                // Bomb Fuse
                ctx.beginPath();
                ctx.moveTo(0, -item.radius);
                ctx.quadraticCurveTo(6, -item.radius - 8, 4, -item.radius - 12);
                ctx.lineWidth = 2.5;
                ctx.strokeStyle = '#8B4513';
                ctx.stroke();

                // Sparkles
                ctx.beginPath();
                ctx.arc(4, -item.radius - 12, 3, 0, Math.PI * 2);
                ctx.fillStyle = '#FF4500';
                ctx.fill();
            } else {
                // Draw Egg Shape (Normal / Golden / Mud)
                ctx.beginPath();
                ctx.scale(1, 1.25);
                ctx.arc(0, 0, item.radius, 0, Math.PI * 2);
                
                // Shiny Metallic/Glossy Radial Gradient for Eggs
                const grad = ctx.createRadialGradient(-item.radius*0.3, -item.radius*0.3, 2, 0, 0, item.radius);
                grad.addColorStop(0, '#FFFFFF');
                grad.addColorStop(0.4, item.color);
                grad.addColorStop(1, item.border);
                
                ctx.fillStyle = grad;
                ctx.fill();
                ctx.lineWidth = 1.5;
                ctx.strokeStyle = item.border;
                ctx.stroke();

                // Mud Spots if Mud Egg
                if (item.type === 'mud') {
                    ctx.fillStyle = '#27150d';
                    ctx.beginPath();
                    ctx.arc(-3, -2, 2.5, 0, Math.PI * 2);
                    ctx.arc(4, 3, 3, 0, Math.PI * 2);
                    ctx.fill();
                }

                // Sparkle Effect for Golden Egg
                if (item.type === 'golden') {
                    ctx.fillStyle = '#FFF';
                    ctx.beginPath();
                    ctx.arc(-4, -4, 2, 0, Math.PI * 2);
                    ctx.fill();
                }
            }

            ctx.restore();
        }

        // --- Main Game Loop ---
        function gameLoop() {
            if (!isGameRunning) return;

            // Clear Screen
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Move Player via Keyboard
            if (keys.left) player.x -= player.speed;
            if (keys.right) player.x += player.speed;
            clampPlayerPosition();

            // Spawn Logic
            itemSpawnTimer++;
            if (itemSpawnTimer >= spawnInterval) {
                spawnItem();
                itemSpawnTimer = 0;
            }

            // Update & Render Items
            for (let i = items.length - 1; i >= 0; i--) {
                const item = items[i];
                item.y += item.speed;
                item.rotation += item.rotSpeed;

                drawItem(item);

                // Collision Detection with Player Basket
                const basketTop = player.y;
                const basketBottom = player.y + player.height;
                const basketLeft = player.x;
                const basketRight = player.x + player.width;

                if (
                    item.y + item.radius >= basketTop &&
                    item.y - item.radius <= basketBottom &&
                    item.x >= basketLeft - 5 &&
                    item.x <= basketRight + 5
                ) {
                    // Collision Caught!
                    if (item.type === 'bomb') {
                        lives--;
                        playSound('bomb');
                        if (lives <= 0) {
                            triggerGameOver("פגעת בפצצה!");
                            return;
                        }
                    } else if (item.type === 'mud') {
                        score = Math.max(0, score + item.points);
                        playSound('mud');
                    } else {
                        // Normal or Golden Egg
                        score += item.points;
                        eggsCaughtCount++;
                        playSound(item.type === 'golden' ? 'bonus' : 'catch');

                        // Increase Speed Every 5 Caught Eggs!
                        if (eggsCaughtCount % 5 === 0) {
                            speedMultiplier += 0.15;
                            spawnInterval = Math.max(25, spawnInterval - 3);
                        }
                    }

                    updateHUD();
                    items.splice(i, 1);
                    continue;
                }

                // Missed / Fell Off Screen
                if (item.y - item.radius > canvas.height) {
                    // If regular or golden egg falls off, lose a life
                    if (item.type === 'normal' || item.type === 'golden') {
                        lives--;
                        playSound('mud');
                        updateHUD();
                        if (lives <= 0) {
                            triggerGameOver("הרבה ביצים נשברו!");
                            return;
                        }
                    }
                    items.splice(i, 1);
                }
            }

            // Draw Basket Character
            drawPlayer();

            // Next Frame
            animationFrameId = requestAnimationFrame(gameLoop);
        }

        // --- Event Listeners for Buttons ---
        document.getElementById('start-btn').addEventListener('click', startGame);
        document.getElementById('restart-btn').addEventListener('click', startGame);

    </script>
</body>
</html>
