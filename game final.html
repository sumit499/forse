<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Minimalist Racer</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      font-family: Arial, sans-serif;
      background: #111;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #gameCanvas {
      border: 2px solid white;
      background: #222;
    }
  </style>
</head>
<body>
  <canvas id="gameCanvas" width="400" height="600"></canvas>
  <script>
    // Canvas setup
    const canvas = document.getElementById("gameCanvas");
    const ctx = canvas.getContext("2d");

    // Game variables
    const player = {
      x: canvas.width / 2 - 15,
      y: canvas.height - 60,
      width: 30,
      height: 30,
      speed: 5 * 1.4 * 2, // Double the horizontal speed of the player
    };
    let obstacles = [];
    let gameSpeed = 1.5;  // Slow down the falling obstacles slightly
    let isGameOver = false;
    let score = 0;

    // Swipe detection
    let touchStartX = null;

    // Function to create obstacles
    function createObstacle() {
      const obstacleWidth = Math.random() * 50 + 30;
      const obstacleX = Math.random() * (canvas.width - obstacleWidth);
      obstacles.push({
        x: obstacleX,
        y: -20,
        width: obstacleWidth,
        height: 20,
      });
    }

    // Function to draw the player
    function drawPlayer() {
      ctx.fillStyle = "white";
      ctx.fillRect(player.x, player.y, player.width, player.height);
    }

    // Function to draw obstacles
    function drawObstacles() {
      ctx.fillStyle = "red";
      obstacles.forEach((obs) => {
        ctx.fillRect(obs.x, obs.y, obs.width, obs.height);
      });
    }

    // Update game state
    function updateGame() {
      if (isGameOver) return;

      // Move obstacles
      obstacles.forEach((obs) => {
        obs.y += gameSpeed; // Obstacles move slower with reduced speed
      });

      // Remove off-screen obstacles
      obstacles = obstacles.filter((obs) => obs.y < canvas.height);

      // Collision detection
      obstacles.forEach((obs) => {
        if (
          player.x < obs.x + obs.width &&
          player.x + player.width > obs.x &&
          player.y < obs.y + obs.height &&
          player.y + player.height > obs.y
        ) {
          isGameOver = true;
        }
      });

      // Increase difficulty more often (every 100 points)
      score++;
      if (score % 100 === 0) {
        gameSpeed += 0.5;  // Obstacles will still speed up over time
      }
    }

    // Draw game elements
    function drawGame() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Draw player and obstacles
      drawPlayer();
      drawObstacles();

      // Display score
      ctx.fillStyle = "white";
      ctx.font = "20px Arial";
      ctx.fillText(`Score: ${score}`, 10, 30);

      // End screen
      if (isGameOver) {
        ctx.fillStyle = "white";
        ctx.font = "20px Arial";
        ctx.fillText(`Final Score: ${score}`, canvas.width / 2 - 80, canvas.height / 2 - 40);

        // Display registration links side by side
        ctx.font = "18px Arial";
        ctx.fillStyle = "lightblue";
        ctx.fillText("Register Here: OpsQuest", canvas.width / 2 - 150, canvas.height / 2);
        ctx.fillText("Register Here: OpsEscape", canvas.width / 2 - 150, canvas.height / 2 + 30);
      }
    }

    // Detect clicks on links
    canvas.addEventListener("click", (e) => {
      if (isGameOver) {
        const rect = canvas.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;

        // Check if OpsQuest link is clicked
        if (x >= canvas.width / 2 - 150 && x <= canvas.width / 2 + 150 && y >= canvas.height / 2 - 15 && y <= canvas.height / 2 + 5) {
          window.open("https://unstop.com/competitions/opsquest25-kjsim-mumbai-1353587", "_blank");
        }

        // Check if OpsEscape link is clicked
        if (x >= canvas.width / 2 - 150 && x <= canvas.width / 2 + 150 && y >= canvas.height / 2 + 15 && y <= canvas.height / 2 + 35) {
          window.open("https://unstop.com/o/XPIEkFs?lb=VSpIorue&utm_medium=Share&utm_source=shortUrl", "_blank");
        }
      }
    });

    // Game loop
    function gameLoop() {
      updateGame();
      drawGame();
      if (!isGameOver) {
        requestAnimationFrame(gameLoop);
      }
    }

    // Event listeners for controls
    window.addEventListener("keydown", (e) => {
      if (e.key === "ArrowLeft" && player.x > 0) {
        player.x -= player.speed;
      } else if (e.key === "ArrowRight" && player.x + player.width < canvas.width) {
        player.x += player.speed;
      }
    });

    canvas.addEventListener("touchstart", (e) => {
      touchStartX = e.touches[0].clientX;
    });

    canvas.addEventListener("touchmove", (e) => {
      if (touchStartX) {
        const touchEndX = e.touches[0].clientX;
        const deltaX = touchEndX - touchStartX;

        if (deltaX > 20 && player.x + player.width < canvas.width) {
          player.x += player.speed;
        } else if (deltaX < -20 && player.x > 0) {
          player.x -= player.speed;
        }
        touchStartX = touchEndX;
      }
    });

    // Start the game
    setInterval(createObstacle, 1000); // Add obstacles every second
    gameLoop();
  </script>
</body>
</html>
