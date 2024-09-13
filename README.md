<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HAPPY BIRTHDAY</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            background-image: url('birthday-background.jpg'); /* Add a background image */
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
            background-color: rgba(255, 255, 255, 0.8); /* Light white background */
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
            border: 5px solid #ff66b2; /* Pink border */
            position: relative;
            overflow: hidden;
        }
        h1 {
            font-size: 48px;
            font-family: 'Playfair Display', serif; /* Use a serif font for headings */
            color: #ff3399;
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
            background-color: #ff66b2;
            color: white;
        }
        .yes-button:hover {
            background-color: #ff3399;
        }
        .no-button {
            background-color: #ff9999;
            color: white;
            position: relative;
        }
        .no-button:hover {
            background-color: #ff6666;
        }

        /* Hidden smiling cat that appears after "Yes" */
        .smiling-cat {
            display: none;
            width: 200px;
            height: auto;
            margin-top: 20px;
            animation: fadeIn 0.5s; /* Add animation to the smiling cat */
        }

        /* Hidden text message */
        .message {
            display: none;
            font-size: 24px;
            color: #ff3399;
            margin-top: 20px;
            animation: fadeIn 0.5s; /* Add animation to the message */
        }

        /* Loading animation */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            background-color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: fadeOut 2s; /* Add animation to the loading animation */
        }
    </style>
</head>
<body>
    <div class="loading">
        <img src="loading.gif" alt="Loading animation">
    </div>
    <div class="proposal-container">
        <h1>HAPPY BIRTHDAY</h1>
        <h1>I WANT TO SAY SOMETHING TO YOU</h1>
        <h1>FROM THE FIRST DAY WHEN I SAW YOU. 😊</h1>
        <div class="buttons">
            <button class="yes-button" id="yesButton">Continue 💖</button>
            <button class="no-button" id="noBtn">Not interested 😢</button>
        </div>

        <!-- Hidden Text Message -->
        <div class="message" id="message">
            From the first time I saw you, I felt a strong connection and love for you. ❤️ I still feel the same way now. 💖 I’m sorry if I ever seemed distant or if I didn’t communicate well. 😔 Sometimes, when I’m with you, I get so overwhelmed by my feelings that I forget to say what’s on my mind. 😅 Please don't take it deeply and I’m sorry if my actions didn’t always show that. 🌹💕 I LOVED YOU FROM THE BOTTOM OF MY HEART 💖🐱
        </div>

        <!-- Hidden Smiling Cat -->
        <img src="smiling-cat.jpg" alt="Smiling cat" class="smiling-cat" id="smilingCat">
    </div>

    <script>
        const yesButton = document.getElementById('yesButton');
        const noBtn = document.getElementById('noBtn');
        const smilingCat = document.getElementById('smilingCat');
        const message = document.getElementById('message');
        const loading = document.querySelector('.loading');

        // Yes Button Event Listener
        yesButton.addEventListener('click', function() {
            alert('PRESS OK TO CONTINUE! 😻');
            smilingCat.style.display = 'block'; // Show the smiling cat
            message.style.display = 'block';   // Show the hidden message
            loading.style.display = 'none'; // Hide the loading animation
        });

        // No Button Event Listener (moves the button)
        noBtn.addEventListener('mouseover', function() {
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            noBtn.style.position = 'absolute';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        });

        // Add animation to the loading animation
        setTimeout(function() {
            loading.style.display = 'none';
        }, 2000);
    </script>
</body
