---
title: Styling Basics
draft: true
---

### META: Lesson summary
This lesson covers:


- **html:** added classes to tag
- **css:** how to use CSS (inline, style tag, *.css)
- **css:** what is a CSS selector
- **css:** selector based on tag 
- **css:** selector based on class
- **css:** selector based on id
- **css:** selector based on location
- **css:** scoping css using parent classes in selectors
- **css:** using multiple CSS classes
- **css:** using multiple CSS classes
- **css:** background images
- **css:** Box model
- **css:** shorthand css properties (margin, padding, etc)
- **css:** px vs em vs rem







## Styling Basics

> CSS (Cascading Style Sheets) is the code you use to style your webpage. Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.
> - Mozilla Developer Network

**Where do we place our CSS?**

We could place all of our CSS in a `style` tag inside the `head` tag, however this could get out of hand with larger sites where we need many lines of CSS to style our pages.

The `<link>` tag allows us to reference a separate CSS file with a syntax similar to `<link rel='stylesheet' href='/path/to/our/styles.css'>`. When the browser sees this `<link>` tag it will retrieve the CSS file referenced in the `href` attribute and make those styles apply to the page.

So far, with `app-app` we get a `style.css` automatically referenced in our `index.html` and we can place our CSS in that file.

### Selectors

Prior to CSS we had to apply styles to individual HTML tags and repeat these styles for each tag whenever used. With CSS we can _select_ certain elements from the HTML and specify that a set of styles apply to that entire group of tags.

In CSS we use a syntax that specifies a `rule` ([MDN Reference](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics#Anatomy_of_a_CSS_ruleset))

Here is a sample:

![Sample CSS Rule](https://mdn.mozillademos.org/files/9461/css-declaration-small.png)

Let's break down each of the components of a CSS rule

*Selector*: This specfies the elements of the document that this rule will apply to. Selectors have their own very flexible and powerful syntax. We'll come back to that in a minute.

*Declaration*: A single statement that specifies which _property_ you want to _style_.

*Property*: Which styling property of the element you wish to control.

*Property Value*: This gives the specific value of the property. Different properties have different valid values and syntax. For each _property_ you will need to reference the documentation to see the possible values and syntax.

Take care to notice the important parts of the syntax:
- Each rule must be contained within curly braces `{}`
- The property value is separated from the property by a colon `:`
- Each declaration ends in a semicolon `;` to separate it from the others.

**Example**

Lets say you would like to have all `<em>` tags be colored `yellow`, have a background color of `red`, and have a small black border around the text.

The rule's `selector` will be `em` since we are selecting all those tags.

```
em {
}
```

The first _declaration_ will define the text color to be `yellow` -- If we look up [a list of all the possible CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index#Keyword_index) we will see a `color` property.

Looking [at that documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/color#Syntax) you will see many options for *how* to specify the color.
- named colors: _red_, _orange_, _blue_, or _rebeccapurple_
- hex colors: `#009900` (a medium green)
- rgb values: `rgb(128, 0, 0)` (a medium red)
- hsl values: `hsl(30, 100%, 50%)` (orange)
- hex/rgb/hsl can be extended with an `alpha` value that represents how opaque vs transparent it should be.

```
em {
  color: yellow;
}
```

Now lets define the background color. We'll see this is the [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color) property.

```
em {
  color: yellow;
  background-color: red;
}
```

Finally we can define the [border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

```
em {
  color: yellow;
  background-color: red;
  border: 1px solid black;
}
```

With this we will have styled all the `<em>` tags on the page.

### Selecting only *some* of the elements on the page


### Specificity and Precedence

## Linking to External Resources

- Cool game to learn CSS selectors: https://flukeout.github.io/

### Stylesheets

### Images


## Demo: Goonies(or other idea) Fan Page

 - Add images and basic styling of text and colors.

