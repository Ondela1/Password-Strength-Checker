Password Strength Checker Tool
This project is a web-based tool that provides real-time feedback on the strength of a user's password. It is built with HTML, CSS, and vanilla JavaScript, and styled with Tailwind CSS.

Features
Real-time Analysis: Get immediate feedback as you type your password.

Visual Strength Meter: A progress bar visually represents the password's strength, changing color from red (weak) to green (very strong).

Detailed Criteria Checklist: See which requirements your password meets, such as length, character types, and uniqueness.

Actionable Suggestions: Receive clear feedback on how to improve your password.

Show/Hide Password: Toggle password visibility for easier typing.

Dark Mode: A sleek dark mode for better user experience, with the preference saved in local storage.

Responsive Design: The tool is fully responsive and works on all screen sizes.

How to Run the Tool
Since this is a front-end application, there is no server-side setup required.

Download the Files: Make sure you have the following three files in the same directory:

index.html

style.css

script.js

Open in Browser: Simply open the index.html file in any modern web browser (like Chrome, Firefox, or Edge).

That's it! The application will run locally in your browser.

How It Works
The tool is composed of three main files:

index.html: This file defines the structure and layout of the application. It includes the password input field, the strength meter, the feedback area, and the dark mode toggle. It links to the style.css and script.js files.

style.css: This file contains the custom styling for the application, primarily defining CSS variables for light and dark themes. The majority of the styling is handled by Tailwind CSS, which is loaded via a CDN in the HTML file.

script.js: This is the core of the application. It contains all the logic for:

Listening for user input in the password field.

Evaluating the password against a set of criteria.

Calculating a strength score.

Dynamically updating the UI (progress bar, feedback text, and criteria list) in real-time.

Handling the password visibility toggle and the dark mode switch.

Scoring Logic
The password strength is calculated out of a total of 100 points. The score is determined by a set of rules, with points awarded or deducted based on different criteria.

Positive Scoring Criteria:
Length:

+25 points if the password is at least 8 characters long.

An additional +15 points if the password is at least 12 characters long.

Character Variety:

+15 points for including lowercase letters (a-z).

+15 points for including uppercase letters (A-Z).

+15 points for including numbers (0-9).

+20 points for including special characters (e.g., !@#$%^&*).

Uniqueness:

+10 points if the password is not on a predefined list of common weak passwords.

Negative Scoring (Penalties):
Common Password: If the password is found on the common password list, the score is capped at a maximum of 20, and a warning is displayed.

Character Repetition: -10 points if three or more identical characters are repeated in a row (e.g., aaa).

Sequential Patterns: -10 points for common keyboard sequences (e.g., abc, qwe).

Strength Levels:
The final score is mapped to a strength label and color:

0-39: Weak (Red)

40-59: Medium (Yellow)

60-79: Strong (Blue)

80-100: Very Strong (Green)

Tech Stack
HTML5

CSS3 (with Tailwind CSS for utility-first styling)

JavaScript (ES6+)
