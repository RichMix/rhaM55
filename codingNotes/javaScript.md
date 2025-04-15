#JS-THM

# Variables

Variables are containers that allow you to store data values in them. Like any other language, variables in JS are similar to containers to store data. 
When you store something in a bucket, you also need to label it so that it can be referenced later on easily. Similarly, in JS, each variable has a name; when we store a certain value in a variable, we assign a name to it to reference it later. 

image of var, let and const typesThere are three ways to declare variables in JS: var, let, and const.
While var is function-scoped, both let, and const are block-scoped, offering better control over variable visibility within specific code blocks.

## Data Types

In JS, data types define the type of value a variable can hold. 
Examples include string (text), number, boolean (true/false), null, undefined, and object (for more complex data like arrays or objects).

## Functions

A function represents a block of code designed to perform a specific task. Inside a function, you group code that needs to perform a similar task. 
For example, you are developing a web application in which you need to print students' results on the web page. 
The ideal case would be to create a function PrintResult(rollNum) that would accept the roll number of the user as an argument.

   <script>
        function PrintResult(rollNum) {
            alert("Username with roll number " + rollNum + " has passed the exam");
            // any other logic to display the result
        }

        for (let i = 0; i < 100; i++) {
            PrintResult(rollNumbers[i]);
        }
    </script>
        
So, instead of writing the same print code for all the students, we will use a simple function to print the result.

## Loops

Loops allow you to run a code block multiple times as long as a condition is true. Common loops in JS are for, while, and do...while, which are used to repeat tasks, like going through a list of items. 
For example, if we want to print the results of 100 students, we can call the PrintResult(rollNum) function 100 times by writing it 100 times, or we can create a loop that will be iterated through 1 to 100 and will call the PrintResult(rollNum) function as shown below.

        // Function to print student result
        function PrintResult(rollNum) {
            alert("Username with roll number " + rollNum + " has passed the exam");
            // any other logic to the display result
        }

        for (let i = 0; i < 100; i++) {
            PrintResult(rollNumbers[i]); // this will be called 100 times 
        }
    
## Request-Response Cycle

In web development, the request-response cycle is when a user's browser (the client) sends a request to a web server, and the server responds with the requested information. 
This could be a webpage, data, or other resources. You can learn more about it here.

# JavaScript Overview

In this task, we’ll use JS to create our first program. JS is an interpreted language, meaning the code is executed directly in the browser without prior compilation. 
Below is a sample JS code demonstrating key concepts, such as defining a variable, understanding data types, using control flow statements, and writing simple functions. 
These essential building blocks help create more dynamic and interactive web apps. Don’t worry if it looks a bit new now - we will discuss each of these concepts in detail later on.

```js
 // Hello, World! program
console.log("Hello, World!");

// Variable and Data Type
let age = 25; // Number type

// Control Flow Statement
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}

// Function
function greet(name) {
    console.log("Hello, " + name + "!");
}

// Calling the function
greet("Bob");
```

JS is primarily executed on the client side, which makes it easy to inspect and interact with HTML directly within the browser. 
We’ll use the Google Chrome Console feature to run our first JS program, allowing us to write and execute JS code easily without additional tools. Follow these steps to get started:

Open Google Chrome by clicking the Google Chrome icon on the Desktop of the VM.
google chrome icon on the desktop of attached VM

Once Chrome is open, press Ctrl + Shift + I to open the Console or right-click anywhere on the page and select Inspect.
how to click inspect element in Chrome

Then, click on the Console tab. This console allows you to run JS code directly in the browser without installing additional software.
Console option in Chrome

Let's create a simple JS program that adds two numbers and displays the result. Below is the code:

```
let x = 5;
let y = 10;
let result = x + y;
console.log("The result is: " + result);
```

In the code above, x and y are variables holding the numbers. x + y is an expression that adds the two numbers together, whereas console.log  is a function used to print the result to the console.
Copy the above code and paste it into the console by pressing the key Ctrl + V. Once pasted, press Enter. You should see the result displayed as:
result of hello world program in Chrome Console

# Integrating JavaScript in HTML

This task assumes you have a basic understanding of HTML and its structure. This section will explore how JS can be integrated into HTML. 
Usually, JS is not used to render content; it works with HTML and CSS to create dynamic and interactive web pages. If you're unfamiliar with HTML, reviewing it through the provided link is recommended. 
There are two main ways to integrate JS into HTML: internally and externally.


# Internal JavaScript

Internal JS refers to embedding the JS code directly within an HTML document. This method is preferable for beginners because it allows them to see how the script interacts with the HTML. 
The script is inserted between <script> tags.
These tags can be placed inside the <head> section, typically used for scripts that need to be loaded before the page content is rendered, or inside the <body> section, where the script can be utilised to interact with elements as they are loaded on the web page.

# Example

To create an HTML document with internal JS, right-click on the Desktop and select Create Document > Empty File. Name the file internal.html. 
Next, right-click the internal.html file and choose Open with Pluma to open it in a text editor.

instruction to open Pluma notepad

Once the editor is open, paste the following code:

 <!DOCTYPE html>
<html lang="en">
<head>
    <title>Internal JS</title>
</head>
<body>
    <h1>Addition of Two Numbers</h1>
    <p id="result"></p>

    <script>
        let x = 5;
        let y = 10;
        let result = x + y;
        document.getElementById("result").innerHTML = "The result is: " + result;
    </script>
</body>
</html>
After pasting the code, click File and select Save, which will save the file to internal.html.Double-click the file to open it in Chrome browser, where you will see the following output:

Internal.html output in Chrome

In this HTML document, we are using internal JS, meaning the code is placed directly inside the HTML file within the <script> tag. The script performs a simple task: it adds two numbers (x and y) and then displays the result on the web page. 
The JS interacts with the HTML by selecting an element (<p> with id="result") and updating its content using document.getElementById("result").innerHTML. 
This internal JS is executed when the browser loads the HTML file.

## External JavaScript

External JS involves creating and storing JS code in a separate file ending with a .js file extension. 
This method helps developers keep the HTML document clean and organised. 
The external JS file can be stored or hosted on the same web server as the HTML document or stored on an external web server such as the cloud.

We will use the same example for external JS but separate the JS code into a different file.

First, create a new file named script.js and save it on the Desktop with the following code:

let x = 5;
let y = 10;
let result = x + y;
document.getElementById("result").innerHTML = "The result is: " + result;

Next, create a new file named external.html and paste the following code (notice that the HTML code is the same as that of the previous example):
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>External JS</title>
</head>
<body>
    <h1>Addition of Two Numbers</h1>
    <p id="result"></p>

    <!-- Link to the external JS file -->
    <script src="script.js"></script>
</body>
</html>


Now, double-click the external.html file and check the results. Do you see any difference? No, the output remains the same as in the previous example.

external.html output in chrome

What we did differently is use the src attribute in the <script> tag to load the JS from an external file. When the browser loads the page, it looks for the script.js file and loads its content into the HTML document. 
This approach allows us to keep the JS code separate from the HTML, making the code more organised and easier to maintain, especially when working on larger projects.

Verifying Internal or External JS

When pen-testing a web application, it is important to check whether the website uses internal or external JS. This can be easily verified by viewing the page's source code. 
To do this, open the page external_test.html located in the exercise folder in Chrome, right-click anywhere on the page, and select View Page Source.

how to view page source in Chrome

This will display the HTML code of the rendered page. Inside the source code, any JS written directly on the page will appear between <script> tags without the src attribute. 
If you see a <script> tag with a src attribute, it indicates that the page is loading external JS from a separate file.

how to view external JS in chrome

For a practical example, visit https://tryhackme.com in your browser and inspect the source code to identify how the website loads the JS internally and from external sources.

Abusing Dialogue Functions
One of the main objectives of JS is to provide dialogue boxes for interaction with users and dynamically update content on web pages. JS provides built-in functions like alert, prompt, and confirm to facilitate this interaction. 
These functions allow developers to display messages, gather input, and obtain user confirmation. 
However, if not implemented securely, attackers may exploit these features to execute attacks like Cross-Site Scripting (XSS), which you will cover later in this module.

We will be using the Google Chrome console in the upcoming exercises.

Alert

The alert function displays a message in a dialogue box with an "OK" button, typically used to convey information or warnings to users. For example, if we want to display "Hello THM" to the user, we would use an alert("HelloTHM");. 
To try it out, open the Chrome console, type alert("Hello THM"), and press Enter. A dialogue box with the message will appear on the screen.

alert in Google chrome


Prompt

The prompt function displays a dialogue box that asks the user for input. It returns the entered value when the user clicks "OK", or null if the user clicks "Cancel". 
For example, to ask the user for their name, we would use prompt("What is your name?");.

To test this, open the Chrome console and paste the following that asks for a username and then greets him.

name = prompt("What is your name?");
    alert("Hello " + name);
Once you paste the code and hit Enter, a dialogue box will appear, and the value entered by the user will be returned to the console. 

prompt dialog box in Google Chrome


Confirm

The confirm function displays a dialogue box with a message and two buttons: "OK" and "Cancel". It returns true if the user clicks "OK" and false if the user clicks "Cancel". 
For example, to ask the user for confirmation, we would use confirm("Are you sure?");. To try this out, open the Chrome console, type confirm("Do you want to proceed?"), and press Enter.

Confirm dialogue box in Google Chrome


A dialogue box will appear, and depending on whether the user clicks "OK" or "Cancel", the value true or false will be returned to the console.

How Hackers Exploit the Functionality

Imagine receiving an email from a stranger with an attached HTML file. The file looks harmless, but when you open it, it contains JS that disrupts your browsing experience. 
For example, the following code will show an alert box with the message "Hacked" three times:

<!DOCTYPE html>
<html lang="en">
<head>
    <title>Hacked</title>
</head>
<body>
    <script>
        for (let i = 0; i < 3; i++) {
            alert("Hacked");
        }
    </script>
</body>
</html>
On the Desktop of the attached VM, create a file called invoice.html and paste the above code. Double-click the file to open it, and the alert message will pop up three times, causing an undesired experience.

invoice.html showing alert dialogue box

Imagine if a bad actor sent you a similar file, but instead of displaying the alert three times, the number is set to 500. You would be forced to keep closing the alert boxes one after another. 
This is a simple example of how malicious JS can be used to create an inconvenience or worse. Therefore, ensuring you only execute JS files from trusted sources is crucial to avoid such an undesired experience.
