# Building a Living Style Guide with Herman

Christopher J. Wells  
Redfin Solutions, LLC

--

# Christopher J. Wells

<img class="secondary" src="https://en.gravatar.com/userimage/45857937/d42cf9e078d9582683fb05a648c0764e.jpg?size=100">

* Owner/Developer/"Full Stack" guy
* Redfin Solutions, LLC - Portland, ME
* Exclusive Drupal shop since Drupal 4.7 (~2005)

---

# Style Guide

* communicates pattern library
* establishes standards / "what's already there"
* *keep designers and developers in sync*

--

# "Living"

* agile
* new needs, new components
* maintenance projects

--

# Herman

* enterprise without dedicated teams and budgets
* dip your toes
* consider it documentation

> If it's not documented, it doesn't exist.  
> *- Miriam Suzanne*

---

# SassDoc

> SassDoc is to Sass what JSDoc is to JavaScript: a documentation system to build pretty and powerful docs in the blink of an eye. <!-- .element: class="align-left" -->

> SassDoc parses your source folder to grab documentation-specific comments. <!-- .element: class="align-left" --> 

--

# Using SassDoc

* All [SassDoc Annotations](http://sassdoc.com/annotations/)
* SassDoc comments begin with three slashes
* `(yarn|npm) add sassdoc`

```
/// A general description.  
/// @group Molecules
.btn {
  ...
}
```

--

# Using SassDoc: Posters

File-level annotations can be used when annotations are shared across a file.

```
////
//// This is called a "poster" and is 4 slashes on blank, 
//// and ends with four slashes on blank. The slashes in between
//// can be any number you want greater than 2. 
//// @group mixins 
////

/// Handles a reponsive wrapper and its embedded iframe. 
/// @author Smashing Magazine
/// @name embed-container
/// @param {number} width [600] - width of the natural element
/// @param {number} height [800] - height of the natural element
@mixin embed-container($width: 600, $height: 800) {
  ...
}
```

--

# Using SassDoc: Configuration

http://sassdoc.com/configuration/#options

Place a .sassdocrc in your project root.

```
dest: ./styleguide
exclude:
  - node_modules
theme: herman
groups:
  - mixins: Mix-ins
  - extends: Placeholders
```

---

# Herman

Herman is a SassDoc theme.

* `(yarn|npm) add sassdoc`
* `(yarn|npm) add sassdoc-theme-herman`
* `(yarn|npm) add node-sass`  
  _(* if displaying example sass/scss)_

Note: v1
 
--

Additional configuration for the .sassdocrc,   
specific to Herman:

```
herman:
  dest: guide
  exclude:
    - node_modules
  theme: herman
```

Note: v2

--

# What they do

* `dest: guide` - where to put the static site
* `exclude` - folders that should not be scanned
* `theme: herman` - use the 'herman' sassdoc theme

--

# Sass Setup

* add some partials
* add some Yarn scripts

---

# Document a Mixin

* free-floating
* @group, @author, @param, @output
* @example

Note: v3

--

# Add a real-life @example

Add _another_ @example, using 'html' as the type.

```
/// @example html -
///   <div><span>a</span></div>
``` 

Note: v4

--

# Document an extend

* similar concept, but additional CSS needed
* use customCSS in your .sassdocrc
* write real Sass as well
* two things to consider
* you need a modern build process

Note: v5

---

# Herman Enhances Groups

* SassDoc has 'groups' concept
* .sassdocrc - slugs to names
* Herman adds ordering & nesting (1 level)

```
groups:
  Utility:
    mixins: Mix-ins
    extends: Placeholders
```

---

# Herman Design Tokens

* colors
* typography
* ratios and sizes
* icons
* nunjucks

--

# Color Palettes

![color palettes](/assets/colors.png)

--

# Typography

![typography](/assets/typography.png)

--

# Ratios

![ratios](/assets/ratios.png)

--

# Sizes

![sizes](/assets/sizes.png)

--

# Icons

![icons](/assets/icons.png)

---

# Nunjucks

![man with nunchuks](http://i.imgur.com/bGLRD5v.gif)

--

# Nunjucks, eh?

> Nunjucks is a full-featured templating engine for Javascript. It is heavily inspired by jinja2.

_Know what else is heavily inspired by jinja2? Twig!_

---

# Questions?

![](https://pbs.twimg.com/media/C9YeDY7UQAEfULN.jpg)