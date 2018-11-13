---
layout: post
section: try
topic: properties
status: reviewing
---

You can use your element's properties in its template. LitElement automatically updates your element when its properties change.

* [Starting code](#start)
* [Editing steps](#edit)
* [Completed code](#completed)

<a name="start">

### Starting code

_my-element.js_

```js
{% include projects/try/properties/before/my-element.js %}
```

{% include project.html folder="try/properties/before" openFile="my-element.js" %}

<a name="edit">

### Editing steps

To create properties and use them in an element template: 

*   Declare your properties. 

    _my-element.js_

    ```js
    static get properties(){
      return {
        // Declare property here.
      };
    }
    ```

    _Add this code to declare a property:_

    ```js
    message: { type: String }
    ```

*   Initialize property values in the element constructor.

    _my-element.js_

    ```js
    constructor(){
      super();
      // Initialize property here.
    }
    ```

    _Add this code to initialize the property:_

    ```js
    this.message='Hello world! From my-element';
    ```

*   Add properties to your template with JavaScript expressions.

    _my-element.js_

    ```js
    render(){
      return html`
        <!-- Add property here. -->
        <p></p>
      `;
    }
    ``` 

    _Add this code to use the property:_

    ```js
    <p>${this.message}</p>
    ```

<a name="completed">

### Completed code

_my-element.js_

```js
{% include projects/try/properties/after/my-element.js %}
```

{% include project.html folder="try/properties/after" openFile="my-element.js" %}


{% include prevnext.html prevurl="use" prevtitle="Use your element in a web page" nexturl="expressions" nexttitle="Loops and conditionals" %}
