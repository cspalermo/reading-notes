### Chapter 3 "Object Literals" pp. 100-105

What is an object?  Objects group together a set of a variables and functions to create a model of something you would recognize from the real world.  In an object, functions and variables take on new names. 

- In an object: variables become knowns as *properties*.  Properties tell us about an object, such as the name of a hotel or the number of rooms.

- In an object: functions become known as *methods*.  Methods represent tasks that are associated with the object.  Example: check how many rooms are available by subtracting the # of booked rooms from the total number of rooms.

Example:  The object represents a hotel.  It has five properties and one method.  The object is in curly braces.  It is stored as a method.

    var hotel = {
        names: 'Quay';
        rooms: 40;
        booked: 25;
        gym: true;
        roomTypes: ['twin', 'double', 'suite'];

        checkAvailability: function () {
            return this.room - this.booked;
        }
    }
Also literal notiation.
 
- In an object, properties and methods have a name and a value, called a *key*.

You can access the properties or methods of an object using a dot notation.  You can also access properties using square brackets.

    var hotelName = hotel.name;
    var roomsFree = hotel.checkAvailability();

    var hotelName = hotel['name'];
    var roomsFree = hotel ['checkAvailability'];

### Chapter 5 "Document Object Model" pp. 183-242

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.  A separate set of rules.
    * Application Programming Interface (API)- lets programs and scripts talk to each other.

Consists of 4 nodes:
- *document node*: at the top of the tree. It represents the entire page and also corresponds to the document object.  When you access any element attribute, it is the starting point for all visits to the DOM tree.

- *element node*: HTML elements describte the structure of an HTML page: h1-h6, etc.  To access the DOM tree, you start by looking for elements, then you can access its text and attribute nodes.

- *attribute node*: the opening tags of HTML elements can carry attributes and are represented by attribute notes.  NOT children of the element that carry them, they are part of the element.

- *text node*: Once you have accessed the element code, you can then reach the text w/in the element.  This is stored in its own text node.  Cannot have children.

Accessing and updating the DOM element tree involves two steps:
1. Locate the node that represents the element you want to work with. eg: getElementbyId(), getElementbyClassName(), etc.
2. Use its context, child elements and attributes, ed nodeValue.

Nodelists: look like arrays, but are collections. () to retrieve items or array syntax.

### Article: Understanding the Problem Domain is the Hardest Part of Programming

- Programmers are often not given complete information about the problem domian, so we don't even have the info we need to understand it.

- Understanding the problem is the most critical piece to the equation.  It is very difficult to solve a problem before you know the question.

- Do 2 things to make understanding easier:
    * make the problem domain easier
    * get a better understanding of the problem domain
    * often beneifical to take a part of the problem and fully understand that part before expanding the problem domain.

