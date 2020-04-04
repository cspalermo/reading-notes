### Chp. 5 "Images" pp. 94-125 (HTML/CSS)
 
Good practice to create an Images folder for your website.

__Adding an Image__

    \<img src="image/quokka.jpg" alt="A family of quokkas" title="An Australian marsupial."/>

add width and height:

    \<img src="images/quokka.jpg" alt="A family of quokkas" width="600" heigh="450" />

Placement is important, depending on how they appear.  Before, inside or in the middle of a paragraph.  

Old code: align left and align right, top, middle, bottom.  Should use CSS to control image placement: margin, padding, float.

__3 Rule for Creating Images__
- Save images in the right format: jpeg, gif or png
- Save images in the right size: save the image at the same width and height it will appear on the website (in pixels)
- Measure images in pixels

Format
- .jpeg format: best for color photos
- .gif or .png: images w/few colors or large areas of the same color

Scalable Vector Graphics (SVG)/Vector images - created by placing points on a grid.  Can increase dimensions of the image w/o affecting the quality of it.

Animated GIFS - show several frames of an image in sequence, used to create simple animations.

Transparency: use GIF if part of the image has straigh edges and 100% transparent. Use PNG if image has diagonal/rounded edges or want semi-opaque transparancy or drop-shadow.

\<figure> - element that contains images. Can have more than one images as long as use the same caption.

\<figcaption> - caption of the image

### Chapter 11 "Color" pp. 246-263

The color property allows you to specify the color of text inside an element in 3 ways:

- RGB/RGBA Values: express colors in terms of how much red, green and blue are used to make it up.  eg. rgb\(100,100,90)

- Hex codes: six digit codes that represent the amount of red, green and blue, preceded by a # eg. #ee3e80

- Color names: 147 predefined color names that are recognized by browswers eg. DarkCyan

Background color: sets the color of the background for that box element.

Contrast: When picking foreground and background colors, it is important to ensure there is enough contrast for the text to be legible.  

In CSS3:

- Opacity - specify a value between 0.0 and 1.0 (0.5 is 50% opacity)
- hsl, hsla - 
    * hue expressed as an angle 0-360
    * saturation is a %
    * lightness is a % - 0% is white, 50% normal, 100% black
        * background-color: hsl (0,0%,78%);
    * hsla - add a 4th property of transparency between 0 and 1.0
        * background-color: hsla(0,100%,1005,0.5;)

### Chapter 12 "Text" pp. 264-299

Typeface terminology
- serif: fonts have extra details on the ends of the main strokes of letters (fancy!)
    * Times New Roman
- sans-serif: straight ends to letters, cleaner design
    * Arial
- monospace: every letter is the same width (like fixed-width) (like orca font)
    * Courier

*If you design on a Mac, it is important to check what the typeface looks like on a PC, can render less smoothly.  PC to Mac okay.*

- font-family: specify typeface.
    * website visitors need to have it installed to view the page.  Use several choices: sans-serif, Arial, Verdana, "Courier New",

- font-size: pixels 16px (default); 200% (=32px); ems: equivalent to width of the letter m.

- @font-face: use a font not installed by directing to the source.  Be sure the license allows this.

    @font-family {

    font-family: 'ChunckFiveRegular';

    src: url('fonts/chunckfive.eot'); }

Resource:  www.fontsquirrel.com/fontface/generator
- also provides CSS code for @font-face rule

#### List of Commands

- font-weight: bold, normal
- font-style: italic, normal, oblique (slant)
- text-transform: uppercase, lowercase, capitalize
- text-decoration: none (removes already applied eg link), underline, overline, line-through, blink (flash on/off)
- line-height: aka leading/ledding, gap between lines of text.  Use ems so gap between lines is relative to the size of the text.
- letter-spacing; word-spacing: Kerning or space between letters.  Ems default about 0.25ems
- text-align: left, right, center, justify (every line in a paragraph should take up the full width of the containing box.)
- vertical-align: most common for inline elements like img.  Baseline, sub, super, top, text-stop, middle bottom, text-bottom, lenght, % pg.286
- text-indent: indent the first line of text within an element.  Can also take negative values to push text off the browser window.
- text-shadow: CSS3.  Used to create a drop box shadow, which is dark version of the word behind it and slightly offset.  Or embossed effect.  Complicated, needs 3 length and a color.
- :first-letter, :first-line: pseudo elements, technically not properties to specify different values for the first letter/first line of text inside an element.
- :link, :visited: two psuedo classes.  Link to set styles for linkes that have not yet been visited.  Visited set styles for clicked links.

        a:visited {
        color: back;}

- :hover, :active, :focus: 3 psuedo classes.
    * hover: when user hovers over an element with a pointer device (mouse) 
    * active: being activly used, like when a button is being clicked
    * focus: any element you interact w/can have focus.  eg tab through the interactive items

Attribute Selectors
- Existence [] p[class]
    * matches a specific attribute
- Equality [=] p[class="dog"]
    * matches a specific attribute with a specific value
- Space [--] p[class~="dog"]
    * matches a specific attribute whose value appears in a space-separated list of words
- Prefix [^=] p[attr^"d"]
    * matches a specific attribute whose value begins with a specific string
- Substring [*=] p[attr*"do"]
    * matches a specific attribute whose value contains a specific substring
- Suffic [$=] p[attr$"g"]
    * matches a specific attribute whose value ends with a specific string

