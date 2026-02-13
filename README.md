<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Sanvi ❤️</title>
    <style>
        body {
            background-color: #ffe6e6;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }

        h1 {
            color: #d63384;
            font-size: 3rem;
            text-shadow: 2px 2px #fff;
            text-align: center;
        }

        .heart {
            background-color: #ff4d4d;
            display: inline-block;
            height: 100px;
            margin: 50px;
            position: relative;
            transform: rotate(-45deg);
            width: 100px;
            animation: beat 0.8s infinite;
        }

        .heart:before, .heart:after {
            content: "";
            background-color: #ff4d4d;
            border-radius: 50%;
            height: 100px;
            position: absolute;
            width: 100px;
        }

        .heart:before { top: -50px; left: 0; }
        .heart:after { left: 50px; top: 0; }

        @keyframes beat {
            0% { transform: scale(1) rotate(-45deg); }
            20% { transform: scale(1.2) rotate(-45deg); }
            40% { transform: scale(1.1) rotate(-45deg); }
            60% { transform: scale(1.4) rotate(-45deg); }
            100% { transform: scale(1) rotate(-45deg); }
        }

        .buttons {
            display: flex;
            gap: 20px;
            margin-top: 20px;
            position: relative;
        }

        button {
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }

        #yesBtn {
            background-color: #28a745;
            color: white;
        }

        #noBtn {
            background-color: #dc3545;
            color: white;
            position: absolute;
            left: 120px;
        }

        .success-msg {
            display: none;
            text-align: center;
            color: #d63384;
        }
    </style>
</head>
<body>

    <div id="main-content">
        <h1>Sanvi, will you be my Valentine?</h1>
        <div style="display: flex; justify-content: center;">
            <div class="heart"></div>
        </div>
        
        <div class="buttons" id="btnContainer">
            <button id="yesBtn" onclick="celebrate()">Yes</button>
            <button id="noBtn" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <div id="celebration" class="success-msg">
        <h1>Yay! I love you, Sanvi! ❤️</h1>
        <p>You've made me the happiest person alive.</p>
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHYxdmZ4ZzBqZzBqZzBqZzBqZzBqZzBqZzBqZzBqZzBqZzBqJmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/KztT2c4u8mYYUiMKdZ/giphy.gif" alt="Happy Cat" width="300">
    </div>

    <script>
        function moveButton() {
            const btn = document.getElementById('noBtn');
            // Move the button to a random position within the viewport
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            
            btn.style.position = 'fixed';
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        function celebrate() {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('celebration').style.display = 'block';
            
            // Trigger a little surprise alert
            setTimeout(() => {
                alert("Best choice ever, Sanvi! 🥰");
            }, 500);
        }
    </script>
</body>
</html>
