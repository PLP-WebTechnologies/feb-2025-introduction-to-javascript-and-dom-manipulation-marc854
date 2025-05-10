# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DOM Manipulation Example</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 id="main-heading">Welcome to My Page</h1>
  </header>

  <section>
    <p id="description">This is a simple JavaScript DOM example.</p>
    <button id="changeTextBtn">Change Text</button>
    <button id="toggleStyleBtn">Toggle Style</button>
    <button id="addElementBtn">Add Element</button>
    <button id="removeElementBtn">Remove Element</button>
  </section>

  <footer>
    <p>Made with ❤️ and JavaScript</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

// Change text content dynamically
document.getElementById("changeTextBtn").addEventListener("click", () => {
  const heading = document.getElementById("main-heading");
  heading.textContent = "You clicked the button!";
});

// Modify CSS styles via JavaScript
document.getElementById("toggleStyleBtn").addEventListener("click", () => {
  const description = document.getElementById("description");
  description.style.color = description.style.color === "blue" ? "black" : "blue";
  description.style.fontWeight = description.style.fontWeight === "bold" ? "normal" : "bold";
});

// Add a new element to the DOM
document.getElementById("addElementBtn").addEventListener("click", () => {
  const newPara = document.createElement("p");
  newPara.textContent = "I am a new paragraph!";
  newPara.id = "newParagraph";
  document.body.appendChild(newPara);
});

// Remove the added element
document.getElementById("removeElementBtn").addEventListener("click", () => {
  const newPara = document.getElementById("newParagraph");
  if (newPara) {
    newPara.remove();
  }
});
