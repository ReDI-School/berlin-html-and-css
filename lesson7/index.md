---
title: Lesson 7 - Using CSS Selectors
nav_order: 7
---
1. Review CSS Type/Element Selector
2. Selector lists
3. CSS class and ID selectors

CHECKIN
- - - -
Before we start the lesson:
You’ll be put into two-person breakout rooms. Share what
you are finding most difficult about
class so far, and ask if they have ideas!

When we return, we will share some things that came up during the chats
5-10min

## Review of CSS type/element selector
quick check in to see if everyone understands/remembers concept
5 mins

Last class, we learned the _CSS type selector_ (also called the _element selector_). Here's an example:

```css
h1 {
  font-family: Arial;
  color: powderblue;
  font-size: 40px;
}
```

This CSS code means: "All h1 elements on the page should have the font family `Arial`, the color `powderblue`, and the size 40 pixels."

## Selector lists

It's possible to put a comma between CSS selectors and apply the same style to all elements matching those selectors.

```html
<h1>I want this heading to be red!</h1>
<p>
  This is a paragraph. I want it to be the same color as the heading. In fact, I
  want ALL of my paragraphs to be the same color as my heading!
</p>
```

```css
h1, p {
  color: red;
}
```

In this case, our CSS means "all elements h1` and all `p` elements should have the style `color: red`."

## CSS Class and ID selectors

That's great if we want a style to apply to every element of that type on our page. But what if we only want some elements of a specific type to have a certain style?

For example, take this HTML:

```html
<h1>I want this heading to be red!</h1>
<h1>And I want this heading to be blue!</h1>
```

If I write the following CSS:

```css
h1 {
  color: red;
}

h1 {
  color: blue;
}
```

Both of my headings will now be blue! This is because when there are two conflicting styles, the one lower down in the CSS will always win. In other words, because `color: blue` comes after `color: red`, the color will always be blue.

To make our two headings different colors, we need to use a different selector. Let's try the _CSS class selector_.

### Class selectors

Up until now, we've used the _type selector_, which selects ALL elements of a specific type (`h1`, `p`, `img`, etc.). A _class selector_ selects _all elements with a specific class attribute_.

Here's an example:

```html
<h1 class="red-heading">I want this heading to be red!</h1>
<h1 class="blue-heading">And I want this heading to be blue!</h1>
```

```css
.red-heading {
  color: red;
}

.blue-heading {
  color: blue;
}
```

In our HTML, we have now set `class` attributes on both of our elements. Remember that `class` is a _global attribute_, which means it can be set on any element.

In our CSS, we have then used a `.` and the name of the class we want to style. The `.` indicates that we are using a class selector.

A class selector can have any name - the only thing required for it to work is that the name must match in the CSS and HTML.

For example, take this code:

```html
<h1 class="asb0180g">I want this heading to be red!</h1>
<h1 class="yellow-chair">And I want this heading to be blue!</h1>
```

```css
.asb0180g {
  color: red;
}

.yellow-chair {
  color: blue;
}
```
This code works _exactly the same_ as our previous code. Again, we set a `class` attribute in our HTML, and then we use a class selector to style those elements. The name of the class does not matter, as long as it matches in the HTML and CSS!

### ID selectors


ID selectors work exactly the same as `class` selectors, but using the `id` attribute and the `#` symbol instead of a `.`:

```html
<h1 id="red-heading">I want this heading to be red!</h1>
<h1 id="blue-heading">And I want this heading to be blue!</h1>
```

#blue-heading {
  color: blue;
}
```
Just like with `class` selectors, our `id` selectors have to match the value in our `id` attribute in the HTML. The values can be anything, as long as they match.
```html
<h1 class="kjng0923jg">I want this heading to be red!</h1>
<h1 class="chocolate-cake">And I want this heading to be blue!</h1>
```
```css
#kjng0923jg {
  color: red;
}

#chocolate-cake {
  color: blue;
}
```

### Class vs. ID selectors

When should you use a class selector and when should you use an ID selector?

Most of the time, you'll use a `class` attribute and the class selector (with `.`).

That's because there are two important differences between the `class=""` attribute and the `id=""` attribute.

First, you _cannot have more than one element with a specific ID attribute_ on your page! But it is perfectly acceptable to have multiple elements with the same class attribute in your HTML.

Second, one element can have multiple classes by separating them with a space, but an element can _not_ have more than one ID.

This is fine:

```html
<h1 class="red-heading large-text">
  I want this heading to be red and have large text!
</h1>
<h1 class="red-heading">Another red heading!</h1>
<h1 class="blue-heading">And I want this heading to be blue!</h1>
<h1 class="blue-heading full-width">
  This one too! And I want it to be extra wide!
</h1>
<h1 class="red-heading">Back to red!</h1>
<h1 class="blue-heading">Back to blue!</h1>
```

Do **not** do this, it is not valid HTML because two elements have the same `id` attribute:

```html
<!-- Don't do this! -->
<h1 id="red-heading">I want this heading to be red!</h1>
<h1 id="red-heading">I should have used a class instead...</h1>
<h1 id="blue-heading small-text">I should have used a class instead...</h1>
<!-- Don't do this! -->
```

It is very useful to be able to have multiple elements with the same `class` attribute. That way, you can apply the same style to a whole group of elements at the same time!

And adding multiple classes to an element means you can make your classes composable, meaning you can combine several classes to achieve a desired result (such as having separate `red-heading` and `large-text` classes, one of which sets a color and one of which sets a font-size).

So what is the point of IDs if they are not reusable?

Well, they are often used for Javascript or for linking to a specific part of a page. And sometimes they are useful for applying CSS styles as well, especially when chaining selectors. More on that topic in following lessons!

## Exercise 1

Fork this CodePen and follow the instructions to add styles using class and ID selectors: https://codepen.io/EsYetsko/pen/abPXPmR?editors=1100

# Exercise Description
Group breakout rooms (3/4 people)
15 minutes
Fork this CodePen and follow the instructions:
Include the following:
1 ID (minimum):
HTML:    id= “id-name”
CSS:    #id-name { }
2 Classes (minimum):
HTML:    class= “class-name”
CSS:    .class-name {  }
1 selector list (minimum):
CSS: h1, h2, p { }
Remember that there is no right answer but each element should have CSS!

# HOMEWORK:
Create your personal biography page until it has all of the following elements, attributes, selectors, and styles:
HTML elements: h1, h2, h3, p, img, ul, ol, li, a
HTML attributes: class, id, src, href
CSS selectors: type (h1, h2, p, etc.), class (.), id (#), selector list (like h1, p {...})
CSS styles: color, font-size, font-family, background-color, border, padding, margin

If part of this feels repetitive, that’s because it is! Repetition helps us remember material and get faster at accessing it in our brains :)


- Read more about different web font families [here](https://www.hostinger.com/tutorials/best-html-web-fonts). Get to know what the different companies are using
- (Optional) Check out the nice [CSS tricks](https://css-tricks.com/almanac/properties/t/text-shadow/) with text shadow

- [Recap of HTML Tree](http://web.simmons.edu/~grabiner/comm244/weekfour/document-tree.html)
- [CSS Descendant Selector](https://www.w3schools.com/css/css_combinators.asp)
- [CSS Basic Colors](https://www.w3schools.com/css/css_colors.asp)
- [CSS Standard Names](https://www.w3schools.com/colors/colors_names.asp)
- [CSS Text](https://www.w3schools.com/css/css_text.asp)
- [CSS Font](https://www.w3schools.com/css/css_font.asp)
- [Web Safe Fonts](https://www.w3schools.com/css/css_font_websafe.asp)


Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSbsiMhh-u4zUQBlAsgoV4rllJv1i1fzCV3oUTXt9W6ybIGNGRm2MD25YEfbNwDJVLul9WyOn4Aul1u/embed" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
