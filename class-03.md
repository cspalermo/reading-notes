### Chapter 3 Lists

Ordered Lists \<ol>, \</ol>
- \<li> for list items \</li>

Unordered Lists \<ul>, \</ul>
- \<li>, \</li> for list items

Definition Lists \<dl>, \</dl>
- usually conists of a series of terms and their defintions.  
    * inside use \<dt>, \</dt>
    * \<dd>, \</dd> used to contain the definition

Nested Lists - You can put a second list inside an \<li> element to create a sub-list or nested list.
    <p>\<ul>, \<li>\</li>,\<li>,\<ul>,\<li>,\</ul></p>

### Chapter 13 "Boxes 

Box Dimensions 
- Pixels - allow accurately control size
- Percentage - the size of the box is relative to the size of the browswer window or, if the box is encased within another box, it is % of the size of the containing box.
- Ems - the size of the box is based on the size of the of text within it.  
\<div> {
   - height: 300px;
   - width: 400px;
   background-color: #ee3e80; 
}
- min-width, max-width
    - some pages designs expand and shrink to fit the size of the user's screen.  The min-width specifies the smallest a box can be dispayed at when the browser window is narrow..
    - the max-width property idicates the max width can stretch to when the browswer window is wide.
    - \td.description { min-width; 450px; max-width: 650px
    }
- min-height, max-height
    - same as min/max width

- overflow content - the overflow property tells the browswer what to do if the content contained w/in a box is larger than the box itself.
    - hidden property simply hides any extra content that does not fit in the box
- scroll adds a scrollbar to see missing content

- border-width used to control the width of a border, either in pixels or: thin, medium, thick.  
    * border-top-width
    * border-right-width
    * border-bottom-width
    * border-left-width
    * also border-width: 2px, 1px, 1px, 2px

- border-style: solid, dotted, dashed, double, groove, ridge, inset, outset, hidden/none
    * border-top-style
    * border-left-style
    * border-right-style
    * border-bottom-style

- border-color: use RBG, hex codes or CSS color names
    * border-top-color (left, right, bottom)
    * border-color: dark cyan deep pink, dark cyan deep pink;

- border allows you to specify the width, style and color of a border in one property (in that specific order)
    * p { width: 250px; border: 3px dotted #0088dd;}

- padding: how much space between content and its border.  Usually in pixels, sometimes % and ems
    * if width is specified, padding is added onto the width of a box
    * padding-top (right, bottom, left)
    * shorthand:  padding: 10px 5px 3px 1px
    * specify for every element that needs to use it

- margin: controls gap between boxes.
    * if width specified, margin added to width of box
    * margin-top (right, bottom, left)
    * shorthand: margin 20px 10px;
    * specify for every element that needs to use it

- centering content
    * specify width of the box, setting the left and right margins to auto will make the browswer put equal gap on each side of the box.  This centers the box on the page or w/in the element.  
    * specify text-align property on the centered box if you don't want the text inside to be centered
        - margin: 10px auto 10px auto;
        - text-align: left;

- display
    * inline - causes block-level element to act like an inline element
        - li { display: inline;
                margin-right: 10px;}
    * block - inline element to act like block-level element
    * inline-block - causes block level element to flow like an inline element, while retaining other features of a block-level element
    * none - hides an element from a page

- visibility - hide boxes from users, but leaves a space where the element would have been
    * visibility: hidden;

- CSS3 border-image
    * applies an image to the border of any box.  Takes an image and slices it into 9 pieces.
    * Requires 3 pieces of info:
        - URL of the image
        - where to slice the image
        - What to do w/the straight edges: stretch, repeat, round (if don't fit exactly they will)
            * border-image: url("")11 11 11 11 stretch;

- CSS3 box-shadow
    * add a drop-shadow around a box
        - horizontal offset, vertical offset, blur distance, spread of shadow
            * box-shadow: inset 5px 5px 5px #777777;}

- CSS3 Rounded Corners: border-radius
    * border-top-right-radius
    * border-bottom-right-radius
    * border-bottom-left-radius
    * border-top-left-radius
    * shorthand: border-radius: 5px, 10px, 5px, 10px;

- CSS# Elliptical Shapes: border radius
    * to create more complex shapes, you can specify different distance for the horizontal and vertial parts of the rounded corners.
        - border-radious: 80px 50px;
    * or just one corner
        - border-top-left-radious: 80px 50px;

### JS: Chapter 4 Decisions and Loops (pp. 162-182)

- If...else statements allows you to provide two sets of code:
    * one set if the condtion evaluates to true
    * another set if the condition is false
        - if (score >= pass) {
        - msg = 'XDG';
        - } else {
            - msg = 'XDXX';}

- switch statements start with a variable called the switch value.  Each case indicates a possible value for this variable and the code that should run if the variable matches the value.  End with break;

- A series of switch statements all checked even if a match has been found (slower than switch)
- switch: you have a default option is no match.  If a match if found, the code runs; then the break statement stopes the rest of the switch statement running (better peformance that if)

- type coercion: JS can convert date types to complete an operation.  can lead to unexpected values and errors.
- weak typing: the data type for a value can change
- strong typing: specify what data type each variable will be.

- falsy values are treated as if they are false, also as the number 0.

- truthy values can be treated as if they true, also as the number 1.

- short circuit (stop) as soon as they have a result - but they return the value that stopped the processing (not necessarily true or false)

## Loops

Loops check a condition.  If it returns true, a code block will run.  Then checked again until the condition returns a false.

3 common types:
- *For*: run a code for a specific number of times.  Condition is usually a counter to tell it how many times to run
    * for (var i = 0; i < 10; i++) {
        document.write(i);}

- *While*: don't know how many times the code should run.  Will continue to loop as long as the condition is true.

- *Do While*: key difference from while - it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.

Keywords:
- break: termination of the loop and tells the interpreter to to onto the next stmt of code outside the loop.

- continue: stop the current iteration, and then update and check the condition again (if true, runs again)

msg = msg + 'new msg' (+=)






    