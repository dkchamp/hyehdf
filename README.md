<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    canvas {
      border: 1px solid #000;
      display: block;
      margin: 20px auto;
    }
  </style>
  <title>Simple Canvas Game</title>
</head>
<body>
  <canvas id="gameCanvas" width="800" height="600"></canvas>

  <script>
    // Get the canvas element and its context
    const canvas = document.getElementById('gameCanvas');
    const ctx = canvas.getContext('2d');

    // Initial player position
    let playerX = 50;
    let playerY = 50;

    // Update the game state
    function update() {
      // Move the player (example: move to the right)
      playerX += 5;

      // Clear the canvas
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Draw the player
      ctx.fillStyle = '#00F';
      ctx.fillRect(playerX, playerY, 50, 50);

      // Request the next animation frame
      requestAnimationFrame(update);
    }

    // Start the game loop
    update();
  </script>
</body>
</html>
