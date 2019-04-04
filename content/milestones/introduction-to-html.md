---
title: "About page: Intro to HTML & CSS"
date: 2019-04-03T09:11:18-07:00
order: 1
---

In this milestone, we'll get acquainted with HTML and CSS, two of the key building blocks of every website. Using what we learn, we'll build a very simple About page for you.

<!-- embed finished sample here -->

## Part 1: HTML Tags and Elements

HTML is what we call a _markup language_. It "marks up" text with additional meaning, like "this bit of text is a heading" or "this part of the text should be italicized." We can also use HTML to add non-text elements like images, videos, and links to our pages as well as interactive things like inputs and buttons. For tooday, let's start with simple text.

### Everything is a tag

Here's what a tag looks like in HTML.

{{<highlight html "linenos=">}}
<p>Hello, everyone!</p>
{{</highlight>}}

This bit of code defines a **paragraph**, using the `<p>...</p>` tag, which stands for a paragraph. Inside the paragraph, we have the text we want to be included in the paragraph. Let's take note of a few things.

- The tag comes in a pair, an **opening tag** `<p>`, and a **closing tag** `</p>`. The pair of opening and closing tags tells us where the paragraph begins an ends, and everything in between is _inside_ the tag.
- The opening tag is a symbol for paragraph, surrounded by angle brackets `< >`. All tags look this way; the tag for the first-level heading, for example, is `<h1>...</h1>`.
- The closing tag looks very similar, but has a forward-slash `/` before the symbol for the tag. This forward slash closes the tag. If you forget the slash, your code may break -- if something seems off, check if you've closed your tags with `/` properly.

Another thing to remember about HTML is that it treats all blank spaces the same. If we wrote, for example, this...

{{<highlight html "linenos=">}}
<p>
    Hello,

        everyone!
</p>
{{</highlight>}}

... this output the same result as the first example, because the large empty space in the middle gets smooshed into a single space in HTML.

Here's HTML for a heading, followed by two paragraphs.

{{<highlight html>}}
<h1>Harry Potter</h1>
<p>... and the Philosopher's Stone</p>
<p>by J. K. Rowling</p>
{{</highlight>}}

There's three tags here, including the `<h1>` tag for a header. All three have closing tags, like they should. You'll also notice the line numbers in front of the sample code -- from here on, I'll label each line of code with the line number, so we can refer to them easier. When you're copying these samples, you should omit them.

### Tags can be inside other tags

HTML tags can be nested inside other tags to give additional structure to our text. If we wanted to have a bold bit of text inside a paragraph, for example, we can write

{{<highlight html>}}
<p>
    Harry Potter was the <strong>chosen one</strong>.
</p>
{{</highlight>}}

Here, we have a paragraph (`<p>`), that contains a `<strong>` tag. The strong tag defines a bit of text that should be bolded on the page.

### Tags with attributes

Sometimes, when we use an HTML tag, we also want to add some additional data about the tag. For example, when we mark up a bit of text saying "this is a link," we'd want to define what the link leads to. We can add additional information like this to tags with **attributes**.

## Part 2: Adding some color with CSS

## Part 3: More styles with CSS
