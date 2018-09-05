---
layout: step
number: 5
title: Formatting Recipes
permalink: step5/
---
Ok now that our homepage is looking better lets get our recipe pages looking nice.

Let's do `traditional-cupcakes.html` first.

Instead of showing you the completed page I'm going to provide some direction and let you figure out the right markup.

1. The document title should be `Traditional Cupcakes`.
1. `Traditional Cupcakes` in the first line should be a level 1 heading.  Remove the line of `-`.
2. Before the level 1 heading, put a link back to our `index.html` with the text of `HOME`.
2. Description should be a paragraph.
3. Make `Ingredients:` a level 2 heading. The ingredients should be in an unordered list.
4. `Method:` should be a level 2 heading as well, but the method directions should be an ordered list.

Step 7 of the method is trickier, right? The good news is, you can nest most things inside of list items - including other lists.  

When you're done, your file should look something like this:

[SCREENSHOT]

Refer to our completed `traditional-cupcakes.html` for hints.

```html
<html>
  <head>
    <title>Traditional Cupcakes</title>
  </head>
  <body>
    <a href="index.html">HOME</a>
    <h1>Traditional cupcakes</h1>
    <p>
      Traditional cupcakes are always a crowd-pleaser.
    </p>

    <h2>Ingredients:</h2>
    <ul>
      <li>2 cups self-raising flour, sifted</li>
      <li>3/4 cup CSR Caster Sugar</li>
      <li>2 eggs, beaten</li>
      <li>3/4 cup milk</li>
      <li>125g butter, melted, cooled</li>
      <li>1 teaspoon vanilla essence</li>
      <li>Sprinkles, to decorate</li>
      <li>1 1/2 cups CSR Pure Icing Sugar</li>
      <li>1-1 1/2 tablespoons water</li>
      <li>food colouring, optional</li>
    </ul>

    <h2>Method:</h2>
    <ol>
      <li>Preheat oven to 200°C or 180°C fan-forced.</li>
      <li>Grease a 12 x 1/3-cup capacity muffin pan. Alternatively, line holes with paper cases.</li>
      <li>Combine flour and caster sugar in a bowl. Make a well in the centre.</li>
      <li>Add milk, butter, eggs and vanilla to flour mixture. Using a large metal spoon, stir gently to combine.</li>
      <li>Spoon mixture into prepared muffin pan. Bake for 12 to 15 minutes, or until a skewer inserted into the centre comes out clean.</li>
      <li>Stand in pan for 5 minutes before transferring to a wire rack to cool.</li>
      <li>Make icing:
          <ol>
            <li>Sift icing sugar into a bowl.</li>
            <li>Add food colouring and water.</li>
            <li>Stir until smooth and well combined.</li>
          </ol>
      </li>
      <li>Spoon icing over cupcakes.</li>
      <li>Decorate with sprinkles.</li>
    </ol>
  </body>
</html>
```
{: .solution }

How did you go?

Now do `muffins.html` as well.  Use the same directions plus the following:

1. Make sure the document has an appropriate title.
2. `Variations:` should be a level 2 heading.
3. Each variation name (i.e. Blueberry, Pecan, etc.) should be a level 3 heading.
4. Make the variant steps an unordered list.

When you're done, your file should look something like this:

[INSERT SCREENSHOT]

Refer to our completed `muffins.html` for hints.

```html
<html>
  <head>
    <title>Muffins</title>
  </head>
  <body>
    <a href="index.html">Home</a>
    <h1>Muffins</h1>
    <p>This recipe makes 12 plain muffins.</p>
    <p>Refer to directions at the bottom for how to modify the recipe for different types of muffins.</p>

    <h2>Ingredients:</h2>

    <ul>
     <li>2 cups white flour</li>
     <li>1 tablespoon baking powder</li>
     <li>1/2 teaspoon salt</li>
     <li>2 tablespoons sugar</li>
     <li>1 egg, slightly beaten</li>
     <li>1 cup milk</li>
     <li>1/4 cup melted butter</li>
   </ul>

    <h2>Method:</h2>
    <ol>
      <li>Preheat the oven to 375°F.</li>
      <li>Butter muffin pans.</li>
      <li>Mix the flour, baking powder, salt, and sugar in a large bowl.</li>
      <li>Add the egg, milk, and butter, stirring only enough to dampen the flour; the batter should not be smooth.</li>
      <li>Spoon into the muffin pans, filling each cup about two-thirds full.</li>
      <li>Bake for about 20 to 25 minutes each.</li>
    </ol>

    <h2>Variations:</h2>
    <h3>Blueberry Muffins:</h3>
    <ul>
      <li>Use 1/2 cup sugar.</li>
      <li>Reserve 1/4 cup of the flour, sprinkle it over 1 cup blueberries, and stir them into the batter last.</li>
    </ul>
    <h3>Pecan Muffins:</h3>
    <ul>
     <li>Use 1/4 cup sugar.</li>
     <li>Add 1/2 cup chopped pecans to the batter.</li>
     <li>After filling the cups, sprinkle with sugar, cinnamon, and more chopped nuts.</li>
   </ul>
    <h3>Whole-Wheat Muffins:</h3>
    <ul>
      <li>Use 3/4 cup whole-wheat flour and 1 cup white flour.</li>
    </ul>
    <h3>Date or Raisin Muffins:</h3>
    <ul>
      <li>Add 1/2 cup chopped pitted dates or 1/3 cup raisins to the batter.</li>
    </ul>
    <h3>Bacon Muffins:</h3>
    <ul>
     <li>Add 3 strips bacon, fried crisp and crumbled, to the batter.</li>
    </ul>
  </body>
</html>
```
{: .solution }


Ok.  Now we have our three pages: two recipes and a homepage.

But it's a bit plain isn't it?  Most recipe sites have images.  Let's look at them in the next step.
