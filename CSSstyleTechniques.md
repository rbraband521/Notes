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

