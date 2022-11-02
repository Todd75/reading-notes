# Course 201 Class Nine "Forms and JS Events"

## The `<form>` element

The `<form>` element formally defines a form and attributes that determine the form's behavior. Each time you want to create an HTML form, you must start it by using this element, nesting all the contents inside. Many assistive technologies and browser plugins can discover `<form>` elements and implement special hooks to make them easier to use.

## The `<fieldset>` and `<legend>` elements

The `<fieldset>` element is a convenient way to create groups of widgets that share the same purpose, for styling and semantic purposes. You can label a `<fieldset>` by including a `<legend>` element just below the opening `<fieldset>` tag. The text content of the `<legend>` formally describes the purpose of the `<fieldset>` it is included inside.

Many assistive technologies will use the `<legend>` element as if it is a part of the label of each control inside the corresponding `<fieldset>` element. For example, some screen readers such as Jaws and NVDA will speak the legend's content before speaking the label of each control.

## The `<label>` element

The `<label>` element is the formal way to define a label for an HTML form widget. This is the most important element if you want to build accessible forms — when implemented properly, screen readers will speak a form element's label along with any related instructions, as well as it being useful for sighted users. Another advantage of properly set up labels is that you can click or tap the label to activate the corresponding widget. This is useful for controls like text inputs, where you can click the label as well as the input to focus it, but it is especially useful for radio buttons and checkboxes — the hit area of such a control can be very small, so it is useful to make it as easy to activate as possible.

## Event objects

Sometimes, inside an event handler function, you'll see a parameter specified with a name such as event, evt, or e. This is called the event object, and it is automatically passed to event handlers to provide extra features and information.

### Questions

- Why are forms so important in web development?

  Forms help to catch information from the visitors to your website. Also used to place an order or get in touch with the company.

- When designing a form, what are some key things to keep in mind when it comes to user experience?

  Order the form logically, ask questions in a logical order.. present fields in a single column layout. Minimize the # of input fields as much as you can.

- List 5 form elements and explain their importance.

  `<fieldset>` is used to creat groups of widgets with a similar purpose. `<legend>` is used to caption the contents of its parent element. `<label>` is used to formally define a label for a HTML form widget. 
  aria-label =defines a string value that labels an interactive element.

- When using the addEventListener() method, what 2 arguments will you need to provide?

  The name of the event and a function to handle that event.

- Describe the event object. Why is the target within the event object useful?

  You can get the element that fired the event, access the properties of the element, and uss Css on it.

- What is the difference between event bubbling and event capturing?

  With bubbling the event is first captured and handled by the innermost element and then propagated to the outer elements but capturing it is captured by the outermost element and propagated to the inner elements.

## Things I want to know more about

I struggle with constructors and I feel like today is going to be a struggle.

## Resources

[How to structure a web form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)

[Introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

### Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
