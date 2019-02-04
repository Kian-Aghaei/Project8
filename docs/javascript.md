<div class="flex">

<div id="split-left" class="overflow-auto fs0 height-viewport-100">

<div class="py1 px2"><input placeholder="Filter" id="filter-input" class="col12 block input" type="text">

<div id="toc">

*   [Todo](#todo)
*   [Controller <span class="icon">▸</span>](#controller)

    <div class="toggle-target display-none">

    *   <span>Instance members</span>
    *   [#setView](#controllersetview)
    *   [#showAll](#controllershowall)
    *   [#showActive](#controllershowactive)
    *   [#showCompleted](#controllershowcompleted)
    *   [#addItem](#controlleradditem)
    *   [#removeItem](#controllerremoveitem)
    *   [#removeCompletedItems](#controllerremovecompleteditems)
    *   [#toggleComplete](#controllertogglecomplete)
    *   [#toggleAll](#controllertoggleall)
    *   [#_updateCount](#controller_updatecount)
    *   [#_filter](#controller_filter)
    *   [#_updateFilterState](#controller_updatefilterstate)

    </div>

*   [Model <span class="icon">▸</span>](#model)

    <div class="toggle-target display-none">

    *   <span>Instance members</span>
    *   [#create](#modelcreate)
    *   [#read](#modelread)
    *   [#update](#modelupdate)
    *   [#remove](#modelremove)
    *   [#removeAll](#modelremoveall)
    *   [#getCount](#modelgetcount)

    </div>

*   [Store <span class="icon">▸</span>](#store)

    <div class="toggle-target display-none">

    *   <span>Instance members</span>
    *   [#find](#storefind)
    *   [#findAll](#storefindall)
    *   [#save](#storesave)
    *   [#remove](#storeremove)
    *   [#drop](#storedrop)

    </div>

*   [Template <span class="icon">▸</span>](#template)

    <div class="toggle-target display-none">

    *   <span>Instance members</span>
    *   [#show](#templateshow)
    *   [#itemCounter](#templateitemcounter)
    *   [#clearCompletedButton](#templateclearcompletedbutton)

    </div>

*   [View](#view)

</div>

<div class="mt1 h6 quiet">[Need help reading this?](https://documentation.js.org/reading-documentation.html)</div>

</div>

</div>

<div id="split-right" class="relative overflow-auto height-viewport-100">

<section class="p2 mb2 clearfix bg-white minishadow">

<div class="clearfix">

### Todo

</div>

Sets up a brand new Todo list.

<div class="pre p1 fill-light mt0">new Todo(name: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">name</span> `([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))` The name of your new to do list.</div>

</div>

</div>

</section>

<section class="p2 mb2 clearfix bg-white minishadow">

<div class="clearfix">

### Controller

</div>

Takes a model and view and acts as the controller between them

<div class="pre p1 fill-light mt0">new Controller(model: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object), view: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">model</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The model instance</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">view</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The view instance</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Instance Members</div>

<div class="clearfix">

<div class="border-bottom" id="controllersetview">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">setView(locationHash, null)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Loads and initialises the view

<div class="pre p1 fill-light mt0">setView(locationHash: any, null: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">locationHash</span> `(any)`</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">null</span> `([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))` '' | 'active' | 'completed'</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllershowall">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">showAll()</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

An event to fire on load. Will get all items and display them in the todo-list

<div class="pre p1 fill-light mt0">showAll()</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllershowactive">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">showActive()</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Renders all active tasks

<div class="pre p1 fill-light mt0">showActive()</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllershowcompleted">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">showCompleted()</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Renders all completed tasks

<div class="pre p1 fill-light mt0">showCompleted()</div>

</section>

</div>

</div>

<div class="border-bottom" id="controlleradditem">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">addItem(title)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

An event to fire whenever you want to add an item. Simply pass in the event object and it'll handle the DOM insertion and saving of the new item.

<div class="pre p1 fill-light mt0">addItem(title: any)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">title</span> `(any)`</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllerremoveitem">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">removeItem(id)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

By giving it an ID it'll find the DOM element matching that ID, remove it from the DOM and also remove it from storage.

<div class="pre p1 fill-light mt0">removeItem(id: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">id</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` The ID of the item to remove from the DOM and storage</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllerremovecompleteditems">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">removeCompletedItems()</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Will remove all completed items from the DOM and storage.

<div class="pre p1 fill-light mt0">removeCompletedItems()</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllertogglecomplete">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">toggleComplete(id, completed, silent, checkbox)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Give it an ID of a model and a checkbox and it will update the item in storage based on the checkbox's state.

<div class="pre p1 fill-light mt0">toggleComplete(id: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), completed: any, silent: ([boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean) | [undefined](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined)), checkbox: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">id</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` The ID of the element to complete or uncomplete</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">completed</span> `(any)`</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">silent</span> `(([boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean) | [undefined](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined)))` Prevent re-filtering the todo items</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">checkbox</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The checkbox to check the state of complete or not</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="controllertoggleall">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">toggleAll(completed)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Will toggle ALL checkboxes' on/off state and completeness of models. Just pass in the event object.

<div class="pre p1 fill-light mt0">toggleAll(completed: any)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">completed</span> `(any)`</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="controller_updatecount">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">_updateCount()</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Updates the pieces of the page which change depending on the remaining number of todos.

<div class="pre p1 fill-light mt0">_updateCount()</div>

</section>

</div>

</div>

<div class="border-bottom" id="controller_filter">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">_filter(force)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Re-filters the todo items, based on the active route.

<div class="pre p1 fill-light mt0">_filter(force: ([boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean) | [undefined](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined)))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">force</span> `(([boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean) | [undefined](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined)))` forces a re-painting of todo items.</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="controller_updatefilterstate">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">_updateFilterState(currentPage)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Simply updates the filter nav's selected states

<div class="pre p1 fill-light mt0">_updateFilterState(currentPage: any)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">currentPage</span> `(any)`</div>

</div>

</div>

</section>

</div>

</div>

</div>

</section>

<section class="p2 mb2 clearfix bg-white minishadow">

<div class="clearfix">

### Model

</div>

Creates a new Model instance and hooks up the storage.

<div class="pre p1 fill-light mt0">new Model(storage: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">storage</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` A reference to the client side storage class</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Instance Members</div>

<div class="clearfix">

<div class="border-bottom" id="modelcreate">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">create(title?, callback?)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Creates a new todo model

<div class="pre p1 fill-light mt0">create(title: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?, callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">title</span> `([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?)` The title of the task</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?)` The callback to fire after the model is created</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="modelread">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">read(query?, callback?)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Finds and returns a model in storage. If no query is given it'll simply return everything. If you pass in a string or number it'll look that up as the ID of the model to find. Lastly, you can pass it an object to match against.

<div class="pre p1 fill-light mt0">read(query: ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) | [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) | [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))?, callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">query</span> `(([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) | [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) | [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))?)` A query to match models against</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?)` The callback to fire after the model is found</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Example</div>

<pre class="p1 overflow-auto round fill-light">model.read(<span class="hljs-number">1</span>, func); <span class="hljs-comment">// Will find the model with an ID of 1</span>
model.read(<span class="hljs-string">'1'</span>); <span class="hljs-comment">// Same as above</span>
<span class="hljs-comment">//Below will find a model with foo equalling bar and hello equalling world.</span>
model.read({ <span class="hljs-attr">foo</span>: <span class="hljs-string">'bar'</span>, <span class="hljs-attr">hello</span>: <span class="hljs-string">'world'</span> });</pre>

</section>

</div>

</div>

<div class="border-bottom" id="modelupdate">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">update(id, data, callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Updates a model by giving it an ID, data to update, and a callback to fire when the update is complete.

<div class="pre p1 fill-light mt0">update(id: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), data: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object), callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">id</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` The id of the model to update</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">data</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The properties to update and their new value</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire when the update is complete.</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="modelremove">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">remove(id, callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Removes a model from storage

<div class="pre p1 fill-light mt0">remove(id: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">id</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` The ID of the model to remove</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire when the removal is complete.</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="modelremoveall">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">removeAll(callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

WARNING: Will remove ALL data from storage.

<div class="pre p1 fill-light mt0">removeAll(callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire when the storage is wiped.</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="modelgetcount">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">getCount(callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Returns a count of all todos

<div class="pre p1 fill-light mt0">getCount(callback: any)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">callback</span> `(any)`</div>

</div>

</div>

</section>

</div>

</div>

</div>

</section>

<section class="p2 mb2 clearfix bg-white minishadow">

<div class="clearfix">

### Store

</div>

Creates a new client side storage object and will create an empty collection if no collection already exists.

<div class="pre p1 fill-light mt0">new Store(name: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String), callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">name</span> `([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))` The name of our DB we want to use</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` Our fake DB uses callbacks because in real life you probably would be making AJAX calls</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Instance Members</div>

<div class="clearfix">

<div class="border-bottom" id="storefind">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">find(query, callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Finds items based on a query given as a JS object

<div class="pre p1 fill-light mt0">find(query: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object), callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">query</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The query to match against (i.e. {foo: 'bar'})</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire when the query has completed running</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Example</div>

<pre class="p1 overflow-auto round fill-light">db.find({<span class="hljs-attr">foo</span>: <span class="hljs-string">'bar'</span>, <span class="hljs-attr">hello</span>: <span class="hljs-string">'world'</span>}, <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">data</span>)</span> {
 <span class="hljs-comment">// data will return any items that have foo: bar and</span>
 <span class="hljs-comment">// hello: world in their properties</span>
});</pre>

</section>

</div>

</div>

<div class="border-bottom" id="storefindall">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">findAll(callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Will retrieve all data from the collection

<div class="pre p1 fill-light mt0">findAll(callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire upon retrieving data</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="storesave">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">save(updateData, callback, id)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Will save the given data to the DB. If no item exists it will create a new item, otherwise it'll simply update an existing item's properties

<div class="pre p1 fill-light mt0">save(updateData: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object), callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function), id: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">updateData</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The data to save back into the DB</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire after saving</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">id</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` An optional param to enter an ID of an item to update</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="storeremove">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">remove(id, callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Will remove an item from the Store based on its ID

<div class="pre p1 fill-light mt0">remove(id: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">id</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` The ID of the item you want to remove</div>

</div>

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire after saving</div>

</div>

</div>

</section>

</div>

</div>

<div class="border-bottom" id="storedrop">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">drop(callback)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Will drop all storage and start fresh

<div class="pre p1 fill-light mt0">drop(callback: [function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">callback</span> `([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function))` The callback to fire after dropping the data</div>

</div>

</div>

</section>

</div>

</div>

</div>

</section>

<section class="p2 mb2 clearfix bg-white minishadow">

<div class="clearfix">

### Template

</div>

Sets up defaults for all the Template methods such as a default template

<div class="pre p1 fill-light mt0">new Template()</div>

<div class="py1 quiet mt1 prose-big">Instance Members</div>

<div class="clearfix">

<div class="border-bottom" id="templateshow">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">show(data)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Creates an

*   HTML string and returns it for placement in your app.

    NOTE: In real life you should be using a templating engine such as Mustache or Handlebars, however, this is a vanilla JS example.

    <div class="pre p1 fill-light mt0">show(data: [object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)): [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)</div>

    <div class="py1 quiet mt1 prose-big">Parameters</div>

    <div class="prose">

    <div class="space-bottom0">

    <div><span class="code bold">data</span> `([object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object))` The object containing keys you want to find in the template to replace.</div>

    </div>

    </div>

    <div class="py1 quiet mt1 prose-big">Returns</div>

    `[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)`: HTML String of an*   element

    <div class="py1 quiet mt1 prose-big">Example</div>

    <pre class="p1 overflow-auto round fill-light">view.show({
    <span class="hljs-attr">id</span>: <span class="hljs-number">1</span>,
    <span class="hljs-attr">title</span>: <span class="hljs-string">"Hello World"</span>,
    <span class="hljs-attr">completed</span>: <span class="hljs-number">0</span>,
    });</pre>

    </section>

</div>

</div>

<div class="border-bottom" id="templateitemcounter">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">itemCounter(activeTodos)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Displays a counter of how many to dos are left to complete

<div class="pre p1 fill-light mt0">itemCounter(activeTodos: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)): [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">activeTodos</span> `([number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number))` The number of active todos.</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Returns</div>

`[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)`: String containing the count</section>

</div>

</div>

<div class="border-bottom" id="templateclearcompletedbutton">

<div class="clearfix small pointer toggle-sibling">

<div class="py1 contain"><a class="icon pin-right py1 dark-link caret-right">▸</a> <span class="code strong strong truncate">clearCompletedButton(completedTodos)</span></div>

</div>

<div class="clearfix display-none toggle-target">

<section class="p2 mb2 clearfix bg-white minishadow">

Updates the text within the "Clear completed" button

<div class="pre p1 fill-light mt0">clearCompletedButton(completedTodos: [type]): [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">completedTodos</span> `([type])` The number of completed todos.</div>

</div>

</div>

<div class="py1 quiet mt1 prose-big">Returns</div>

`[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)`: String containing the count</section>

</div>

</div>

</div>

</section>

<section class="p2 mb2 clearfix bg-white minishadow">

<div class="clearfix">

### View

</div>

View that abstracts away the browser's DOM completely. It has two simple entry points:

*   bind(eventName, handler) Takes a todo application event and registers the handler
*   render(command, parameterObject) Renders the given command with the options

<div class="pre p1 fill-light mt0">new View(template: any)</div>

<div class="py1 quiet mt1 prose-big">Parameters</div>

<div class="prose">

<div class="space-bottom0">

<div><span class="code bold">template</span> `(any)`</div>

</div>

</div>

</section>

</div>

</div>