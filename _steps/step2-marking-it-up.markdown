---
layout: step
number: 2
title: marking it up
permalink: step2/
---

So let's get started with our first page, `index.html` which is our site's homepage.

Open up `index.html` in your browser.

[SCREENSHOT]

Ok ... so that looks like a hot mess. What's with that?

Your browser assumes that a file with `.html` or `.htm` contains HTML content and it treats it as such.  
Because we didn't actually include any HTML tags in the file, the browser just displays the raw text and since HTML ignores newline characters it gets displayed like one big paragraph.

Oh and notice how the browser tab has the file path in it, prefixed with `file://`?  Not great either right?

So since that isn't quite what we had in mind, lets add some HTML to it.


Update `index.html` so it has :

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Tiny Cakes!</title>
    <meta charset="UTF-8" />
  </head>
  <body>
  Tiny Cakes!
  -----------

  Welcome to my recipes web site all about Tiny Cakes!

  Here are the recipes that we have:

   * Traditional cupcakes
   * Muffins
  </body>
</html>
```

Save it, refresh our browser window & it does look the same, but if you look closely you'll see that the browser tab now reads "Tiny Cakes!" instead of the filename.

[SCREENSHOT]

We've added a few pieces of HTML here which are like the scaffolding or frame of the document.  We haven't actually added any formatting instructions yet which is why it looks mostly the same.

So let's look at what we did and what they mean.

1. `<!DOCTYPE html>`

The very first line is the document type declaration.  This tells the browser the version of HTML it should expect this document to be in.

The `html` in the declaration means "the latest version of html". Right now the latest version is version 5, and that will probably be the latest version for a long time to come.

You might also see declarations about older versions. Those are more complicated, like this:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

Technically this line is optional.  But if you don't include it, most browsers default to "quirks mode" which basically means "turn on all the weird non-standard stuff from the 90s that we mostly agreed was a bad idea but we keep around for backwards compatibility". Which is mostly fine ... but specifying a doctype lets you be a bit more certain that your page will work the same in different browsers.

2. `<html>`

Every HTML document should start with `<html>` and finish with `</html>`.  Everything between them is considered to be part of the document.  Most tags work like this with an opening tag and a closing tag.

3. `<head>` and `<title>`

Inside the document we have two main parts, the document head and the document body.  The document head is enclosed by the `<head>` tags and can contain several other tags which provide mostly contains information about the document.  In this case we have two tags within the head: `<title>` and `<meta>`.

`<title>` tells the browser what the title of the document is.  Most browsers display this in the browser tab and window title. It also gets used when bookmarking a page.  See how the browser tab is now _Tiny Cakes!_ instead of the filename? The `<title>` tag is why.

`<meta>` is a way of providing some additional information to the browser about the page.  Here we are using it to tell the browser that we will be using the UTF-8 character set.  This is optional but recommended to ensure unicode characters are displayed correctly.

There are a few other tags that can be used in head but we aren't going to deal with those yet.

4. `<body>`

The `<body>` tag contains the content that the page is going to display.

That sets out the basic framework of a HTML document. Now, let's look at formatting the content in `<body>` so that the browser displays it nicely.
