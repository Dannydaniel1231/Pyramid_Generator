# Pyramid_Generator
Pyramid Generator
This project generates a pyramid of characters using HTML, CSS, and JavaScript. The pyramid's appearance and behavior can be customized by adjusting the provided variables and functions in the script.

File Structure
Copy code
.
├── index.html
├── style.css
index.html
The main HTML file that sets up the structure of the webpage and includes the script to generate the pyramid.

html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Pyramid_Generator</title>
</head>
<body>
    <h1> Hello Pyramid!!</h1>
</body>
<script>
    // Declare and assign variables
    const character = "!";
    const count = 10;
    const rows = [];
    const inverted = true;

    // Function to pad each row
    function PadRow(rowNumber, rowCount) {
        return " ".repeat(rowCount - rowNumber) + character.repeat(2 * rowNumber - 1) + " ".repeat(rowCount - rowNumber);
    }

    // Generate pyramid rows
    for (let i = 1; i <= count; i++) {
        if (inverted) {
            rows.unshift(PadRow(i, count));
        } else {
            rows.push(PadRow(i, count));
        }
    }

    // Build the final result string
    let result = "";
    for (const row of rows) {
        result = result + "\n" + row;
    }
    
    // Display the result in the console (can be modified to display on the webpage)
    console.log(result);
</script>
</html>
style.css
This CSS file can be used to style the pyramid and the rest of the webpage. (Note: The current example does not use any specific CSS styles for the pyramid).

css
Copy code
/* style.css */

/* General body styling */
body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
}

/* Heading style */
h1 {
    margin-top: 20px;
    color: #333;
}
How to Use
Modify the Character: Change the character variable to use a different character in the pyramid.
Adjust the Height: Change the count variable to increase or decrease the number of rows in the pyramid.
Invert the Pyramid: Toggle the inverted variable between true and false to invert the pyramid