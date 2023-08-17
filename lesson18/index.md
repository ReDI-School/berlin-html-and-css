---
title: Lesson 18 - CSS Grid Part II
nav_order: 18
---

# CSS Grid Part II

In this lesson, we'll continue to build our grid skills, learning new ways to position items in a grid and getting lots of practice!

## Agenda

1. `grid-template-areas` and `grid-area`
2. Overlapping items in a grid using `z-index`
3. `grid-auto-rows` and `grid-auto-columns`
4. Final project intro

## `grid-template-areas` and `grid-area`

There are two common ways to position items in a grid: using `grid-column/row-start/end` and `grid-template-areas` + `grid-area`.

In the last lesson, you learned how to position items in a grid using `grid-row-start`, `grid-row-end`, `grid-column-start`, `grid-column-end`, and the shorthand properties `grid-row` and `grid-column`.

`grid-template-areas` lets you define a named _area_ in a grid. `grid-area` then is applied to an element to tell it to fill up that area.

Let's look at an example:

```html
<body>
  <div class="grid-container">
    <div class="blue"></div>
    <div class="white"></div>
    <div class="green"></div>
    <div class="red"></div>
  </div>
</body>
```

```css
.grid-container {
  /* 
  We have to define a width and height because our divs have no content (images/text).
  By default, a grid will size the rows and columns according to the contents inside.
  */
  height: 500px;
  width: 500px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-template-areas:
    "blue blue blue"
    "red white white"
    "green green green";
}

.blue {
  grid-area: blue;
  background-color: blue;
}

.red {
  grid-area: red;
  background-color: red;
}

.white {
  grid-area: white;
  background-color: white;
}

.green {
  grid-area: green;
  background-color: green;
}
```

This code produces the following:

<img width="500px" alt="Screenshot with a grid example" src="example-grid-colorful.png" />

To create this layout, we named areas of our grid using `grid-template-areas`. Then we used `grid-area` on individual elements to put them in the named areas of the grid.

You can name your grid areas anything you want, as long as the name in `grid-template-areas` matches `grid-area`:

There are two important restrictions to remember when positioning items using `grid-template-areas`:

1. Your areas must be contiguous. In other words, you cannot split one area into two pieces. Why? Because one HTML element cannot be in two separate places at the same time
2. Your areas must be rectangular

## Slides

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTQCkKjklGtEJrjTJ-2u3mQA5F7iF-uXxmRWSsdALFeQ6Zr1O5VXQu39akejsI0kQ3dOhlShZoHUDnN/embed" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
