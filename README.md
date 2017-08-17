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
_Note: CSS uses american grammar so it's **color** not colour_

### Text, Lists & Links

#### Text
We can change the size, font-weight, font and color of the text on our page with CSS.

Let's assume we want all the text on our page to be the same font, add the following line to your css file:

```css
  body { font-family: 'Ubuntu', sans-serif; }
```

This line tells our HTML in the browser to use the 'Ubuntu' font, if it doesn't have 'Ubuntu', it'll use the first sans-serif font it finds. Fonts depend on what fonts your end user has installed on their machine so it's best to use web safe fonts, these are fonts that are pre-installed on most computers. Find a list of web-safe fonts [here](http://www.cssfontstack.com/Web-Fonts).

Okay, so let's ensure our paragraph looks the same in every browser. Add the following lines:

```css
  p {
    font-size: 24px;
    font-weight: lighter;
    color: gray;
  }
```
Here, we've declared all the `<p>` tags to be `24px` and `gray`. We've also said the `font-weight` should be `lighter`, this can be also take the numerical values `100` - `900` and the terms `bold`, `bolder`, `normal`. Experiment with the size, colour and weight until you find something you like.

We can add these same styles to headings, lists and links, pretty much any text element but lists and links come with added syntax we can use to be spesific.

#### Lists
List elements have two parts the `<ul>` or `<ol>` and the `<li>`. It important to give the right element the right style otherwise we will get unexpected results. The `<ul>` is offers unique styling options that allow us to do thnigs like remove the default bullet points, let's try by adding the following line to our CSS:

``` css
  ul { list-style: none; }
```
If we had done `li { list-style: none; }` we wouldn't have seen the results we wanted. Change the selector to see for yourself.

#### Links
Like links, lists have their own ways to be styled. Lists have various **states**: `:hover`, `:visited`, `:focus` and `:link`, `:active`, and you can style links dependent on their state. Add the following:

```css
a:link {
  color: coral;
  text-decoration: none;
}
```
We want all links to be `coral` and to have no text-decorations, including underline. On a website, different colours are used to denote different states so, let's do that.

```css
a:hover {
  color: green;
  text-decoration: underline;
}

a:visited {
  color: gray;
}
```
Users can now easily spot links and see what links they've visited or are about to visit.

### Margins, Paddings & Floats

### Backgrounds

## Finishing up


## Bonus
Remember those extra pages we linked to in our `navigation`? Try creating those pages so our links work.

Above we're linking to `about.html`, so you can create that file and put it in the same folder as our `index.html`. Try using the tags in different ways to create your pages. You could even research other tags not covered in this tutorial and use those. Check our [HTML Cheatsheet](https://github.com/blackgirltech/cheatsheets/blob/master/html-cheat-sheet.md) for more.
