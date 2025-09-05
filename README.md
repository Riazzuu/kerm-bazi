<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بازی کرم</title>
    <style>
        @font-face {
            font-family: 'Vazir';
            src: url('https://cdn.fontcdn.ir/Font/Persian/Vazir/Vazir.eot');
            src: url('https://cdn.fontcdn.ir/Font/Persian/Vazir/Vazir.eot?#iefix') format('embedded-opentype'),
                 url('https://cdn.fontcdn.ir/Font/Persian/Vazir/Vazir.woff2') format('woff2'),
                 url('https://cdn.fontcdn.ir/Font/Persian/Vazir/Vazir.woff') format('woff'),
                 url('https://cdn.fontcdn.ir/Font/Persian/Vazir/Vazir.ttf') format('truetype');
            font-weight: normal;
            font-style: normal;
        }
        
        body {
            font-family: 'Vazir', sans-serif;
            direction: rtl;
            text-align: center;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            margin: 0;
            padding: 20px;
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            touch-action: manipulation;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            max-width: 900px;
            width: 100%;
        }
        
        .blog-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin: 0 auto 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            background: transparent;
        }
        
        .blog-icon img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .instruction {
            color: #ff6b6b;
            margin-bottom: 15px;
            font-size: 18px;
            font-weight: bold;
        }
        
        .score {
            font-size: 24px;
            color: #4ecdc4;
            font-weight: bold;
            margin-bottom: 15px;
        }
        
        .game-area {
            display: flex;
            justify-content: center;
            margin: 20px 0;
            position: relative;
        }
        
        .game-board-container {
            position: relative;
            width: 400px;
            height: 400px;
        }
        
        .game-board {
            position: absolute;
            width: 100%;
            height: 100%;
            border: 3px solid #ffd93d;
            border-radius: 15px;
            background-color: #f7f7f7;
            overflow: hidden;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
        }
        
        /* کنترل‌های لبه‌ای */
        .edge-control {
            position: absolute;
            background-color: rgba(78, 205, 196, 0.3);
            transition: background-color 0.3s;
            z-index: 20;
        }
        
        .edge-control:active {
            background-color: rgba(78, 205, 196, 0.6);
        }
        
        .edge-top {
            top: 0;
            left: 0;
            right: 0;
            height: 40px;
            cursor: pointer;
            border-top-left-radius: 12px;
            border-top-right-radius: 12px;
        }
        
        .edge-bottom {
            bottom: 0;
            left: 0;
            right: 0;
            height: 40px;
            cursor: pointer;
            border-bottom-left-radius: 12px;
            border-bottom-right-radius: 12px;
        }
        
        .edge-left {
            top: 40px;
            bottom: 40px;
            left: 0;
            width: 40px;
            cursor: pointer;
            border-top-left-radius: 12px;
            border-bottom-left-radius: 12px;
        }
        
        .edge-right {
            top: 40px;
            bottom: 40px;
            right: 0;
            width: 40px;
            cursor: pointer;
            border-top-right-radius: 12px;
            border-bottom-right-radius: 12px;
        }
        
        /* فلش‌های جهت‌نما */
        .arrow {
            position: absolute;
            font-size: 24px;
            color: #4ecdc4;
            font-weight: bold;
        }
        
        .arrow-up {
            top: 8px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .arrow-down {
            bottom: 8px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .arrow-left {
            left: 8px;
            top: 50%;
            transform: translateY(-50%);
        }
        
        .arrow-right {
            right: 8px;
            top: 50%;
            transform: translateY(-50%);
        }
        
        .worm {
            position: absolute;
            width: 20px;
            height: 20px;
            background: linear-gradient(45deg, #36d1dc, #5b86e5);
            border-radius: 50%;
            z-index: 10;
        }
        
        .worm-eye {
            position: absolute;
            width: 6px;
            height: 6px;
            background-color: black;
            border-radius: 50%;
            z-index: 11;
        }
        
        .worm-body {
            position: absolute;
            width: 18px;
            height: 18px;
            background: linear-gradient(45deg, #5b86e5, #36d1dc);
            border-radius: 50%;
        }
        
        .number {
            position: absolute;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-weight: bold;
            color: white;
            background: linear-gradient(45deg, #ff7e5f, #feb47b);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            font-size: 14px;
            z-index: 5;
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .control-btn {
            padding: 12px 25px;
            font-size: 16px;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            font-family: 'Vazir', sans-serif;
            transition: all 0.3s;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .start-btn {
            background: linear-gradient(45deg, #56ab2f, #a8e063);
            color: white;
        }
        
        .pause-btn {
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            color: white;
        }
        
        .speed-btn {
            background: linear-gradient(45deg, #4a00e0, #8e2de2);
            color: white;
        }
        
        .control-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            padding: 10px 0;
        }
        
        .custom-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            background: transparent;
        }
        
        .custom-icon:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
        }
        
        .custom-icon img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        @media (max-width: 768px) {
            .game-board-container {
                width: 300px;
                height: 300px;
            }
            
            .controls {
                flex-wrap: wrap;
            }
            
            .control-btn {
                padding: 10px 20px;
                font-size: 14px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <a href="https://riazzuu.blogfa.com/" class="blog-icon" target="_blank" title="وبلاگ">
            <img src="https://raw.githubusercontent.com/Riazzuu/logo/main/Riazzuu.jpg" alt="وبلاگ">
        </a>
        
        <div class="instruction">اگر زوج‌ها را بخوری بزرگ می‌شوی کرمعلی!</div>
        
        <div class="score">امتیاز: <span id="score">0</span></div>
        
        <div class="game-area">
            <div class="game-board-container">
                <div class="game-board" id="gameBoard"></div>
                
                <!-- کنترل‌های لبه‌ای -->
                <div class="edge-control edge-top" ontouchstart="handleDirection('up')" onclick="handleDirection('up')">
                    <div class="arrow arrow-up">↑</div>
                </div>
                <div class="edge-control edge-bottom" ontouchstart="handleDirection('down')" onclick="handleDirection('down')">
                    <div class="arrow arrow-down">↓</div>
                </div>
                <div class="edge-control edge-left" ontouchstart="handleDirection('left')" onclick="handleDirection('left')">
                    <div class="arrow arrow-left">←</div>
                </div>
                <div class="edge-control edge-right" ontouchstart="handleDirection('right')" onclick="handleDirection('right')">
                    <div class="arrow arrow-right">→</div>
                </div>
            </div>
        </div>
        
        <div class="controls">
            <button class="control-btn start-btn" id="startBtn">شروع بازی</button>
            <button class="control-btn pause-btn" id="pauseBtn">توقف</button>
            <button class="control-btn speed-btn" ontouchstart="increaseSpeed()" ontouchend="resetSpeed()" onmousedown="increaseSpeed()" onmouseup="resetSpeed()">شتاب</button>
        </div>
        
        <div class="social-icons">
            <a href="https://www.aparat.com/Riazzuu" class="custom-icon" target="_blank" title="آپارات">
                <img src="https://raw.githubusercontent.com/Riazzuu/logo/main/Aparat.jpg" alt="آپارات">
            </a>
            <a href="https://www.instagram.com/Riazzuu/" class="custom-icon" target="_blank" title="اینستاگرام">
                <img src="https://raw.githubusercontent.com/Riazzuu/logo/main/Instagram.jpg" alt="اینستاگرام">
            </a>
            <a href="https://www.youtube.com/@Riazzuu" class="custom-icon" target="_blank" title="یوتیوب">
                <img src="https://raw.githubusercontent.com/Riazzuu/logo/main/youtube.jpg" alt="یوتیوب">
            </a>
        </div>
    </div>

    <script>
        // متغیرهای بازی
        let gameBoard = document.getElementById('gameBoard');
        let scoreDisplay = document.getElementById('score');
        let startBtn = document.getElementById('startBtn');
        let pauseBtn = document.getElementById('pauseBtn');
        
        let gameInterval;
        let worm = [];
        let direction = 'right';
        let score = 0;
        let numbers = [];
        let gameRunning = false;
        let wormSize = 3;
        let gameSpeed = 100;
        let isSpeedBoost = false;
        let numberTimer;
        let numbersGenerated = 0;
        let wormColors = [
            'linear-gradient(45deg, #36d1dc, #5b86e5)',
            'linear-gradient(45deg, #ff5e62, #ff9966)',
            'linear-gradient(45deg, #11998e, #38ef7d)',
            'linear-gradient(45deg, #a8ff78, #78ffd6)',
            'linear-gradient(45deg, #f46b45, #eea849)'
        ];
        let currentColorIndex = 0;
        
        // ابعاد صفحه بازی
        const boardWidth = 400;
        const boardHeight = 400;
        
        // ایجاد کرم اولیه
        function createWorm() {
            // حذف کرم موجود اگر وجود دارد
            worm.forEach(segment => {
                if (segment.parentNode) {
                    segment.parentNode.removeChild(segment);
                }
            });
            
            worm = [];
            
            // ایجاد سر کرم
            let head = document.createElement('div');
            head.className = 'worm';
            head.style.left = '190px';
            head.style.top = '190px';
            head.style.background = wormColors[currentColorIndex];
            gameBoard.appendChild(head);
            worm.push(head);
            
            // اضافه کردن چشم‌ها به سر کرم
            let leftEye = document.createElement('div');
            leftEye.className = 'worm-eye';
            leftEye.style.left = '5px';
            leftEye.style.top = '5px';
            head.appendChild(leftEye);
            
            let rightEye = document.createElement('div');
            rightEye.className = 'worm-eye';
            rightEye.style.left = '5px';
            rightEye.style.top = '12px';
            head.appendChild(rightEye);
            
            // ایجاد بدنه کرم
            for (let i = 1; i < wormSize; i++) {
                addWormSegment();
            }
        }
        
        // اضافه کردن بخش جدید به کرم
        function addWormSegment() {
            let lastSegment = worm[worm.length - 1];
            let segment = document.createElement('div');
            segment.className = 'worm-body';
            segment.style.background = wormColors[currentColorIndex];
            
            // قرار دادن بخش جدید در موقعیت بخش قبلی
            segment.style.left = lastSegment.style.left;
            segment.style.top = lastSegment.style.top;
            
            gameBoard.appendChild(segment);
            worm.push(segment);
            
            // تغییر رنگ کرم پس از هر 5 واحد دراز شدن
            if (wormSize % 5 === 0) {
                currentColorIndex = (currentColorIndex + 1) % wormColors.length;
                updateWormColor();
            }
        }
        
        // به‌روزرسانی رنگ کرم
        function updateWormColor() {
            worm.forEach(segment => {
                segment.style.background = wormColors[currentColorIndex];
            });
        }
        
        // حرکت کرم
        function moveWorm() {
            if (!gameRunning) return;
            
            // ذخیره موقعیت قبلی سر کرم
            let head = worm[0];
            let headX = parseInt(head.style.left || 0);
            let headY = parseInt(head.style.top || 0);
            
            // حرکت بخش‌های بدن کرم
            for (let i = worm.length - 1; i > 0; i--) {
                let segment = worm[i];
                let prevSegment = worm[i - 1];
                
                segment.style.left = prevSegment.style.left;
                segment.style.top = prevSegment.style.top;
            }
            
            // حرکت سر کرم بر اساس جهت
            let speed = isSpeedBoost ? 8 : 5;
            
            switch(direction) {
                case 'up':
                    head.style.top = (headY - speed) + 'px';
                    break;
                case 'down':
                    head.style.top = (headY + speed) + 'px';
                    break;
                case 'left':
                    head.style.left = (headX - speed) + 'px';
                    break;
                case 'right':
                    head.style.left = (headX + speed) + 'px';
                    break;
            }
            
            // بررسی برخورد با دیوارها
            checkWallCollision();
            
            // بررسی برخورد با اعداد
            checkNumberCollision();
        }
        
        // بررسی برخورد با دیوارها
        function checkWallCollision() {
            let head = worm[0];
            let headX = parseInt(head.style.left);
            let headY = parseInt(head.style.top);
            
            if (headX < 0 || headX > boardWidth - 20 || headY < 0 || headY > boardHeight - 20) {
                gameOver();
            }
        }
        
        // بررسی برخورد با اعداد
        function checkNumberCollision() {
            let head = worm[0];
            let headX = parseInt(head.style.left);
            let headY = parseInt(head.style.top);
            
            for (let i = 0; i < numbers.length; i++) {
                let number = numbers[i];
                let numX = parseInt(number.style.left);
                let numY = parseInt(number.style.top);
                
                // بررسی برخورد
                if (Math.abs(headX - numX) < 20 && Math.abs(headY - numY) < 20) {
                    let numValue = parseInt(number.textContent);
                    
                    // حذف عدد خورده شده
                    gameBoard.removeChild(number);
                    numbers.splice(i, 1);
                    
                    // بررسی زوج یا فرد بودن عدد
                    if (numValue === 0) {
                        // عدد صفر - هیچ تغییری در اندازه کرم ایجاد نمی‌کند
                        score += 5;
                        playSuccessSound();
                    } else if (numValue % 2 === 0) {
                        // عدد زوج - بزرگ شدن کرم
                        wormSize++;
                        addWormSegment();
                        score += numValue * 2;
                        playSuccessSound();
                    } else {
                        // عدد فرد - کوچک شدن کرم
                        if (wormSize > 1) {
                            let lastSegment = worm.pop();
                            gameBoard.removeChild(lastSegment);
                            wormSize--;
                        }
                        score += numValue;
                    }
                    
                    scoreDisplay.textContent = score;
                    
                    // ایجاد عدد جدید
                    createNumber();
                    break;
                }
            }
        }
        
        // پخش صدای تایید
        function playSuccessSound() {
            try {
                // ایجاد صدای تیک تایید
                const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                const oscillator = audioContext.createOscillator();
                const gainNode = audioContext.createGain();
                
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                
                oscillator.type = 'sine';
                oscillator.frequency.value = 1000;
                gainNode.gain.value = 0.3;
                
                oscillator.start();
                gainNode.gain.exponentialRampToValueAtTime(0.00001, audioContext.currentTime + 0.15);
                
                setTimeout(() => {
                    oscillator.stop();
                }, 150);
            } catch (e) {
                console.log('خطا در پخش صدا:', e);
            }
        }
        
        // ایجاد عدد جدید
        function createNumber() {
            // اگر بیش از 3 عدد وجود دارد، ابتدا اعداد فرد را برای حذف بررسی کن
            if (numbers.length >= 3) {
                let oddNumberIndex = -1;
                
                // پیدا کردن اولین عدد فرد برای حذف
                for (let i = 0; i < numbers.length; i++) {
                    let numValue = parseInt(numbers[i].textContent);
                    if (numValue % 2 !== 0 && numValue !== 0) {
                        oddNumberIndex = i;
                        break;
                    }
                }
                
                // اگر عدد فرد پیدا شد، آن را حذف کن
                if (oddNumberIndex !== -1) {
                    let numberToRemove = numbers[oddNumberIndex];
                    if (numberToRemove.parentNode) {
                        gameBoard.removeChild(numberToRemove);
                    }
                    numbers.splice(oddNumberIndex, 1);
                } else {
                    // اگر عدد فردی وجود نداشت، قدیمی‌ترین عدد را حذف کن
                    let oldestNumber = numbers.shift();
                    if (oldestNumber.parentNode) {
                        gameBoard.removeChild(oldestNumber);
                    }
                }
            }
            
            // ایجاد عدد جدید
            let number = document.createElement('div');
            let numValue;
            
            // بعد از 10 عدد تولید شده، عدد صفر را نمایش بده
            if (numbersGenerated > 0 && numbersGenerated % 10 === 0) {
                numValue = 0;
            } else {
                numValue = Math.floor(Math.random() * 20) + 1; // عدد بین 1 تا 20
            }
            
            numbersGenerated++;
            
            number.className = 'number';
            number.textContent = numValue;
            
            // قرار دادن عدد در موقعیت تصادفی
            let posX = Math.floor(Math.random() * (boardWidth - 40));
            let posY = Math.floor(Math.random() * (boardHeight - 40));
            
            number.style.left = posX + 'px';
            number.style.top = posY + 'px';
            
            gameBoard.appendChild(number);
            numbers.push(number);
        }
        
        // شروع ایجاد اعداد به صورت دوره‌ای
        function startNumberGeneration() {
            clearInterval(numberTimer);
            // ایجاد عدد جدید هر 2 ثانیه
            numberTimer = setInterval(createNumber, 2000);
        }
        
        // توقف ایجاد اعداد
        function stopNumberGeneration() {
            clearInterval(numberTimer);
        }
        
        // تغییر جهت کرم
        function changeDirection(newDirection) {
            // جلوگیری از تغییر جهت به مسیر مخالف
            if (
                (direction === 'up' && newDirection === 'down') ||
                (direction === 'down' && newDirection === 'up') ||
                (direction === 'left' && newDirection === 'right') ||
                (direction === 'right' && newDirection === 'left')
            ) {
                return;
            }
            
            direction = newDirection;
        }
        
        // مدیریت جهت‌ها (ادامه بازی اگر متوقف شده)
        function handleDirection(newDirection) {
            if (!gameRunning) {
                resumeGame();
            }
            changeDirection(newDirection);
        }
        
        // افزایش سرعت با دکمه شتاب
        function increaseSpeed() {
            isSpeedBoost = true;
        }
        
        // بازگشت به سرعت عادی
        function resetSpeed() {
            isSpeedBoost = false;
        }
        
        // شروع بازی
        function startGame() {
            if (gameRunning) {
                resetGame();
                return;
            }
            
            gameRunning = true;
            resetGame();
            
            gameInterval = setInterval(() => {
                moveWorm();
            }, gameSpeed);
            
            // شروع ایجاد اعداد
            startNumberGeneration();
            
            startBtn.textContent = 'شروع مجدد';
            pauseBtn.textContent = 'توقف';
        }
        
        // توقف بازی
        function pauseGame() {
            if (!gameRunning) return;
            
            gameRunning = false;
            clearInterval(gameInterval);
            stopNumberGeneration();
            pauseBtn.textContent = 'ادامه';
        }
        
        // ادامه بازی
        function resumeGame() {
            if (gameRunning) return;
            
            gameRunning = true;
            gameInterval = setInterval(() => {
                moveWorm();
            }, gameSpeed);
            
            // شروع ایجاد اعداد
            startNumberGeneration();
            
            pauseBtn.textContent = 'توقف';
        }
        
        // بازی تمام شد
        function gameOver() {
            gameRunning = false;
            clearInterval(gameInterval);
            stopNumberGeneration();
            alert(`بازی تمام شد! امتیاز شما: ${score}`);
        }
        
        // ریست کردن بازی
        function resetGame() {
            // پاک کردن صفحه بازی
            while (gameBoard.firstChild) {
                gameBoard.removeChild(gameBoard.firstChild);
            }
            
            // ریست کردن متغیرها
            worm = [];
            numbers = [];
            score = 0;
            wormSize = 3;
            direction = 'right';
            numbersGenerated = 0;
            currentColorIndex = 0;
            
            scoreDisplay.textContent = '0';
            
            // ایجاد کرم و اعداد جدید
            createWorm();
            createNumber();
            createNumber();
        }
        
        // رویدادهای کلیک بر دکمه‌ها
        startBtn.addEventListener('click', startGame);
        pauseBtn.addEventListener('click', function() {
            if (gameRunning) {
                pauseGame();
            } else {
                resumeGame();
            }
        });
        
        // کنترل با صفحه کلید
        document.addEventListener('keydown', (e) => {
            if (!gameRunning) {
                resumeGame();
            }
            
            switch(e.key) {
                case 'ArrowUp':
                    changeDirection('up');
                    break;
                case 'ArrowDown':
                    changeDirection('down');
                    break;
                case 'ArrowLeft':
                    changeDirection('left');
                    break;
                case 'ArrowRight':
                    changeDirection('right');
                    break;
            }
        });
        
        // مقداردهی اولیه
        createWorm();
        createNumber();
        createNumber();
    </script>
</body>
</html>
