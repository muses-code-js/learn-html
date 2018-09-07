---
layout: step
number: 4
title: Formatting the Homepage
permalink: step4/
---

For a browser to know how to display content, we need to tell it what each piece of content actually is, e.g. a heading, a paragraph, a list etc.

Looking at the content in our homepage we can see that we have a heading, two single sentence paragraphs, and then a bulleted list of two items.

```
Tiny Cakes!
-----------

Welcome to my recipes web site all about Tiny Cakes!

Here are the recipes that we have:

 * Traditional cupcakes
 * Muffins
```

So let's add HTML to reflect that.  We call the act of adding HTML to content like this "marking up the document".

The terms "markup" & "marking up" come from the book publishing world, where an editor would review the typed pages of a manuscript and write notes on the text about how it should be formatted for printing. https://en.wikipedia.org/wiki/Markup_language#Etymology

Replace the content inside the `<body>` tags in `index.html` with the following:

```html
  <h1>Tiny Cakes!</h1>

  <p>
  Welcome to <em>my</em> recipes web site all
  about <strong>Tiny Cakes!</strong>
  </p>

  <p>
  Here are the recipes that we have:
  </p>

  <ul>
    <li>Traditional Cupcakes</li>
    <li>Muffins</li>
  </ul>
```

Save the file and refresh your browser. It should look a bit nicer.

![The marked-up home page](../assets/browser-formatted-homepage.png){:title="The marked-up home page" class="img-responsive"}

Much better, so lets talk about the HTML tags we used here.

`<h1>`
: This is a heading tag.  Specifically it is the **Level 1 Heading**.  There is also a `<h2>`, `<h3>`, etc. up to `<h6>`.  You use them to indicate headings and sub-headings. A bigger number indicates a deeper level, and the size of a heading on the page usually decreases as its number goes up.

`<p>`
: The **paragraph** tag indicates a single block of text.  
<!-- Note that HTML doesn't display line breaks. -->

`<strong>`
: The **strong** tag indicates text that is important.  Browsers usually display this as bold by default.  

`<em>`
: The **emphasis** tag indicates text that requires emphasis (no really).  Browsers usually display this as italics by default.

`<ul>`
: The **unordered list** tag is used for a list with bullet points.

You can also create numbered lists with the **ordered list** tag `<ol>`.

`<li>`
: The **list item** tag is used for each item in an ordered or unordered list.

And that is mostly as hard as HTML gets.  There are a lot more tags than just these few but the same basic concept applies:

1. You use HTML tags to specify how a web browser should treat different pieces of content.
2. You use opening & closing tags to indicate where to start and finish doing it.

## Nesting tags & Inline vs Block tags

There are two primary types of tags: **inline** and **block**.

You can think of block tags as always starting on a new line and taking up the whole line.  Inline tags don't start a new line and only take up the minimum space required.  (it is more complicated than that but it's not completely inaccurate)

All of the tags we used above except for `<em>` & `<strong>` are block tags.

Notice how we used `<em>` and `<strong>` inside of a `<p>`?  We call this **nesting** tags.

You *can* nest any tags however you want.  But they don't always make complete sense, even if they might still look how you expect.  

For example:

```html
<p>
Welcome to <em>my</em> recipes web site all
about <strong>Tiny Cakes!</strong>
<h2>Recipes:</h2>
Here are the recipes that we have:
</p>
```

But this will create some problems for you.  Browsers are a bit inconsistent with handling weird combinations like this. And when we get to using CSS later on, CSS isn't going to like it either.

Also, some tags must be nested inside others, because they don't make sense without them - like `<li>`, which has to be inside of either `<ol>` or `<ul>`. You can't have a list item without a list!


## Hyperlinks

There is one more super important HTML tag we need to mention before we head on to the next step: `<a>` the **anchor** tag AKA the hyperlink tag.

The `<a>` tag is how we create hyperlinks, i.e. links to other pages on our site or on the internet.

Let's make our list of recipes into a list of hyperlinks to our other recipes pages.  Replace our `<ul>` with:

```html
<ul>
  <li><a href="traditional-cupcakes.html">Traditional Cupcakes</a></li>
  <li><a href="muffins.html">Muffins</a></li>
</ul>
```

Now refresh your page and the list should be hyperlinks, which are usually blue and underlined by default.

![Adding links to the list](../assets/browser-formatted-home-links.png){:title="Adding links to the list" class="img-responsive"}

If you click on one of them, your browser will navigate to that page and you'll see the unformatted content because we haven't added any markup to those yet.  Click the back button in your browser to get back to the original page.

Notice the `href="muffins.html"` part of the tag?  This is called an attribute.  Specifically it is the **hypertext reference** attribute.  The quotes contain the URL that clicking on the link will navigate to.  Here we just put the file name of the page with nothing else because your files are all in the same directory.

If you want to link to a different site, you have to put the whole URL like:

```html
<a href="http://nodegirls.com.au/brisbane.html">Node Girls: Brisbane</a>
```

Some tags require attributes for specific features.

Ok, let's move on to marking up our recipes pages.
