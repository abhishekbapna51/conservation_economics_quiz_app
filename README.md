# Conservation Economics Quiz App
An interactive quiz application built with React to help students practice and revise concepts from Conservation Economics (Weeks 1–12).  
The app provides instant feedback, score tracking, and a review of incorrect answers in a clean, user-friendly interface.

---

## Features

### Week-wise Quiz Selection
Choose any week (1–12) and practice only that week's questions.

### Shuffle-All Mode
Mixes all questions from all weeks for a complete revision test.

### Instant Feedback
- Correct answer highlighted in green  
- Wrong answer highlighted in red  
- Automatically moves to the next question after a short delay

### Score Tracking
Displays current score and total score at the end of the quiz.

### Wrong Answer Review
Shows all incorrectly answered questions with:
- Your selected answer  
- The correct answer

### Clean and Responsive UI
Simple design that works smoothly on desktop and mobile.

---

## Tech Stack

- React (Hooks: useState, useEffect, useMemo)
- JavaScript ES6+
- CSS / Inline Styles
- Fully client-side with no backend required

---

## Project Structure
src/App.js
src/index.js
src/index.css
src/reportWebVitals.js
src/questionsData (embedded inside App.js)

---

## Running the Project Locally

### 1. Clone the repository
```bash
git clone https://github.com/abhishekbapna51/conservation_economics_quiz_app.git
```
### 2. Install dependencies
```bash
npm install
```
### 3. Start the development server
```bash
npm start
```
### The app will run at:
http://localhost:3000

---

## How the App Works
- Select a week or click Shuffle All
- Start the quiz
- The quiz begins from question 1
- Selecting an answer shows instant feedback
- After a short delay, the next question loads
- At the end, the score and wrong answers are displayed
- You may retry the quiz or return to the main screen

## Key Challenges and Solutions
1. Preventing Double Clicks
- Users could click options multiple times quickly.
- Solution: Added an isChecking state flag to temporarily disable option buttons until feedback is shown.

2. Smooth Feedback Before Switching Questions
- The user needed to see right/wrong feedback before moving on.
- Solution: Used a setTimeout delay to show feedback for 700ms, then updated the question index.

3. Managing a Large Question Dataset
- Handling week-wise questions separately was messy.
- Solution: Used a unified questionsData object and a prepareQuiz() function to load or shuffle questions efficiently.
