---
title: Lesson 5 - HTML Recap & Introduction to CSS
nav_order: 5
---

# HTML Recap & Introduction to CSS

## Class Agenda

- Review what we've learned about HTML
- Write CSS styles using element selectors

# HTML Recap

## HTML Tags

So far we've learned the following tags:

- Heading tags: `<h1></h1>, <h2></h2>...<h6></h6>`
- The paragraph tag: `<p></p>`
- The div tag: `<div></div>`
- Order and unordered list tags, and the list item tag: `<ol></ol>, <ul></ul>, <li></li>`
- The image tag: `<img>`
- The anchor tag: `<a></a>`
- The family of table tags: `<table></table>, <thead></thead>, <th></th>, <tr></tr>, <td></td>`

Hopefully you have already used most of these tags at least once! You'll have more chances to practice as the semester goes on.

If you feel confused or uncertain about what any of those tags are for at this point, please review the materials for the previous lessons, make sure you have attempted the homeworks, and ask questions on Slack!

## HTML Attributes

We've also learned about HTML attributes. Attributes are always part of the _opening tag_ of an HTML element. They take the form `attributename="attribute-value"`, such as `<a href="https://google.com">Link to Google</a>`. In this case, we are using the `href` attribute to make google.com the destination of our link.

Another example is `<img src="https://placekitten.com/200/300" />`. In this case, we are using the `src` attribute to display the image that exists at https://placekitten.com/200/300.

So far, we have focused on the 4 most common HTML attributes:

- `href`, which is used most often with an `<a>` tag to link from one page to another.
- `src`, which is used most often with an `<img>` tag to determine which image to display.
- `class`, which is used most often to style elements with CSS. We'll work with classes lots more starting next lesson.
- `id`, short for "identifier," which is used to uniquely identify an element. It may be used for CSS styling, or in combination with Javascript to add specific behavior to an element, or for other purposes. Again, we will get more practice with ID in the futrue.

It's OK if you still don't feel comfortable using all of the elements or attributes. For now, just practice using them, and ask questions when you don't understand. We'll use them lots more this semester.

[Kahoot Quiz](https://create.kahoot.it/details/f53295fd-3126-40f1-bb45-004014445707) (Teacher link; log in with ReDI credentials)

# Introduction to CSS

CSS allows us to change how our HTML looks. To add CSS styles to our HTML, we have to follow two steps:

1. _Select_ elements
2. _Apply_ styles to those elements

## Selecting elements

What do we mean by "select elements"? Let's say we want to make all of the `<h1>` headers on our page red, but we want to keep all text within `<p>` tags black. To do this, we have to be able to say "this style should only apply to certain elements! Not all text on the page should be red!" So that's what "selecting" elements means: choosing which elements should receive a style.

There are many different ways to select certain elements and apply styles to them, which we will learn about in the coming sessions. For today, we'll learn to select elements using the _element selector_.

To use an _element selector_, we write the name of the element in our CSS, like this:

```css
h1 {
}
```

The `h1` in this code block is the _selector_. It is followed by _curly braces_ `{}` (also known as _curly brackets_; you may hear teachers use both words. They mean the same thing), which have nothing between them at the moment. This is standard CSS syntax: we have to write a selector followed by curly braces. Inside the curly braces we will write which styles should apply to the selected elements.

## Applying styles to the selected elements

Once we have used a selector to specify which elements will receive styles, we can apply styles! Remember that we want to color our `h1` headers red. To do so, we will add a _declaration_, with a _property_ and _value_.

```css
h1 {
  color: red;
}
```

In this case, our _declaration_ is `color: red;`. The _property_ is `color`, and the _value_ is `red`.

This code means "select all `h1` elements in the HTML and make them red." What if we wanted to change them to be blue? We could simply update the _value_ in our declaration:

```css
h1 {
  color: blue;
}
```

What if we want to change how the text looks? To do that, we can use a CSS _property_ called `font-family`, like this:

```css
h1 {
  color: blue;
  font-family: Arial;
}
```

We've added to our styles! Now our headings will be blue, AND they will use a different font than before. The new _declaration_ is `font-family: Arial;`. The _property_ is `font-family`, and the _value_ is `Arial;`.

## CSS properties

We've used two CSS properties so far, `color`, and `font-family`. There are many more properties that we can use! It's not always easy to know exactly which CSS property to use if you want to achieve a specific result. If you're not sure what to use, Google it or ask in the class Slack channel.

Here are a few more common CSS properties that we will use this semester:

- Use the CSS color property for text colors
- Use the CSS font-family property for text fonts
- Use the CSS font-size property for text sizes
- Use the CSS border property for borders
- Use the CSS padding property for space inside the border
- Use the CSS margin property for space outside the

## CSS comments

Just like in HTML, you can use a comment to add notes to your CSS that will not affect the styles of your page. CSS comments begin with `/*` and end with `*/`, like this:

```css
/* This is a comment, so it will not affect my styles.

If I write a selector and a style, but it is in my comment, it has no effect!

p {
  color: pink;
}

See? That did not have any effect!
*/

h1 {
  color: blue;
  font-family: Arial;
}
```

# Exercises

Fork this CodePen and make the changes requested in the comments of the HTML and CSS section.
1. Create a TOC for the web page HTML structure of Lesson 5 with the ordered <ol> list in Codepen. The list should contain the title and subtitles of the section heading <h1>, <h2>, <h3> elements. [Link to the exercise](https://codepen.io/redi-school/pen/RwOZWKp).
2. Create the same TOC for the web page HTML structure Lesson 5 with the table <table> element in Codepen. The list contains the title and subtitles of the section heading <h1>, <h2>, <h3> elements. The table cells contains the title and subtitles of the section heading <h1>, <h2>, <h3> elements and their consecutive number of levels. [Link to the exercise.](https://codepen.io/redi-school/pen/rNbzOYX)
3. Edit HTML & CSS according to the comments. For this third exercise you do not have to modify the HTML at all! [Link to the exercise.](https://codepen.io/redi-school/pen/bGxywzN)

# Homework

Fork this CodePen and modify the CSS styles until it looks something like this image. It's OK if it's not exactly the same! Feel free to experiment!

CodePen link: [https://codepen.io/redi-school/pen/VwGOpJq](https://codepen.io/redi-school/pen/VwGOpJq)

<img width="400px" alt="Scrennshot of what your page should look like at the end" src="final-product.png" />

# Glossary & Terminology

- CSS Selector: A CSS selector is the first part of a CSS Rule. It is a pattern of elements and other terms that tell the browser which HTML elements should be selected to have the CSS property values inside the rule applied to them. More on this [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors#what_is_a_selector).

# Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSu5nyjXiuL95InwXE2ut10Jnu9zqT9bFwmJYpjPI9ihblyIxFC48qr84iioeAYAZuNlkPDOZk1giOH/embed" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
