# Carousel JS
carousel js is a class based npm package used to quickly get the JS logic set up for a carousel

## Install
```
npm install @johang/carouseljs
```

## Basic setup example
```
const projectList = document.getElementsByClassName("carousel-list-project");
const projectItem = document.getElementsByClassName("carousel-item-project");

let projectListClasses = {
  wrapper: "carousel-list-project",
  selected: "carousel-list-selected",
  base: "carousel-list",
  hover: "carousel-list-hover",
};

let projectItemClasses = {
  wrapper: "carousel-item-project",
  selected: "project-item-selected",
  base: "carousel-item",
  hover: "carousel-project-item-hover",
};

const projectCarousel = new Carousel(projectListClasses, projectItemClasses);
projectCarousel.setListAndItems(projectList, projectItem, projects);
projectCarousel.setPositionStyle("margin", 20);

projectCarousel.setCarouselItemsPosition();
projectCarousel.addPositionListeners();
```