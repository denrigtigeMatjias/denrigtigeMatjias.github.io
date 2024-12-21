<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Execution Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Times my scripts has been executed</h1>
    </header>
    <main>
        <section class="tracker">
            <p>The script has been executed:</p>
            <h2 id="count">Loading...</h2>
        </section>
    </main>
    <footer>
        <p>Created with ❤️ by [Your Name]</p>
    </footer>

    <script>
        // Fetch and display the execution count
        async function fetchCount() {
            try {
                const response = await fetch('https://your-backend-url.com/count');
                const data = await response.json();
                document.getElementById('count').textContent = data.count;
            } catch (error) {
                document.getElementById('count').textContent = "Error loading count";
                console.error("Failed to fetch count:", error);
            }
        }

        fetchCount();
    </script>
</body>
</html>

/* General Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    color: #333;
    background: linear-gradient(135deg, #f0f0f0, #e0e0e0);
    text-align: center;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

/* Header */
header {
    background-color: #4CAF50;
    color: white;
    padding: 1rem 0;
}

header h1 {
    font-size: 2.5rem;
}

/* Main Section */
main {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem;
}

.tracker {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    width: 100%;
}

.tracker p {
    font-size: 1.2rem;
}

.tracker h2 {
    font-size: 3rem;
    margin: 1rem 0;
    color: #4CAF50;
}

/* Footer */
footer {
    background-color: #333;
    color: white;
    padding: 1rem 0;
}

footer p {
    font-size: 0.9rem;
}

