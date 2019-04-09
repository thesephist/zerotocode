# [ZeroToCode.org](https://zerotocode.org)

Zero To Code is **a free-forever online course about making stuff on the web**, using fundamental web technologies: HTML, CSS, and JavaScript. I want ZTC to be the best place on the web to learn to make stuff with code. Zero to Code uses [Codeframe](https://github.com/thesephist/codeframe) as its learning environment, for its shareability, fast feedback loop, and focus on the fundamentals.

This is the source repository that contains the [Hugo site](https://gohugo.io/) for Zero to Code, including all of the open curriculum. You can read more about the project itself on the website.

## Contributing: beginners welcome! 👋

Zero to Code is a static site built with Hugo. Hugo is a static site generator, which takes Markdown documents and HTML/CSS/JS templates and generates a bundle of static HTML/CSS/JS files that forms a static site. You can learn more about how to use Hugo at [gohugo.io](https://gohugo.io/). This section of the README covers how to work with Hugo on ZTC's repository.

### Generating the site

You can generate a new version of the static site from templates and Markdown pages once by running `hugo`.

```sh
$ hugo
...
[some info about the generated files]
```

If you're writing and want to see the results as you're writing a page or modifying templates, you can run the development server with `hugo server -D`.

```sh
$ hugo server -D
... serving development server at localhost:1313
```

When you start the server this way, you can go to `localhost:1313` on your browser to see a live-reloading version of the site as you edit.

### ZTC's customizations

Zero To Code has a couple of customizations we use on top of Hugo's bare functionality to make tutorials more effective.

#### Syntax-highlighted code blocks with "Try this" buttons.

The most important customization that ZTC has on top of Hugo is the way we build syntax-highlighted code blocks. Rather than use Markdown's triple-backtick syntax, we use Hugo's custom syntax to define a syntax highlighted code block, like this:

```
{{<highlight html>}}
<h1>this is a highlighted block</h1>
{{</highlight>}}
```

You can also define a `css` or `javascript` code block rather than `html`, and we can tell Hugo to highlight certain lines with the `"hl_lines=N1 N2 N3-N5"` syntax.

```
{{<highlight javascript "hl_lines=1">}}
console.log('hi');
{{</highlight>}}
```

When we define a highlighted code block in this way, on `single.html` pages (single tutorial pages), we also have a script that goes through alll `.highlight`ed code blocks on the page and adds a **Try this ->** button at the top right of each code block, which opens Codeframe with the code sample specified.

#### Embedded Codeframe editors

Sometimes we want to embed a live, interactive instance of a Codeframe editor on the page. Currently, the best way to do this is to create a `.fixed.button.liveEditorContainer` div which contains an `<iframe>` element pointing to a Codeframe editor URL, like this example from the overview lesson.

```html
<div class="liveEditorContainer fixed button">
    <iframe src="https://codeframe.co/new" frameborder="0" class="liveEditor"></iframe>
</div>
```

This embeds the Codeframe editor specified by the URL onto the page, at the right size.

#### The `button` class and boxes with shadows

Most interactive elements and certain emphasized elements (like highlighted code blocks and images) are raised from the surface of the page with a shadow. The `.button` class, imported from Codeframe's stylesheet, is responsible for this apperance. When you want to make some element raised with a box shadow like Codeframe's buttons, use the `.button` class.

If you want the element not to be interactive, you can apply the `.fixed.button` classes to the element, which will disable hover and active animations on the button.

## Support Zero to Code

If you like the Zero to Code project want to support what I make going forward, please consider making a donation to Zero to Code through [PayPal](https://www.paypal.me/thesephist) or [Venmo](https://venmo.com/thesephist) 🙏.

Alternatively, please consider donating to some of the best nonprofit organizations doing great work in the CS education space, [KhanAcademy](https://www.khanacademy.org/donate), [Hack Club](https://hackclub.com/donate/), and [StuTech](https://grants.stutech.org).
