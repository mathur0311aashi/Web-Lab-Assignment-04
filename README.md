const quizQuestions = [
    { question: "What is the capital of India?", answer: "delhi" },
    { question: "What does HTML stand for?", answer: "hypertext markup language" },
    { question: "What is 2 + 2?", answer: "4" },
    { question: "Which programming language is used for web styling?", answer: "css" },
    { question: "What keyword is used to declare a variable in JavaScript?", answer: "let" }
];
function runQuiz() {
    let score = 0; // Score Initialization
for (let i = 0; i < quizQuestions.length; i++) {
        let userInput = prompt(quizQuestions[i].question);
if (userInput === null) {
          alert("You cancelled the quiz.");
          return;
        }
userInput = userInput.toLowerCase().trim();
 if (userInput === quizQuestions[i].answer) {
            score++;
            alert("Correct!");
        } else {
            alert("Incorrect! Correct answer is: " + quizQuestions[i].answer);
        }
    }
    alert("Quiz Completed!\nYour Score: " + score + " out of " + quizQuestions.length);
}
runQuiz();
