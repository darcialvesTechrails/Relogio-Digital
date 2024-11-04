Digital ClocK (Relogio Digital)

A simple digital clock implemented with HTML, CSS, and JavaScript.

Table of Contents
Introduction

Features

Technologies Used
Setup
Usage
Code Overview
Contributing
License

Introduction
This project is a basic digital clock that displays the current time and updates every second. 
It's built using HTML for the structure, CSS for styling, and JavaScript for functionality.

Features
Displays the current time in hours, minutes, and seconds.
Automatically updates every second.

Technologies Used
HTML
CSS
JavaScript

Setup
To run this project locally, follow these steps:

Clone the repository:
bash
git clone https://github.com/darcialvesTechrails/digital-clock.git
Navigate to the project directory:

bash
cd digital-clock
Open index.html in your web browser.

Usage
Once you open index.html, you will see the digital clock displaying the current time. The time will update automatically every second.

Code Overview
HTML (index.html)
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="clock">
        <h1 id="time">00:00:00</h1>
    </div>
    <script src="script.js"></script>
</body>
</html>

CSS (style.css)
css
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #282c34;
    color: white;
}

.clock {
    text-align: center;
}

#time {
    font-size: 5rem;
}

JavaScript (script.js)
javascript
function updateTime() {
    const timeElement = document.getElementById('time');
    const now = new Date();
    const hours = String(now.getHours()).padStart(2, '0');
    const minutes = String(now.getMinutes()).padStart(2, '0');
    const seconds = String(now.getSeconds()).padStart(2, '0');
    timeElement.textContent = `${hours}:${minutes}:${seconds}`;
}

setInterval(updateTime, 1000);
updateTime(); // initial call to display the time immediately
Contributing
Contributions are welcome! If you have any suggestions or improvements, please submit a pull request or open an issue.

License
This project is licensed under the MIT License.
