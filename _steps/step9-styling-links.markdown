---
layout: step
number: 9
title: Styling Links
permalink: step9/
---

Our links are pretty plain.
Just the default underlined blue text which turns purple once you have visited the link.
Let's make it more inline with our Tiny Cakes! brand.

First let's just change the default appearance of `<a>`:

```css
a {
  color: #2f4f4f;
  text-decoration: none;
  background-color: #ffe4e1;
  padding: 2px 4px;
  border-bottom: 2px dashed #ffb6c1;
}
```

Save and refresh the homepage to check it out.

![Fancy links](../assets/css-fancy-links.png){:title="Fancy links" class="img-responsive imgbox"}

The `text-decoration` declaration is what controls the underlining of a link.  Here we set that to `none` to turn it off.  Then we use `border-bottom` to create our own underline, and we use the `dashed` border system.  That is what lets us have the dashed-style underline.

Hmmm, that looks nicer but if you look at the homepage they are kind of mashed together a bit in the list.
So let's space out our lists a little, the items were a little too close together for my liking anyway.

```css
li {
  margin-bottom: 10px;
}
```

![Spaced links](../assets/css-spaced-links.png){:title="Spaced links" class="img-responsive imgbox"}

(You can't see the cursor in this screenshot, but it's hovering over the bottom link.)

Ok.
That's a bit better.
But there is much more you can do with links.

The `<a>` element is interesting because it exists in multiple states:

1. When the page the link points to hasn't been visited.
2. When the page has been visited.
3. When the mouse is over it.
4. When the keyboard focus on it.  
4. When the mouse is actually clicking on it.

Each of these states is styled independently using **pseudo classes**.
Pseudo classes are like special classes that the browser uses to identify each state.

The pseudo-classes for the `<a>` states listed above are:

1. `link`
2. `visited`
3. `hover`
4. `focus`
5. `active`

Now let's style each one.

To use a pseudo-class you put a `:` between the element name and it's pseudo-class.

```css
a:visited {
  color: #778899;
}

a:focus {
  border: 3px dashed #ffb6c1;
}


a:hover {
  border-bottom: 3px solid #ffb6c1;
}

a:active {
  color: purple;
  border: 3px solid #ffb6c1;
}
```

We didn't style `:link` here because styling `a` does the same thing for our case.

![Fancier links](../assets/css-fancier-links.png){:title="Fancier links" class="img-responsive imgbox"}

This order is important because the link styles build on one another, for example the styles in the first rule will apply to all the subsequent ones, and when a link is being activated, it is also being hovered over.  If you put the styles in a different order than you might get weird effects.

Note that these are pretty dramatic changes to link styling.  People are mostly used to the underlined text style so be careful changing it too dramatically. It can confuse and annoy people - and if the change is too dramatic, such as a change in font size that moves the text away from the tip of the mouse cursor, it might actually make your link impossible to click on.

You can learn much more about styling of links at
<a href="https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_links" target="_blank">https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_links</a>
