### Table of Contents
-  [Introduction](#Introduction)
-  [Specification](#Specification)
-  [Bug Fixing](#Bug-fixing)
-  [Testing](#Testing)
-  [Audit](#Audit)
-  [Competitor's audit result](#Competitor-audit-result)
-  [Performance comparison](#Performance-comparison)
-  [Summery](#Summery)

---

## Introduction
This web app is a simple to-do list application which could store user tasks. It also can add, removes, updates and toggles between states of tasks. Because of the minimalistic design of it, it has a fast and simple interface to work with.

The application is developed according to the "MVC" (Model-View-Controller) pattern. Basically, this method contains three major part. The model which is responsible to structure the data in a reliable form and prepares it based on the controller’s instructions. The view which displays data to the user in an easy-to-understand format, based on the user’s actions and finally the Controller that takes in user commands, sends commands to the model for data updates and sends instructions to view to update interface. Using MVC gives us lots of flexibility to maintain and good opportunity to expand the application in future much faster and easier but on the other hand, it adds up a bit more complexity to the code structure in general.

You can test its functionality here:
*[todo-list-app](https://kian-aghaei.github.io/Project8/)* 
and also visit its repository *[here!](https://github.com/Kian-Aghaei/Project8)*

## Specification
This application is written by the use of three major tools/languages of front-end development. HTML/CSS/JavaScript. Besides recently added “uuid” library, this app is developed with pure JavaScript (Vanilla JS) with the help of no forms of external libraries or frameworks.

#### *HTML*:
 There is only one HTML file in the project (index.html) which is the entry point to the app.
   
#### *CSS*:
There is one active CSS file (index.css) as part of a npm module (todomvc-app-css). Another CSS file also resides in the project (base.css) which is not functional due to the removal of some part of the original HTML file (sidebar). 

#### *JavaScript*:
There are 7 main JavaScript files in the project :
 - **store.js**: Simply create a new client-side storage object (with window.localStorage) in order to store the tasks and their states.
 - **template.js**: Acts as a substitute to templating engines (like Mustache or Handlebars) and delivers functions such as listing items and changing button states.
 - **helper.js**: It delivers functions in order to facilitate interactions between DOM and JS such as selecting elements and attaching handlers to specific elements.
 - **model.js**: Creates a new Model instance based on the MVC concept and hooks up the storage in order to give the access of it to the Controller.
 - **view.js**: It wraps around the DOM and provides users with two major functionalities. First taking a todo application event and registers the handler and second, renders the page based on the given command with the correct data and options.
 - **controller.js**: It takes both model and view instances and acts as the controller between them.
 - **app.js**: It creates a new instance of the app itself by initializing the model, view, and controller.
