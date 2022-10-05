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


Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
