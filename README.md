<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HAPPY BIRTHDAY</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* ... existing styles ... */
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
        <img src="download.jpeg" alt="Smiling cat" class="smiling-cat" id="smilingCat">
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
</body>
</html>
