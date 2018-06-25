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

### Using Markdown instead of HTML

You can also put your slides in an external Markdown file, and separate slides with separators.

## More Reading

* [The Reveal.JS project/documentation](https://github.com/hakimel/reveal.js)
