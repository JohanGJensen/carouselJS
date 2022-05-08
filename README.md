# Carousel JS
Carousel js is a class based npm package used to quickly get the JS logic set up for a carousel

## Install
```
npm install @johang/carouseljs
```

## Understanding the core principle
### The idea of providing your own classes
This carousel module is ONLY meant to add the basic needed JS logic to a carousel. This means that no styling would otherwise change or happen in the browser.
The module works by you providing your classes that you then style yourself, this module changes the classes according to what carousel item you hover and click.
### Menu & Items
This module works with either a list/menu, items or both. Meaning that if you select something in either the menu or in the items, both should update their classes so you can style them accordingly.

## Basic setup example
``` javascript
const items = [
      {
        li: "Javascript",
        children: [
          {
            element: "div",
            class: "carousel-item-header",
            style: "background-color: #F9DD79",
            children: [{ element: "h3", text: "Javascript" }],
          },
        ],
      },
      {
        li: "React",
        children: [
          {
            element: "div",
            class: "carousel-item-header",
            style: "background-color: #6189C6",
            children: [{ element: "h3", text: "React" }],
          },
        ],
      },
    ];

    const menuClasses = {
      wrapper: "carousel-list-know",
      selected: "carousel-list-selected",
      base: "carousel-list",
      hover: "carousel-list-hover",
    };
    const itemClasses = {
      wrapper: "carousel-item-know",
      selected: "carousel-item-selected",
      base: "carousel-item",
      hover: "carousel-item-hover",
    };

    const classes = {
      menu: menuClasses,
      item: itemClasses,
    }

    const carousel = new Carousel(classes, items);
    carousel.init();
```