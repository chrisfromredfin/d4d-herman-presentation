# Redfin Solutions, LLC
Reveal.JS example slide deck

## Getting started
To get working on a new slideshow, fork this repository into one of your own on Jerry, for the specific slideshow you 
want. 

Clone your forked repository down into a folder. 

Run `yarn install` to get dependencies.

Run `yarn build` to compile the theme sass into css.

While developing, you may use `yarn watch` to automatically compile, and `yarn bs` to run browsersync.

## Building Slides

The way Reveal.JS works, is that each `<section>` inside of the .slides div in index.html becomes a new slide. You may 
nest another section tag inside, and that will create vertical slides. You can nest them infinitely, but they will 
always continue to run down vertically.

In Redfin's template, you may add a class on each section depending on the type of slide you want. The available
classes are:

* .slide--card
* .slide--more-narrow
* .slide--narrow
* .slide--short
* .slide--subtitle
* .slide--title
* .slide--title-and-body
* .slide--two-column

The available slides are here:

![slide layouts](https://i.imgur.com/4uQKQJd.png "Slide Layouts")

### Using Markdown instead of HTML

Currently, the use of Markdown is supported by Reveal.JS, but not our theme. For some reason, markdown is not appended
inside of the .slides div, and this causes issues for us.

## More Reading

* [The Reveal.JS project/documentation](https://github.com/hakimel/reveal.js)
