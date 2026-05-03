<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>AnimalClick</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Quicksand:wght@400;700&display=swap');

        body {
            margin: 0;
            overflow: hidden;
            font-family: 'Quicksand', sans-serif;
            touch-action: manipulation;
            user-select: none;
            background: #222;
        }

        #game-container {
            position: relative;
            width: 100vw;
            height: 100vh;
            background: linear-gradient(to bottom, #4facfe 0%, #00f2fe 100%);
            overflow: hidden;
        }

        .grass-layer {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 50%;
            background: linear-gradient(to bottom, #7cfc00 0%, #2e8b57 100%);
            border-top: 10px solid #55cc00;
        }

        .cloud {
            position: absolute;
            background: white;
            border-radius: 50px;
            opacity: 0.8;
            filter: blur(5px);
            animation: moveClouds linear infinite;
        }

        @keyframes moveClouds {
            from { left: -200px; }
            to { left: 100vw; }
        }

        .flower {
            position: absolute;
            width: 8px;
            height: 8px;
            background: white;
            border-radius: 50%;
            opacity: 0.6;
        }

        .animal {
            position: absolute;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 10;
            transition: transform 0.1s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .animal-emoji {
            font-size: 4rem;
            filter: drop-shadow(4px 4px 6px rgba(0,0,0,0.3));
            user-select: none;
        }

        .health-bar {
            width: 50px;
            height: 8px;
            background: rgba(0,0,0,0.3);
            border-radius: 4px;
            border: 1px solid white;
            margin-top: 5px;
            overflow: hidden;
        }

        .health-fill {
            height: 100%;
            background: #ff4757;
            width: 100%;
            transition: width 0.2s ease;
        }

        .score-float, .time-float {
            position: absolute;
            font-weight: 900;
            text-shadow: 2px 2px 0 #000;
            pointer-events: none;
            animation: floatUp 1s ease-out forwards;
            z-index: 60;
        }

        .score-float { color: #ffd700; font-size: 1.5rem; }
        .time-float { color: #00f2fe; font-size: 1.8rem; }

        @keyframes floatUp {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-100px) scale(1.5); opacity: 0; }
        }

        #ui-layer {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px;
            pointer-events: none;
            z-index: 100;
            display: flex;
            justify-content: space-between;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        #mute-btn {
            pointer-events: auto;
            background: rgba(255, 255, 255, 0.2);
            border: 2px solid rgba(255, 255, 255, 0.5);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            cursor: pointer;
            backdrop-filter: blur(4px);
            transition: transform 0.1s, background 0.2s;
        }

        #mute-btn:active { transform: scale(0.9); }

        .btn {
            pointer-events: auto;
            background: #ff6b6b;
            padding: 16px 40px;
            border-radius: 50px;
            font-family: 'Fredoka One', cursive;
            font-size: 1.5rem;
            color: white;
            border: 4px solid #ee5253;
            cursor: pointer;
            box-shadow: 0 6px 0 #c0392b;
            transition: all 0.1s;
        }

        .btn:active {
            box-shadow: 0 2px 0 #c0392b;
            transform: translateY(4px);
        }

        .btn-secondary {
            background: #4facfe;
            border-color: #0088cc;
            box-shadow: 0 6px 0 #006699;
        }

        #overlay {
            position: absolute;
            inset: 0;
            background: rgba(0,0,0,0.7);
            backdrop-filter: blur(8px);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 200;
            color: white;
            text-align: center;
            overflow-y: auto;
            padding: 40px 20px;
        }

        .game-title {
            font-family: 'Fredoka One', cursive;
            font-size: clamp(3rem, 10vw, 5rem);
            background: linear-gradient(to bottom, #ffeb3b, #f44336);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(4px 4px 0px rgba(0,0,0,0.2));
            margin-bottom: 10px;
        }

        .achievement-card {
            background: rgba(255,255,255,0.05);
            border-radius: 15px;
            padding: 10px;
            border: 2px solid rgba(255,255,255,0.05);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        /* Colores de Maestría */
        .mastery-0 { border-color: rgba(255,255,255,0.1); opacity: 0.6; filter: grayscale(1); }
        .mastery-1 { border-color: #cd7f32; background: rgba(205, 127, 50, 0.1); } /* Bronce */
        .mastery-2 { border-color: #c0c0c0; background: rgba(192, 192, 192, 0.1); } /* Plata */
        .mastery-3 { border-color: #ffd700; background: rgba(255, 215, 0, 0.1); } /* Oro */
        .mastery-4 { border-color: #e5e4e2; background: rgba(229, 228, 226, 0.15); box-shadow: 0 0 10px rgba(255,255,255,0.2); } /* Platino/Maestro */

        .achievement-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            width: 100%;
            max-width: 550px;
            margin-top: 20px;
        }

        .shake { animation: shake 0.2s ease-in-out; }
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        .time-pulse { animation: timePulse 0.5s ease-out; }
        @keyframes timePulse {
            0% { transform: scale(1); color: white; }
            50% { transform: scale(1.4); color: #00f2fe; }
            100% { transform: scale(1); color: white; }
        }

        #overlay::-webkit-scrollbar { width: 0; background: transparent; }
    </style>
</head>
<body>

<div id="game-container">
    <div id="clouds-container"></div>
    <div class="grass-layer">
        <div id="flowers-container"></div>
    </div>

    <div id="ui-layer">
        <div>
            <div class="text-3xl font-bold" style="font-family: 'Fredoka One'">PUNTOS: <span id="score">0</span></div>
            <div class="text-lg opacity-90">Récord: <span id="high-score-ui">0</span></div>
        </div>
        <div class="flex items-start gap-4">
            <div class="text-center">
                <div class="text-4xl font-black bg-white/20 px-4 py-1 rounded-full inline-block min-w-[80px]" id="timer">30</div>
                <div class="text-xs mt-1 font-bold">TIEMPO</div>
            </div>
            <button id="mute-btn">🔊</button>
        </div>
    </div>

    <div id="overlay"></div>
</div>

<script>
    // --- ESTADO GLOBAL Y PERSISTENCIA ---
    const appId = typeof __app_id !== 'undefined' ? __app_id : 'animal-clicker-v1';
    
    let stats = JSON.parse(localStorage.getItem(appId + '-stats')) || {
        '🦋': 0, '🐇': 0, '🐦': 0, '🦊': 0, '🦌': 0, '⏳': 0
    };
    
    let highScore = localStorage.getItem(appId + '-highscore') || 0;

    // --- CONFIGURACIÓN DE LOGROS Y MAESTRÍAS ---
    const MASTERIES = [
        { name: 'Novato', color: '#888', min: 0 },
        { name: 'Bronce', color: '#cd7f32', min: 1 },
        { name: 'Plata', color: '#c0c0c0', min: 2 },
        { name: 'Oro', color: '#ffd700', min: 3 },
        { name: 'Maestro', color: '#e5e4e2', min: 4 }
    ];

    const ACHIEVEMENT_CONFIG = {
        '🦋': { name: 'Entomólogo', steps: [20, 50, 100, 250] },
        '🐇': { name: 'Velocista', steps: [15, 40, 80, 200] },
        '🐦': { name: 'Aviador', steps: [10, 30, 60, 150] },
        '🦊': { name: 'Astuto', steps: [5, 20, 50, 120] },
        '🦌': { name: 'Majestuoso', steps: [5, 15, 40, 100] },
        '⏳': { name: 'Crononauta', steps: [10, 25, 50, 100] }
    };

    // --- AUDIO ---
    const audioCtx = new (window.AudioContext || window.webkitAudioContext)();
    const masterGain = audioCtx.createGain();
    masterGain.connect(audioCtx.destination);
    
    let musicInterval = null;
    let currentMusicType = null;
    let isMuted = false;

    function playSound(freq, type, duration, vol = 0.1) {
        if (audioCtx.state === 'suspended') audioCtx.resume();
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = type;
        osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
        gain.gain.setValueAtTime(vol, audioCtx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + duration);
        osc.connect(gain);
        gain.connect(masterGain);
        osc.start();
        osc.stop(audioCtx.currentTime + duration);
    }

    function toggleMute() {
        isMuted = !isMuted;
        masterGain.gain.setValueAtTime(isMuted ? 0 : 1, audioCtx.currentTime);
        document.getElementById('mute-btn').innerText = isMuted ? '🔇' : '🔊';
    }

    document.getElementById('mute-btn').onclick = (e) => { e.stopPropagation(); toggleMute(); };

    function updateMusic(type) {
        if (currentMusicType === type) return;
        currentMusicType = type;
        if (musicInterval) clearInterval(musicInterval);

        if (type === 'menu') {
            const menuNotes = [329.63, 0, 392.00, 0, 440.00, 0, 392.00, 0]; 
            let step = 0;
            musicInterval = setInterval(() => {
                if (gameActive) return;
                if (menuNotes[step % menuNotes.length] > 0) playSound(menuNotes[step % menuNotes.length], 'triangle', 0.8, 0.03);
                step++;
            }, 600);
        } else if (type === 'game') {
            const gameNotes = [261.63, 261.63, 392.00, 392.00, 440.00, 440.00, 392.00, 0, 349.23, 349.23, 329.63, 329.63, 293.66, 293.66, 261.63, 0];
            let step = 0;
            musicInterval = setInterval(() => {
                if (!gameActive) return;
                const freq = gameNotes[step % gameNotes.length];
                if (freq > 0) {
                    playSound(freq, 'square', 0.2, 0.03);
                    if (step % 2 === 0) playSound(freq / 2, 'sine', 0.2, 0.05);
                }
                if (step % 4 === 0) playSound(50, 'sawtooth', 0.05, 0.04);
                step++;
            }, 150);
        }
    }

    // --- LÓGICA DEL JUEGO ---
    const container = document.getElementById('game-container');
    const cloudsContainer = document.getElementById('clouds-container');
    const flowersContainer = document.getElementById('flowers-container');
    const scoreEl = document.getElementById('score');
    const highScoreUI = document.getElementById('high-score-ui');
    const timerEl = document.getElementById('timer');
    const overlay = document.getElementById('overlay');

    let score = 0;
    let timeLeft = 30;
    let gameActive = false;
    let gameInterval;
    let spawnInterval;
    let sessionCaptures = { '🦋': 0, '🐇': 0, '🐦': 0, '🦊': 0, '🦌': 0, '⏳': 0 };

    highScoreUI.innerText = highScore;

    function createEnvironment() {
        cloudsContainer.innerHTML = '';
        flowersContainer.innerHTML = '';
        for(let i=0; i<5; i++) {
            const cloud = document.createElement('div');
            cloud.className = 'cloud';
            cloud.style.width = (Math.random() * 150 + 100) + 'px';
            cloud.style.height = (Math.random() * 40 + 30) + 'px';
            cloud.style.top = (Math.random() * 40) + '%';
            cloud.style.animationDuration = (Math.random() * 20 + 20) + 's';
            cloud.style.animationDelay = (Math.random() * -20) + 's';
            cloudsContainer.appendChild(cloud);
        }
        for(let i=0; i<40; i++) {
            const flower = document.createElement('div');
            flower.className = 'flower';
            flower.style.left = Math.random() * 100 + '%';
            flower.style.top = Math.random() * 100 + '%';
            flower.style.backgroundColor = ['#fff', '#ffeb3b', '#f48fb1', '#ce93d8'][Math.floor(Math.random()*4)];
            flowersContainer.appendChild(flower);
        }
    }
    createEnvironment();

    const ANIMAL_TYPES = [
        { emoji: '🦋', points: 10, speed: 2.2, clicks: 1, chance: 0.35, type: 'animal' },
        { emoji: '🐇', points: 25, speed: 3.8, clicks: 1, chance: 0.25, type: 'animal' },
        { emoji: '🐦', points: 50, speed: 5.8, clicks: 1, chance: 0.2, type: 'animal' },
        { emoji: '🦊', points: 100, speed: 7.8, clicks: 2, chance: 0.1, type: 'animal' },
        { emoji: '🦌', points: 250, speed: 10, clicks: 3, chance: 0.05, type: 'animal' },
        { emoji: '⏳', points: 0, speed: 3.5, clicks: 1, chance: 0.08, type: 'item' } 
    ];

    function showMainMenu() {
        gameActive = false;
        updateMusic('menu');
        overlay.style.display = 'flex';
        
        let achievementsHTML = Object.entries(ACHIEVEMENT_CONFIG).map(([id, config]) => {
            const total = stats[id] || 0;
            let level = 0;
            for(let i=0; i < config.steps.length; i++) {
                if(total >= config.steps[i]) level = i + 1;
            }
            
            const nextGoal = level < config.steps.length ? config.steps[level] : config.steps[config.steps.length - 1];
            const prevGoal = level > 0 ? config.steps[level - 1] : 0;
            
            // Progreso relativo al nivel actual
            const relativeTotal = total - prevGoal;
            const relativeGoal = nextGoal - prevGoal;
            const progress = level < config.steps.length ? Math.min(100, (relativeTotal / relativeGoal) * 100) : 100;
            
            const mastery = MASTERIES[level];

            return `
                <div class="achievement-card mastery-${level}">
                    <div class="flex justify-between items-start mb-1">
                        <div class="text-2xl">${id}</div>
                        <div class="text-[9px] font-bold px-1.5 py-0.5 rounded bg-white/10" style="color: ${mastery.color}">
                            ${mastery.name.toUpperCase()}
                        </div>
                    </div>
                    <div class="text-[10px] font-bold uppercase text-white/80">${config.name}</div>
                    <div class="text-[8px] mb-2 opacity-60">Lvl ${level} • Total: ${total}</div>
                    <div class="w-full bg-black/30 h-1.5 rounded-full overflow-hidden">
                        <div class="h-full transition-all" style="width: ${progress}%; background-color: ${mastery.color}"></div>
                    </div>
                    <div class="text-[8px] mt-1 text-right font-mono">
                        ${level < config.steps.length ? `${total}/${nextGoal}` : 'MÁXIMO'}
                    </div>
                </div>
            `;
        }).join('');

        overlay.innerHTML = `
            <h1 class="game-title">AnimalClick</h1>
            <p class="text-xl mb-2">¡Captura animales y mejora tus maestrías!</p>
            <div class="text-yellow-400 font-bold text-2xl mb-6">🏆 Récord: <span>${highScore}</span></div>
            
            <button id="start-btn" class="btn mb-10">¡JUGAR AHORA!</button>

            <div class="w-full max-w-xl">
                <h3 class="font-bold text-lg border-b border-white/20 pb-2 mb-4">🎖️ MAESTRÍAS FORESTALES</h3>
                <div class="achievement-grid">
                    ${achievementsHTML}
                </div>
            </div>
        `;
        
        document.getElementById('start-btn').onclick = () => {
            if (audioCtx.state === 'suspended') audioCtx.resume();
            startGame();
        };
    }

    function createEntity(forceItem = false) {
        if (!gameActive) return;
        let type;
        if (forceItem) {
            type = ANIMAL_TYPES.find(t => t.type === 'item');
        } else {
            let rand = Math.random();
            let cumulative = 0;
            type = ANIMAL_TYPES[0];
            for (const t of ANIMAL_TYPES) {
                cumulative += t.chance;
                if (rand < cumulative) { type = t; break; }
            }
        }

        const entity = document.createElement('div');
        entity.className = 'animal';
        let health = type.clicks;
        entity.innerHTML = `
            <div class="animal-emoji">${type.emoji}</div>
            <div class="health-bar" style="display: ${type.clicks > 1 ? 'block' : 'none'}">
                <div class="health-fill"></div>
            </div>
        `;

        const side = Math.floor(Math.random() * 4);
        let startX, startY, endX, endY;
        const pad = 120;
        if (side === 0) { startX = -pad; startY = Math.random() * window.innerHeight; endX = window.innerWidth + pad; endY = Math.random() * window.innerHeight; }
        else if (side === 1) { startX = window.innerWidth + pad; startY = Math.random() * window.innerHeight; endX = -pad; endY = Math.random() * window.innerHeight; }
        else if (side === 2) { startX = Math.random() * window.innerWidth; startY = -pad; endX = Math.random() * window.innerWidth; endY = window.innerHeight + pad; }
        else { startX = Math.random() * window.innerWidth; startY = window.innerHeight + pad; endX = Math.random() * window.innerWidth; endY = -pad; }

        entity.style.left = `${startX}px`;
        entity.style.top = `${startY}px`;
        container.appendChild(entity);

        if (type.type === 'item') {
            const clocksCaughtSession = sessionCaptures['⏳'];
            const effectiveSpeed = type.speed + (clocksCaughtSession * 0.4); 
            const duration = (10000 / effectiveSpeed) + (Math.random() * 1000);
            const startTime = performance.now();
            const amplitude = 50 + (clocksCaughtSession * 25); 
            const frequency = 0.005 + (clocksCaughtSession * 0.001);

            function updateClockPos(currentTime) {
                if (!gameActive || !entity.parentElement) return;
                const elapsed = currentTime - startTime;
                const progress = Math.min(elapsed / duration, 1);
                const curX = startX + (endX - startX) * progress;
                const curY = startY + (endY - startY) * progress;
                const angle = Math.atan2(endY - startY, endX - startX);
                const offset = Math.sin(elapsed * frequency) * amplitude * (1 - progress);
                const finalX = curX + Math.cos(angle + Math.PI/2) * offset;
                const finalY = curY + Math.sin(angle + Math.PI/2) * offset;
                entity.style.left = `${finalX}px`;
                entity.style.top = `${finalY}px`;
                if (progress < 1) requestAnimationFrame(updateClockPos);
                else entity.remove();
            }
            requestAnimationFrame(updateClockPos);
        } else {
            const duration = (10000 / type.speed) + (Math.random() * 1000);
            const animation = entity.animate([
                { left: `${startX}px`, top: `${startY}px` },
                { left: `${endX}px`, top: `${endY}px` }
            ], { duration, easing: 'linear' });
            animation.onfinish = () => entity.remove();
        }

        const handler = (e) => {
            e.preventDefault();
            if (!gameActive) return;
            health--;
            if (health > 0) {
                playSound(100, 'sawtooth', 0.1, 0.08);
                const fill = entity.querySelector('.health-fill');
                if (fill) fill.style.width = `${(health / type.clicks) * 100}%`;
                entity.classList.remove('shake');
                void entity.offsetWidth;
                entity.classList.add('shake');
                return;
            }
            
            sessionCaptures[type.emoji]++;
            if (type.type === 'item') {
                timeLeft += 5;
                timerEl.innerText = timeLeft;
                timerEl.classList.add('time-pulse');
                setTimeout(() => timerEl.classList.remove('time-pulse'), 500);
                playSound(1318, 'triangle', 0.5, 0.1);
            } else {
                score += type.points;
                scoreEl.innerText = score;
                playSound(600 + (Math.random() * 200), 'sine', 0.2, 0.1);
            }
            
            const float = document.createElement('div');
            float.className = type.type === 'item' ? 'time-float' : 'score-float';
            float.innerText = type.type === 'item' ? '+5s' : `+${type.points}`;
            float.style.left = `${entity.offsetLeft}px`;
            float.style.top = `${entity.offsetTop}px`;
            container.appendChild(float);
            setTimeout(() => float.remove(), 800);
            entity.remove();
        };
        entity.addEventListener('mousedown', handler);
        entity.addEventListener('touchstart', handler, {passive: false});
    }

    function startGame() {
        score = 0;
        timeLeft = 30;
        sessionCaptures = { '🦋': 0, '🐇': 0, '🐦': 0, '🦊': 0, '🦌': 0, '⏳': 0 };
        gameActive = true;
        scoreEl.innerText = score;
        timerEl.innerText = timeLeft;
        overlay.style.display = 'none';
        updateMusic('game');

        document.querySelectorAll('.animal').forEach(a => a.remove());

        spawnInterval = setInterval(() => {
            createEntity();
            if (score > 500 && Math.random() > 0.6) createEntity();
            if (timeLeft < 15 && Math.random() > 0.75) createEntity(true);
        }, 750);

        gameInterval = setInterval(() => {
            timeLeft--;
            timerEl.innerText = timeLeft;
            if (timeLeft <= 0) endGame();
        }, 1000);
    }

    function endGame() {
        gameActive = false;
        clearInterval(gameInterval);
        clearInterval(spawnInterval);
        
        Object.keys(sessionCaptures).forEach(key => {
            stats[key] = (stats[key] || 0) + sessionCaptures[key];
        });
        localStorage.setItem(appId + '-stats', JSON.stringify(stats));

        if (score > highScore) {
            highScore = score;
            localStorage.setItem(appId + '-highscore', highScore);
            highScoreUI.innerText = highScore;
        }

        overlay.innerHTML = `
            <h1 class="game-title">¡TIEMPO AGOTADO!</h1>
            <div class="text-4xl mb-4 font-bold text-yellow-300">${score} PUNTOS</div>
            
            <div class="bg-black/30 p-4 rounded-3xl mb-8 w-full max-w-sm border border-white/10">
                <h4 class="text-sm font-bold opacity-70 mb-3 uppercase tracking-widest">Resumen de captura</h4>
                <div class="grid grid-cols-3 gap-2">
                    ${Object.entries(sessionCaptures).map(([emoji, count]) => `
                        <div class="bg-white/5 rounded-xl p-2">
                            <span class="text-xl">${emoji}</span>
                            <div class="text-lg font-bold">${count}</div>
                        </div>
                    `).join('')}
                </div>
            </div>
            
            <div class="flex flex-col gap-4 w-full max-w-xs">
                <button id="restart-btn" class="btn w-full">REINTENTAR</button>
                <button id="main-menu-btn" class="btn btn-secondary w-full">MENU Y LOGROS</button>
            </div>
        `;
        overlay.style.display = 'flex';
        
        document.getElementById('restart-btn').onclick = () => startGame();
        document.getElementById('main-menu-btn').onclick = () => showMainMenu();
    }

    window.addEventListener('click', () => {
        if (audioCtx.state === 'suspended') audioCtx.resume();
        if (!gameActive && currentMusicType !== 'menu') updateMusic('menu');
    }, { once: false });

    showMainMenu();
</script>

</body>
</html>
