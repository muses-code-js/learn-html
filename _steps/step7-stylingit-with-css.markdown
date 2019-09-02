---
layout: step
number: 7
title: "Stylin' with CSS"
permalink: step7/
---

So far our pages look pretty plain.
This is because we haven't specified any styles for them.

When you don't specify any styles, the browser uses its default style for the "look" of the page.
Most browsers use pretty similar default styles.

The system used by webpages to specify styles is called **Cascading Style Sheets** or **CSS**.

Let's create some simple styles for our pages.  

Create a new file called `tinycakes.css` with the following content:

```CSS
html {
  background-color: pink;
}
```

Note the American spelling of colour.  

Now edit `index.html` and each of the recipe pages & add the following line inside the `<head>` section of each page.

```html
<link rel="stylesheet" href="tinycakes.css" />
```

So for example `index.html` would have a `<head>` that looks like:

```html
<head>
  <title>Tiny Cakes!</title>
    <link rel="stylesheet" href="tinycakes.css" />
</head>
```

Refresh the page and it should now have a lovely pink background.

![Homepage with pink background](../assets/css-home-background.png){:title="Homepage with pink background" class="img-responsive imgbox"}

The `<link>` tag tells the page to use `tinycakes.css` as a stylesheet.

Stylesheets are made up of one or more styles.
A style is made up of a **selector** and a list of style **declarations** surrounded by braces.
Each declaration must have a semicolon at the end.

The selector specifies what elements the style applies to.  

The declarations specify the style properties of the elements to set and what value to set them to.

In our example, the selector is `html` and the single declaration is `background-color: pink`.
This obviously sets the background colour of the html element to pink.

There are many style properties that you can set on each element.
You can find a full list of them and how they can be used here:
<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference" target="_blank">https://developer.mozilla.org/en-US/docs/Web/CSS/Reference</a>

<!-- <div class="aside"> -->
### About Colours

There are three different ways you can specify a colour:

1. By using a colour keyword: `pink` is pink
2. By using functional notation: `rgb(255, 192, 203)` is pink
3. By using hexadecimal (HEX) notation: `#ffc0cb` is also pink.

The functional notation uses three values, one for red, one for green, and one for blue, AKA RGB values.
The values are from 0 to 255.
There is also a `rgba` version of this where you can specify a fourth value, a percentage to represent transparency (or **alpha** value).  

The hexadecimal notation has a `#` character followed by three numbers in hexadecimal format to represent the same three red, green, and blue values.

Many graphics apps will let you pick a colour and get the hexadecimal or RGB values for it.
If you Google for colour pickers you will find many apps and web apps that let you do this too.

There is good documentation on colour values here:
https://developer.mozilla.org/en-US/docs/Web/CSS/color_value
<!-- </div> -->


Let's add a style for `<body>`.
Add the following to `tinycakes.css` after the `html` style.

```CSS
body {
  background-color: white;
  max-width: 800px;
  margin: 20px auto;
  padding: 20px;
  font-family: sans-serif;
}
```

Refresh our page.  That looks a bit nicer.  Lets have a look at what we did.

![A pink background and white body background](../assets/css-home-body-bg.png){:title="A pink background and white body background" class="img-responsive imgbox"}

1. We set the background color to white.  
2. We set the maximum width of the body to 800 pixels.  By default `<body>` will have a width of 100% because it is a block element.  Setting `max-width` means it will still try to be 100% but will never go wider than 800px.
3. We use the `margin` property to set the top and bottom margins to `20px` and the left and right margins to `auto`.  The `margin` property is the space around an element. `auto` means it will make both left and right margins equal to the width of the page minus the width of the element.  This effectively centers the element.  Try re-sizing the browser window to see this effect.
4. We set `padding` to `20px`.  Padding is the space between the outer edge of the element and its content.  
5. We specified a sans serif font for the text. By default most browsers use a serif font.  We could have also named a specific font, like "Times New Roman" or "Courier", but if that font doesn't exist on the user's machine then their browser will just use its default font anyway.

Now that we've seen some more examples of style properties let's go to the next step and examine selectors more carefully.
