* block, inline-block, inline
  - block: separate line
  - inline-block: same line separate blocks
  - inline: same line no blocks

### Using fonts
  * Quotes go around font family in CSS declarations
    - font-family: "Gotham Rounded";
    - always create a font stack, incase one isn't installed on the users computer

### If we use Webfonts, it is downloaded automatically
#### Importing your Webfont
@font-face {
  font-family: 'Abolition regular';
  src: url('../fonts/abolition-regular-webfont.woff')
}

### Using the imported web font

h1, h2 {
  font-family: 'Abolition Regular', Impact, Charcoal, sans-serif;
  font-weight: normal;
}

---

# What to use instead of Webfonts
## Google fonts
 * Use it, but don't use too many, it will slow down loading time
 * Google writes the the @font-face automatically
---

### Other Properties

#### line-height
  - refers to space between lines

* Consolidating font styles

Consider the following
```
body {
  font-family: 'Work-sans';
  color: orange;
  font-weight: 300;
  line-height: 1.5;
}
```
This can be rewritten much like with the border properties

```
body {
  color: orange;
  font: 300 100%/1.5 'Work Sans', sans-serif;
}
```
#### letter-spacing
  - It's self explanatory, just keep it in mind

#### text-align
  - left, right, center, justify
  * Center
    - Works best for shorter headers
  * Justify
    - Adjusted so the space on either side is equal/probably avoid


#### HYPHENS
  * Good practice to set `hyphens: auto;` in the main section so words are hyphenated at the end of a line instead of cutoff

#### text-shadow
  * horizontal offset, vertical offset, blur, color
  ``` -10px 5px 0 blue; ```
  * You can stack shadows on top of each other, they are read in order
  * rgba color value will allow you to use opacity (red, green, blue, opacity)

#### box-shadow
  * same as text shadow except it has a fourth value to control the spread of the shadow
  * the INSET keyword creates the shadow inside the box

#### border-radius
  * makes rounded edges
  * can also be consolidated into one declaration
   - first value is the top left
   - horizontal/vertical

#### Adding using CSS
  * Adding content with CSS means it will be ignored by a screen reader
  * Not everything on a webpage is funcitonal content
  * If something is purely decorational, it probably doesn't need to be read by a screen reader
  * Text added this way cannot be selected with the mouse
  * https://css-tricks.com/almanac/selectors/a/after-and-before/

#### Background images
  * position
  * reapeat
    - how often the image repeats y-axis, x-axis, no-repeat
  * background shorthand
    - ``` background: url(.../img/bear.jpg) center / cover no-repeat #454959; ```

  * Blend-modes
    - https://css-tricks.com/almanac/properties/b/background-blend-mode/
    - Not part of the background shorthand, needs to be specified separately
    - background-blend-mode
    - blends your background picture with a color, it's awesome

#### Gradients
  * linear
    - to top
    - to bottom
    - to left
    - to right
    - angle parameters: starts at bottom ```(0deg, orange, papayawhip)```
  * radial
    - don't have to start at center, ```(center at top right, orange, papayawhip)```
  * ```background-image: radial-gradient(orange, papayawhip);```
  * Written in background image because technically the gradient is an img created by the CSS
  ##### Color Stops
  * adding another color in the gradient ```(orange, firebrick, papayawhip)```
    - use % values after each color stop to control where the changes occur
    ```(#b40 0%, #d63 50%, #c51 51%, #e74 100%)```
    - creates shine with the drastic color stop (change) between 50 and 51%
    - use rgba colors to create opacity

#### Vertical Spacing
  ```
  section {
    padding: 4rem 0;
    border-bottom: 1px dashed grey;
  }
  ```

  * This creates space in between each section of the page so the user can clearly see where content ends and starts
  * And adds a slight border


#### calc()
  * https://developer.mozilla.org/en-US/docs/Web/CSS/calc()
  * good for two side by side columns