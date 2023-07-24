# PM-LLM-Case-Studies
Here is a simple code to survey PM practitioners using random selection of case studies to evaluate LLMs
<!DOCTYPE html>
<html>
<head>
    <title>README: GPT-4 Case Studies</title>
</head>
<body>
    <h1>GPT-4 Case Studies</h1>
    <p>This HTML document uses JavaScript to interact with Firebase and Firestore. Its primary functionality includes:</p>
    <ul>
        <li>Loading and displaying data exported from GPT-4.</li>
        <li>Storing visit data in Firestore.</li>
    </ul>
    <h2>How It Works</h2>
    <h3>Script Imports</h3>
    <p>The HTML document first imports the Firebase SDK and Firestore library from the Firebase CDN. It also imports required Firebase functions from the Firebase SDK:</p>
    <ul>
        <li>initializeApp</li>
        <li>getAnalytics</li>
        <li>getFirestore</li>
        <li>collection</li>
        <li>addDoc</li>
        <li>serverTimestamp</li>
    </ul>
    <h3>Initializations</h3>
    <p>The Firebase app is then initialized with the web app's Firebase configuration. Firebase Analytics and Firestore are also initialized.</p>
    <h3>GPT-4 Data Loading</h3>
    <p>Data exported from GPT-4 is stored in a JSON array named 'jsonData' inside the script.</p>
    <h3>Displaying Data</h3>
    <p>When the window loads, a function is called which:</p>
    <ul>
        <li>Selects a random conversation from the 'jsonData' array.</li>
        <li>Parses the conversation to extract the messages.</li>
        <li>Creates and populates a 'div' element for each conversation, with its associated messages.</li>
        <li>Appends the conversation 'div' to the root 'div' element in the HTML body.</li>
    </ul>
    <h3>Storing Visit Data</h3>
    <p>After displaying the data, the same function creates a new Firestore document in the 'visits' collection. This document contains the index of the randomly selected conversation and the timestamp of the visit.</p>
    <h2>How To Use</h2>
    <p>1. Populate 'jsonData' array with your exported GPT-4 data.</p>
    <p>2. Replace the '// API config data //' placeholders in the 'firebaseConfig' object with your Firebase app's configuration data.</p>
    <p>3. Host the HTML file on a server that can serve HTML files (Firebase Hosting, for example).</p>
    <p>4. Visit the hosted HTML file's URL in a web browser to see it in action.</p>
</body>
</html>
