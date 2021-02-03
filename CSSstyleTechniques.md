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