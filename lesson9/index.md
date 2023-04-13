---
title: Lesson 9 - CSS Layout
nav_order: 9
---

# CSS Layout

## Class Agenda

1. Introduction to CSS Layout
2. Introduction to flexbox


## 1. Introduction to CSS Layout

A website is divided into different parts, that together add to a layout. E.g. you have a header, a footer, navigation and main and side-content. All this needs can be structured with CSS.

<img width="400px" alt="Example of a layout" src="./css_layout_example.png" />


You can use various techniques in CSS to control the layout. 
We will focus mainly on

- The flow layout
- Flexbox
- Grid

There are other techniques, like positioning and using the table for layouting, which is not used anymore nowadays with more modern approaches. If you are curious, you can find some more on the history of CSS layouting [here](https://dev.to/dianale/css-layouts-history-from-float-to-flexbox-and-grid-5af7)


## Display property

The most frequently used values of the `display` property are:

- `display: block`
- `display: inline`
- `display: inline-block`
- `display: flex`
- `display: grid`
- `display: none`

The display property defines how an element is treated on your website in regards to layout. 
The values `block`, `inline` and `inline-block`, are using the [Flow Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flow_Layout) while flex and grid have their own layout system.

## Flow layout with block, inline and inline-block

<img width="400px" alt="Example of a flow layout" src="./flow_layout.png" />

### display: inline

- `inline` elements behave like words in a sentence. 
- They sit next to each other in the inline direction.
- You can't set an explicit width and height on inline elements. Any block level margin and padding will be ignored by the surrounding elements.
- Elements such as \<span\>, \<a\>, \<strong\>, are inline by default. 

#### display: block

- `block` elements create a new line for themselves. 
- A block element will expand to the full width by default. 
- The margin, width and height on all sides of a block element can be added
- Elements such as \<div\>, \<h1\> and \<p\> (paragraph), are block by default. 

#### display: inline-block

- `inline-block` combines features of both inline and block elements
- Inline-block elements can appear next to each other and we can set their dimensions using the width and height properties. 
- \<img\> are the best example of default inline-block elements

You can play around with [this example](https://codepen.io/redi-school/pen/WNarxpY) and solve [this exercise](https://codepen.io/redi-school/pen/wvYMWdE)

## Quiz
[Here](https://create.kahoot.it/share/berlin-html-css-s23-lesson-9/82fefecc-3845-483f-8759-dba7668d3f7e) a small quiz to test your knowledge.




# Homework

- Finish the box model [excersise](https://codepen.io/redi-school/pen/NWOxrRL)
- Finish the CSS layout [exercise](https://codepen.io/redi-school/pen/wvYMWdE)

# Resources

- [The CSS Box Model Explained by Living in a Boring Suburban Neighborhood](https://www.freecodecamp.org/news/css-box-model-explained-by-living-in-a-boring-suburban-neighborhood-9a9e692773c1)
- [CSS Layout](https://www.smashingmagazine.com/2018/05/guide-css-layout/)
- [History of CSS Layout](https://dev.to/dianale/css-layouts-history-from-float-to-flexbox-and-grid-5af7)
- [Slides](https://docs.google.com/presentation/d/1-lUopHb5vePTrahBO0XBxU4MD4H07ybszNUS8CFx0To/edit?usp=sharing)

