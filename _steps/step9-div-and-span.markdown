---
layout: step
number: 9
title: div and span
permalink: step9/
---
Ok let's jump back to HTML for a moment and look at two more tags that are really useful with CSS: `<div>` and `<span>`.

`<div>` is a general purpose block element which you can use as a container for related content.
It is most useful to group together content so those elements can be targeted more easily with CSS.
You can also set borders, padding, margins and colours on `<div>`s themselves.

`<span>` is the inline version of `<div>`.

Let's look at how to use them.

## Using `<div>`

If you look at our recipe pages, I want the `<h2>`s, the titles for ingredients, etc. to go right across the white `<body>` area.
Unfortunately we can't do that easily because the reason they don't reach right across is because of the padding set on the body element.

So let's update our CSS to set the left and right padding on `<body>` to 0.

<!-- We could just remove the padding style but we are going to be implementing changes here that assume that it is going to be zero.
Someone might have a browser that doesn't have a zero value for body padding. -->

```css
body {
  margin: 20px auto;
  max-width: 800px;
  background-color: rgba(255, 255, 255);
  padding: 20px 0px;
  font-family: sans-serif;
}
```

Save and refresh and you will see that our headings to what we want them to now.  

[SCREENSHOT]

But we have a new problem, all of our other content is right up against the left and side without any padding.

This is where a `<div>` can help.

Then let's put everything that we want to have padding on either side in a `<div>` with the class of `container`

Let's start with the top content of the page: the home link, recipe title and description:

```html
<body>
  <div class="container">
    <a href="index.html">Home</a>

    <h1>Muffins</h1>

    <p>This recipe makes 12 plain muffins.</p>

    <p>Refer to directions at the bottom for how to modify the recipe for different types of muffins.</p>
  </div>
```

Add the style for `div.container`:

```css
div.container {
  padding: 0px 20px;
}
```

Refresh and now you should see that first part is inset from the edge.

[SCREENSHOT]

Now add a `<div>` with the class of `container` to each of the ingredients, method and variations.

For example, for ingredients:

```html
<h2 class="recipepart ingredients">Ingredients:</h2>
<div class="container">
    <ul>
     <li>2 cups white flour</li>
     <li>1 tablespoon baking powder</li>
     <li>1/2 teaspoon salt</li>
     <li>2 tablespoons sugar</li>
     <li>1 egg, slightly beaten</li>
     <li>1 cup milk</li>
     <li>1/4 cup melted butter</li>
   </ul>
</div>
```

Update each of them (in both the cupcakes and muffins pages) and we should see our content nicely spaced from the edges and the headings going all the way across.

[SCREENSHOT]

But oops, if we look at our homepage we have a problem because we removed the body padding.  

[SCREENSHOT]

Easy to fix, just add `<div>` with class `container` around all the content we want to be inset like this:

```html
<body>
  <div class="container">
    <img src="tinycakes.png" title="Tiny Cakes!" alt="The Tiny Cakes logo, a stylized cartoon cupcake." height="128px" width="128px" />
    <h1 id="sitetitle">Tiny Cakes!</h1>
    <p>
      Welcome to <em>my</em> recipes web site all about <strong>Tiny Cakes!</strong>
    </p>
    <p>
    Here are the recipes that we have:
    </p>
    <ul>
      <li><a href="traditional-cupcakes.html">Traditional Cupcakes</a></li>
      <li><a href="muffins.html">Muffins</a></li>
    </ul>
  </div>
</body>
```

[SCREENSHOT]

Much better.

`<div>` basically gives you a general purpose box that you can put around any elements you want to apply styles to.  It's very useful.

## Using `<span>`

`<span>` is a bit like a `<div>` in that it is a general purpose container, but an inline one instead of a block one.  You can use this to attach styles to any piece of text you want.

Let's do some special formatting for temperatures in recipes.

Add the following CSS:

```css
span.temp {
  font-weight: bold;
  border: 2px solid red;
  background-color: pink;
  border-radius: 15px;
  padding: 5px 8px 4px 8px;
}
```

Now add a `<span>` with the class of `temp` around all the temperatures in the recipes.

Like this:

```html
<li>Preheat oven to <span class="temp">200°C</span> or <span class="temp">180°C</span> fan-forced.</li>
```

[SCREENSHOT]

Any text you want to apply specific styles to just wrap it in a span, give it a class and write a style for the class.
