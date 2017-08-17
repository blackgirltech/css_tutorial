# BGT CSS Tutorial

## Why CSS?

### Cascading Stylesheets
In our [HTML tutorial](https://github.com/blackgirltech/html_tutorial) we learnt that HTML is the bedrock of the web, it's how we're able to see the webpages we do, the web is linked together with a series of HTML files. HTML is the house, CSS is the paint and style. CSS tells the HTML how to look and does this simply by giving the HTML a CSS file.
These documents are called Cascading Stylesheets, or CSS, which is used to style the content of your webpage.

### The Box Model
Everything you see in on a webpage lives in a rectangular box, a HTML file is made up of a number of boxes arranged in a certain way. There are two types of boxes, a `div` which is a type of block (_vertical_) box and a `span` which is a type of inline (_horizontal_) box. Elements are either a type of `div` e.g. `<img>`, `<p>`, `<ul>` or a type of `span` e.g. `<a>`, `<input>`, `<em>`. Each element looks like this:
![The box model](/assets/img/box_model.jpg)

Each element has a margin, border & padding, we'll cover more of this later.

## First Steps
If you've taken our HTML tutorial, skip straight to [I've Done the HTML Tutorial](#i've-done-the-html-tutorial)

### I'm A Complete Newbie
So, let's grab our starter files:

1. [Click here](https://github.com/blackgirltech/css_tutorial) to visit our css tutorial repo
2. Click on the green `Clone or download` button and select `Download ZIP`
3. Open this folder on your computer

The `index.html` file is essentially your website. Open this file in Chrome, Firefox or your web browser of choice. You’ll see it has a few things on it, a header, some links and a few paragraphs but apart from that it's pretty plain. The `index.css` file is where we'll be styling things.

### Text Editor

Next we'll download a text editor for us to write code in. [Sublime Text](https://www.sublimetext.com/2) suits our needs just fine.

### I've Done the HTML Tutorial

If you've done our HTML tutorial, you can use that same folder.
1. In your __assets__ folder create a new folder called __stylesheets__
2. Open your text editor, Sublime
2. In your __stylesheets__ folder create a new file called **_index.css_**

## Let’s Build
OK, so now we have some background knowledge it's time to put theory into practice. The first thing we want to do is let our HTML file know that our CSS exists, we do that by linking the two files together.
In our `index.html` we'll want to add the following line in between our `<head>` tags:

```html
  <link rel="stylesheet" type="text/css" href="assets/stylesheets/index.css">
```
The `href` attribute tells the HTML file _where_ the CSS file lives. The `rel` attribute tells the HTML what the relationship is and the `type` attribute tells the HTML what type of style the file is written in.

Your `head` element should look like this:
```html
  <head>
    <link rel="stylesheet" type="text/css" href="assets/stylesheets/index.css">
    <title>
        My portfolio site
    </title>
  </head>
```
We won't see any changes yet because our `index.css` is empty but let's fill it in and get our page looking presentable.

### Elements & Classes

CSS is written differently to HTML and we can tell the HTML to look a different way by using _selectors_. Selectors allow us to style different elements on the HTML page or give declare a common style. There are three different types of selectors.

#### Elements
We can style elements by using the element/tag name directly, add the line below to your css and see what happens.

```css
  li { background-color: red; }
```
Open your `index.html` file in your browser and you should see the `background-color` of your `<li>`s are now red. This line is saying find all the `<li>`s in the HTML and change the `background-color` to red. We don't always want to do this, and there is a way to avoid it.

_Note: CSS uses american grammar so it's **color** not colour_

#### Classes
Sometimes we only want to apply a style to a few elements or we want different elements to have the same style, we can do this by using classes. Change your line in your css to the following:

```css
  .red-bg { background-color: red; }
```
Then change one of your `<li>`s to the following:
```html
  <li class="red-bg">
```
So here, instead of saying find all the `<li>` and change their `background-color` to red, we're saying find anything with the class `red-bg` and change it to red. Add `class="red-bg"` to some other elements in your HTML and you should see their background colours change too.

With both examples you may have noticed that we use `{ }` to store the styles, these brackets are important because they group all the styles for an element/class together and tell the HTML what styles to use for each element/class. **Always remember to close your brackets**. We also use `;` to separate individual styles, so **always remember to add a `;` after each style declaration**.

### Fonts, Text, Lists & Links

### Margins, Paddings & Floats

### Backgrounds

## Finishing up


## Bonus
Remember those extra pages we linked to in our `navigation`? Try creating those pages so our links work.

Above we're linking to `about.html`, so you can create that file and put it in the same folder as our `index.html`. Try using the tags in different ways to create your pages. You could even research other tags not covered in this tutorial and use those. Check our [HTML Cheatsheet](https://github.com/blackgirltech/cheatsheets/blob/master/html-cheat-sheet.md) for more.
