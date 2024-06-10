# Lab - JavaScript Events

## Overview

This lab will further help you understand how JavaScript Events work.

The Flatburger restaurant wants to add functionality to their website that displays a menu of burgers to sell to its customers. You will need to use your knowledge of JavaScript Events to complete this lab.

## Tools and Resources

It is recommended that you use the Visual Studio Code (VSCode) IDE for this lab.

Useful considerations and terminology:

**Event**: Something a user does on a web page or something that happens on a web page.

**Event handler**: A callback function that executes code in response to an event.

**click event**: An event that occurs when a user clicks on an element on a web page.

**change event**: An event that occurs when a user selects or changes a value for an element on a web page that contains a value attribute.

Here are some other useful resources:

- MDN
  - [Introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)
  - [Event reference (Web Events)](https://developer.mozilla.org/en-US/docs/Web/Events)
  - [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)
    - [Element: click event](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
  - [HTMLElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement)
    - [HTMLElement: change event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event)

## Instructions

In this lab, you will practice adding event listeners to allow for elements to listen for events and execute code in response to events.

**Fork and clone** this lab into your local environment. Navigate into its
directory in the terminal, then run `code .` to open the files in Visual Studio
Code.

Then, open the `index.html` file on your browser to run the application.

Write your code in the `index.js` file. There is some starter code provided in `index.js`.

These are your tasks:

1. `addBurgerImageToMenu(burger)`: The `addBurgerImageToMenu()` function has been declared for you and most of the code for this function has been written for you. It has 1 parameter named `burger` whose value is an `object` that contains the following keys: `name`, `image`, `description`, and `healthy`. Write the code to add an event listener to the `<img>` element stored in the `burgerImage` variable that will allow the `<img>` element to listen for a `click` event. The event handler (callback function) for the event listener should call the `displayBurgerDetails()` function and pass in the `burger` parameter as an argument to the `displayBurgerDetails()` function.
2. Add an event listener to the `<select>` element with the id of `burger-select` that will allow the `<select>` element to listen for a `change` event and will call the `updateBurgerMenu()` function in response to the `change` event.
3. `updateBurgerMenu(event)`: The `updateBurgerMenu()` function has been declared for you, but you will need to write the code that should go inside of this function. It has 1 parameter named `event` whose value should be an Event object through which you can access the value for the selected option from the `<select>` element’s dropdown menu via `event.target.value`, when the `updateBurgerMenu()` function is the event handler (callback function) that is invoked in response to the `change` event from the previous task. When the `updateBurgerMenu()` function is called, the following actions should take place:
    - The contents of the `<div>` element with the id of `burger-menu` are cleared so it no longer has any elements nested inside it.
    - `If` the selected option from the `<select>` element’s dropdown menu is `all`:
      - Iterate over the array stored in the `burgers` variable using an array iterator method such as `forEach()`. For each of the burgers in the array stored in the `burgers` variable, the `addBurgerImageToMenu()` function is called and the burger is passed in as an argument to the `addBurgerImageToMenu()` function.
    - `If` the selected option from the `<select>` element’s dropdown menu is `healthy`:
      - Iterate over the array stored in the `burgers` variable using an array iterator method such as `forEach()`. For each of the burgers in the array stored in the `burgers` variable, the `addHealthyBurgerToMenu()` function is called and the burger is passed in as an argument to the `addHealthyBurgerToMenu()` function.
4. `addHealthyBurgerToMenu(burger)`: The `addHealthyBurgerToMenu()` function has been declared for you, but you will need to write the code that should go inside of this function. It has 1 parameter named `burger` whose value should be an `object` that contains the following keys: `name`, `image`, `description`, and `healthy`, when the correct value is passed as an argument into the function. When the `addHealthyBurgerToMenu()` function is called, the following actions should take place:
    - `If` the value of the `healthy` key of the `object` referenced by the `burger` parameter is `true`, the `addBurgerImageToMenu()` function is called and the `burger` parameter is passed in as an argument to the `addBurgerImageToMenu()` function.

## Submission and Grading Criteria

When you're done with this lab, remember to commit and push your changes up to GitHub, then
submit your work to Canvas using CodeGrade.
