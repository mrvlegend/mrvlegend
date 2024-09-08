<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You love Me?</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
      <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Play</title>
    <link rel="shortcut icon" type="image/png" href="/img/media/favicon.png" />
    <link rel="stylesheet" href="https://wow.truefriend.life/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://wow.truefriend.life/css/mycss.css">
    <link rel="stylesheet" href="https://wow.truefriend.life/css/my-css4ads.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script defer src="https://kit.fontawesome.com/47eafd82ac.js" crossorigin="anonymous"></script>

    <style>
     body {
            /* Set your background image URL here */
            background: url('https://wow.truefriend.life/img/media/your-background-image.jpg') no-repeat center center fixed;
            background-size: cover;
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        h1 {
            font-size: 48px;
            color: white;
        }
        .content {
            background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent background */
            padding: 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="content">
        <h1>Welcome to the Game!</h1>
        <!-- Additional content can go here -->
    </div>

    <!-- Google Tag Manager -->
    <script async src="https://www.googletagmanager.com/gtm.js?id=GTM-NX3TNSFB"></script>
</body>
        body {
            font-family: 'Poppins', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
            margin: 0;
        }
        .proposal-container {
            text-align: center;
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            font-size: 36px;
            color: #333;
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
        <h1>Will You Marry Me?</h1>
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
