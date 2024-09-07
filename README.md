
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Favorite Things Survey</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div id="form-section">
            <h1>Favorite Things Survey</h1>
            <form id="survey-form">
                <label for="favorite-food">Favorite Food:</label>
                <input type="text" id="favorite-food" name="favorite-food" required>

                <label for="favorite-movie">Favorite Movie:</label>
                <input type="text" id="favorite-movie" name="favorite-movie" required>

                <label for="favorite-color">Favorite Color:</label>
                <input type="text" id="favorite-color" name="favorite-color" required>

                <label for="user-image">Upload an Image:</label>
                <input type="file" id="user-image" name="user-image" accept="image/*" required>

                <button type="button" onclick="submitForm()">Submit</button>
            </form>
        </div>

        <div id="results-section" style="display: none;">
            <h1>Your Favorite Things</h1>
            <div id="results"></div>
            <button onclick="goBack()">Go Back</button>
        </div>
    </div>

    <script>
        function submitForm() {
            // Get form values
            const food = document.getElementById('favorite-food').value;
            const movie = document.getElementById('favorite-movie').value;
            const color = document.getElementById('favorite-color').value;
            const image = document.getElementById('user-image').files[0];

            // Validate form
            if (!food || !movie || !color || !image) {
                alert('Please fill out all fields and upload an image.');
                return;
            }

            // Generate result score
            const score = calculateScore(food, movie, color);

            // Hide form section and show results section
            document.getElementById('form-section').style.display = 'none';
            document.getElementById('results-section').style.display = 'block';

            // Display results
            const resultsDiv = document.getElementById('results');
            resultsDiv.innerHTML = `
                <p><strong>Favorite Food:</strong> ${food}</p>
                <p><strong>Favorite Movie:</strong> ${movie}</p>
                <p><strong>Favorite Color:</strong> ${color}</p>
                <p><strong>Your Score:</strong> ${score}</p>
                <p><strong>Your Image:</strong> <img src="${URL.createObjectURL(image)}" alt="User Image" style="max-width: 200px; height: auto;"></p>
            `;
        }

        function calculateScore(food, movie, color) {
            // Simple score calculation based on user inputs (for demonstration purposes)
            let score = 0;
            score += food.length;
            score += movie.length;
            score += color.length;
            return score;
        }

        function goBack() {
            // Hide results section and show form section
            document.getElementById('results-section').style.display = 'none';
            document.getElementById('form-section').style.display = 'block';
            
            // Reset form
            document.getElementById('survey-form').reset();
        }
    </script>
</body>
</html>
