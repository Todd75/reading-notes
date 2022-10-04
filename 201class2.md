# Course 201 Class Two "Basics of HTML, CSS & JS"

## The basics: headings and paragraphs

In HTML, each paragraph has to be wrapped in a `<p></p>` element. Each heading has to be wrapped in a heading element `<h1></h1>`.
Yoyu should use structural hierarchy when utilizing the 6 heading tags.

## Semantics

Semantics are relied on everywhere around us & we rely on previous experience to tell us what the function of an everyday object is; when we see something, we know what its function will be.

We need to make sure we are using the correct elements, giving our content the correct meaning, function, or appearance. In this context, the `<h1>` element is also a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

## Lists

### Unordered Lists

Used when the order of the list does not matter. Starts with the element

    <ul>
      <li>Item Name</li>
      <li>Item name</li>
    </ul>

### Ordered Lists

Used when the order of the items on the list does matter.

Starts with the element

    <ol>
      <li>Step One</li>
      <li>Step Two</li>
      <li>Step Three</li>
    </ol>

You can nest one list inside another one. You might want to have some sub-bullets sitting below a top-level bullet.

**Emphasis:** Use the `<em></em>` (emphasis) element to stress the emphasized words. It will show as italics in text but will stress the word in voice as well and that it the reason to use `<em></em>` instead of `<span>`

**Strong Importance:** Use the tag `<strong></strong>` to emphasize the word. It will be bold in written text but the tag can be read by screen readers as well.


`<!-- place comments in html in these tags to keep them from showing in the content -->` or you can use `// and what is behind this on the line in commented out`

## Description lists

The purpose of these lists is to mark up a set of items and their associated descriptions, such as terms and definitions, or questions and answers.
Description lists use a different wrapper than the other list types — `<dl>;` in addition each term is wrapped in a `<dt>` (description term) element, and each description is wrapped in a `<dd>` (description definition) element.

    <dl>
      <dt>term being defined</dt>
      <dd>definition of the term being defined
      </dd>
      <dt>term being defined</dt>
      <dd>definition of the term being defined</dd>
    </dl>

A term may have multiple definitions by using multiple `<dd></dd>` tags with in the `<dt></dt>` tag.

## Blockquotes

If a section of block level content (be it a paragraph, multiple paragraphs, a list, etc.) is quoted from somewhere else, you should wrap it inside a `<blockquote>` element to signify this, and include a URL pointing to the source of the quote inside a cite attribute.

    <p>Here is a blockquote:</p>
    <blockquote
      cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote">
      <p>
        The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong> (or
        <em>HTML Block Quotation Element</em>) indicates that the enclosed text is
        an extended quotation.
      </p>
    </blockquote>

## Abbreviations

 `<abbr>` used to wrap around an abbreviation or acronym. When including either, provide a full expansion of the term in plain text on first use, along with the `<abbr>` to mark up the abbreviation. This provides a hint to user agents on how to announce/display the content while informing all users what the abbreviation means.
 If providing the expansion in addition to the abbreviation makes little sense, and the abbreviation or acronym is a fairly shortened term, provide the full expansion of the term as the value of title attribute.

## Questions

    1. Why is it important to use semantic elements in our HTML?

    It is important because semantic elements have preset styling and help keep the code clean.

    2. How many levels of headings are there in HTML?

    There are six levels of headings in HTML.

    3. What are some uses for the <sup> and <sub> elements?

    The <sup> element can be used in dates and math equations as the sqared, cubed, or etc function. The <sub> can be used in chemical formulas. 
    
    4. When using the <abbr> element, what attribute must be added to provide the full expansion of the term?

    The <title> attribute is used for the full expansion of the term.

## Applying CSS to HTML

Three methods of applying CSS to a document: with an external stylesheet, with an internal stylesheet, and with inline styles.

- **External stylesheet:**
An external stylesheet contains CSS in a separate file with a .css extension. This is the most common and useful method of bringing CSS to a document. You can link a single CSS file to multiple web pages, styling all of them with the same CSS stylesheet.
- **Internal stylesheet:**
An internal stylesheet resides within an HTML document. To create an internal stylesheet, you place CSS inside a `<style>` element contained inside the HTML `<head>`.
- **Inline styles:**
Inline styles are CSS declarations that affect a single HTML element, contained within a style attribute. They should be avoided whenever possible.

## Properties and values

**Properties:** These are human-readable identifiers that indicate which stylistic features you want to modify. For example, font-size, width, background-color.

**Values:** Each property is assigned a value. This value indicates how to style the property.

When a property is paired with a value, this pairing is called a CSS declaration. CSS declarations are found within CSS Declaration Blocks. In the example below, highlighting identifies the CSS declaration block.

## Functions

A function consists of the function name, and parentheses to enclose the values for the function.

## Questions this Section

    1. What are ways we can apply CSS to our HTML?

    We can use inline, internal, or external styling.
    
    2. Why should we avoid using inline styles?

    Because inline styling will superceed any other styling elements you add.

    3. Review the block of code below and answer the following questions:

      1. What is representing the selector?

      H2 represents the selector.

      2. Which components are the CSS declarations?

      color: black;
      padding: 5px;

      3. Which components are considered properties?

      Color and padding are considered properties

## JavaScript Basics

JavaScript is a programming language that adds interactivity to your website.
Variables are containers that store values. You start by declaring a variable with the let keyword, followed by the name you give to the variable.

let myVariable = "nameofvariable";

**String:** This is a sequence of text known as a string. To signify that the value is a string, enclose it in single quote marks.

**Number:** This is a number. Numbers don't have quotes around them.

**Boolean:** This is a True/False value. The words true and false are special keywords that don't need quote marks.

**Array:** This is a structure that allows you to store multiple values in a single reference.

**Object:** This can be anything. Everything in JavaScript is an object and can be stored in a variable. Keep this in mind as you learn.

**Comments:** Comments are snippets of text that can be added along with code. The browser ignores text marked as comments. You can write comments in JavaScript just as you can in CSS:

    /*
    Commented Out
    */

If your comment contains no line breaks, it's an option to put it behind two slashes like this:

    // This is commented out

**Operators:** An operator is a mathematical symbol that produces a result based on two values (or variables).

**Conditionals:** Conditionals are code structures used to test if an expression returns true or not. A very common form of conditionals is the if...else statement.



Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
