### Chapter 4 Links (HTML)

- Links are created using the \<a> element.  Specify which page you want to link to using the href attribute.
    * \<a href="http://www.mkgseattle.com">MKG Seattle\</a>
        * full web address is the absolute URL or Uniform Resource Locator.  Made of domain name followed by the path to that page or image.
    
    * *Linking To Other Pages on the Same Site*
        * use a relative URL, no need to specify domain name, just the folder name
        * \<a href="index.html">Home\</a>
            * useful for nav bars, table of contents, menu, etc

- It is a good idea to organize your code by placing pages for each different section into a new folder.  Folders on a website are sometimes referred to as *directories*
    - __Root__: Top level folder.  Contains all of the other files and folders for a website.
    - Structure is like a family tree: Parents, children, grandparents
    - The main homepage for a HTML site is called the __index.html__.  Default is no file name specified.

- Relative Link Type
    * Same folder/: \<a href="reviews.html">Reviews\</a>

    * *Child folder*:  Use a forward slash \<a> href="music/listings.html">Listings\</a>

    * *Grandchild folder*: Use the name of the child folder, followed by a forward slash, then the name of the granchild folder, followed bu another forward slash, then file name.  \<a href="movies/dvd/reviews.html">Reviews\</a>

    * *Parent folder*: Use ../ to indicate the folder above the current one, then file name \<a href="../index.html">Home\</a>

    * *Grandparent folder*: Repeat the ../ to go up two folders, then file name \<a href="../../index.html">Home\</a>

- Email Links
    * \<a href="mailto:jon@example.org">Email Jon\</a>

- Open Links in a New Window
    * Target: \<a href="http://www.imdb.com" target="_blank>Internet Movie Database\</a>

- Linking to a Specific Part of the Same Page #
    * Identify the point in the page that the link will go using the id attribute
        * \<h1 id="top">Film-Making Terms\</h1>
        * \<a href="#arc-shot">Arc Shot\</a>\<br \/>
        * \<h2 id="arc_shot">Arc Shot\</h2>
            * \<p>Text about Arc Shot\</p>

- Linking to a Specific Part of Another Page
    * As long as the other page has id attributes
    * \<a href="http:/www.htmlandcssbook.com/#bottom">

### Chapter 15 Layout

CSS treats each HTML element as if it is in its own box.  This box will either be a block-level box or an inline box.

- __Block level__ boxes start on a new line and act as the main building blocks of any layout.
    * Examples: \<h1>, \<p>, \<ul>, \<li>

- __Inline boxes__ flow between surrounding text.
    * Examples: \<img>, \<b>, \<i>

- Containing element: if one block-level element sits inside another block-level element, the outer block is known as the containing or parent element.  
    * \<div> can be used to group a number of elements together.

#### Controlling The Position of Elements

Specify the position scheme using the __position__ property or __float__.
- *Normal Flow*: (default, position: static;) Every block-levele element appears on a new line, causing each item to appear lower down on the page than the previous one, even if w X h specified.

- *Relative Positioning*: This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom or left of where it would have been placed.  Does NOT affect the position of the surrounding elements.

- *Absolute Positioning*: This positions the element in relation to its containing element.  It is taken out of normal flow, does not affect position of surrounding elements (they ignore the space).  Move as users scroll the page.
    * h1 {
        - position: absolute;
    }

__Box Offset Properties__

To tell the browser how far from the top/bottom or left/right it should be placed.

- *Fixed Positioning*: A form of absolute positioning, but in relation to the browser window and do not move when scrolling.
    * h1 {
        - position: fixed;
    }

- *Floating Elements*: Take out of flow and position far left or far right of a containing box.  Becomes block-level around which other content can flow.
    * z-index: if boxes overlap, allows you to control which box appears on top.

- *position: relative* moves an element in relation to where it would have been in normal flow e.g. top: 10px; left: 100px;

__focus up to pg. 364__

### Chp. 3 Functions, Methods and Objects (JS) pp. 88-99 only

Functions let you group a series of statements together to perform a specific task to help organize code.  
- a way to store the steps needed to achieve a task and can be called when needed by name, stored in a code block, {}
    * function updateMessage() {
    * what to do
    *  }
- paramenters: pieces of info passed to a function (e.g. height/width)
- response expected = return value

__Declaring a Function__
 
 To create a function, give it a name and then write the statements needed to achieves its task inside the curly braces.  
- *function declaration*

- To declare a function, use the __function__ keyword.
- Give the function a __name__ follwed by parenthesis and opening curly brace.
- The statements that perform the task sit in a code block inside the {}

        function sayHello() {
            console.log('Hello!);
        }

Declaring functions that needs information

    function getArea(width, height) { 
    return width * height;
    }

Paramenters - values in the parenthesis, called __arguments__ 

    - Arguments as values
        getArea(3, 5)

Arguments as Variables

    wallWidth = 3;
    wallHeight = 5;
    getArea(wallWidth, wallHeight);

Function declaration creates a function that you can call later in your code, you must give it a name = named functions.

Function expression - if you put a function where the interpreter would expect to see an expression.  The name is usually omitted.

Anonymous function - expression with no name

    var area = function(width, height) {
    return width * height;
    };
    var size = area(3 *4);

In a function expression, the function is not processed until the interpreter gets to that statement.  You cannot call the function before the interpreter has discovered it.

- Immediately Invoked Function Expressions (IFFE)
    - Used for code that only needs to run once w/in a task.  Commonly used as a wrapper around a set of code.  
    - Any variables declared w/in that anonymous function are effectively protected from variables in other scrips that might have the same namen = Scope.

__Variable Scope__

The location where you declare a variable will affect where it can be used w/in your code.  If you declare it w/in a function, it can only be used w/in that function.

- local variable/function level: created *inside* a function using the var keyword.  Local scope or function-level scope, it cannot be assessed outside of the function.
    - uses less memory

- global variable/global scope: created outside the function and can be used anywhere w/in the script.
    - uses more memory

### Article 6 "Reasons for Pair Programming"

The practice of two developers sharing a single workstation to interactively tackle a coding task together.

- Driver: the programmer who is typing and the only on whose hands are on the keyboard.  Handles the "mechanics" of coding managing the text editor, switching files, version control and writing code.

- Navigator: big picture thinker, what comes next, how an algorithm might be converted in to code, while scanning for bugs/typos.  Might utilize their computer as a second screen to look up things, but not writing any code.

Pair programming uses 4 skills: listening, speaking, reading, writing

Benefits:

1.  Greater efficiency - with a higher quality code in the end.
2. Engaged collaboration - more focused than when working along and knowing when to ask for help.
3.  Learing from fellow students - each has different skills sets and can beneift by learning from each other.
4. Social skills - communication is key and working well with others.
5.  Job interview readiness - prep for interviews and show collab and comm style.
6.  Work environment readiness -  Prepped for work and how to deliver a product.   
