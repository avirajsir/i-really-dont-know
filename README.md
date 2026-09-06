<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jam Build</title>
    <style>
        body { 
            margin: 0; 
            overflow: hidden; 
            background: #222; 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
        }
        canvas { 
            background: #333; 
            box-shadow: 0 0 15px rgba(0,0,0,0.8); 
        }
    </style>
</head>
<body>
    <canvas id="gameCanvas" width="800" height="600"></canvas>
    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        
        let lastTime = 0;

        function update(deltaTime) {
            // Add state logic here
        }

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Default placeholder rendering
            ctx.fillStyle = '#00ff88';
            ctx.font = '24px monospace';
            ctx.fillText('Jam Started...', 320, 300);
        }

        function loop(timestamp) {
            const deltaTime = timestamp - lastTime;
            lastTime = timestamp;
            
            update(deltaTime);
            draw();
            
            requestAnimationFrame(loop);
        }
        
        // Start loop
        requestAnimationFrame(loop);
    </script>
</body>
</html>
