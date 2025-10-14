<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammed Yazeen M M - Full Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #1a1f2e 100%);
            color: #e5e7eb;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        header {
            text-align: center;
            margin-bottom: 60px;
            animation: fadeIn 0.8s ease-in;
        }

        h1 {
            font-size: 3em;
            color: #6366f1;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .subtitle {
            font-size: 1.3em;
            color: #f59e0b;
            margin-bottom: 20px;
            letter-spacing: 1px;
        }

        .tagline {
            font-size: 1.1em;
            color: #a8afc4;
            font-style: italic;
            margin-bottom: 30px;
        }

        section {
            margin-bottom: 50px;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            border-left: 4px solid #6366f1;
            animation: slideIn 0.6s ease-in;
        }

        section h2 {
            font-size: 2em;
            color: #6366f1;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        section h2::before {
            content: '';
            width: 8px;
            height: 8px;
            background: #f59e0b;
            border-radius: 50%;
            display: inline-block;
        }

        .about-content {
            font-size: 1.1em;
            color: #d1d5db;
            line-height: 1.8;
            padding: 15px 0;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .tech-item {
            text-align: center;
            padding: 20px;
            background: rgba(99, 102, 241, 0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
            border: 1px solid rgba(99, 102, 241, 0.3);
        }

        .tech-item:hover {
            background: rgba(99, 102, 241, 0.2);
            transform: translateY(-5px);
            border-color: #f59e0b;
        }

        .tech-item img {
            width: 50px;
            height: 50px;
            margin-bottom: 10px;
        }

        .tech-item p {
            font-weight: 600;
            color: #e5e7eb;
            font-size: 0.95em;
        }

        .focus-box {
            background: rgba(245, 158, 11, 0.1);
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid #f59e0b;
            margin: 20px 0;
        }

        .focus-box h3 {
            color: #f59e0b;
            margin-bottom: 12px;
            font-size: 1.2em;
        }

        .focus-item {
            margin-bottom: 12px;
            color: #d1d5db;
            display: flex;
            align-items: flex-start;
            gap: 10px;
        }

        .focus-item::before {
            content: '✓';
            color: #f59e0b;
            font-weight: bold;
            flex-shrink: 0;
        }

        .connect-section {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .contact-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 24px;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            color: white;
            text-decoration: none;
            border-radius: 8px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(99, 102, 241, 0.4);
            border-color: #f59e0b;
        }

        .contact-btn.email {
            background: linear-gradient(135deg, #ea4335 0%, #fbbc04 100%);
        }

        .contact-btn.linkedin {
            background: linear-gradient(135deg, #0077b5 0%, #00a8e1 100%);
        }

        .contact-btn.github {
            background: linear-gradient(135deg, #333 0%, #555 100%);
        }

        .highlights {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .highlight-card {
            background: rgba(99, 102, 241, 0.1);
            padding: 20px;
            border-radius: 10px;
            border: 1px solid rgba(99, 102, 241, 0.3);
            transition: all 0.3s ease;
        }

        .highlight-card:hover {
            border-color: #f59e0b;
            background: rgba(245, 158, 11, 0.1);
        }

        .highlight-card h4 {
            color: #6366f1;
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        .highlight-card p {
            color: #d1d5db;
            font-size: 0.95em;
            line-height: 1.6;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .stat-card {
            background: rgba(245, 158, 11, 0.1);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid rgba(245, 158, 11, 0.3);
        }

        .stat-number {
            font-size: 2.5em;
            color: #f59e0b;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .stat-label {
            color: #a8afc4;
            font-size: 0.95em;
        }

        .snake-animation {
            width: 100%;
            max-width: 800px;
            margin: 40px auto;
            padding: 20px;
            background: rgba(99, 102, 241, 0.1);
            border-radius: 12px;
            border: 1px solid rgba(99, 102, 241, 0.3);
        }

        .snake-animation h3 {
            text-align: center;
            color: #6366f1;
            margin-bottom: 20px;
            font-size: 1.2em;
        }

        canvas {
            display: block;
            width: 100%;
            background: #0d1117;
            border-radius: 8px;
            margin-top: 15px;
        }

        footer {
            text-align: center;
            padding: 20px;
            color: #6b7280;
            margin-top: 40px;
            border-top: 1px solid rgba(99, 102, 241, 0.2);
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }
            
            section {
                padding: 20px;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <h1>Muhammed Yazeen M M</h1>
            <p class="subtitle">Full Stack Developer | AI & ML Enthusiast | UI/UX Designer</p>
            <p class="tagline">Crafting intelligent, user-focused solutions through innovative technology</p>
        </header>

        <!-- About Section -->
        <section>
            <h2>About Me</h2>
            <div class="about-content">
                <p>I'm a Computer Science undergraduate at Ilahia College of Engineering with hands-on experience in cross-platform app development, API integration, and AI implementation. I have a proven ability to lead in collaborative projects, internships, and hackathons, delivering user-focused solutions that enhance functionality and user experience.</p>
                <p style="margin-top: 15px;">I'm passionate about building intelligent applications that solve real-world problems by combining modern development practices with cutting-edge AI technologies.</p>
            </div>
        </section>

        <!-- Snake Animation -->
        <div class="snake-animation">
            <h3>🐍 GitHub Contribution Visualization</h3>
            <canvas id="snakeCanvas"></canvas>
        </div>

        <!-- Current Focus & Achievements -->
        <section>
            <h2>Current Focus & Achievements</h2>
            
            <div class="focus-box">
                <h3>🎯 Primary Focus</h3>
                <p style="color: #d1d5db;">Building AI-powered mobile applications with Flutter & Firebase</p>
            </div>

            <div class="highlights">
                <div class="highlight-card">
                    <h4>📱 Application Development</h4>
                    <p>Internship at Genzee Technologies with experience developing production-ready mobile applications</p>
                </div>
                <div class="highlight-card">
                    <h4>🤖 AI Integration</h4>
                    <p>Integrated LLaMA AI for personalized learning experiences in mobile applications</p>
                </div>
                <div class="highlight-card">
                    <h4>⚙️ Full Stack Development</h4>
                    <p>Experience with cross-platform development, backend services, and modern UI/UX design</p>
                </div>
            </div>

            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">2+</div>
                    <div class="stat-label">Production Apps</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">5+</div>
                    <div class="stat-label">Programming Languages</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">10+</div>
                    <div class="stat-label">Technologies & Tools</div>
                </div>
            </div>
        </section>

        <!-- Tech Stack -->
        <section>
            <h2>Technical Skills</h2>
            
            <h3 style="color: #6366f1; margin-top: 20px; margin-bottom: 15px;">Mobile Development</h3>
            <div class="tech-grid">
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg" alt="Flutter">
                    <p>Flutter</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg" alt="Dart">
                    <p>Dart</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/android/android-original.svg" alt="Android">
                    <p>Android</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apple/apple-original.svg" alt="iOS">
                    <p>iOS</p>
                </div>
            </div>

            <h3 style="color: #6366f1; margin-top: 30px; margin-bottom: 15px;">Programming Languages</h3>
            <div class="tech-grid">
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python">
                    <p>Python</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java">
                    <p>Java</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" alt="C">
                    <p>C</p>
                </div>
            </div>

            <h3 style="color: #6366f1; margin-top: 30px; margin-bottom: 15px;">Backend & Database</h3>
            <div class="tech-grid">
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" alt="Firebase">
                    <p>Firebase</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL">
                    <p>MySQL</p>
                </div>
            </div>

            <h3 style="color: #6366f1; margin-top: 30px; margin-bottom: 15px;">Design & Tools</h3>
            <div class="tech-grid">
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" alt="Figma">
                    <p>Figma</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/xd/xd-plain.svg" alt="Adobe XD">
                    <p>Adobe XD</p>
                </div>
                <div class="tech-item">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git">
                    <p>Git</p>
                </div>
            </div>
        </section>




            <p>© 2025 Muhammed Yazeen M M. All rights reserved. | Based in Kanayannur, Kerala</p>
        </footer>
    </div>

    <script>
        // Snake Animation - GitHub Contribution Visualization
        const canvas = document.getElementById('snakeCanvas');
        const ctx = canvas.getContext('2d');

        // Set canvas size
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.offsetWidth - 40;
            canvas.height = 300;
        }
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);

        // Snake game variables
        const gridSize = 20;
        const tileCount = Math.floor(canvas.width / gridSize);
        let snake = [{x: Math.floor(tileCount / 2), y: Math.floor(canvas.height / gridSize / 2)}];
        let food = {x: Math.floor(Math.random() * tileCount), y: Math.floor(Math.random() * (canvas.height / gridSize))};
        let dx = 1;
        let dy = 0;
        let nextDx = 1;
        let nextDy = 0;
        let score = 0;
        let gameSpeed = 8;
        let frameCount = 0;

        // Contribution grid (GitHub-style)
        const weeks = 52;
        const daysPerWeek = 7;
        const contributionData = [];

        // Generate random contribution data
        for (let w = 0; w < weeks; w++) {
            for (let d = 0; d < daysPerWeek; d++) {
                contributionData.push(Math.random() > 0.6 ? 1 : 0);
            }
        }

        // Draw contribution grid behind snake
        function drawContributionGrid() {
            const cellSize = 12;
            const padding = 15;
            let index = 0;

            for (let w = 0; w < weeks; w++) {
                for (let d = 0; d < daysPerWeek; d++) {
                    const x = padding + w * (cellSize + 3);
                    const y = padding + d * (cellSize + 3);
                    
                    if (contributionData[index]) {
                        ctx.fillStyle = 'rgba(99, 102, 241, 0.3)';
                    } else {
                        ctx.fillStyle = 'rgba(99, 102, 241, 0.1)';
                    }
                    
                    ctx.fillRect(x, y, cellSize, cellSize);
                    ctx.strokeStyle = 'rgba(99, 102, 241, 0.2)';
                    ctx.lineWidth = 0.5;
                    ctx.strokeRect(x, y, cellSize, cellSize);
                    
                    index++;
                }
            }
        }

        // Draw snake
        function drawSnake() {
            snake.forEach((segment, index) => {
                const x = segment.x * gridSize;
                const y = segment.y * gridSize;

                if (index === 0) {
                    // Snake head
                    ctx.fillStyle = '#f59e0b';
                    ctx.shadowColor = 'rgba(245, 158, 11, 0.8)';
                    ctx.shadowBlur = 10;
                } else {
                    // Snake body with gradient
                    const gradient = ctx.createLinearGradient(x, y, x + gridSize, y + gridSize);
                    gradient.addColorStop(0, '#6366f1');
                    gradient.addColorStop(1, '#8b5cf6');
                    ctx.fillStyle = gradient;
                    ctx.shadowColor = 'rgba(99, 102, 241, 0.4)';
                    ctx.shadowBlur = 5;
                }

                ctx.fillRect(x + 2, y + 2, gridSize - 4, gridSize - 4);
                ctx.shadowColor = 'transparent';
            });
        }

        // Draw food
        function drawFood() {
            const x = food.x * gridSize;
            const y = food.y * gridSize;
            
            ctx.fillStyle = '#10b981';
            ctx.shadowColor = 'rgba(16, 185, 129, 0.8)';
            ctx.shadowBlur = 10;
            ctx.beginPath();
            ctx.arc(x + gridSize / 2, y + gridSize / 2, gridSize / 2 - 2, 0, Math.PI * 2);
            ctx.fill();
            ctx.shadowColor = 'transparent';
        }

        // Draw score
        function drawScore() {
            ctx.fillStyle = '#e5e7eb';
            ctx.font = 'bold 16px Segoe UI';
            ctx.fillText('Score: ' + score, 15, canvas.height - 15);
        }

        // Update game
        function update() {
            dx = nextDx;
            dy = nextDy;

            const head = {x: snake[0].x + dx, y: snake[0].y + dy};

            // Wrap around edges
            head.x = (head.x + tileCount) % tileCount;
            head.y = (head.y + Math.floor(canvas.height / gridSize)) % Math.floor(canvas.height / gridSize);

            // Check collision with self
            for (let segment of snake) {
                if (head.x === segment.x && head.y === segment.y) {
                    snake = [{x: Math.floor(tileCount / 2), y: Math.floor(canvas.height / gridSize / 2)}];
                    score = 0;
                    return;
                }
            }

            snake.unshift(head);

            // Check if food eaten
            if (head.x === food.x && head.y === food.y) {
                score += 10;
                gameSpeed = Math.min(gameSpeed + 0.5, 15);
                food = {x: Math.floor(Math.random() * tileCount), y: Math.floor(Math.random() * Math.floor(canvas.height / gridSize))};
            } else {
                snake.pop();
            }
        }

        // Handle keyboard input
        document.addEventListener('keydown', (e) => {
            switch(e.key) {
                case 'ArrowUp':
                    if (dy === 0) { nextDx = 0; nextDy = -1; }
                    e.preventDefault();
                    break;
                case 'ArrowDown':
                    if (dy === 0) { nextDx = 0; nextDy = 1; }
                    e.preventDefault();
                    break;
                case 'ArrowLeft':
                    if (dx === 0) { nextDx = -1; nextDy = 0; }
                    e.preventDefault();
                    break;
                case 'ArrowRight':
                    if (dx === 0) { nextDx = 1; nextDy = 0; }
                    e.preventDefault();
                    break;
            }
        });

        // Game loop
        function gameLoop() {
            ctx.fillStyle = 'rgba(13, 17, 23, 0.8)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            drawContributionGrid();

            frameCount++;
            if (frameCount >= Math.floor(18 / gameSpeed)) {
                update();
                frameCount = 0;
            }

            drawSnake();
            drawFood();
            drawScore();

            requestAnimationFrame(gameLoop);
        }

        gameLoop();
    </script>
</body>
</html>
