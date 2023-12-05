<!-- ---
title: Lesson 16 - CSS Positioning
nav_order: 16
--- -->

# CSS Positioning

## Introduction

The positioning of elements can be controlled via the CSS `position` rule. It allows you to take elements out of their normal flow. This section briefly introduces CSS Positioning and available values.

position: static - This is the default positioning which HTML elements are using.

position: relative - takes an element out of its normal flow and places it relative to its normal flow. To do this relative placement one needs to use the following CSS rules: `top`, `right`, `bottom`, `left`.

position: absolute - places elements with respect to their parent or ancestor containers. It is used to create more complex layouts and features. Absolute positioning is a very special one because it can introduce different behavior based on the [positioning context](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning#positioning_contexts) of the element on which we apply this position type.

position: fixed - fixes an element relative to the visible viewport.

position: sticky - This positioning type is a combination between relative positioning and fixed positioning. [Differences](https://dev.to/suryawiguna/css-position-fixed-vs-sticky-5232#:~:text=What's%20the%20difference%3F,offset%2C%20like%20top%3A%2010px%20.) between fixed and sticky positioning.

## Syntax

```css
nav {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
}
```

## Exercise

[Codepen](https://codepen.io/eporubin/pen/XWxBgPp)

## Glossary & Terminology

- `Positioning` - The characteristic of elements, which defines where exactly on the webpage they are placed. Whether that is with a normal flow or taken out of the normal flow.

- `Z-Index` - The `z-index` CSS property sets the z-order (i.e. z-axis placement) of a positioned element and its descendant items. Overlapping elements with a larger z-index cover those with a smaller one. More on this can be seen [here](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)

---

## Homework

[Codepen](https://codepen.io/eporubin/pen/BaqPZbg)

## Resources

- [Positioning](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning#positioning_contexts)
- [z-index](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)
- [fixed vs sticky](https://dev.to/suryawiguna/css-position-fixed-vs-sticky-5232#:~:text=What%27s%20the%20difference%3F,offset%2C%20like%20top%3A%2010px%20.)
- [w3 schools - positioning](https://www.w3schools.com/css/css_positioning.asp)

## Slides

<iframe src="https://docs.google.com/presentation/d/159gqnSTK9KfKxATmxguJBAHM-4Qb3lqR/embed" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
