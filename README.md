### Names of people you have worked with on this assignment

* **Sara Morell (shmorell)**
* Amy Chew (amychew)
* Elizabeth Brown (elibrown)
* Kara Dailey (kadailey)
* Annabelle Tsai (altsai)

## Questions & code instructions

### The first questions address the `jsPracticeLab.html` file.

* **What does a code comment look like in JavaScript? What character/s do you have to put before a comment?**

To provide a code comment in JavaScript, a coder must put "//" before their comment. Any line that begins with "//" can include relevant information that the computer will know not to run.

* **Explain what needs to happen to get a JavaScript program to "run", given the JavaScript you've seen in this assignment.**

You need a script tag, which is where you include the Javascript code itself. This looks like:

```js
"<script> some code here </script>"
```
You also need an "onload" command, which runs the function that you used in your script. I commented out the onload command and it ran the html code without the JavaScript changes.

* **What functions in JavaScript seem to be similar in function to the `print` function in Python? (There are two.) Why might you use one and not the other? Explain briefly.**

alert() and console.log() are the two functions that seem to be printing information on the website. The alert function creates a popup. In the case of our code, it makes the word "hello" appear as a popup. Console.log prints information directly to the website.

* **What code would have to comment out to get rid of the pop-up box when you load the page? (Related to the last question.) Do that in the code file, and then, add code so that a text box will appear that contains the current date and time! *HINT:* Look through the rest of the code first...**

We would comment out alert() to get ride of the popup box. We would put in "new Date()" into the alert()
 command so that it prints out the current date and time. (See my code for the relevant edits).

* **How can you put your own name at the top where it currently says "A name"? Explain very briefly how to do so, and replace `A name` in the web page with your own name.**

To replace that code with my name, I would need to put "Sara" in quotations after:
```js
 document.querySelector('h1').innerHTML =.
```

This assigns "Sara" to the position of h1, which I googled and found out means header 1. So I would assume that explains why "Sara" ends up at the top of the page.

* **What does the word `document` represent in this code? Explain briefly.**

It refers to the document we're using for this code. It serves a similar purpose to the word "self" in Python. I figured this out, because "document.querySelector" seems to appear every time we're assigning a new value. So I would assume that it is calling the document, via the query and telling it what to change.

* **What is happening in line 12 (
		`document.querySelector('#items').innerHTML = document.getElementsByTagName('li').length`
)? Explain, briefly (<= 2 sentences).**

It's assigning to the "items" id the number of elements that are tagged "li." It does this by using the "getElementsbyTagName" function, which finds all of the elements in the code that are listed between ```js"<li> </li>."``` It then finds the length of that list of items, using ".length," which allows us to count the number of items included in these lists.

* **What color would the background of this page be <u>if there were no JavaScript in this page</u>?**

The background color would become white. We can check this by commenting out the line:
```js
body.style.background = "#CCEE00";
```

However, I have changed this line to:```js body.style.background = "#CCEE00"; ``` because my group in class decided that color was prettier.

* **Why are there a couple of gray boxes on the screen with a different colored border? How could you edit this code to make them a different color? Explain briefly. Then edit the code to make those boxes some shade of blue, of your choosing.**

The gray boxes with white borders are created by the code within the section labeled "p{}." This seems to create a new section of the webpage, with a specific colored background and border. The border color is different, because of the line:

```js
border: 3px solid #FFFFFF;
```
We can edit this code to make the box a different color, by changing the hexcode for the color listed after "background-color". Our code now has boxes with a nice turquoise background.

* **Edit the code so that, if you highlight `McGill University` and copy it, you see the text `O Canada` near the bottom of the page. Briefly explain why you made the edits that you did -- how did you know/figure out what to do?**

To edit the code to make copying "McGill University" say "O Canada," I looked at the code that made Michigan say "Go Blue!" I created a similar function, which I called "copyLocation()." This function consists of the line:

```js
document.querySelector('#canada').innerHTML += "O Canada<br>"
```
This line of code queries the document and assigns the id "#canda" to the string "O Canada." The += line, I would assume adds the string to the webpage. This explains why you can add as many "O Canadas" as you want, by simply continuing to copy McGill multiple times.

* **In the original code, when you click the button that says `Wow`, you see a text box! Wow. Explain briefly in your own words why the following code causes that to happen:**

```js
function handleClick(){
	alert("hello");
}
```
**and**

```js
<button onclick=handleClick() id="wow-button">Wow</button>
```
We have already talked about how the alert function causes a popup of the string that appears in the function. So the handle click function causes a "hello" alert to pop up.

The "button" tag seems to create the button on the website. Then it calls the function "handleClick" by assigning the function to a variable called "onclick." It would make sense that "onclick" causes the function to occur when the button is clicked.

The id assigns the name of the button to be "wow-button." The text in between "<button></button>" is the text that will display on the button. In this case, it is "Wow."

* **Knowing what you learned from the previous question, add code/markup to the `jsPracticeLab.html` file *so that* there is a button with the text `Spring Equinox 2019` on it somewhere on the page, and when that button is clicked, a text box containing the text `March 20, 2019` appears. (There's no function -- that I am aware of -- to automatically get this info, you've got to type it yourself.)**

See my edited jsPracticeLab for the changes made to the code. The Spring Equinox 2019 button appears next to the Wow button the webpage.

### The next few questions address the `jquerylib_submit_example.html` file.

* **When you enter input that isn't valid, you see an error that is red. Why is the error in red? Why is the response for valid inputs blue?**

The error color is red because in the section denoted "<style></style>," there is a line that says:

```js
.error{
        color: red;
    }
```

The response inputs are blue, because similarly there is a line that says:

```js
.good {
		color: blue;
}
```

Later in the code, when it is creating those response messages, it is assigning them to the classes "error" and "good."

* **What is this line `var regex = /^[a-zA-Z]+$/;` helping with? And if you googled something to figure that out, what did you google, and what, briefly, did you learn? (If you didn't need to google, you can leave that out, but explain briefly what that line is helping the program do, anyway.)**

It is telling the computer that the variables inputed into the phrase box have to be either within a-z OR A-Z. I.e. they can be uppercase or lowercase, but they must be letters. Regex (short for regular expressions) tends to refer to the type of expression, and a-z means "lowercase letters" and "A-Z" means "uppercase letters."

* **What's different about the syntax of conditional statements in JavaScript, compared to Python?**

In JavaScript, if statements are immediately followed by (), which is where you put the body of the if statement. After the if statement is complete, you put {}, which is where you tell the computer what should happen if the if statement is true or false.

* **What do you think the `10000` refers to in the code `.fadeOut(10000)`?**

.fadeOut(10000) comes immediately after two lines of code. The first is the error message and the second is the message that tells you that you submitted the correct thing. It appears immediately after ".show," which I assume shows the value. Therefore, I would expect that fadeOut tells the computer to remove the message either after a certain number of iterations or a certain amount of time and the 10000 likely refers either to time or iterations.

I am unsure of this, because I cannot understand why the red error message remains on the page until you type in another phrase and yet the blue non-error message fades away immediately.

* **What do you think is going on with the following code at the beginning of the program? Note that the most important thing to do for answering this question is to be thoughtful and clear, not to be absolutely correct:**

```js
$(document).ready(function(){}
    $("form").submit(function(event)
```
This line of code occurs within the JavaScript "<script></script>" and so is part of the code telling the website what to do. It starts with "document," which serves a similar purpose to self, so I would guess that it's calling the code to be ready for use to change the html code. Then the second line of code includes the word form in quotations with ".submit" afterwards. I would assume this allows the computer to submit the text that is written into the input as an event.

* **Add some code to the `jquerylib_submit_example.html` file so that, if the input is valid and is specifically the text `hello`, rather than the visible output being `Nice!` in blue, the visible output should be `Hello to you too!`, also in blue, just like `Nice!` is.**
	* *HINT:* You'll have to make some changes to the conditional statement, and possibly look up some JavaScript conditional syntax. You'll also need to look carefully at what generates visible output right now.

See my code for jquerylib_submit_example.html for how I edited the code to say "Hello to you too!"
