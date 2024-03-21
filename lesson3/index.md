---
title: Lesson 3 - HTML Building Blocks
nav_order: 3
---

# HTML Building Blocks

## Class Agenda

* Elements
* Whitespace
* Comments
* Combining elements
* Overview of some basic html tags
* Paragraph tag
* Heading tags
* Pens
* Quiz
* Homework

## Elements

HTML documents consist of a set of elements. In order to define elements and how they relate to each other, we mark up text content using tags.

### Anatomy of a typical HTML element

A simple HTML element - in this case a paragraph - looks like this:

```html
  <p>Text contents</p>
```

#### Opening tag

The part `<p>` is the **opening tag**. it gives the browser information about the element's type, in this case `p`, which represents a paragraph, surrounded by angle brackets (`<` and `>`). We also use the term "tag name" for `p` in this case. The browser will consider everything following the opening tag up to the point where it finds a closing tag (of the matching type/name) to be the element's content.

#### Content

The **content** of an element is everything between its opening and closing tag. The content can consist of text, other HTML elements or nothing at all. In our example, the content is `Text contents`.

An empty element - in this case a table cell - could look like this:

```html
<td></td>
```

#### Closing tag

Just like the opening tag, the **closing tag** also contains the type of the element. It is written with an additional `/`. In our first example, our closing tag is `</p>`, because our element is of the type `p`, representing a paragraph.

#### Attributes

While closing tags always look the same, opening tags can contain extra information in the form of **attributes**.

```html
<p class="my-class">Text contents</p>
<a href="https://www.redi-school.org">To the ReDI Website</a>
```

You can put as many attributes into an opening tag as you like.

```html
<a href="https://www.redi-school.org" class="featured-link" title="Click me!">To the ReDI Website</a>
```

Some attributes don't even need a value, but are complete as a single word.

```html
<p hidden>The browser will not display this element.</p>
```

### Anatomy of a void element

A void element is special type of element that must not contain anything. No text, no HTML elements. This is why a void element also **must not** have a closing tag.

The following code inserts three different void elements:

```html
<hr>
<br>
<img src="dog.jpeg">
```

Never do this:

```html
<hr></hr>
<br></br>
<img src="dog.jpeg"></img>
```

You might encounter void elements that contain a trailing `/`, e.g.

```html
<br />
<hr/>
```

Some developers prefer to write void elements like this, so they're easier to recognize. In modern HTML, any opening tag can contain a trailing `/`, which will just be ignored by the browser.

## Whitespace

You might think that space characters, line breaks and tabs in HTML are displayed in an unexpected way. The following two code examples are equivalent:

```html
<p>HTML is so much fun!</p>
```

```html
    <p   >       HTML   
  is  so     

        
      much
  fun!
</p>
```

Generally, the browser will interpret every number of so-called **whitespace** characters (spaces, tabs or line breaks) as one single space character, as long as it's greater than 0.

This is why whitespace is perfect for formatting, i.e. making our code more readable. Instead of just something like...

```html
<ul><li>Lorem</li><li>Ipsum</li><li>Dolor</li></ul>
```

...we can make our code nice and readable:

```html
<ul>
  <li>Lorem</li>
  <li>Ipsum</li>
  <li>Dolor</li>
</ul>
```

## Comments

**Comments** are parts of the code that are always ignored by the browser. There are numerous reasons why you as a developer might want to use them, with the most common ones being:

* Explaining your code to your future self or other developers
* Increasing the readability of your code
* Temporarily deactivating some of your code

Comments are not HTML elements, although they look quite similar:

```html
<!-- This is a comment -->
<p>This sentence contains five <!-- and not eight --> words</p>
<p>This is one <!-- </p>
<p> --> single paragraph</p>
```

## Combining elements

Elements can't only contain text contents, but also other elements. Actually, every HTML page is just one single element (of the type `html`) that contains other elements. For now, we'll keep things simple and will concentrate on the visible parts of a document.

When an element contains another element, the **child element** is **nested** within its **parent element**.

```html
<div><!-- opening tag of the parent element -->

  Some text content of the parent element.

  <div><!-- opening tag of the child element -->
    Contents of the child element.
  </div><!-- closing tag of the child element -->

  More text content of the parent element.

</div><!-- closing tag of the parent element -->
```

In this case, the content of the parent element consists of three lines of text (including the child element's content).

When a child element is surrounded by a parent element, you could also say it is wrapped in it.

When you structure your document, you can nest elements infinitely and put them next to each other almost any way you like.

```html
<header>
  <nav>
    <ul>
      <li>
        <a href="home.html">
          Home
        </a>
      <li>
      <li>
        <a href="contact.html">
          Contact
        </a>
      </li>
      <!-- ... -->
    </ul>
  </nav>
  <input type="text" placeholder="Search...">
</header>
<main>
  <article><!-- ... --></article>
  <article><!-- ... --></article>
  <!-- ... -->
</main>
```
## Overview of some basic html tags

* `<!DOCTYPE html>`: This declaration defines the document type and version of HTML you are using, typically HTML5.
* `<html>`: Root element that contains all other HTML elements on the page.
* `<head>`: Contains meta-information about the document, such as the title of the page and links to external resources like stylesheets and scripts.
* `<title>`: Sets the title of the web page, which appears in the browser's title bar or tab.
* `<meta>`: Provides metadata about the HTML document, like character encoding and viewport settings.
* `<link>`: Specifies external resources like stylesheets (CSS) to be used with the HTML document.
* `<style>`: Used to define inline CSS styles for specific elements on the page.
* `<script>`: Includes JavaScript code or references an external JavaScript file.
* `<body>`: Contains the content that is displayed on the web page, such as text, images, and other HTML elements.
* `<h1>, <h2>, ..., <h6>`: Headings from 1 (largest and most important) to 6 (smallest and least important).
* `<p>`: Defines a paragraph of text.
* `<a>`: Creates hyperlinks to other web pages or resources.
* `<img>`: Embeds images on the page.
* `<ul>`: Defines an unordered (bulleted) list.
* `<ol>`: Defines an ordered (numbered) list.
* `<li>`: Used within `<ul>` or `<ol>` to define list items.
* `<div>`: A generic container element used to group and style content.
* `<span>`: A generic inline container element for styling or scripting purposes.
* `<br>`: Inserts a line break within text.
* `<hr>`: Creates a horizontal line or thematic break.
* `<form>`: Defines a form to collect user input.
* `<input>`: A form element for various types of input, like text fields, checkboxes, and radio buttons.
* `<textarea>`: Defines a multiline text input field.
* `<button>`: Creates clickable buttons within forms or web pages.
* `<table>`: Defines an HTML table.
* `<tr>`: Defines a table row.
* `<td>`: Defines a table cell.

## Paragraph tag

The `<p>` tag stands for "paragraph" in HTML. It is used to structure and format text content on a web page. When you want to separate text into distinct paragraphs, you use the `<p>` tag to indicate the beginning and end of each paragraph.

Basic Syntax:
```html
<p>This is a paragraph of text.</p>
```
The basic syntax of the `<p>` tag is as follows:

- `<p>` is the opening tag.
- `</p>` is the closing tag.
- The text content you want to display as a paragraph goes between the opening and closing tags.

Example:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Paragraphs Example</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is the first paragraph. It contains some text.</p>
    <p>This is the second paragraph. More text here.</p>
    <p>And here's a third paragraph. You can keep adding more as needed.</p>
</body>
</html>
```

Key Points:
1. **Opening and Closing Tags**: The `<p>` tag always comes in pairs. The opening tag `<p>` marks the beginning of a paragraph, and the closing tag `</p>` marks the end of the paragraph.
2. **Whitespace**: HTML ignores extra white spaces (like spaces, tabs, and line breaks) within the `<p>` tags. It automatically formats the text to display as a block of text with appropriate spacing.
3. **Nesting**: Paragraphs can contain other HTML elements, such as links, images, or lists. You can nest other HTML elements within `<p>` tags to create rich content.
4. **Semantic Meaning**: The `<p>` tag is a way to give semantic meaning to your content. It tells browsers and search engines that the enclosed text is a separate paragraph, which can be useful for accessibility and SEO.

## Heading tags
HTML heading tags, denoted by `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, and `<h6>`, are used to define headings and subheadings on a web page. These tags represent a hierarchical structure, where `<h1>` is the most important and usually represents the main title of the page, while `<h6>` is the least important and represents a minor heading or sub-subheading.

Example:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
</head>
<body>
    <h1>Main Heading</h1>
    <p>This is some content of the page.</p>
    <h2>Subheading 1</h2>
    <p>This is some content under Subheading 1.</p>
    <h3>Sub-subheading 1.1</h3>
    <p>Content under Sub-subheading 1.1.</p>
    <h2>Subheading 2</h2>
    <p>Content under Subheading 2.</p>
</body>
</html>
```

Key Points:

1. **Hierarchy**: Use heading tags in a hierarchical order, starting with `<h1>` for the main title and descending to `<h6>` for less important headings.
2. **Semantic Meaning**: Headings provide semantic meaning to your content, helping search engines and screen readers understand the structure of your page.
3. **Styling**: By default, browsers render headings with different font sizes, making them stand out. You can further style them with CSS (Cascading Style Sheets).
4. **Accessibility**: Properly structured headings improve accessibility for users with disabilities. Screen readers can announce headings, aiding navigation.
5. **SEO**: Search engines use headings to understand the content of a page. Properly structured headings can positively affect your site's search engine ranking.
6. **Use as Needed**: Use the appropriate heading level for the importance of the content. Don't skip levels (e.g., going from `<h2>` to `<h4>` without using `<h3>`).

## Pens


* [Simple HTML elements: Find and fix all mistakes](https://codepen.io/redi-school/pen/GRLWGmW?editors=1000) ([Solution](https://codepen.io/redi-school/pen/xxaQoWz))
* [Wheel of Fortune](https://codepen.io/redi-school/pen/VwGVqKw)
* [Updating a simple blog page](https://codepen.io/redi-school/pen/ZEMmVmw) ([Solution](https://codepen.io/redi-school/pen/mdGQNmP))
* [Comments](https://codepen.io/redi-school/pen/QWVJPjM) ([Solution](https://codepen.io/redi-school/pen/rNZQXRg))

Bonus Pens we didn't cover:
* [Bold and italic text in one line](https://codepen.io/redi-school/pen/MWqzxdO)
* [Line breaks - inline vs. block elements](https://codepen.io/redi-school/pen/oNPQOwN)

## Quiz

* [Quiz](https://create.kahoot.it/share/lesson-3-html-css-lesson-3-quiz-on-the-building-blocks-of-html/5aeef43f-74c4-4ce1-a7ff-d60fa1285f92) / [live](https://kahoot.it/?pin=9441788&refer_method=link)

* Match the HTML tags on the left with their descriptions on the right.  
  `<p>`:            a. Used for creating lists with numbered points.  
  `<h1>`:           b. Defines a paragraph of text.  
  `<div>`:          c. Used for creating lists with bullet points.  
  `<ul>`:           d. Creates a large, top-level heading.  
  `<li>`:           e. A generic container for styling or scripting.  
  `<ol>`:           f. Defines a subheading or lower-level heading.  
  `<h2>`:           g. Represents a list item.  


## Homework

[You can find today's homework on CodePen: Build your own HTML page](https://codepen.io/redi-school/pen/xxeqzJw?editors=1000)

Assignment:
1. Build a basic HTML page using the following elements:
- headers
- paragraph
- void element
- list
- comments 
