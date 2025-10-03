# ALX_Simple_Quiz
ALX week 6 activity on JavaScript Deep dive.

# ALX Simple Quiz 🧠

A lightweight, interactive quiz web-app built using HTML, CSS, and vanilla JavaScript.  
Part of the **ALX JavaScript Deep Dive** curriculum — demonstrates client-side logic for validating quiz answers and providing immediate feedback.

---

## 🚀 Live Demo

(If deployed)  
[View the Quiz Live](https://damilola8909.github.io/ALX_Simple_Quiz/)

---

## 📸 Screenshot

![Quiz Screenshot](https://raw.githubusercontent.com/DAMILOLA8909/ALX_Simple_Quiz/main/screenshots/quiz-screenshot.png)  
*(Add a `screenshots/quiz-screenshot.png` file in your repo for this to show properly.)*

---

## 📁 Repository Structure

ALX_Simple_Quiz/
│

├── index.html # The quiz UI and markup

├── style.css # Styling for layout and feedback

├── quiz.js # JavaScript logic for answer checking

├── screenshots/ # (optional) images to include in README

└── README.md # This document


---

## ✅ Features & Behavior

- Presents a quiz question and multiple choice answers (via radio buttons).  
- On clicking “Submit Answer”, JavaScript executes logic to:
  - Determine which radio option the user selected.
  - Compare the user’s answer to the correct one.
  - Display immediate feedback in the UI:
    - “Correct! Well done.” if the answer is correct.
    - “That’s incorrect. Try again!” if the answer is wrong.
- Simple, read-only logic — no server or backend component.

---

## 🛠 Implementation Details

In **quiz.js**:

1. A function **`checkAnswer()`** is declared.  
2. Inside it:
   - `correctAnswer` is set to `"4"` (string).  
   - `userAnswer` is retrieved via  
     ```js
     document.querySelector('input[name="quiz"]:checked').value
     ```  
   - An `if` compares `userAnswer === correctAnswer`.  
     - On match, the element `#feedback` gets `"Correct! Well done."`.  
     - Otherwise, it gets `"That’s incorrect. Try again!"`.  
3. Then an event listener is attached to the button `#submit-answer`:
   ```js
   document.getElementById("submit-answer")
     .addEventListener("click", checkAnswer);

🛒 Usage / Setup

1. Clone the repository:
   git clone https://github.com/DAMILOLA8909/ALX_Simple_Quiz.git
   
2. Open index.html in your browser (no build or server needed).

3. Answer the quiz and click “Submit Answer” to see feedback immediately.
