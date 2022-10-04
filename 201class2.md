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








Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
