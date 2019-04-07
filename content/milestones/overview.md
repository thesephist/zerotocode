---
title: "Overview and Orientation"
date: 2019-04-03T09:11:18-07:00
order: 0
---

Before you begin working through the milestones, this overview covers a few things you should know to move through the course, including what you'll learn, how to use our code editor, Codeframe, and how to learn to code effectively using the resources available online, in addition to what's here already.

## What we'll learn

Zero to Code is a course about making interesting, useful things on the web using technologies that are core to any website: **HTML, CSS, and JavaScript**. We'll work through a series of small projects in increasing complexity to get you more and more familiar with concepts in these languages, and how to combine them to build beautiful, useful websites.

### Things we'll cover

You'll get a solid understanding of...

- How to use HTML, CSS, and modern JavaScript to build webpages
- Basic of good design on the web, from typography to color and layout to animation and interaction design
- How to create and code responsive design that work across different screen sizes
- How to think about accessibility, so as many people as possible can use what you make
- How to break down a design or wireframe to go from sketch to code
- How to share the websites you build under your own domain name on the Internet, so evryone can access it.
- Where to go and what to learn after Zero to Code, if you want to continue learning

In short, think about it this way: you'll walk out of the course with a rockin' personal webpage.

### Things we won't cover in depth (yet)

There are some topics that are important or interesting, but for which I think there are other high-quality tutorial or courses available online, or for which I don't currently have time to built curriculum, so we don't cover yet. These are...

- How to build dynamic web apps and services that require login, user accounts, profiles, and APIs
- Search engine optimization (SEO)
- Content management systems like Wordpress
- JavaScript frameworks like React, Angular, Vue, Svelte, and Polymer (though we'll briefly discuss the merits of frameworks)
- JavaScript libraries like Underscore, Lodash, and jQuery
- Modern JavaScript development tools like Webpack, Babel, Next.js
- Other languages or environments used for the web like Node.js, PHP, Python, Ruby on Rails...

If you're interested in learning about any of these topics, the aren't out of the question! Drop me a line at [@thesephist](https://twitter.com/thesephist) or reach out from the about page.

## Using Codeframe, our code editor

[Codeframe](https://codeframe.co) is the code editor we'll use through most of this course to build projects and experiment with new concepts. It looks like this.

You can edit the HTML, CSS (inside the `<style>` block), and JavaScript code on the right/bottom pane, and see the result on the left/top pane as you type. If you want to save or share what you've made, you can hit the <span class="fixed inline button">Save &amp; Reload</span> button to save your work, which will give you a link and a preview button you can use to share what you've made with anyone else on the planet, just by sharing that link!

<div class="liveEditorContainer fixed button">
    <iframe src="https://beta.codeframe.co/new?from=ztc_about" frameborder="0" class="liveEditor"></iframe>
</div>

For a gentle introduction to Codeframe, let's write some HTML! Make sure the <span class="fixed inline active button">HTML</span> mode is selected (it is by default), and type this snippet of HTML code into the editor pane, replacing `[your name]` with your name:

{{<highlight html "linenos=">}}
<h1>Hi Codeframe!</h1>
<p>My name is <strong>[your name]</strong>.</p>
<button>Click Me!</button>
{{</highlight>}}

As you type, you should see something appear on the preview pane. What do you see?

You should see three things:

- A big, bold header that says **Hi Codeframe!**
- A smaller bit of text that corresponds to what you typed in between the `<p>...</p>`
- A small button

This is HTML! Try hitting <span class="inline fixed button">Save &amp; Reload</span>, and tap the preview button to see the webpage you just made open in a separate tab. To share what you just wrote with anyone, you can open it in a new tab and copy the link, like we just did here, or you can copy the link in the URL bar in the preview pane of the editor itself (they're the same link).

After you save your work, you can always come back to the _same version of the file_ with the URL. If you copy the URL to the editor itself, you can come back and continue to edit the code you've been editing.

This is Codeframe! Experiment with the HTML code in the editor, and see if the website you see in the preview behaves the way you expect it to. We'll explore HTML in depth in the first milestone project.

## Some tips on learning to code

Like learning anything new, learning to code requires a bit of a mindset shift. Here are some tips I've found useful in learning to code without getting to frustrated or bored, and to get the most out of the materials I have.

- At first, it might feel like there's a lot to memorize. You don't have to memorize most things you come across (I'll tell you when you need to remember something specific). Google is your friend, and the key is to remember _that there's a way to do something_, not necessary to remember _exactly_ how to do it. As you practice and create more and more, you'll learn these shortcuts and keywords by heart.
- Whenever you're copying some sample code into the editor, if it's not too much, try typing it out by hand instead of copy-pasting it. This will help us get it in our fingers faster, and make us think more consciously about what we're writing.
- Add more tips here...

## Resources elsewhere on the web

There's so many resources online that'll be helpful for you as you learn web design and development. Here are a few of my favorites that I'd recommend you find, if you're ever stuck or want some inspiration.

### MDN (formerly Mozilla Developer Network)

MDN is the _de facto_ documentation site for HTML, CSS, and JavaScript. It can be too technical for a beginner, but anytime you have a specific question about a specific way to do something, MDN can usually help you find the right answer.

### Stack Overflow

Stack Overflow is a question-and-answer site for developers of all kinds -- not just web developers -- and almost every developer turns to it when they can't troubleshoot or debug an issue on their own. It's just as useful a resource or us as we explore HTML, CSS, and JavaScript. Stack Overflow is great for answer questions like "How do I do X in HTML/CSS?" or "What function do I use to do Y in JavaScript?"

### CSS Tricks

CSS Tricks is a blog dedicated specifically to design on the web. It covers actual "tricks" in CSS to achieve certain design styles, but it also contains lots of generally useful web design advice. Often, if you're looking for a way to achieve a specific visual effect with CSS, CSS Tricks is a good destination.

### W3Schools

W3Schools is a tutorial site that covers the basics of HTML, CSS, and JavaScript in a friendlier language than MDN might, so it's a good resource as you're starting out to learn about these technologies.
