1. While vs Do...While
While Statement
The while statement executes a block of code repeatedly as long as a specified condition evaluates to true.
The condition is checked before executing the code block. Therefore, if the condition is initially false, the code inside the loop will not execute at all.
Do...While Statement
The do...while statement executes a block of code once before checking the condition. If the condition evaluates to true, the loop continues executing.
Unlike the while loop, the do...while loop always executes its code block at least once, even if the condition is initially false.
Main Differences

Feature	while	do...while
Condition checking	Before execution	After execution
Minimum executions	Zero	One
If the condition is initially false	The code is skipped	The code executes once
Typical use	Repeat while a condition is true	Execute once, then repeat if needed
Source:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while.
Source:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while.

Example

let i = 0;

while (i < 3) {
  console.log(i);
  i++;
}

Output:

0
1
2

The loop checks the condition before each iteration.
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 3);

Output:
0
1
2

The output is the same in this example, but the execution order differs.
When the condition is initially false:
let i = 5;

while (i < 3) {
  console.log(i);
}


Output: Nothing.
let i = 5;

do {
  console.log(i);
} while (i < 3);


Output:
5


Conclusion: Use while when the loop should only run if the condition is true from the beginning. Use do...while when the code must execute at least once.


2. If vs Switch
If Statement
The if statement executes a block of code when a condition is truthy. The optional else block executes when the condition is falsy. Multiple conditions can be checked using else if.
It is useful when decisions depend on comparisons, ranges, or complex logical conditions.
Switch Statement
The switch statement evaluates an expression and compares its result against multiple case values. When a matching case is found, its code executes.
The break statement normally stops execution from continuing into subsequent cases. The optional default case handles situations where no case matches.

Source:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else.
Source:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch.


Main Differences
Feature	if...else	switch
Conditions	Supports complex Boolean expressions	Matches an expression against case values
Comparisons	Supports >, <, >=, ===, and logical operators	Uses strict equality to match case values
Multiple alternatives	Uses else if	Uses multiple case clauses
Default behavior	Uses else	Uses default
Stopping execution	Executes the selected branch	Usually uses break to prevent fall-through
Example Using If...Else
let score = 85;

if (score >= 90) {
  console.log("Excellent");
} else if (score >= 75) {
  console.log("Very Good");
} else if (score >= 50) {
  console.log("Pass");
} else {
  console.log("Fail");
}


Output:
Very Good


Explanation: The conditions are checked in order. Since 85 >= 75 is true, the program prints "Very Good" and skips the remaining branches.
Example Using Switch
let day = 2;

switch (day) {
  case 1:
    console.log("Sunday");
    break;
  case 2:
    console.log("Monday");
    break;
  case 3:
    console.log("Tuesday");
    break;
  default:
    console.log("Invalid day");
}


Output:
Monday


Explanation: The value of day matches case 2, so "Monday" is printed. The break statement exits the switch block.
When Should You Use Each?
- Use if...else when checking ranges, validating input, or evaluating complex conditions.
- Use switch when one value needs to be compared against several specific alternatives, such as menu options, status codes, or days of the week.
Conclusion: Both statements control the flow of a program, but if...else is more flexible for different types of conditions, while switch can make multiple fixed-value choices easier to read.

References — MDN Web Docs
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while.
2. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while.
3. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else.
4. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch.
5. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration.

