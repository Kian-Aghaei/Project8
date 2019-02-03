### Table of Contents
-  [Introduction](#Introduction)
-  [Specification](#Specification)
-  [Bug Fixing](#Bug-fixing)
-  [Best Practice and Performance Improvement](#Best-Practice-and-Performance-Improvement)
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
>This application is written by the use of three major tools/languages of front-end development. HTML/CSS/JavaScript. Besides recently added “uuid” library, this app is developed with pure JavaScript (Vanilla JS) with the help of no forms of external libraries or frameworks.

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

## Bug Fixing
>During the program’s manual test three bugs have been found. One of them was a simple typo, the other was the potential possibility of assigning an identical ID to two different entities on DB, and the last was a missing id of an input tag.
 - In *controller.js*:
 
    <code>Controller.prototype.adddItem</code>
    
    replaced with:
    
    <code>Controller.prototype.addItem</code>
    
 - In *store.js*:
 
    Faulty ID generation process:
    
    ```javascript
    var newId = "";
    var charset = "0123456789";
    for (var i = 0; i < 6; i++) {
        newId += charset.charAt(Math.floor(Math.random() * charset.length));
    }
          
    updateData.id = parseInt(newId);
    ```
    replaced with the use of “uuid” module in order to generate unique ID for each entry in DB:
    ```javascript
    // Generate a new ID
    updateData.id = uuid();
    ```
    In order to make the use of new type of ID through the program correctly, there were some necessary changes in both *[view.js](https://github.com/Kian-Aghaei/Project8/commit/ae3e9548ca885081447daa9b0ee682ab01f17dca)*
    and *[model.js](https://github.com/Kian-Aghaei/Project8/commit/7dbbe1277f356ea2749ccf13087fdecdd852ca3f)* files.
    
 - In *index.html*:
 
    There was a missing id for an "input" tag so this line of code:
    ```html
    <input class="toggle-all" type="checkbox">
    ```
    replaced with:
  
   ```html
    <input class="toggle-all" id="toggle-all" type="checkbox">
   ```
## Best Practice and Performance Improvement
>There were some parts of code which have been modified to improve its performance.
- In *store.js*:

    In order to remove redundant piece of code and unnecessary loop this method:
     ```javascript
     Store.prototype.remove = function (id, callback) {
        var data = JSON.parse(localStorage[this._dbName]);
        var todos = data.todos;
        var todoId;
        
        for (var i = 0; i < todos.length; i++) {
           if (todos[i].id == id) {
              todoId = todos[i].id;
           }
        }
     
        for (var i = 0; i < todos.length; i++) {
           if (todos[i].id == todoId) {
              todos.splice(i, 1);
           }
        }
     
        localStorage[this._dbName] = JSON.stringify(data);
        callback.call(this, todos);
     };
    ```
    replaced with:
    ```javascript
    Store.prototype.remove = function (id, callback) {
       var data = JSON.parse(localStorage.getItem(this._dbName));
       var todos = data.todos;
    
       for (var i = 0; i < todos.length; i++) {
          if (todos[i].id === id) {
             todos.splice(i, 1);
             break;
          }
       }
    
       localStorage.setItem(this._dbName, JSON.stringify(data));
       callback.call(this, todos);
    };
    ```
    And also all the bracket notation use of “localStorage” object replaced with proper default method of it (<code>setItem()</code> or <code>getItem()</code>).
    
    For example:
    ```javascript
    var data = JSON.parse(localStorage[this._dbName]);
    ```
    replaced with
    ```javascript
    var data = JSON.parse(localStorage.getItem(this._dbName));
    ```
    In controllerSpec.js, in one of the specs (“should add a new todo to the view”) there were two unnecessary reset call on two of spies which have been removed:
    ```javascript
    view.render.calls.reset();
    model.read.calls.reset();
    ```
## Testing
>For testing the different functionalities of the app we have used a testing framework, Jasmine. Some tests should have been added to the already written ones based on previously stablished premise. Here is the list of Specs which new tests were written to meet the expectations.
1.	should show entries on start-up
2.	should show active entries
3.	should show completed entries
4.	should highlight "All" filter by default
5.	should highlight "Active" filter when switching to active view
6.	should toggle all todos to completed
7.	should update the view
8.	should add a new todo to the model
9.	should remove an entry from the model

## Audit

