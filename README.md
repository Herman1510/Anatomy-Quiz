<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz: Self-Mark Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .question {
            margin-bottom: 20px;
        }
        .result {
            margin-top: 20px;
            font-size: 20px;
        }
    </style>
</head>
<body>

<h1>Quiz: Self-Mark Example</h1>

<script>
    // Password protection logic
    const password = "1510"; // The required password

    let enteredPassword = prompt("Enter password to access the quiz:");

    if (enteredPassword !== password) {
        alert("Incorrect password.");
        window.location.href = "about:blank"; // Redirect to a blank page if the password is incorrect
    } else {
        // Display the quiz if the password is correct
        document.getElementById('quizContent').style.display = 'block';
    }
</script>

<div id="quizContent" style="display:none;">
    <form id="quizForm">
        <!-- Question 1 -->
        <div class="question">
            <label for="q1">Trauma to the pterion threatens injury to which artery?</label><br>
            <input type="radio" name="q1" value="a"> Anterior pterygoid<br>
            <input type="radio" name="q1" value="b"> Posterior auricular<br>
            <input type="radio" name="q1" value="c"> Common maxillary<br>
            <input type="radio" name="q1" value="d"> External carotid<br>
            <input type="radio" name="q1" value="e"> Middle meningeal<br>
        </div>

        <!-- Question 2 -->
        <div class="question">
            <label for="q2">Amyotrophic Lateral Sclerosis (ALS) mostly affects:</label><br>
            <input type="radio" name="q2" value="a"> Anterior gray horn<br>
            <input type="radio" name="q2" value="b"> Nucleus dorsalis of Clarke<br>
            <input type="radio" name="q2" value="c"> Lateral gray horn<br>
            <input type="radio" name="q2" value="d"> Posterior gray horn<br>
            <input type="radio" name="q2" value="e"> Substância gelatinosa<br>
        </div>

        <!-- Question 3 -->
        <div class="question">
            <label for="q3">The right subclavian artery branches from the:</label><br>
            <input type="radio" name="q3" value="a"> Ascending aorta<br>
            <input type="radio" name="q3" value="b"> Arch of the aorta<br>
            <input type="radio" name="q3" value="c"> Brachiocephalic trunk<br>
            <input type="radio" name="q3" value="d"> Common carotid artery<br>
            <input type="radio" name="q3" value="e"> Descending aorta<br>
        </div>

        <!-- Question 4 -->
        <div class="question">
            <label for="q4">Find the correct statement regarding the stomach:</label><br>
            <input type="radio" name="q4" value="a"> Its lymphatic drainage is direct into the thoracic duct<br>
            <input type="radio" name="q4" value="b"> Its blood supply is mainly from superior mesenteric artery<br>
            <input type="radio" name="q4" value="c"> It has lesser and greater curvatures<br>
            <input type="radio" name="q4" value="d"> It has superior and inferior angles<br>
            <input type="radio" name="q4" value="e"> Its fundus is on its distal one third<br>
        </div>

        <!-- Question 5 -->
        <div class="question">
            <label for="q5">The greater sciatic foramen transmits the following except:</label><br>
            <input type="radio" name="q5" value="a"> The pudendal nerve<br>
            <input type="radio" name="q5" value="b"> The superior gluteal nerve and vessels<br>
            <input type="radio" name="q5" value="c"> The popliteal artery<br>
            <input type="radio" name="q5" value="d"> The sciatic nerve<br>
            <input type="radio" name="q5" value="e"> The piriformis muscle<br>
        </div>

        <button type="button" onclick="checkAnswers()">Submit</button>
    </form>

    <div class="result" id="result"></div>

    <script>
        function checkAnswers() {
            // Correct answers
            const correctAnswers = {
                q1: 'e',
                q2: 'a',
                q3: 'c',
                q4: 'c',
                q5: 'c'
            };

            const form = document.getElementById('quizForm');
            const resultDiv = document.getElementById('result');
            let score = 0;

            for (let q in correctAnswers) {
                const userAnswer = form.querySelector(`input[name="${q}"]:checked`);
                if (userAnswer && userAnswer.value === correctAnswers[q]) {
                    score++;
                }
            }

            resultDiv.innerHTML = `You scored ${score} out of 5.`;
        }
    </script>
</div>

</body>
</html>
