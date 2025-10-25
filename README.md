Muhammed Yazeen M M

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=300&size=24&duration=2500&pause=800&color=6366F1&center=true&vCenter=true&width=500&height=60&lines=Full+Stack+Developer;AI+%26+ML+Enthusiast;UI%2FUX+Designer" alt="Typing Animation" />
</div>

📊 GitHub Statistics

<div align="center">
  <img width="48%" src="https://github-readme-stats.vercel.app/api?username=mhmd-yazeen&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=6366f1&icon_color=f59e0b&text_color=e5e7eb&count_private=true&include_all_commits=true" alt="Muhammed Yazeen's GitHub Stats" />
  <img width="48%" src="https://github-readme-streak-stats.herokuapp.com/?user=mhmd-yazeen&theme=github-dark-blue&hide_border=true&background=0D1117&stroke=6366F1&ring=F59E0B&fire=F59E0B&currStreakLabel=E5E7EB" alt="Muhammed Yazeen's GitHub Streak" />
</div>

🐍 GitHub Contribution Graph

<div align="center">
  <img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" alt="GitHub Contribution Snake Animation" />
</div>

🎮 Play the Snake Game Below!

<details>
<summary><b>Click to Play Interactive Snake Game</b></summary>

<!DOCTYPE html>
<html>
<head>
<style>
  body { background: #0d1117; margin: 0; padding: 20px; display: flex; justify-content: center; align-items: center; min-height: 100vh; font-family: Arial; }
  canvas { border: 2px solid #6366f1; background: #0d1117; display: block; margin: 20px auto; }
  .container { text-align: center; background: rgba(99, 102, 241, 0.1); padding: 30px; border-radius: 12px; border: 1px solid rgba(99, 102, 241, 0.3); max-width: 600px; }
  h2 { color: #6366f1; }
  p { color: #d1d5db; }
  .controls { color: #a8afc4; font-size: 14px; margin-top: 15px; }
</style>
</head>
<body>
<div class="container">
  <h2>🐍 GitHub Contribution Snake</h2>
  <p>Use Arrow Keys to control the snake. Eat green squares to grow!</p>
  <canvas id="snakeCanvas" width="600" height="400"></canvas>
  <div class="controls">
    <p>⬆️ ⬇️ ⬅️ ➡️ = Move | Score increases as you play</p>
    <p>Colliding with yourself resets the game</p>
  </div>
</div>

<script>
  const canvas = document.getElementById('snakeCanvas');
  const ctx = canvas.getContext('2d');

  const gridSize = 20;
  const tileCount = canvas.width / gridSize;
  
  let snake = [{x: Math.floor(tileCount / 2), y: Math.floor(canvas.height / gridSize / 2)}];
  let food = {x: Math.floor(Math.random() * tileCount), y: Math.floor(Math.random() * (canvas.height / gridSize))};
  let dx = 1;
  let dy = 0;
  let nextDx = 1;
  let nextDy = 0;
  let score = 0;
  let gameSpeed = 8;
  let frameCount = 0;

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

  function update() {
    dx = nextDx;
    dy = nextDy;

    const head = {x: snake[0].x + dx, y: snake[0].y + dy};
    head.x = (head.x + tileCount) % tileCount;
    head.y = (head.y + Math.floor(canvas.height / gridSize)) % Math.floor(canvas.height / gridSize);

    for (let segment of snake) {
      if (head.x === segment.x && head.y === segment.y) {
        snake = [{x: Math.floor(tileCount / 2), y: Math.floor(canvas.height / gridSize / 2)}];
        score = 0;
        return;
      }
    }

    snake.unshift(head);

    if (head.x === food.x && head.y === food.y) {
      score += 10;
      gameSpeed = Math.min(gameSpeed + 0.5, 15);
      food = {x: Math.floor(Math.random() * tileCount), y: Math.floor(Math.random() * Math.floor(canvas.height / gridSize))};
    } else {
      snake.pop();
    }
  }

  function draw() {
    // Background with contribution grid pattern
    ctx.fillStyle = 'rgba(13, 17, 23, 0.9)';
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    // Draw grid pattern (like GitHub contributions)
    ctx.strokeStyle = 'rgba(99, 102, 241, 0.1)';
    ctx.lineWidth = 0.5;
    for (let i = 0; i <= tileCount; i++) {
      ctx.beginPath();
      ctx.moveTo(i * gridSize, 0);
      ctx.lineTo(i * gridSize, canvas.height);
      ctx.stroke();
    }
    for (let i = 0; i <= canvas.height / gridSize; i++) {
      ctx.beginPath();
      ctx.moveTo(0, i * gridSize);
      ctx.lineTo(canvas.width, i * gridSize);
      ctx.stroke();
    }

    // Draw snake
    snake.forEach((segment, index) => {
      const x = segment.x * gridSize;
      const y = segment.y * gridSize;

      if (index === 0) {
        ctx.fillStyle = '#f59e0b';
        ctx.shadowColor = 'rgba(245, 158, 11, 0.8)';
        ctx.shadowBlur = 10;
      } else {
        ctx.fillStyle = '#6366f1';
        ctx.shadowColor = 'rgba(99, 102, 241, 0.4)';
        ctx.shadowBlur = 5;
      }
      ctx.fillRect(x + 2, y + 2, gridSize - 4, gridSize - 4);
    });
    ctx.shadowColor = 'transparent';

    // Draw food
    ctx.fillStyle = '#10b981';
    ctx.shadowColor = 'rgba(16, 185, 129, 0.8)';
    ctx.shadowBlur = 10;
_    ctx.beginPath();
    ctx.arc(food.x * gridSize + gridSize / 2, food.y * gridSize + gridSize / 2, gridSize / 2 - 2, 0, Math.PI * 2);
    ctx.fill();
    ctx.shadowColor = 'transparent';

    // Draw score
    ctx.fillStyle = '#e5e7eb';
    ctx.font = 'bold 16px Arial';
    ctx.fillText('Score: ' + score, 15, canvas.height - 15);
  }

  function gameLoop() {
    frameCount++;
    if (frameCount >= Math.floor(18 / gameSpeed)) {
      update();
      frameCount = 0;
    }
    draw();
    requestAnimationFrame(gameLoop);
  }

  gameLoop();
</script>
</body>
</html>


How to add this to your GitHub README:

Copy the HTML code above

Save it as an .html file in your repository

Or embed it using GitHub Pages

For a live version:

Create a snake-game.html file in your repo

Enable GitHub Pages in your repository settings

Reference it: [Play Snake Game](https://yourusername.github.io/yourrepo/snake-game.html)

</details>

🧑‍💻 About Me

I'm a Computer Science undergraduate at Ilahia College of Engineering with hands-on experience in cross-platform app development, API integration, and AI implementation. I have a proven ability to lead in collaborative projects, internships, and hackathons, delivering user-focused solutions that improve functionality and experience.

Passionate about building intelligent applications that solve real-world problems by combining modern development practices with cutting-edge AI technologies.

🎯 Current Focus & Achievements

🔸 Primary Focus
   └─ Building AI-powered mobile applications with Flutter & Firebase

🔸 Experience
   ├─ Application Development Intern at Genzee Technologies
   ├─ Developed 2+ production-ready mobile apps
   ├─ Integrated LLaMA AI for personalized learning experiences
   └─ Led collaborative projects in hackathons and team environments

🔸 Key Skills
   ├─ Cross-platform mobile development (Flutter/Dart)
   ├─ AI integration and LLM implementation
   ├─ Backend services (Firebase, REST APIs)
   └─ UI/UX design (Figma, Adobe XD)


🧰 My Tech Stack

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg" width="40" height="40" alt="Flutter" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg" width="40" height="40" alt="Dart" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/android/android-original.svg" width="40" height="40" alt="Android" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apple/apple-original.svg" width="40" height="40" alt="iOS" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40" height="40" alt="Python" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="40" height="40" alt="Java" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" width="40" height="40" alt="C" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" width="40" height="40" alt="Firebase" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="40" height="40" alt="MySQL" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" width="40" height="40" alt="Figma" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/xd/xd-plain.svg" width="40" height="40" alt="Adobe XD" />
We  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40" alt="Git" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="40" height="40" alt="VS Code" />
</div>

📊 Top Languages

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mhmd-yazeen&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=6366f1&text_color=e5e7eb&card_width=500&langs_count=8" alt="Top Languages" />
</div>

🌟 Highlights

🚀 2+ Production Apps - Successfully developed and deployed multiple mobile applications

🤖 AI Integration - Implemented LLaMA AI for intelligent, personalized user experiences

💼 Professional Experience - Internship at Genzee Technologies focusing on full-stack development

🎨 UI/UX Design - Proficient in creating intuitive and engaging user interfaces

🔧 Full Stack Development - Experienced across frontend, backend, and database technologies

<div align="center">

</div>

📈 My Journey

I'm continuously learning and growing in the field of software development. My focus is on building scalable, AI-powered applications that make a real impact. I enjoy collaborating with talented developers and designers to create innovative solutions.

Currently exploring: Advanced AI/ML implementations, Cloud Architecture, and Modern App Development Patterns

<div align="center">

⭐ If you find my work interesting, feel free to star some of my repositories!

</div>
