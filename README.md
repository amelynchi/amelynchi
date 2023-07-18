<!DOCTYPE html>
<html>
<head>
    <title>Guess the Number</title>
    <style>
        body {
            text-align: center;
            margin-top: 100px;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>
    <h1>Guess the Number</h1>
    <p>Guess a number between 1 and 10:</p>
    <input type="number" id="guessInput">
    <button onclick="checkGuess()">Submit</button>
    <p id="result"></p>

    <script>
        // Generate a random number between 1 and 10
        const randomNumber = Math.floor(Math.random() * 10) + 1;

        function checkGuess() {
            // Get the user's guess
            const guess = parseInt(document.getElementById("guessInput").value);

            // Check if the guess matches the random number
            if (guess === randomNumber) {
                document.getElementById("result").textContent = "Congratulations! You guessed the correct number!";
            } else {
                document.getElementById("result").textContent = "Sorry, the number was " + randomNumber + ". Try again!";
            }
        }
    </script>
</body>
</html>
