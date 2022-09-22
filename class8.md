# Reading Notes Expressions and Operators

## Expressions

At a high level, an expression is a valid unit of code that resolves to a value. There are two types of expressions: those that have side effects (such as assigning values) and those that purely evaluate. The expression x = 7 is an example of the first type. This expression uses the = operator to assign the value seven to the variable x. The expression itself evaluates to 7. The expression 3 + 4 is an example of the second type. This expression uses the + operator to add 3 and 4 together and produces a value, 7. However, if it's not eventually part of a bigger construct (for example, a variable declaration like const z = 3 + 4), its result will be immediately discarded — this is usually a programmer mistake because the evaluation doesn't produce any effects.

## Types of Operators

- Assignment operators
- Comparison operators
- Arithmetic operators
- Bitwise operators
- Logical operators
- BigInt operators
- String operators
- Conditional (ternary) operator
- Comma operator
- Unary operators
- Relational operators

JavaScript has both binary and unary operators, and one special ternary operator, the conditional operator. A binary operator requires two operands, one before the operator and one after the operator:

operand1 operator operand2

For example, 3 + 4 or x * y. This form is called an infix binary operator, because the operator is placed between two operands. All binary operators in JavaScript are infix.

A unary operator requires a single operand, either before or after the operator:

operator operand

operand operator

## Assignment Operators

     Name	Shorthand operator	Meaning
     Assignment	x = f()	x = f()
     Addition assignment	x += f()	x = x + f()
     Subtraction assignment	x -= f()	x = x - f()
     Multiplication assignment	x *= f()	x = x * f()
     Division assignment	x /= f()	x = x / f()
     Remainder assignment	x %= f()	x = x % f()
     Exponentiation assignment	x **= f()	x = x ** f()
     Left shift assignment	x <<= f()	x = x << f()
     Right shift assignment	x >>= f()	x = x >> f()
     Unsigned right shift assignment	x >>>= f()	x = x >>> f()
     Bitwise AND assignment	x &= f()	x = x & f()
     Bitwise XOR assignment	x ^= f()	x = x ^ f()
     Bitwise OR assignment	x |= f()	x = x | f()
     Logical AND assignment	x &&= f()	x && (x = f())
     Logical OR assignment	x ||= f()	x || (x = f())
     Logical nullish assignment	x ??= f()	x ?? (x = f())

## Destructuring

For more complex assignments, the destructuring assignment syntax is a JavaScript expression that makes it possible to extract data from arrays or objects using a syntax that mirrors the construction of array and object literals.

     const foo = ['one', 'two', 'three'];

     // without destructuring
     const one   = foo[0];
     const two   = foo[1];
     const three = foo[2];

     // with destructuring
     const [one, two, three] = foo;

## Comparison Operators

A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically. The sole exceptions to type conversion within comparisons involve the === and !== operators, which perform strict equality and inequality comparisons. These operators do not attempt to convert the operands to compatible types before checking equality. The following table describes the comparison operators in terms of this sample code:

     const var1 = 3;
     const var2 = 4;

## Arithmetic operators

An arithmetic operator takes numerical values (either literals or variables) as their operands and returns a single numerical value. The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/). These operators work as they do in most other programming languages when used with floating point numbers (in particular, note that division by zero produces Infinity). For example:

     1 / 2; // 0.5
     1 / 2 === 1.0 / 2.0; // this is true

## Bitwise Operators

A bitwise operator treats their operands as a set of 32 bits (zeros and ones), rather than as decimal, hexadecimal, or octal numbers. For example, the decimal number nine has a binary representation of 1001. Bitwise operators perform their operations on such binary representations, but they return standard JavaScript numerical values.

Bitwise logical operators: 
Conceptually, the bitwise logical operators work as follows:

- The operands are converted to thirty-two-bit integers and expressed by a series of bits (zeros and ones). Numbers with more than 32 bits get their most significant bits discarded. For example, the following integer with more than 32 bits will be converted to a 32-bit integer:

     Before: 1110 0110 1111 1010 0000 0000 0000 0110 0000 0000 0001

     After:                 1010 0000 0000 0000 0110 0000 0000 0001

- Each bit in the first operand is paired with the corresponding bit in the second operand: first bit to first bit, second bit to second bit, and so on.
- The operator is applied to each pair of bits, and the result is constructed bitwise.

## Bitwise shift operators

The bitwise shift operators take two operands: the first is a quantity to be shifted, and the second specifies the number of bit positions by which the first operand is to be shifted. The direction of the shift operation is controlled by the operator used. Shift operators convert their operands to thirty-two-bit integers and return a result of either type Number or BigInt: specifically, if the type of the left operand is BigInt, they return BigInt; otherwise, they return Number.

## Logical operators

Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value.

- Logical AND (&&)	expr1 && expr2	Returns expr1 if it can be converted to false; otherwise, returns expr2. Thus, when used with Boolean values, && returns true if both operands are true; otherwise, returns false.
- Logical OR (||)	expr1 || expr2	Returns expr1 if it can be converted to true; otherwise, returns expr2. Thus, when used with Boolean values, || returns true if either operand is true; if both are false, returns false.
- Logical NOT (!)	!expr	Returns false if its single operand that can be converted to true; otherwise, returns true.

## Loops and iteration

Loops offer a quick and easy way to do something repeatedly. This chapter of the JavaScript Guide introduces the different iteration statements available to JavaScript.

You can think of a loop as a computerized version of the game where you tell someone to take X steps in one direction, then Y steps in another. For example, the idea "Go five steps to the east" could be expressed this way as a loop:

     for (let step = 0; step < 5; step++) {
       // Runs 5 times, with values of step 0 through 4.
       console.log('Walking east one step');
     }

### The statements for loops provided in JavaScript are:

- for statement
- do...while statement
- while statement
- labeled statement
- break statement
- continue statement
- for...in statement
- for...of statement

### for statement

A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.

A for statement looks as follows:

    for ([initialExpression]; [conditionExpression]; 
    [incrementExpression])
      statement

When a for loop executes, the following occurs:

- The initializing expression initialExpression, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
- The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. Otherwise, the for loop terminates. (If the conditionExpression expression is omitted entirely, the condition is assumed to be true.)
- The statement executes. To execute multiple statements, use a block statement ({ }) to group those statements.
- If present, the update expression incrementExpression is executed.
- Control returns to Step 2.

JavaScript:
Here, the for statement declares the variable i and initializes it to 0. It checks that i is less than the number of options in the `<select>` element, performs the succeeding if statement, and increments i by 1 after each pass through the loop.

    function howMany(selectObject) {
      let numberSelected = 0;
      for (let i = 0; i < selectObject.options.length; i++) {
        if (selectObject.options[i].selected) {
          numberSelected++;
        }
      }
      return numberSelected;
    }

    const btn = document.getElementById('btn');

    btn.addEventListener('click', () => {
      const musicTypes = document.selectForm.musicTypes;
      console.log(`You have selected ${howMany(musicTypes)} option(s).`);
    });

### while statement

A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:

     while (condition)
       statement     

If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.
The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.
To execute multiple statements, use a block statement ({ }) to group those statements.
Return to the Table of Contents: 

[Table of Contents](https://todd75.github.io/reading-notes/)