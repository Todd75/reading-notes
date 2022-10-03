# Course 201 Class 1 "Foundations of Software Development"

## Clients and servers

**Clients:** are the typical web user's internet-connected devices (for example, your computer connected to your Wi-Fi, or your phone connected to your mobile network) and web-accessing software available on those devices (usually a web browser like Firefox or Chrome). 

**Servers:** are computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser.

In addition to the client and the server we have:

- **Your internet connection:** Allows you to send and receive data on the web. It's basically like the street between your house and the shop.
- **TCP/IP:** Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the internet. This is like the transport mechanisms that let you place an order, go to the shop, and buy your goods. In our example, this is like a car or a bike (or however else you might get around).
- **DNS:** Domain Name System is like an address book for websites. When you type a web address in your browser, the browser looks at the DNS to find the website's IP address before it can retrieve the website. The browser needs to find out which server the website lives on, so it can send HTTP messages to the right place (see below). This is like looking up the address of the shop so you can access it.
- **HTTP:** Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other. This is like the language you use to order your goods.
- **Component files:** A website is made up of many different files, which are like the different parts of the goods you buy from the shop. These files come in two main types:

     1. _Code files:_ Websites are built primarily from HTML, CSS, and JavaScript, though you'll meet other technologies a bit later.
     2. _Assets:_ This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.

### Explanation of what happens when you type a web address into your browser

1. The browser goes to the DNS server, and finds the real(numerical) address of the server that the website lives on.
2. The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client. This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.
3. If the server approves the client's request, the server sends the client a "200 OK" message and then starts sending the website's files to the browser as a series of small chunks called data packets.
4. The browser assembles the small chunks into a complete web page and displays it to you.

## Order in which component files are parsed

- The browser parses the HTML file first, and that leads to the browser recognizing any `<link>`-element references to external CSS stylesheets and any `<script>`-element references to scripts.
- As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from `<link>` elements, and any JavaScript files it has found from `<script>` elements, and from those, then parses the CSS and JavaScript.
- The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.
- As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JavaScript, a visual representation of the page is painted to the screen, and the user sees the page content and can begin to interact with it.

### JavaScript Basics

A powerful programming language that can add interactivity to a website.

_Variables:_ are containers that store values. You start by declaring a variable with the let keyword, followed by the name you give to the variable.

**JavaScript is case sensitive.** When you have issues remember this and check your variable names.

_Comments:_ are snippets of text that can be added along with code. The browser ignores text marked as comments. You can write comments in JavaScript just as you can in CSS. use `/* */` to open and close comments or `//` and everything behind it is a comment.

_Operators:_ Mathmatecial symbols that produce a result based on tw or more inputs.(numerical or variables)

_Functions:_ Are a way of repackaging code you want to resue or recall later. The use of functions saves time and helps keep the code clean.

## Intro to HTML

HTML(HyperText Markup Language) is a markup language that tells web browsers how to structure the web page you are viewing.

The HTML Element is made up an opening tag, attributes, content, and a closing tag. 

**JavaScript running order:** When the browser encounters a block of JavaScript, it generally runs it in order, from top to bottom. This means that you need to be careful what order you put things in.

**Dynamic versus static code:** The ability to update the display of a web page/app to show different things in different circumstances, generating new content as required whereas Static code shows the same content all the time.

**Interpreted versus compiled code:** In interpreted languages you don't have to transform the code into a different form before it is ran, but in compiled languages are transformed or "compiled" into another form before that code is ran by the computer.

## Things I want to know more about

- The different use cases for internal vs external JavaScript on web pages.
- When do we use inline JavaScript as it is said to be bad practice but we are shown how to do it.
- Need more explanation on JavaScript "Script Loading" strategies and the use of "event listeners" to properly place the script in our HTML
- Detailed explanation of async and defer and when/how to knopw to use them.
- Comments... how do I make and leave good ones in my code? What should the comment be about? How specific about the changes I made?

**Questions Related to "How the Web Works" Reading:**

    1. Compose a short poem describing how HTTP sends data between computers.

     The browser you are using contacts the DNS and finds the website's numerical address. Then the browser uses HTTP request to contact the server asking it to send a copy of the website back to the client side. If the server approves the request it send small chunk of data called packets back to the client. The client's browser reorders the packets into the correct sequence and displays the web page.(I am not sure this actually qualifies as a poem)

    2. Describe how HTML, CSS, and JS files are “parsed” in the browser.
     
     The HTML is parsed first. This allows for links to CSS and JavaScript files to be recognized. The browser uses data from those files to build a Document Object Model(DOM) tree and a CSS Object Model(CSSOM) structure from the parsed CSS files. It also compiles and executes the parsed JavaScript. The browser as it builds the DOM file is also executing the CSS styling and executing the Javascript which builds the inteactive web page.
    
    3. How can you find images to add to a Website?

     You can use Google to find Creative Commons licenses or public domain photos to use. You could also use personal images you took and own the copyright to if they are appropriate to the project. 
    
    4. How do you create a String vs a Number in JavaScript?
     
     You enclose the string with single quotation marks where as a number does not have quotations around it.
    
    5. What is a Variable and why are they important in JavaScript?
     
     A variable is a container that stores values. They are imprortant because they allow you to assign a name to any vale you desire and recall it later in the code. This can save time and keep your code clean.

**Questions related to HTML reading:**

    1. What is an HTML attribute?

     An HTML attribute is a part of the element that contains extra information about the elemnet that will not show up in the content.
    
    2. Describe the Anatomy of an HTMl element.

     The element starts with an opening tag followed by the attribute within the opening tag if the element has an attribute. After the opening tag is the content followed by the closing tag.

    3. What is the Difference between <article> and <section> element tags?

     The <article> element tag is a more specific kind of <section> tag that refers to a specific self-contained or independent block of related content.

    4. What Elements does a “typical” website include?

     It would include a head which contains metadata about the document. It would also include a body section. The body would have the header, all the content a viewer sees, and the footer included in it.

    5. How does metadata influence Search Engine Optimization?

     The type and amount of data you include could greatly influence serch engine results. Without a correct name and description you could be left out of relevant searches. Well defined metadata could increase you hits in searches. Adding things like author's name could drive traffic toward your site.

    6. How is the <meta> HTML tag used when specifying metadata?

     It is used as a self-closing tag style.

**Miscellaneous Questions:**

- What is the first step to designing a Website?

   _Project ideation is the first step of designing a website._

- What is the most important question to answer when designing a Website?

  _Thinking about what you intend to accomplish with the website by listing the goals you are trying to attain and ordering them by importance._

- Why should you use an `<h1>` element over a `<span>` element to display a top level heading?

  _You shoulod use an `<h1>` element over a `<span>` element because the `<h1>` element is a semantic element tag and has preset default sizes that will make it look like a header automatically on your web page whereas the `<span>` element is just a container with no preset styling._

- What are the benefits of using semantic tags in our HTML?

  _The benefits are that semantic tags come with preset styling and give tags roles which helps to keep the code clean and makes styling easier/faster._

- Describe 2 things that require JavaScript in the Browser?

  _Two things that require JavaScript in our browser are dynamically updating content and animated images._

- How can you add JavaScript to an HTML document?

  _You can add JavaScript to an HTML document by using the `<script>` element this can be done internally or externally._

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)