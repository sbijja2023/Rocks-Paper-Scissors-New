# Webpage-India-New
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Rock, Paper, Scissors Game</title>
    <style>
        /* Basic styling for the game */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        .buttons {
            margin: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
    <script>
        // Function to play the game and determine the result
        function playGame(playerChoice) {
            // Generate a random choice for the computer
            var choices = ["rock", "paper", "scissors"];
            var computerChoice = choices[Math.floor(Math.random() * choices.length)];

            // Determine the result based on the choices
            var result;
            if (playerChoice === computerChoice) {
                result = "It's a tie!";
            } else if (
                (playerChoice === "rock" && computerChoice === "scissors") ||
                (playerChoice === "paper" && computerChoice === "rock") ||
                (playerChoice === "scissors" && computerChoice === "paper")
            ) {
                result = "You win!";
            } else {
                result = "Computer wins!";
            }

            // Display the choices and the result
            document.getElementById("player-choice").innerText = "You chose: " + playerChoice;
            document.getElementById("computer-choice").innerText = "Computer chose: " + computerChoice;
            document.getElementById("game-result").innerText = result;
        }
    </script>
</head>
<body>
    <h1>Rock, Paper, Scissors Game</h1>

    <!-- Buttons for player to choose rock, paper, or scissors -->
    <div class="buttons">
        <button onclick="playGame('rock')">Rock</button>
        <button onclick="playGame('paper')">Paper</button>
        <button onclick="playGame('scissors')">Scissors</button>
    </div>

    <!-- Display the game result -->
    <div class="result">
        <p id="player-choice"></p>
        <p id="computer-choice"></p>
        <p id="game-result"></p>
    </div>
</body>
</html>
