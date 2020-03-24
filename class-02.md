## Chapter 2 \"Text"
- \<abbr> if you use an abbreviation or acronym.  A title attribute on the opening tag is used to specify the full term.
    - \<p>\<abbr title\="Professor">Prof\</abbr> Stepehn Hawing is a theoretical physicist\</p>
- \<cite> element can be used to indicate where the citiation is from such as a book title

- \<dfn> element is used to indicate the defining instance of a new term.

- \<address> specific use: to contain the contact details for the author of the page

- \<ins>,\<del> can be used to show content that has been inserted into a doc.  \<del> element usually has a line through it

- \<s> indicates something that is no longer accurate or relevant, but should not be deleted.  Visually, the content of a \<s> element will be displayed with a line through it.

## Chapter 10 Introducing CSS

The key to understanding how CSS works is to imagine that there is an invisible box around every HTML element.

- Block level elements look like they start on a new line including \<h1>, \<h6>, \<p>, \<div>

- Inline elements flow within the text and do not start on a new line, examples \<b>, \<i>, \<img>, \<em>, \<span>

CSS works by associating rules with HTML elements.  These rules govern how the content of a specified element should be displayed.  A CSS rule contains two parts: a selector and a declaration.  P=selector, font-family=declaration

    p {
        font-family: Arial;
    }

Declarations are split into two parts (a property and a value) and are separated by a colon.  EX.  color: yellow (color/property; yellow/value)

Using Internal CSS

- \<link> can be used to tell the browswer where to find the CSS file.  An empty element, no closing tag needed and lives inside the HEAD element.  It has 3 attrbutes:
    * \<href>="css/style.css" type=text/css" rel="stylesheet" />
    * type specifies the type of document being linked to, text/css
    * rel sepcifies the relationship between the HTML page and file it is linked to.  The value should be stylesheet when linking to a CSS file.
- \<style> in the HEAD element, can place CSS rules inside the element
    * style type="text/css"
- Common CSS Selectors
    * Universal \* {}
    * Type h1, h2, etc
    * Class .note {}
    * ID \#introduction {}
    * Child li>a {}
    * Descendent p a {}
    * Adjacent Sibling h1+p {}
    * General sibling h1~p {}

If two selectors are identical, the latter of the two will take precendence.  If one selector is more specific than the others, the more specific rule will take precendence over more general ones.  You can create generic rules that apply to mose elements and the override the properties on individual elements.

### Chapter 2 Basic Javascript Instructions

A script is a series of instructions that a computer can follow one-by-one.  Each individual instruction is known as a statement.  Statements should end with a semicolon.  

Before you can use a variable, you need to announce you want to use it.  This involves creating a variable and giving it a name.  Programmers say that you declare a variable.  Tell it what info you would like it to store.  Assign a variable.

var quanitity = 3; 

- Data types
    * Numeric
    * String - letters and other characters
        - "Hi, Ivy!"
    * Boolean - true or false

- Array - stores a list of values or a set of values that are related to each other, such as a shopping list.
    * Array literal - var followed by array name, the values are assigned inside [] separated by a comma.
    * Array constructor - uses new keyword followed by Array ();
        - var colors = new Array ('white');
    * Values start at 0 not 1 (index value)

- Concatenation - process of joining together two or more strings to create one new string

### Chapter 4 Decisions and Loops

Conditional statement - based on a concept of if/then/else; *if* a condition is met, *then* your code executes one or more statements, *else* your codes does something different.

- == is equal to
- != compares two values to see if they are *not* the same
- === strict equal to
- !== strict not equal to, to check that both data type and value are not the same.

- Logical Operators - allow you to compare the results of more than one comparison operator
    * && Logical and; tests more than one condition.  If both expressions evaluate to true, then the expression returns true.  If one returns false, then the expression is false.
    * || (pipes!) Tests at least one condition.
    * ! Logical not - takes a single Boolean value and inverts it.  
- Logical expression are read left to right.  If the first condition cna provide enough info to get the answer, there is no need to eval the second. 
- IF statements evaluate a condition.  If the condition evaluates to true, any statementsin the subsequent code block are executed.
    * if false, the statements in the code block are not run.
- ELSE IF statements checks a condition.  If it resolves to true the first code block is executed.  If the condition resolves to false, the second code block is run instead.

    * if (score >=50) { congratulate();}
    * else { encourage();}







