# Class 7 Programming with JavaScript

## Control Flow

The control flow is the order in which the computer executes statements in a script. Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops. For example, imagine a script used to validate user data from a webpage form. The script submits validated data, but if the user, say, leaves a required field empty, the script prompts them to fill it in. To do this, the script uses a conditional structure or if...else, so that different code executes depending on whether the form is complete or not:

if (isEmpty(field)) {

  promptUser();

} else {

  submitForm();

}

A typical script in JavaScript or PHP (and the like) includes many control structures, including conditionals, loops and functions. Parts of a script may also be set to execute when events occur. For example, the above excerpt might be inside a function that runs when the user clicks the Submit button for the form. The function could also include a loop, which iterates through all of the fields in the form, checking each one in turn. Looking back at the code in the if and else sections, the lines promptUser and submitForm could also be calls to other functions in the script. As you can see, control structures can dictate complex flows of processing even with only a few lines of code. Control flow means that when you read a script, you must not only read from start to finish but also look at program structure and how it affects order of execution.

## JavaScript Functions

A JavaScript function is a block of code designed to perform a particular task. A JavaScript function is executed when "something" invokes it (calls it).

*Example:*

     function myFunction(p1, p2) {
        return p1 * p2;   // The function returns the product of p1 and p2
    }

## JavaScript Function Syntax

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses (). Function names can contain letters, digits, underscores, and dollar signs (same rules as variables). The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...) The code to be executed, by the function, is placed inside curly brackets: {}


    function name(parameter1, parameter2, parameter3) { 
        // code to be executed
    }

Function parameters are listed inside the parentheses () in the function definition. Function arguments are the values received by the function when it is invoked. Inside the function, the arguments (the parameters) behave as local variables.

## Function Invocation

The code inside the function will execute when "something" invokes (calls) the function: When an event occurs (when a user clicks a button) or When it is invoked (called) from JavaScript code or Automatically (self invoked)

## Function Return

When JavaScript reaches a return statement, the function will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.

Functions often compute a return value. The return value is "returned" back to the "caller"

## Functions Used as Variable Values

Functions can be used the same way as you use variables, in all types of formulas, assignments, and calculations.

Instead of using a variable to store the return value of a function:

     let x = toCelsius(77);
     let text = "The temperature is " + x + " Celsius";

You can use the function directly, as a variable value:

     let text = "The temperature is " + toCelsius(77) + " Celsius";

## Local Variables

Variables declared within a JavaScript function, become LOCAL to the function.

Local variables can only be accessed from within the function.

     // code here can NOT use carName

     function myFunction() {
       let carName = "Volvo";
       // code here CAN use carName
     }

     // code here can NOT use carName

## Types of JavaScript Operators

Aritmetic Operators,
Assignment Operators,
Comparison Operators,
Logical Operators,
Conditional Operators,
Type Operators

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)