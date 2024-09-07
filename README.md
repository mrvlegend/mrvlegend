<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Favorite Things Showcase</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.5.2/css/bootstrap.min.css">
    <link rel="stylesheet" href="styles.css"> <!-- Your custom styles -->
    <script defer src="https://kit.fontawesome.com/47eafd82ac.js"></script>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" href="#">Favorite Showcase</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <a class="nav-link" href="#form-section">Submit</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#submissions-section">View Submissions</a>
                </li>
            </ul>
        </div>
    </nav>

    <div class="container mt-5">
        <!-- Form Section -->
        <section id="form-section">
            <h2 class="text-center">Share Your Favorite Things</h2>
            <form id="favorite-form">
                <div class="form-group">
                    <label for="name">Your Name:</label>
                    <input type="text" class="form-control" id="name" required>
                </div>
                <div class="form-group">
                    <label for="favorite-thing">Favorite Thing:</label>
                    <input type="text" class="form-control" id="favorite-thing" required>
                </div>
                <div class="form-group">
                    <label for="image-url">Image URL:</label>
                    <input type="url" class="form-control" id="image-url" required>
                </div>
                <div class="form-group">
                    <label for="answer">Your Answer to a Question:</label>
                    <textarea class="form-control" id="answer" rows="3" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary">Submit</button>
            </form>
        </section>

        <!-- Submissions Section -->
        <section id="submissions-section" class="mt-5">
            <h2 class="text-center">Submitted Favorites</h2>
            <div id="submissions-list" class="row">
                <!-- Dynamic content will be injected here -->
            </div>
        </section>
    </div>

    <footer class="bg-dark text-white text-center py-3 mt-5">
        &copy; 2024 Favorite Showcase. All rights reserved.
    </footer>

    <script>
        document.getElementById('favorite-form').addEventListener('submit', function(event) {
            event.preventDefault();

            // Get form values
            const name = document.getElementById('name').value;
            const favoriteThing = document.getElementById('favorite-thing').value;
            const imageUrl = document.getElementById('image-url').value;
            const answer = document.getElementById('answer').value;

            // Create new submission element
            const submissionDiv = document.createElement('div');
            submissionDiv.classList.add('col-md-4', 'mb-4');
            submissionDiv.innerHTML = `
                <div class="card">
                    <img src="${imageUrl}" class="card-img-top" alt="${favoriteThing}">
                    <div class="card-body">
                        <h5 class="card-title">${favoriteThing}</h5>
                        <p class="card-text">Submitted by: ${name}</p>
                        <p class="card-text">Answer: ${answer}</p>
                        <button class="btn btn-primary share-button" data-name="${name}" data-favorite="${favoriteThing}">Share</button>
                    </div>
                </div>
            `;

            // Add new submission to the list
            document.getElementById('submissions-list').appendChild(submissionDiv);

            // Clear the form
            document.getElementById('favorite-form').reset();
        });

        // Share functionality
        document.getElementById('submissions-list').addEventListener('click', function(event) {
            if (event.target.classList.contains('share-button')) {
                const name = event.target.getAttribute('data-name');
                const favoriteThing = event.target.getAttribute('data-favorite');
                const shareText = `Check out ${name}'s favorite thing: ${favoriteThing}!`;

                if (navigator.share) {
                    navigator.share({
                        title: 'Favorite Showcase',
                        text: shareText,
                        url: window.location.href
                    }).catch(console.error);
                } else {
                    alert(shareText);
                }
            }
        });
    </script>
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.3/dist/umd/popper.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
