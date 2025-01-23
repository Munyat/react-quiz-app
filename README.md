# React Quiz App

A fully functional React-based quiz application designed to provide an interactive quiz experience with a timer, progress tracking, and a scoring system. The app fetches quiz questions from an API and includes features like high scores and error handling.

## Features

- **Start Screen**: Welcomes the user and provides the total number of questions.
- **Quiz Flow**: Displays one question at a time with multiple-choice options.
- **Progress Tracking**: Tracks the user's progress, points earned, and remaining questions.
- **Timer**: Limits the time to answer each question.
- **Finish Screen**: Displays the user's total score and high score.
- **Error Handling**: Handles errors gracefully, such as issues with data fetching.
- **State Management**: Managed using the `useReducer` hook for predictable state updates.

## File Structure

```plaintext
.
├── App.js              // Main component and application logic
├── DateCounter.js      // (Optional) For additional date-related features
├── Error.js            // Displays error messages
├── FinishScreen.js     // Displays the user's score and high score
├── Footer.js           // Footer component containing navigation and timer
├── Header.js           // App title and header
├── Loader.js           // Loading spinner during data fetching
├── Main.js             // Main container for the app content
├── NextButton.js       // Button to navigate to the next question
├── Options.js          // Displays the multiple-choice options for a question
├── Progress.js         // Progress bar and stats during the quiz
├── Question.js         // Displays the current question
├── StartScreen.js      // Start screen of the quiz
└── Timer.js            // Timer for each question
```

## Installation and Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/react-quiz-app.git
   cd react-quiz-app
   ```

2. **Install Dependencies**  
   Make sure you have [Node.js](https://nodejs.org/) installed, then run:

   ```bash
   npm install
   ```

3. **Run the JSON Server**  
   Start a JSON server to serve the quiz questions.

   ```bash
   npx json-server --watch db.json --port 5555
   ```

   Ensure that the `db.json` file contains the quiz questions in the following format:

   ```json
   [
     {
       "question": "Which is the most popular JavaScript framework?",
       "options": ["Angular", "React", "Svelte", "Vue"],
       "correctOption": 1,
       "points": 10
     }
   ]
   ```

4. **Start the App**  
   Run the development server:

   ```bash
   npm start
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## How It Works

1. The app fetches questions from the JSON server on load.
2. The user starts the quiz by clicking the start button.
3. Each question is displayed with multiple-choice options and a timer.
4. Users earn points for each correct answer.
5. The quiz ends when all questions are answered or time runs out.
6. The final score and high score are displayed on the finish screen.

## State Management

The app uses the `useReducer` hook to manage the following states:

- `questions`: Array of quiz questions fetched from the API.
- `status`: Current app status (`loading`, `ready`, `active`, `finished`, or `error`).
- `index`: Current question index.
- `answer`: User's selected answer for the current question.
- `points`: Total points earned.
- `highscore`: Highest score achieved by the user.
- `secondsRemaining`: Time left to complete the quiz.

## Key Components

- **App.js**: Main application logic and state management.
- **Header.js**: Displays the app title.
- **Main.js**: Renders the dynamic content based on the app's status.
- **StartScreen.js**: Displays the start button and quiz information.
- **Question.js**: Renders the current question and options.
- **Progress.js**: Shows the user's progress and score.
- **Timer.js**: Handles the countdown timer for the quiz.
- **FinishScreen.js**: Displays the final score and high score.
- **Error.js**: Shows an error message if data fetching fails.

## Customization

You can modify the `db.json` file to add or update quiz questions. The app will dynamically adapt to the changes.

## License

This project is licensed under the MIT License. Feel free to modify and distribute it as needed.

---

Feel free to reach out with any questions or suggestions for improvement! 😊
