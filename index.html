<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maze Game with Animated Elephant, Custom Questions, and Answers</title>
    <style>
        body {
    margin: 0;
    overflow: hidden;
    background-image: url('https://www.123rf.com/photo_100610574_savannah-landscape.html?is_plus=1')
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
}

        body {
            margin: 0;
            overflow: hidden;
        }

        #start-page {
            text-align: center;
            padding: 20px;
        }

        #start-page textarea {
            width: 80%;
            margin-bottom: 10px;
        }

        #start-page button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #3498db;
            color: #fff;
            text-decoration: none;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        #game-container {
            position: relative;
            width: 300px;
            height: 340px;
            margin: auto;
            background-color: #f4f4f4;
            border: 2px solid #333;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        #level {
            font-size: 18px;
            margin-top: 10px;
        }

        #player {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 40px;
            height: 40px;
        }

        #question {
            position: absolute;
            display: none;
            background-color: #fff;
            padding: 10px;
            border: 1px solid #333;
            z-index: 3;
        }

        #question-text {
            margin-bottom: 10px;
        }

        #answer {
            margin-top: 5px;
            padding: 5px;
            width: 100%;
        }

        #goal {
            position: absolute;
            top: 240px;
            left: 240px;
            font-size: 20px;
        }

        .wall {
            position: absolute;
            background-color: #333;
        }
    </style>
</head>
<body>
    
    <div id="start-page">
        <h1>Welcome to the Elephant Runner Game!</h1>
        <p>Add your own questions and answers:</p>
        <textarea id="userQuestions" rows="4" cols="50" placeholder="Enter your questions and answers here (format: Q: Question? A: Answer)"></textarea>
        <button onclick="startGame()">Start Game</button>
    </div>

    <div id="game-container">
        <div id="level">Level: 1</div>
        <img id="player" src="https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/47fa6c71805451.5ca68ac7a25a7.gif" alt="Running Elephant">
        <div id="goal">🌸</div>
        <div id="question">
            <div id="question-text"></div>
            <input type="text" id="answer" placeholder="Type your answer">
            <button onclick="submitAnswer()">Submit Answer</button>
        </div>
    </div>

    <script>
        const gameContainer = document.getElementById('game-container');
        const player = document.getElementById('player');
        const goal = document.getElementById('goal');
        const levelDisplay = document.getElementById('level');
        const questionContainer = document.getElementById('question');
        const questionText = document.getElementById('question-text');
        const answerInput = document.getElementById('answer');

        document.addEventListener('keydown', movePlayer);

        let walls = [];
        let level = 1;
        let isQuestionDisplayed = false;
        let userQuestionsAndAnswers = [];

        function startGame() {
            const userInput = document.getElementById('userQuestions').value;
            userQuestionsAndAnswers = parseUserInput(userInput);
            generateRandomWalls();
        }

        function parseUserInput(input) {
            const lines = input.split('\n');
            const questionsAndAnswers = [];

            for (const line of lines) {
                const trimmedLine = line.trim();
                if (trimmedLine.startsWith('Q:') && trimmedLine.includes('A:')) {
                    const questionIndex = trimmedLine.indexOf('Q:') + 2;
                    const answerIndex = trimmedLine.indexOf('A:') + 2;
                    const question = trimmedLine.substring(questionIndex, answerIndex - 2).trim();
                    const answer = trimmedLine.substring(answerIndex).trim();
                    questionsAndAnswers.push({ question, answer });
                }
            }

            return questionsAndAnswers;
        }

        function movePlayer(event) {
            if (isQuestionDisplayed) return;

            const step = 10;
            const currentTop = parseInt(player.style.top) || 0;
            const currentLeft = parseInt(player.style.left) || 0;

            switch (event.key) {
                case 'ArrowUp':
                    if (currentTop - step >= 0 && !isCollision(currentTop - step, currentLeft)) {
                        player.style.top = `${currentTop - step}px`;
                    }
                    break;
                case 'ArrowDown':
                    if (currentTop + step <= gameContainer.offsetHeight - 40 && !isCollision(currentTop + step, currentLeft)) {
                        player.style.top = `${currentTop + step}px`;
                    }
                    break;
                case 'ArrowLeft':
                    if (currentLeft - step >= 0 && !isCollision(currentTop, currentLeft - step)) {
                        player.style.left = `${currentLeft - step}px`;
                    }
                    break;
                case 'ArrowRight':
                    if (currentLeft + step <= gameContainer.offsetWidth - 40 && !isCollision(currentTop, currentLeft + step)) {
                        player.style.left = `${currentLeft + step}px`;
                    }
                    break;
            }

            if (Math.random() < 0.05) {
                displayRandomUserQuestion();
            }

            if (checkGoal()) {
                alert(`You reached the goal! Congratulations! Proceed to Level ${++level}`);
                levelDisplay.textContent = `Level: ${level}`;
                resetGame();
                generateRandomWalls();
            }
        }

        function isCollision(top, left) {
            const playerRect = player.getBoundingClientRect();
            const proposedRect = { top, left, right: left + playerRect.width, bottom: top + playerRect.height };

            return walls.some(wall => {
                const wallRect = wall.getBoundingClientRect();
                return (
                    proposedRect.right > wallRect.left &&
                    proposedRect.left < wallRect.right &&
                    proposedRect.bottom > wallRect.top &&
                    proposedRect.top < wallRect.bottom
                );
            });
        }

        function checkGoal() {
            const playerRect = player.getBoundingClientRect();
            const goalRect = goal.getBoundingClientRect();

            return (
                playerRect.right > goalRect.left &&
                playerRect.left < goalRect.right &&
                playerRect.bottom > goalRect.top &&
                playerRect.top < goalRect.bottom
            );
        }

        function displayRandomUserQuestion() {
            if (userQuestionsAndAnswers.length === 0) return;

            const randomIndex = Math.floor(Math.random() * userQuestionsAndAnswers.length);
            const { question, answer } = userQuestionsAndAnswers[randomIndex];

            isQuestionDisplayed = true;
            questionText.textContent = question;
            questionContainer.style.display = 'block';

            // Pause the game until the answer is submitted
            document.removeEventListener('keydown', movePlayer);
        }

        function submitAnswer() {
            const userAnswer = answerInput.value.trim().toLowerCase();

            if (userQuestionsAndAnswers.some(qa => qa.answer.toLowerCase() === userAnswer)) {
                alert("Correct! You may continue.");
            } else {
                alert("Incorrect. Try again!");
                resetGame();
            }

            // Resume the game
            questionContainer.style.display = 'none';
            isQuestionDisplayed = false;
            document.addEventListener('keydown', movePlayer);
        }

        function generateRandomWalls() {
            walls.forEach(wall => wall.remove());
            walls = [];

            const numWalls = Math.floor(Math.random() * 5) + 3;

            for (let i = 0; i < numWalls; i++) {
                const wall = document.createElement('div');
                wall.classList.add('wall');
                const wallWidth = Math.floor(Math.random() * 50) + 30;
                const wallHeight = Math.floor(Math.random() * 50) + 30;
                const wallTop = Math.floor(Math.random() * (gameContainer.offsetHeight - wallHeight));
                const wallLeft = Math.floor(Math.random() * (gameContainer.offsetWidth - wallWidth));

                wall.style.width = `${wallWidth}px`;
                wall.style.height = `${wallHeight}px`;
                wall.style.top = `${wallTop}px`;
                wall.style.left = `${wallLeft}px`;

                gameContainer.appendChild(wall);
                walls.push(wall);
            }
        }

        function resetGame() {
            player.style.top = '10px';
            player.style.left = '10px';
        }
    </script>

</body>
</html>
