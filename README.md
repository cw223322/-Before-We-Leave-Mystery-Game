<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Before We Leave... Solve the Mystery!</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            color: #333;
            text-align: center;
            padding: 20px;
        }
        h1 {
            color: #5d3a3a;
            font-size: 2.5em;
        }
        .clue {
            background-color: #fff;
            border-radius: 8px;
            padding: 20px;
            margin: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        input[type="text"] {
            padding: 10px;
            font-size: 1.2em;
            border-radius: 4px;
            border: 2px solid #ddd;
            margin: 10px 0;
            width: 80%;
        }
        .button {
            padding: 10px 20px;
            background-color: #8fc7e2;
            color: #fff;
            border: none;
            font-size: 1.2em;
            border-radius: 4px;
            cursor: pointer;
        }
        .button:hover {
            background-color: #6aa9c1;
        }
        #result {
            font-size: 1.5em;
            color: green;
            margin-top: 20px;
        }
        .hidden {
            display: none;
        }
        .incorrect {
            font-size: 1em;
            color: red;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Before We Leave... Solve the Mystery! <span class="emoji">🕵️‍♂️🧩</span></h1>
    
    <div class="clue">
        <p><strong>Clue 1:</strong> I am something you often find in a home, and I’m used to create warmth or light. I may have a shade, or even a bulb. <span class="emoji">🏠💡</span></p>
        <input type="text" id="answer1" placeholder="Enter your answer...">
        <button class="button" onclick="checkAnswer1()">Check Answer</button>
        <p id="result1" class="hidden">Correct! The answer is 'lamp'. <span class="emoji">✔️</span></p>
        <p id="incorrect1" class="incorrect hidden">Incorrect Vagabond! ❌ Are you sure you're 26 years of age? <span class="emoji">🤔</span> Try again! <span class="emoji">😘</span></p>
    </div>
    
    <div class="clue">
        <p><strong>Clue 2:</strong> I come in a glass, clear and sometimes paired with tonic or citrus. I’ve been a part of British tradition for centuries. <span class="emoji">🍸🌿</span></p>
        <input type="text" id="answer2" placeholder="Enter your answer...">
        <button class="button" onclick="checkAnswer2()">Check Answer</button>
        <p id="result2" class="hidden">Correct! The answer is 'gin' (hint: rearrange). <span class="emoji">✔️</span></p>
        <p id="incorrect2" class="incorrect hidden">Incorrect Vagabond! ❌ Are you sure you're 26 years of age? <span class="emoji">🤔</span> Try again! <span class="emoji">😘</span></p>
    </div>

    <div class="clue">
        <p><strong>Clue 3:</strong> Think of ‘garden’, ‘eggs’, and ‘magic’. What do they have in common? <span class="emoji">🌱✨</span></p>
        <input type="text" id="answer3" placeholder="Enter your answer...">
        <button class="button" onclick="checkAnswer3()">Check Answer</button>
        <p id="result3" class="hidden">Correct! The common letter is 'g'. <span class="emoji">✔️</span></p>
        <p id="incorrect3" class="incorrect hidden">Incorrect Vagabond! ❌ Are you sure you're 26 years of age? <span class="emoji">🤔</span> Try again! <span class="emoji">😘</span></p>
    </div>

    <div class="clue">
        <p><strong>Final Clue:</strong> Combine what you’ve learned: a light,Hoath House, Chiddingstonedden in plain sight. What experience do these clues lead to? <span class="emoji">🔍🛋️</span></p>
        <input type="text" id="finalAnswer" placeholder="Enter final keyword...">
        <button class="button" onclick="checkFinalAnswer()">Check Final Answer</button>
        <p id="finalResult" class="hidden">Correct! You're going glamping at Hoath House! <span class="emoji">✔️</span></p>
        <p id="incorrectFinal" class="incorrect hidden">Incorrect Vagabond! ❌ Are you sure you're 26 years of age? <span class="emoji">🤔</span> Try again! <span class="emoji">😘</span></p>
    </div>

    <div id="address" class="hidden">
        <p><strong>Destination:</strong> <span class="emoji">📍🏡</span> Hoath House, Chiddingstone House, TN8 7DB</p>
    </div>

    <script>
        function checkAnswer1() {
            const answer1 = document.getElementById('answer1').value.toLowerCase();
            if (answer1 === 'lamp') {
                document.getElementById('result1').classList.remove('hidden');
                document.getElementById('incorrect1').classList.add('hidden');
            } else {
                document.getElementById('result1').classList.add('hidden');
                document.getElementById('incorrect1').classList.remove('hidden');
            }
        }

        function checkAnswer2() {
            const answer2 = document.getElementById('answer2').value.toLowerCase();
            if (answer2 === 'gin' || answer2 === 'ing') {
                document.getElementById('result2').classList.remove('hidden');
                document.getElementById('incorrect2').classList.add('hidden');
            } else {
                document.getElementById('result2').classList.add('hidden');
                document.getElementById('incorrect2').classList.remove('hidden');
            }
        }

        function checkAnswer3() {
            const answer3 = document.getElementById('answer3').value.toLowerCase();
            if (answer3 === 'g') {
                document.getElementById('result3').classList.remove('hidden');
                document.getElementById('incorrect3').classList.add('hidden');
            } else {
                document.getElementById('result3').classList.add('hidden');
                document.getElementById('incorrect3').classList.remove('hidden');
            }
        }

        function checkFinalAnswer() {
            const finalAnswer = document.getElementById('finalAnswer').value.toLowerCase();
            if (finalAnswer === 'glamping') {
                document.getElementById('finalResult').classList.remove('hidden');
                document.getElementById('address').classList.remove('hidden');
                document.getElementById('incorrectFinal').classList.add('hidden');
            } else {
                document.getElementById('finalResult').classList.add('hidden');
                document.getElementById('address').classList.add('hidden');
                document.getElementById('incorrectFinal').classList.remove('hidden');
            }
        }
    </script>
</body>
</html>
