---
layout: step
number: 8
title: Styling Links
permalink: step8/
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

[SCREENSHOT]

The `text-decoration` declaration is what controls the underlining of a link.  Here we set that to `none` to turn it off.  Then we use `border-bottom` to create our own underline, and we use the `dashed` border system.  That is what lets us have the dashed-style underline.

Hmmm, that looks nicer but if you look at the homepage they are kind of mashed together a bit in the list.
So let's space out our lists a little, the items were a little too close together for my liking anyway.

```css
li {
  margin-bottom: 10px;
}
```

[SCREENSHOT]

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

[SCREENSHOT]

This order is important because the link styles build on one another, for example the styles in the first rule will apply to all the subsequent ones, and when a link is being activated, it is also being hovered over.  If you put the styles in a different order than you might get weird effects.

Note that these are pretty dramatic changes to link styling.  People are mostly used to the underlined text style so be careful changing it too dramatically. It can confuse and annoy people - and if the change is too dramatic, such as a change in font size that moves the text away from the tip of the mouse cursor, it might actually make your link impossible to click on.

You can learn much more about styling of links at
https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_links
