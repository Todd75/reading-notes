# Course 201 Class Four "HTML Links, JS Functions, and Intro to CSS Layout"

## Hyperlinks

Hyperlinks allow us to link documents to other documents or resources, link to specific parts of documents, or make apps available at a web address. Almost any web content can be converted to a link so that when clicked or otherwise activated the web browser goes to another web address (URL).

A basic link is created by wrapping the text or other content inside an `<a>` element and using the `href` attribute, also known as a Hypertext Reference, or target, that contains the web address.

An attribute you may want to add to your links is title. The title contains additional information about the link, such as which kind of information the page contains, or things to be aware of on the website.

*absolute URL:* Points to a location defined by its absolute location on the web, including protocol and domain name.

*relative URL:* Points to a location that is relative to the file you are linking from, more like what we looked at in the previous section.
*Use clear link wording*

- Screen reader users like jumping around from link to link on the page, and reading links out of context.
- Search engines use link text to index target files, so it is a good idea to include keywords in your link text to effectively describe what is being linked to.
- Visual readers skim over the page rather than reading every word, and their eyes will be drawn to page features that stand out, like links. They will find descriptive link text useful.
- Don't repeat the URL as part of the link text — URLs look ugly, and sound even uglier when a screen reader reads them out letter by letter.
- Don't say "link" or "links to" in the link text — it's just noise. Screen readers tell people there's a link. Visual users will also know there's a link, because links are generally styled in a different color and underlined (this convention generally shouldn't be broken, as users are used to it).
- Keep your link text as short as possible — this is helpful because screen readers need to interpret the entire link text.
- Minimize instances where multiple copies of the same text are linked to different places. This can cause problems for screen reader users, if there's a list of links out of context that are labeled "click here", "click here", "click here".

## Questions

1. To create a basic link, we wrap text or other content inside what element?

Inside of an anchor element `<a>`

2. The href attribute contains what information?

The hypertext refernece contains the web address.

3. What are some ways we can ensure links on our pages are accessible to all readers?

Use clear link wording when making links so screen readers and search engines can find you easily.

## CSS Positioning

Positioning allows you to take elements out of normal document flow and make them behave differently, for example, by sitting on top of one another or by always remaining in the same place inside the browser viewport.

### Static Positioning

Static positioning is the default that every element gets. It just means "put the element into its normal position in the document flow — nothing special to see here."

### Relative positioning

This is very similar to static positioning, except that once the positioned element has taken its place in the normal flow, you can then modify its final position, including making it overlap other elements on the page. Go ahead and update the position declaration in your code: `position: relative;`

### Absolute positioning

Absolutely positioned element no longer exists in the normal document flow. Instead, it sits on its own layer separate from everything else. This is very useful: it means that we can create isolated UI features that don't interfere with the layout of other elements on the page. For example, popup information boxes, control menus, rollover panels, UI features that can be dragged and dropped anywhere on the page, and so on.

This is because top, bottom, left, and right behave in a different way with absolute positioning. Rather than positioning the element based on its relative position within the normal document flow, they specify the distance the element should be from each of the containing element's sides. So in this case, we are saying that the absolutely positioned element should sit 30px from the top of the "containing element" and 30px from the left. (In this case, the "containing element" is the initial containing block.

### z-index

Web pages also have a z-axis: an imaginary line that runs from the surface of your screen towards your face (or whatever else you like to have in front of the screen). z-index values affect where positioned elements sit on that axis; positive values move them higher up the stack, negative values move them lower down the stack. By default, positioned elements all have a z-index of auto, which is effectively 0.

To change the stacking order, try adding the following declaration to your p:nth-of-type(1) rule:
`z-index: 1;`
Note that z-index only accepts unitless index values; you can't specify that you want one element to be 23 pixels up the Z-axis — it doesn't work like that. Higher values will go above lower values and it's up to you what values you use. Using values of 2 or 3 would give the same effect as values of 300 or 40000.

### Fixed positioning

This works in exactly the same way as absolute positioning, with one key difference: whereas absolute positioning fixes an element in place relative to its nearest positioned ancestor (the initial containing block if there isn't one), fixed positioning usually fixes an element in place relative to the visible portion of the viewport. (An exception to this occurs if one of the element's ancestors is a fixed containing block because its transform property has a value other than none.) This means that you can create useful UI items that are fixed in place, like persistent navigation menus that are always visible no matter how much the page scrolls.

### Sticky positioning

`position: sticky;`, which is somewhat newer than the others. This is basically a hybrid between relative and fixed position. It allows a positioned element to act like it's relatively positioned until it's scrolled to a certain threshold (e.g., 10px from the top of the viewport), after which it becomes fixed.

*Questions*

1. What is meant by “normal flow”?

Normal flow is the way block and inline elements are displayed on a page before changes are made to it.

2. What are a few differences between block-level and inline elements?

Block level elements take up the whole line and inline elements do not. Block levels elements cause a new line to appear and inloine elements do not. Block level elements are typically structural think header or footer.

3. ___ positioning is the default for every html element.

Static

4. Name a few advantages to using absolute positioning on an element.

The absolutely positioned element is taken out of the normal document flow and now sits on its own layer.

5. What is a key difference between fixed positioning and absolute positioning?

Fixed positioning fixes an element in place relative to the visible portion of the website so the user can always interact with the element.

## Functions

Functions allow you to store a piece of code that does a single task inside a defined block, and then call that code whenever you need it using a single short command — rather than having to type out the same code multiple times.

### Questions Functions:

1. Describe the difference between a function declaration and a function invocation.

In the declaration you declare what the function is and write the code, but it doesnt start running until you invoke the function.

2. What is the difference between a parameter and an argument?

A parameter is sometimes called an arguement so i dont think there is one.

Anonymous Functions have no name in the parenthesis. You'll often see anonymous functions when a function expects to receive another function as a parameter. In this case the function parameter is often passed as an anonymous function.

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
