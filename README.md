# [ZeroToCode.org](https://zerotocode.org)

Zero To Code is **a free-forever online course about making stuff on the web**, using fundamental web technologies: HTML, CSS, and JavaScript. I want ZTC to be the best place on the web to learn to make stuff with code. Zero to Code uses [Codeframe](https://github.com/thesephist/codeframe) as its learning environment, for its shareability, fast feedback loop, and simplicity and focus on the fundamentals.

This is the source repository that contains the [Hugo site](https://gohugo.io/) for Zero to Code. You can read more about the project itself on the website.

## Contributing (beginners welcome!)

Zero to Code is a static site built with Hugo. Hugo is a static site generator, which takes Markdown documents and HTML/CSS/JS templates and generates a bundle of static HTML/CSS/JS files that forms a static site. You can learn more about how to use Hugo at [gohugo.io](https://gohugo.io/). This section of the README covers how to work with Hugo on ZTC's repository.

### Generating the site

You can generate a new version of the static site from templates and Markdown pages once by running `hugo`.

```sh
$ hugo
...
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

#### Embedded Codeframe editors

## Support

If you like the Zero to Code project want to support what I make going forward, please consider making a donation to Zero to Code through [PayPal](https://www.paypal.me/thesephist) or [Venmo](https://venmo.com/thesephist) 🙏.

Alternatively, please consider donating to some of the best nonprofit organizations doing great work in the CS education space, [KhanAcademy](https://www.khanacademy.org/donate), [Hack Club](https://hackclub.com/donate/), and [StuTech](https://grants.stutech.org).

