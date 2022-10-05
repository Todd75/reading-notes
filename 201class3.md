# Couese 201 Class 3 "HTML Lists, Control Flow with JS, and the CSS Box Model"

## `<ol>`: The Ordered List element

Represents an ordered list of items — typically rendered as a numbered list. This element also accepts the global attributes type, start, reversed.

### Reversed

This Boolean attribute specifies that the list's items are in reverse order. Items will be numbered from high to low.

### Start

An integer to start counting from for the list items. Always an Arabic numeral (1, 2, 3, etc.), even when the numbering type is letters or Roman numerals. For example, to start numbering elements from the letter "d" or the Roman numeral "iv," use start="4".

### Type

Set the numbering type as follows:

- a for lowercase letters
- A for uppercase letters
- i for lowercase Roman numerals
- I for uppercase Roman numerals
- 1 for numbers (default)

      <ol type="i">

        <li>Cheese</li>

        <li>Salad</li>

        <li>Bacon</li> 

      </ol>
    <ol type="i">
      <li>Introduction</li>
      <li>List of Grievances</li>
      <li>Conclusion</li>
    </ol>

This creates an ordered list in roman numerals

**Nesting Lists:**
   
    <ol>
      <li>first item</li>
      <li>
        second item
        <!-- closing </li> tag is not here! -->
        <ol>
          <li>second item first subitem</li>
          <li>second item second subitem</li>
          <li>second item third subitem</li>
        </ol>
      </li>
      <!-- Here's the closing </li> tag -->
      <li>third item</li>
    </ol>

<ol>
  <li>first item</li>
  <li>
    second item
    <!-- closing </li> tag is not here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
  </li>
  <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>

You can also have ordered or unordered lists inside of ordered or unordered lists.

**Questions:**

1. When should you use an unordered list in your HTML document? You should use one when the order of the list doesnt matter.
2. How do you change the bullet style of unordered list items? By using list-style-type with CSS and changing it.
3. When should you use an ordered list vs an unorder list in your HTML document? Use an ordered list when the sequence matter like for recipes.
4. Describe two ways you can change the numbers on list items provided by an ordered list? By using the start attribute to start at a number other than 1 or by using the reversed attribute and starting in reverse order.

## CSS The box model

Everything in CSS has a box around it, and understanding these boxes is key to being able to create more complex layouts with CSS, or to align items with other items.

In CSS we broadly have two types of boxes — block boxes and inline boxes. The type refers to how the box behaves in terms of page flow and in relation to other boxes on the page. Boxes have an inner display type and an outer display type.

**Outer display type:**
If a box has an outer display type of block, then:

- The box will break onto a new line.
- The width and height properties are respected.
- Padding, margin and border will cause other elements to be pushed away from the box.
- The box will extend in the inline direction to fill the space available in its container. In most cases, the box will become as wide as its container, filling up 100% of the space available.

Some HTML elements, such as `<h1>` and `<p>`, use block as their outer display type by default.

*If a box has an outer display type of inline, then:*

- The box will not break onto a new line.
- The width and height properties will not apply.
- Vertical padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
- Horizontal padding, margins, and borders will apply and will cause other inline boxes to move away from the box.

Some HTML elements, such as `<a>`, `<span>`, `<em>` and `<strong>` use inline as their outer display type by default.

**Inner display type:**
Boxes also have an inner display type, which dictates how elements inside that box are laid out.

Block and inline layout is the default way things behave on the web. By default and without any other instruction, the elements inside a box are also laid out in normal flow and behave as block or inline boxes.

You can change the inner display type for example by setting display: flex;. The element will still use the outer display type block but this changes the inner display type to flex. Any direct children of this box will become flex items and behave according to the Flexbox specification.

## What is the CSS box model?

The CSS box model as a whole applies to block boxes and defines how the different parts of a box — margin, border, padding, and content — work together to create a box that you can see on a page. Inline boxes use just some of the behavior defined in the box model.

To add complexity, there is a standard and an alternate box model. By default, browsers use the standard box model.
Parts of a box
Making up a block box in CSS we have the:

- Content box: The area where your content is displayed; size it using properties like inline-size and block-size or width and height.
- Padding box: The padding sits around the content as white space; size it using padding and related properties.
- Border box: The border box wraps the content and any padding; size it using border and related properties.
- Margin box: The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using margin and related properties.

In the standard box model, if you give a box an inline-size and a block-size (or width and a height) attributes, this defines the inline-size and block-size (width and height in horizontal languages) of the content box. Any padding and border is then added to those dimensions to get the total size taken up by the box (see image below).

## Margins, padding, and borders

### Margin

The margin is an invisible space around your box. It pushes other elements away from the box. Margins can have positive or negative values. Setting a negative margin on one side of your box can cause it to overlap other things on the page. Whether you are using the standard or alternative box model, the margin is always added after the size of the visible box has been calculated.

We can control all margins of an element at once using the margin property, or each side individually using the equivalent longhand properties.
Margin collapsing
Depending on whether two elements whose margins touch have positive or negative margins, the results will be different:

- Two positive margins will combine to become one margin. Its size will be equal to the largest individual margin.
- Two negative margins will collapse and the smallest (furthest from zero) value will be used.
- If one margin is negative, its value will be subtracted from the total.

### Borders

The border is drawn between the margin and the padding of a box. If you are using the standard box model, the size of the border is added to the width and height of the box. If you are using the alternative box model then the size of the border makes the content box smaller as it takes up some of that available width and height.

For styling borders, there are a large number of properties — there are four borders, and each border has a style, width, and color that we might want to manipulate.

You can set the width, style, or color of all four borders at once using the border property.

### Padding

The padding sits between the border and the content area and is used to push the content away from the border. Unlike margins, you cannot have a negative padding. Any background applied to your element will display behind the padding.

The padding property controls the padding on all sides of an element.

**The box model and inline boxes:**
All of the above fully applies to block boxes. Some of the properties can apply to inline boxes too, such as those created by a `<span>` element.

**Using display: inline-block:**
display: inline-block is a special value of display, which provides a middle ground between inline and block. Use it if you do not want an item to break onto a new line, but do want it to respect width and height and avoid the overlapping seen above.

An element with display: inline-block does a subset of the block things we already know about:
- The width and height properties are respected.
- padding, margin, and border will cause other elements to be pushed away from the box.

It does not, however, break onto a new line, and will only become larger than its content if you explicitly add width and height properties.

**Questions:**

1. Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?
The margins can be used to push things away from our box. Whereas padding sits between the border and the content area.
2. List and describe the four parts of an HTML elements box as referred to by the box model.

- You have the content box which is the area where content is displayed.
- You have the padding box whixh is the area between the border and the content.
- There is the border box which wraps the content and the padding.
-And finally you have the margin box which is the outermost layer wrapping the content, padding, and border as white space between this box and other elements.

## Expressions and operators

An **expression** is a valid unit of code that resolves to a value. There are two types of expressions: those that have side effects (such as assigning values) and those that purely evaluate.

The expression x = 7 is an example of the first type. This expression uses the = operator to assign the value seven to the variable x. The expression itself evaluates to 7.

An **assignment operator** assigns a value to its left operand based on the value of its right operand. The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand. That is, x = f() is an assignment expression that assigns the value of f() to x.

*Assigning to properties:*
If an expression evaluates to an object, then the left-hand side of an assignment expression may make assignments to properties of that expression.

### Comparison operators

A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically. The sole exceptions to type conversion within comparisons involve the === and !== operators, which perform strict equality and inequality comparisons. These operators do not attempt to convert the operands to compatible types before checking equality.

### Arithmetic operators

An arithmetic operator takes numerical values (either literals or variables) as their operands and returns a single numerical value. The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/). These operators work as they do in most other programming languages when used with floating point numbers (in particular, note that division by zero produces Infinity).

### Bitwise operators

A bitwise operator treats their operands as a set of 32 bits (zeros and ones), rather than as decimal, hexadecimal, or octal numbers. For example, the decimal number nine has a binary representation of 1001. Bitwise operators perform their operations on such binary representations, but they return standard JavaScript numerical values.

### Logical operators

Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value.

### BigInt operators

Most operators that can be used between numbers can be used between BigInt values as well.
One exception is unsigned right shift (>>>), which is not defined for BigInt values. This is because a BigInt does not have a fixed width, so technically it does not have a "highest bit".
BigInts and numbers are not mutually replaceable — you cannot mix them in calculations.

### String operators

In addition to the comparison operators, which can be used on string values, the concatenation operator (+) concatenates two string values together, returning another string that is the union of the two operand strings.

### Conditional (ternary) operator

The conditional operator is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition.

### Relational operators

A relational operator compares its operands and returns a Boolean value based on whether the comparison is true.

### Basic expressions

All operators eventually operate on one or more basic expressions. These basic expressions include identifiers and literals, but there are a few other kinds as well.
**learn these better**

### Questions

1. What data types can you store inside of an Array?
All data types?
2. List five shorthand operators for assignment in javascript and describe what they do.
The = sign is assignment, the % is remanider assignment, the + sign is addition, the - sign is subtraction, and the && is a logical AND assignment.
3. Give an example of when a Loop is useful in JavaScript.
A loop is useful when you want to force an answer to a question like password until they get it correct.
4. Describe a real world example of when a conditional statement should be used in a JavaScript program.
You could use an if statement for different greeting when someone visits your website based on month, time, year, or whatever you want.

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
