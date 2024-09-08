<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Marry Me?</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="shortcut icon" type="image/png" href="/img/media/favicon.png" />
    <link rel="stylesheet" href="https://wow.truefriend.life/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://wow.truefriend.life/css/mycss.css">
    <link rel="stylesheet" href="https://wow.truefriend.life/css/my-css4ads.css">
    <style>
        body {
            background: url('https://wow.truefriend.life/img/media/your-background-image.jpg') no-repeat center center fixed;
            background-size: cover;
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Poppins', sans-serif;
        }
        .proposal-container {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent background */
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
        }
        h1 {
            font-size: 48px;
            color: white;
            margin-bottom: 20px;
        }
        .buttons {
            margin-top: 30px;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .yes-button {
            background-color: #28a745;
            color: white;
        }
        .yes-button:hover {
            background-color: #218838;
        }
        .no-button {
            background-color: #dc3545;
            color: white;
            position: relative;
        }
        .no-button:hover {
            background-color: #c82333;
        }
    </style>
</head>
<body>
    <div class="proposal-container">
        <h1>Will You love Me?</h1>
        <div class="buttons">
            <button class="yes-button" onclick="alert('Yay! I love you!')">Yes 💖</button>
            <button class="no-button" id="noBtn">No 😢</button>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        noBtn.addEventListener('mouseover', function() {
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            noBtn.style.position = 'absolute';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        });
    </script>
</body>
</html>
