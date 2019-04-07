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

### HTML Comments

Consider this bit of HTML.

{{<highlight html>}}
<!-- this is a comment! -->
<p>This is not a comment! This is a real thing.</p>
{{</highlight>}}

If you copy this HTML into your editor, you'll see that the first part, the part surrounded by `<!--...-->`, doesn't show up. This is a _comment_, and comments are ignored by browsers when they display your HTML on the page. All comments are surrounded by `<!--` and `-->`, and can span multiple lines. Developers use comments like this to point out things in our code or add annotations or, well, comments, in our code, for other people to read. In this course, I'll use them to point out things in the middle of our code blocks.

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
    <!-- this link below has an attribute, pointing to a URL -->
    <a href="https://instagram.com/thesephist">my Instagram!</a>
</p>
{{</highlight>}}

The `href` stands for something roughly like "hyperlink reference", and is an _attribute_ we can add specifically to the `<a>` tag to denote where the link should point to. In this case, the `href` attribute also has a **value**, which is the URL that the link should navigate the user to, when tapped. Attributes all live in side the opening tag of an element, and follows the tag name (`a` in this case).

Attributes are everywhere. We use them to denote where image files are when we add images, what buttons should do, where forms should be sent, where download links are, and so on. We'll encounter more and more of these use cases of HTML attributes as we delve deeper into HTML.

## Part 2: Adding some color with CSS

As you've played around with your HTML code, you may have noticed that a webpage made of just HTML has a pretty boring, plain look. All of the text has a very _Times New Roman_ feel to it, with set text sizes, set margins, and no sense of design. That's because HTML focuses on one thing, and does just that one thing very well: structuring your webpage. It defines headings, paragraphs, buttons, and boxes, and that's its only concern.

This is a common pattern in well-designed software: **complex things are built up from smaller, simpler parts that to small things very well.**

But that must mean there's some other tool that handles makings things look a bit better! That other thing is **CSS**.

### CSS, the Style Sheet

CSS is a different type of code (you may say a different language) that's embedded inside our HTML pages to modify how our HTML pages look. There's a few different ways to embed CSS code into our HTML pages, but we're going to start with the simples way, which is to put our CSS inside a `<style>...</style>` tag.

Let's say we have this HTML...

{{<highlight html>}}
<h1>Hello there!</h1>
<p>Welcome to CSS</p>
{{</highlight>}}

... and we'd like to change some things about how the heading (`<h1>`) looks. Specifically, we want to make it bright red, and we want to make it larger. We can do this with some CSS. Let's try...

{{<highlight html>}}
<!-- our CSS goes here, in between these tags -->
<style>
    h1 {
        color: red;
        font-size: 40px;
    }
</style>

<!-- our HTML from before -->
<h1>Hello there!</h1>
<p>Welcome to CSS</p>
<p>Let's get colorful.</p>
{{</highlight>}}

Adding these four lines of CSS changes the _appearance_ of our HTML tags. Trying playing around with the values `red` and `40px`. Try different colors, and different font sizes. Let's break down this CSS code.

### Selectors, properties, and values

Here's our CSS from before.

{{<highlight css>}}
h1 {
    color: red;
    font-size: 40px;
}
{{</highlight>}}

Intuitively, here's what this CSS code says:

>For all `<h1>` tags in this HTML page, set the (text) **color** to be "red", and set the **font size** to be 40 pixels tall.

See how parts of the description correlate with the code? There's a few parts to this short bit of CSS.

- `h1` is a **selector**. It "selects" the parts of the HTML document that the following rules should apply to.
- The selector is followed by a block of code in curly braces `{...}`, which contains the CSS "declarations", or rules, that apply to all `<h1>`s.
- Inside the curly braces, there are a list of declarations. Each declaration has a **property**, like `color` or `font-size`, and a **value**, like `red` or `40px`.

Let's say we wanted to add another rule: we want all `<h1>`s to have a yellow background. We can add another line of CSS, like this (I've temporarily omitted the HTML code here for brevity).

{{<highlight css "hl_lines=4">}}
h1 {
    color: red;
    font-size: 40px;
    background-color: yellow;
}
{{</highlight>}}

The `background-color` property controls, yep, the background color of some HTML element.

**An aside**: CSS knows about a surprisingly large number of colors! There's `orangered` and `aquamarine` and `sandybrown`, all of which correspond to specific shades of color. You can find the full list of color labels [here on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value). If your color isn't on there, you can also use a [hexadecimal color value](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#RGB_colors). If you don't understand what that is, don't worry about it just yet.

### Styling different tags

Almost always, we're not content with styling just one element on the page. In this example, we may want to also apply some styles to our paragraph tag, `<p>`. Adding new rules to new elements in CSS is straightforward: just add another section with the new selector.

{{<highlight html "hl_lines=6-9">}}
<style>
    h1 {
        color: red;
        font-size: 40px;
    }
    p {
        color: blue;
        font-style: italic;
    }
</style>

<h1>Hello there!</h1>
<p>Welcome to CSS</p>
<p>Let's get colorful.</p>
{{</highlight>}}

These four new lines of code says this:

>For all `<p>` tags in this HTML page, set the (text) **color** to be "blue", and set the **font style** to be italic (italicize the text inside).

You'll notice that the rules affect _all_ `<p>` tags on the page, not just the first one. This is usually what we want, because that'll keep our design consistent.

### Fancy selectors: classes and children selectors

Consistency is _usually_ what we want, but sometimes, we might want something to stick out. Let's say we have three paragraphs.

{{<highlight html>}}
<p>First paragraph</p>
<p>Paragraph the second!</p>
<p>Paragraph number three</p>
{{</highlight>}}

But let's say our second paragraph is _super_ important -- we want just the second paragraph to be bright orange. How can we select just the second paragraph? We might try to use the `p` selector, but that'll select _all_ paragraphs. Instead, we can select specific elements on the page with **classes**.

A **class** is an attribute you can give to HTML elements (tags) that labels those specific elements. Classes can have any name you like, as long as it's all one-word, no spaces. Let's mark our second paragraph with a `special` class.

{{<highlight html "hl_lines=2">}}
<p>First paragraph</p>
<p class="special">Paragraph the second!</p>
<p>Paragraph number three</p>
{{</highlight>}}

Once we've marked the special paragraph with this class, we can _select_ just this paragraph tag using the class in CSS. In CSS, we select by class name by using a dot `.` before the class name, like this.

{{<highlight html "hl_lines=1-5">}}
<style>
    p.special {
        color: orange;
    }
</style>

<p>First paragraph</p>
<p class="special">Paragraph the second!</p>
<p>Paragraph number three</p>
{{</highlight>}}

This CSS says,

>Only select `<p>` tags that also have a `special` class on them, and make those orange.

In this case, the only thing that has the `special` class is a paragraph tag. So we can select with just the class name, without the tag name `p`:

{{<highlight html "hl_lines=2">}}
<style>
    .special {
        color: orange;
    }
</style>

<p>First paragraph</p>
<p class="special">Paragraph the second!</p>
<p>Paragraph number three</p>
{{</highlight>}}

Classes are very powerful. We can have multiple classes, and we can apply classes to multiple different things. Take this more advanced example:

{{<highlight html>}}
<style>
    /* This is what a comment looks like in CSS */
    /* A comment can span
        multiple lines! */
    /* I'll use comments to explain what's going on here */

    /* We can separate selectors with commas to select
        multiple things in one block of CSS rules */
    h1, h2 {
        color: blue;
        /* This underlines text */
        text-decoration: underline;
    }
    p {
        /* This set the size of all paragraphs
            to 18 pixels high */
        font-size: 18px;
    }
    p.first-paragraph {
        font-style: italic;
    }
    /* this selects both h1.special and p.special */
    .special {
        background: pink;
    }
</style>

<h1 class="special">About Linus</h1>
<!-- when we separate class names with spaces in HTML,
    the element gets two classes, not a single class
    that's called "first-paragraph special" -->
<p class="first-paragraph special">
    Linus is a programmer and designer
    from West Lafayette, Indiana, USA.
</p>

<!-- this tag creates a horizontal line separator -->
<hr/>

<h2>Contact</h2>
<p>You can find Linus at <a href="https://linus.zone/now">his website</a>.</p>
<p>He is also on Twitter, at @thesephist.</p>
{{</highlight>}}

CSS gives us a _huge_ amount of freedom as web designers and developers to express our creativity on the canvas of the web, and once you get a grasp of the basics from above, you can create lots of interesting designs.

We'll explore more and more CSS properties as we move forward, so there's no need to learn every property now. For this milestone, take the last sample above, copy-paste it into a Codeframe, and try these changes:

- Change `color` property values for different elements on the page, and see if the results fit your expectations.
- Take the last paragraph that begins with "He is also on twitter...", and make the font larger (24px) for _just_ that paragraph. You may need to give that element a new class to do this.
- On the link element (`<a>`)...
    - By default, links appear blue (like on Google Search). Make the link here appear purple.
    - Let's make the link stand out a bit more. Make the text inside the link bolder, using just CSS. Google for the `font-weight` CSS property to help here.

Once you've explored CSS a bit here, we're ready to dive into our first milestone project! Let's build you an about-you page, completely from scratch, that you can put on the web.

## Part 3: About page - Putting it all together

We'll go about building your about page in two main steps, first writing the HTML, then adding some CSS.

### The HTML

Your about page can include virtually anything you like, but should at least include...

- A first-level header (`<h1>`) at the top of the page, that says "About [your name]"
- An image, which will be your profile picture
- A tweet-sized, 1-2 sentence bio about you
- A couple of subsections, each section under an `<h2>` (since they're under the big main `<h1>` section). What are you interested in? What are you working on? What music or films do you like?

Remember that the tag we use to include an image is `<img>`. The image tag also needs an `href` attribute, which should be set equal to a link to the image.

#### A brief primer on making a list

One new element that may be useful, if you're making a list of activites, films, songs, or places, is the HTML tag for making lists, `<ul>`. Let's see how this works.

{{<highlight html>}}
<p>My travel bucket list:</p>
<ul>
    <li>Isle of Skye</li>
    <li>Polynesia</li>
    <li>Tel Aviv</li>
    <li>Monaco</li>
    <li>Santorini</li>
</ul>
{{</highlight>}}

A list in HTML is actually made up of two different tags: the `<ul>` tag, which stands for "unordered list", and the `<li>` tag, which stands for "list item". Why "unordered", you ask? Well, an unordered list will produce a bulleted list. There's also the `<ol>`, which is an "ordered list". Let's see how that looks...

{{<highlight html "hl_lines=2 8">}}
<p>My travel bucket list:</p>
<ol>
    <li>Isle of Skye</li>
    <li>Polynesia</li>
    <li>Tel Aviv</li>
    <li>Monaco</li>
    <li>Santorini</li>
</ol>
{{</highlight>}}

An `<ol>` produces a list with numbers as labels, instead of bullets.

### Adding styles with CSS

Now that you have some content for your about page, let's make it look a bit prettier.

One change that you might be itching to make is to change the font on your page to something less reminiscent of a school report. We can control styles on the entire page by selecting the entire "body" of the page, like this:

{{<highlight html>}}
<style>
    body {
        /* sans-serif refers to a style of font */
        font-family: sans-serif;
    }
</style>
{{</highlight>}}

What's `sans-serif`? "Serif" and "sans-serif" are two styles of fonts, or font families. You can read more about their difference [here](https://about.easil.com/support/serif-vs-sans-serif/), but this should give your text a bit of a modern facelift.

If you included an image, you may also find that the image is too big or too small. You can adjust the size of the image by setting the `width` and/or the `height` CSS properties on the image tag, like this.

{{<highlight css>}}
img {
    height: 300px;
    /* or */
    width: 300px;
}
{{</highlight>}}

If you set _both_ width and height, you may find that it distorts the image's aspect ratio.

From here, you can add and apply styles to your HTML page to make it look the way you want. Here's some CSS properties you might find useful as you explore ways to style your about page.

#### Adding borders around things

Here's an example of a paragraph with a border around it:

<p style="border: 5px solid purple">
    I've got a border around me!
</p>

This border was added with this CSS:

{{<highlight css>}}
p.purple-border {
    border-width: 5px;
    border-style: solid;
    border-color: purple;
}

/* We can also write this in shorthand, like this */
p.purple-border {
    border: 5px solid purple;
}
{{</highlight>}}

Experiment with different values for border thickness (`border-width`), color, and style (you can pick between `dotted`, `dashed`, and `solid`) to see what you like.

#### Padding inside borders and backgrounds

If you care about aesthetics, you might have felt that the bordered paragraph above feels a little off -- there's no margin between the paragraph and the border, so it all feels a little cramped. We can fix that by adding some `padding` to the paragraph.

As we'll learn more about later, in CSS, `padding` represents the space between what's inside the tag, and the border.

Let's set padding to `8px` in this case:

{{<highlight css "hl_lines=3">}}
p.purple-border {
    border: 5px solid purple;
    padding: 8px;
}
{{</highlight>}}

This will add 8 pixels of breathing room around our paragraph, like this:

<p style="border: 5px solid purple; padding: 8px;">
    I've got a border around me!
</p>

#### Curved corners with `border-radius`

Another neat trick is to add some curved corners around our boxes, like this:

<p style="border: 5px solid purple; padding: 8px; border-radius: 10px">
    I've got a border around me!
</p>

We can add curves to borders using the `border-radius` property, which looks like this:

{{<highlight css "hl_lines=4">}}
p.purple-border {
    border: 5px solid purple;
    padding: 8px;
    border-radius: 10px;
}
{{</highlight>}}
