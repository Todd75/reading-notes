# Reading Notes Class 6

## JavaScript

JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Apache CouchDB and Adobe Acrobat. JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.

The standards for JavaScript are the ECMAScript Language Specification (ECMA-262) and the ECMAScript Internationalization API specification (ECMA-402). As soon as one browser implements a feature, we try to document it. This means that cases where some proposals for new ECMAScript features have already been implemented in browsers, documentation and examples in MDN articles may use some of those new features. Most of the time, this happens between the stages 3 and 4, and is usually before the spec is officially published.

Do not confuse JavaScript with the Java programming language. Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantics, and use.

## Introduction to JavaScript - basic output

**We can distinguish 3 major parts of what we usually refer to as "JavaScript".**

- The language itself. This is fairly standard among the various environments, both in the various browsers and in the various server-side environments.
- The DOM API - how the language can interact with the various parts of a web page while in the browser. While in this respect the various browsers are getting closer to each other they still differ. Several libraries, most prominently JQuery, is trying to provide a unified API.
- The server API (or just API) provided by Node.js or one of the other server-side systems.

### Embed or include

You can either embed the JavaScript code directly inside the HTML file, or you can put a line in the HTML file that will include the external JavaScript file. In most cases the latter is recommended, but for our first examples, in order to make the whole thing work in a single file, we'll embed the JavaScript code inside some HTML.

In order to do that we add the `<script>` opening and `</script>` closing tags. Between the two we write our JavaScript code.

### Input Output

The very first thing we need to learn is how to interact with the JavaScript code running in the browse. There are a number of way JavaScript can display text for the user (output). The most simple one is by using the `alert` function:

### alert

This will show a pop-up in the browser with the text. (You can click on Try! that will open the specific script in a separate window.) The `alert()` function is actually rarely used, but it is an easy way to show the use of JavaScript.

`<script language="javascript">`

`alert("Hello World");`

`</script>`

### prompt

will show a pop-up window with the text provided as the first parameter and with a textbox the user can fill in. When the user presses OK, the value in the text box will be returned by the prompt() function. Then, in this example we use the document.write method to update the html with the text.

`<script>`

`var name = prompt("Your name:", "");`

`document.write("Hello ", name);`

`</script>`

### confirm

It allows the developer to ask a Yes/No question. Calling the `confirm()` function will show a pop-up window with the provided texts and with two buttons. If the user presses `OK` the `confirm()` function will return `true`, if the user presses `cancel` or hits the `ESC` key, the function will return `false`.

Of course in order for this to make more sense you'll have to understand what `true` and `false` really mean and what this `if - else` construct does. If you have programming background then you probably already understand the code, and even if you don't have programming background you might figure out.

That code can basically be translated to the following English sentence:

`If confirm returned true, print "Hello World", otherwise print "OK, I won't print it."`

Or even better:

`If the user presses OK when we asked "Shall I print Hello World?", then print "Hello World", otherwise print "OK, I won't print it."`

`<script>`
 
`if (confirm("Shall I print Hello World?")) {

    document.write("Hello World");`

`} else {

    document.write("OK, I won't print it.");
}`
 
`</script>`

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)