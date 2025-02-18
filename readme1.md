<!-- HTML Code Explained

<!DOCTYPE html>: Declares the document type as HTML5.
<html lang="en">: The root element of the HTML document, specifying the language as English.
<head>: Contains meta-information about the HTML document, such as character set, viewport settings, title, and links to stylesheets.
<meta> tags: Provide metadata about the HTML document.
<title>Astrology Insights</title>: Sets the title that appears in the browser's title bar or tab.
<link rel="stylesheet" href="./style.css">: Links an external stylesheet named "style.css" to the HTML.
<body>: Contains the visible content of the HTML document.
<div class="container">: Creates a container element to hold the content, styled using the "container" class in CSS.
<h1>Astrology Insights</h1>: A main heading for the page.
<form id="astroForm">: Creates a form for user input. id="astroForm" is crucial for JavaScript to interact with it.
<label> elements: Provide labels for the form input fields.
<input type="text">: Creates text input fields for name and surname. required ensures the user fills them in.
<input type="number">: Creates number input fields for day, month, and year, with min and max attributes for validation.
<input type="submit" value="Get Insights">: Creates a submit button that triggers form submission.
<div class="result" id="result"></div>: A div where the results will be displayed. id="result" is used by JavaScript.
<script src="./app.js"></script>: Includes the JavaScript file "app.js" at the end of the body, which handles the form submission and logic. 

-->

<!-- JS Code Explained -->

<!-- Arrays: The code starts by defining several arrays: zodiacSigns, compliments, victimCardCompliments, recommendations, and predictions. These arrays hold the possible values for zodiac signs, compliments, "victim card" compliments (humorous), recommendations, and predictions.

Event Listener:

document.getElementById('astroForm').addEventListener('submit', function (event) { ... });: This line is the heart of the JavaScript. It gets the form element by its ID (astroForm) and attaches an event listener to it. The event listener waits for the submit event (when the user clicks the "Get Insights" button). When the submit event occurs, the provided function is executed.
event.preventDefault();: This line is crucial. It stops the default form submission behavior, which would cause the page to reload. We want to handle the form data with JavaScript without a page reload.
Getting Form Values:

const name = document.getElementById('name').value;: Gets the value entered in the "name" input field.
Similar lines retrieve the surname, day, month, and year values. Note the use of Number() to convert the string values from the number input fields into numbers.
Creating Messages:

const first_message = \Hello ${name} ${surname}.`;`: Creates a welcome message using template literals (backticks). Template literals allow you to embed variables directly in strings.
const second_message = \Your Zodiac sign is ${zodiacSigns[month - 1]}.`;`: Determines the zodiac sign based on the entered month. Remember that array indices start from 0, so we subtract 1 from the month.
Generating Random Responses:

const index1 = Math.floor(Math.random() * victimCardCompliments.length);: Generates a random index within the victimCardCompliments array.
const fourth_message = victimCardCompliments[index1];: Selects a random "victim card" compliment using the generated index.
Similar logic is used to select a random recommendation and prediction using different formulas for generating the index.
Displaying Results:

result.innerHTML = \${first_message} ${second_message} ${fourth_message} <br><br> Our Recommendation for you: ${fifth_message} <br><br> Your Future Prediction: ${sixth_message}`;: Sets the content of theresultdiv (which was initially empty) to the generated messages.<br><br>adds line breaks.innerHTML` is used to insert HTML content. -->