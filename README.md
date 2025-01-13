h1>Quiz: Self-Mark Example</h1>

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
            q1: 'e', // Middle meningeal
            q2: 'a', // Anterior gray horn
            q3: 'c', // Brachiocephalic trunk
            q4: 'c', // It has lesser and greater curvatures
            q5: 'c'  // The popliteal artery
        };

        // Get all form inputs
        const form = document.getElementById('quizForm');
        const resultDiv = document.getElementById('result');
        let score = 0;

        // Loop through each question and check the selected answer
        for (let q in correctAnswers) {
            const userAnswer = form.querySelector(`input[name="${q}"]:checked`);

            if (userAnswer) {
                if (userAnswer.value === correctAnswers[q]) {
                    score++;
                }
            }
        }

        // Show the score
        resultDiv.innerHTML = `You scored ${score} out of 5.`;
    }
</script>

</body>
</html># Anatomy-Quiz
Hey there we go
