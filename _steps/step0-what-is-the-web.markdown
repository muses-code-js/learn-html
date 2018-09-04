---
layout: step
number: 0
title: What is the Web?
permalink: step0/
---

## What we're doing today

The main thing we're going to learn in this workshop is how to make simple web pages.

We're going to use two languages to do this:

- HTML (**H**yper**T**ext **M**arkup **L**anguage), and
- CSS (**C**ascading **S**tyle **S**heets)

Web pages can contain a lot of other things that aren't HTML or CSS, like images or sound files, and even other code like JavaScript. But to make a simple page, HTML and CSS are all you need.

But before we start learning new languages, let's take a moment to make sure we're all on the same web page. ;)

## The web

Let's talk about the web, and the internet.

We've all used the web:
we've typed addresses into Firefox or Internet Explorer to get to a certain web page,
and we've clicked links to go to other related web pages.

But how much do you know about what does on behind the scenes? What really happens when you click a link or type in a page address?

There are actually a lot of things going on behind each of these small actions!

But the good news is, you don't need to know all of it.

You only need to learn a little bit about how the web works to start making web pages.

Anything else you need, you can learn when you have a specific problem or idea.

Learning new things as you need them is a big part of being a developer.
You don't have to learn everything at once. :)

## How the web works

In simple terms, the web works like this:

1. You ask your browser for a web page.
2. Your browser asks another computer for that web page.
3. The other computer sends the web page back.
4. Your browser receives the web page and displays it for you.

Let's break that down in a little more detail.

### 1. You ask for a web page.

Normally, you type a web page address into your browser or click on a link to ask for a web page.

We call these web page addresses **URL**s.

A URL has three parts:
1. A **protocol** - the way that the web page should be sent. For web pages, this is usually **http** or **https**.
2. A **host name** - the name of the computer that has the page you asked for.
3. A **path** - the location of the page on the computer that has it.

### 2. Your browser asks another computer for that web page.

The parts of a URL give your browser all the information it needs to go and ask another computer for that page. We call computers that send web pages on request **web servers**.

Let's look at the URL for the Node Girls Brisbane page, `http://nodegirls.com.au/brisbane.html`, as an example.

In this URL, the protocol is `http`, the host name is `nodegirls.com.au`, and the path is `brisbane.html`. That means that the web server called `nodegirls.com.au` has sent us the `brisbane.html` file using the `http` protocol.

Look at the address bar of your browser right now, as you're reading this page.
Can you tell what the different parts are?

### 3. The other computer sends a web page back.

If the web server has the web page file that your browser asked for, it sends that file to your browser.

If the web server doesn't have that file in the exact place you asked for, it will send an error page to your browser instead.

### 4. Your browser receives the web page and displays it for you.

Most web pages are written in a combination of the two languages we mentioned earlier: HTML and CSS.

Your browser reads the HTML and CSS in the web page, and then uses those rules to display the web page for you.

## Pretty simple, right?

The case that we've gone through here is pretty simple: a server has a web page file, and sends it to you when you ask for it.

In reality, a web server might not actually have a file ready for every URL that it gets asked for.

Sometimes, web servers use other software to look at incoming browser requests and write out a web page to fit that request when asked.

That might sound fancy and complicated, but if you've ever done a mail-merge to make up letters to send to customers, or put together a burger or a pizza order, it's a very similar idea.

## Let's make it simpler, just for now

In this workshop, we're going to do something a little different.

We're going to use the **file** protocol instead of **http** or **https**.

Basically, your browser is going to be asking your own computer for a file, and then displaying that file for you.

All this means is that we don't have to run our own web server to receive page requests and send back web pages.

The protocol is the only thing we're going to change.
The underlying HTML and CSS will be exactly the same.

Ready? Let's go!
