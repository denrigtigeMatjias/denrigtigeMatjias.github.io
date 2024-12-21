<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Execution Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Lua Script Execution Tracker</h1>
    </header>
    <main>
        <section class="tracker">
            <p>The script has been executed:</p>
            <h2 id="count">Loading...</h2>
            <p>times</p>
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
