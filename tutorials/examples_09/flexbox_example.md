# Flexbox example explained

[w3schools CSS3 flexbox](https://www.w3schools.com/css/css3_flexbox.asp)
Explore `display: flex` declaration, `flex-wrap` property, `order` property

### Start with valid HTML5 document.  This is a standard content layout, with header, footer, navigation, article and aside.

```html
<body>
  <header><h1>Page Heading</h1></header>  
  <nav>
      <a href="#">Article One</a>
      <a href="#">Article Two</a>
      <a href="#">Article Three</a>
      <a href="#">Article Four</a>
  </nav>  
  <article>
    <h1>Article Heading</h1>
    <p>Lorem ipsum dolor sit amet, ... clus et quam.</p>
    <p>Sed aliquam id ligula ac ...nec aliquet.</p>
  </article>  
  <aside>
    <h5>Aside Heading</h5>
    <p>Vivamus in ex neque. Maecenas ... pulvinar in sed elit.</p>
  </aside>	
  <footer><address>SYST10049 Web Development © Sheridan College</address></footer>
</body>
```
Figure 82. ![](flex82.png)


### Styling

* change the value of box-sizing and set outline for all elements.  (at the end remove the outline declaration)

Figure 83. ![](flex83.png)


* set font-family to "Lucida Sans",sans-serif for HTML selector
* set padding to 0, margin to 0, and display to block for BODY, HEADER, FOOTER, NAV, ARTICLE, ASIDE, and A
* set padding to 1em for HEADER and FOOTER (this is redefinition)
* set the background color to #93c and foreground color to #fff for HEADER (note that we are trying to reduce the number of declarations)
* set padding to 0.5em for ARTICLE, ASIDE, and A when descendant of NAV

Figure 84. ![](flex84.png)


* set margin to 0.5 em, background color to #33b5e5, text color #fff, and box shadow for A when descendant of NAV

```css
/* note that there are two shadows declared, separated by a comma */
box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24)
```

* set background color to #09c for A when descendant of NAV, when the hover event occurs

Figure 85. ![](flex85.png)

## Flexbox

* BODY is the parent container of HEADER, FOOTER, NAV, ARTICLE, and ASIDE. Add the rule

```css
body { 
  /* body container allowing flex properties */
  display: flex;  
  /* The wrap value specifies that the flex items will wrap */
  flex-wrap: wrap;
}
```

Figure 86. ![](flex86.png)

* you can easily change change the order of the elements; for example, if you want the navigation on the right and aside on the left:

```css
body > header  { order: 1; width: 100%; }
body > nav     { order: 4; width: 20%; }
body > article { order: 3; min-width: 12em; flex:1; }
body > aside   { order: 2; width: 30%; }
body > footer  { order: 5; width: 100%; }
```
Figure 87. ![](flex89.png)


## Media Query
* All rules nested inside the media query will be applied when all conditions are met, in this case, it can be any media ( ) and the width of the screen is at least 799 pixels


```css
@media all and (min-width: 799px) {
}
```

Figure 87. ![](flex87.png)

* When the above conditions are not met (showing width of screen less than 799 pixels), the flexbox declarations are not applied.


Figure 88. ![](flex88.png)

---
> SYST10049 Web Development @ Sheridan College



