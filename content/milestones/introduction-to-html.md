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

This bit of code defines a short **paragraph**, using the `<p>...</p>` tag, which stands for a paragraph. Inside the paragraph, we have the text we want to be included in the paragraph. Let's take note of a few things.

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

... this output the same result as the first example, because the large empty space in the middle gets smooshed into a single space in HTML. Try this for yourself in Codeframe, and see what kinds of spaces make a difference.

Here's HTML for a heading, followed by two paragraphs.

{{<highlight html>}}
<h1>Harry Potter</h1>
<p>... and the Philosopher's Stone</p>
<p>by J. K. Rowling</p>
{{</highlight>}}

There's three tags here, including the `<h1>` tag for a header. All three have closing tags, like they should. You'll also notice the line numbers in front of the sample code -- from here on, I'll label each line of code with the line number, so we can refer to them easier. When you're copying these samples to test them on your own, you should omit them.

### Tags can be inside other tags

HTML tags can be nested inside other tags to give additional structure to our text. If we wanted to have a bold bit of text inside a paragraph, for example, we can write

{{<highlight html>}}
<p>
    Harry Potter was the <strong>chosen one</strong>.
</p>
{{</highlight>}}

Here, we have a paragraph (`<p>`), that contains a `<strong>` tag. The strong tag defines a bit of text that should be bolded on the page. We can even nest further

{{<highlight html>}}
<main>
    <p>
        Harry Potter was the <strong><em>chosen</em> one</strong>.
    </p>
</main>
{{</highlight>}}

Here, we use the `<em>` tag, which represents some text to be _italicized_ on the page. If you've written HTML before, you may have come across `<b>` and `<i>` tags, which bold and italicize as well. However, `<em>` and `<strong>` are their modern equivalents; when you have a choice, bias for the modern replacements.

You may also notice that we've started indenting nested parts of our code further to the right. Because HTML doesn't really care about "whitespace" or spaces, indentation is a matter of taste and personal preference. However, indenting different nested parts of your HTML code will help keep the structure of your page straight, as you build more complex sites. **Get in the habit of indenting HTML code!** It'll be helpful in the long run.

### Beware of common tag mistakes

There are two common mistakes I see from students new to HTML. The first is simply forgetting to close a tag. What's wrong with this sample?

{{<highlight html "linenos=">}}
<p>This is some paragraph text!<p>
{{</highlight>}}

It's almost right, but on close inspection you might see that the closing tag doesn't actually close -- the closing tag needs to be `</p>`, not `<p>`.

The second mistake has to do with the order of nested tags. Consider this example.

{{<highlight html "linenos=">}}
<p>I'm <em>mismatched</p></em>
{{</highlight>}}

Surprisingly, almost all web browsers will take this HTML, and output exactly what you'd expect. But there's a subtle mistake hiding here that browsers are forgiving us for ignoring. Since we opened the `<p>` tag first, then the `<em>` tag, we need to close the inner tag `<em>` _first_, then the `<p>` tag should be closed. The closing tags here are out of order. While this won't cause immediate issues, it's good to get in the habit of noticing these mistakes.

### Tags with attributes

Sometimes, when we use an HTML tag, we also want to add some additional data about the tag. For example, when we mark up a bit of text saying "this is a link," we'd want to define what the link leads to. We can add additional information like this to tags with **attributes**.

Let's consider this link example. Links in HTML are marked with the `<a>` tag. (It's represented by the letter "a," apparently, because it stands for "anchor".) We can add a link in the middle of our paragraph like this.

{{<highlight html>}}
<p>
    Please check out
    <a>my Instagram!</a>
</p>
{{</highlight>}}

If you try this sample, you'll notice that nothing actually happens (yet) when we click on the link. It looks like a link, but doesn't go anywhere, because we haven't told it where to go. How might we do that? We can add an **attribute** to our anchor tag, like this.

{{<highlight html>}}
<p>
    Please check out
    <a href="https://instagram.com/thesephist">my Instagram!</a>
</p>
{{</highlight>}}

The `href` stands for something roughly like "hyperlink reference", and is an _attribute_ we can add specifically to the `<a>` tag to denote where the link should point to. In this case, the `href` attribute also has a **value**, which is the URL that the link should navigate the user to, when tapped.

Attributes are everywhere. We use them to denote where image files are when we add images, what buttons should do, where forms should be sent, where download links are, and so on.

## Part 2: Adding some color with CSS

## Part 3: More styles with CSS
