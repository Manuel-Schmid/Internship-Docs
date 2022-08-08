# Vue.js
### 1. What is Vue.js? 

Vue.js is a open-source frontend JavaScript framework. It allows building user interfaces and SPAs. It uses a virtual
DOM (like React)

But it is important to keep in mind that "Vue.js itself is not a full-blown framework - it is focused on the view layer only."

### 2. Why do we need a framework like Vue.js?
Vue.js offers functionality to HTML applications and allows to extend HTML with HTML attributes called directives which can be user
defined. (But there are built-in ones as well)


### 02. How is Vue.js different from other frameworks?
Vue builds on top of HTML, CSS & JS, in React everything is inside of JavaScript (JSX). 
Every pure HTML-File is a valid Vue template therefore you can use pure-html files without changing the code at all. 
It is also easier for developers who have been working with HTML to read and write familiar code.
It it **very** easy to integrate into a project. All you have to do is drop a single script tag into the page:


### 03. What is Vue.js CLI?
The Vue.js CLI is a npm package which allows using the vue command in the terminal. There is a GUI-Version with the same capabilities as well, it's called Vue UI.


### 04. Which browsers supports Vue.js?
Vue.js supports all browsers that are ES5-compliant (IE8 and below are not supported).
A list of such browsers can be found here: https://kangax.github.io/compat-table/es5/


### 05. What are Vue objects?
A new Vue object is created with ```new Vue()```. The property ```el:``` binds the new Vue object to the HTML element with 
id="app". When a Vue object is bound to an HTML element, the HTML element will change when the Vue object changes:

```html
<div id="app">
<h1>{{ message }}</h1>
</div>

<script>
var myObject = new Vue({
    el: '#app',
    data: {message: 'Hello Vue!'}
})

function myFunction() {
    myObject.message = "John Doe";
}
</script>
```

### 06. Attribute Bindings
Mustaches cannot be used inside HTML attributes. Instead, use a ```v-bind directive```:
Anything inside the " " when you bind a property using v-bind or : is javascript.
So you can do any single line expressions that you do in JavaScript


```html
<div v-bind:id="dynamicId"></div>
<!--Because v-bind is so commonly used there is a shorter version of this:-->
<div :id="dynamicId"></div>
```

### 07. Two-Way-Bindings
The v-model directive binds the value of HTML elements to application data.

```html
<input v-model="message">
```

### 08. What is Vue Loop Binding ?

```html
<div id="app">
  <ul>
    <li v-for="x in todos">
      {{ x.text }}
    </li>
  </ul>
</div>

<script>
myObject = new Vue({
  el: '#app',
  data: {
    todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue.js' },
      { text: 'Build Something Awesome' }
    ]
  }
})
</script>
```

Result:

    * Learn JavaScript
    * Learn Vue.js
    * Build Something Awesome




### 09. What is AOT Compilation?
ahead-of-time compilation is the act of compiling an higher-level programming language into an lower-level language 
*before* execution of a program, usually at build-time, to reduce the amount of work needed to be performed at run time


### 10. How is AOT different from JIT Compilation?
Just-in-time compilation executes computer code *during* execution of a program rather than before execution.

### 11. What are Vue Components?
Components are reusable Vue instances with custom HTML elements. Components can be reused as many times as you want
or used in another component, making it a child component. Data, computed, watch, and methods can be used in a Vue component.

### 12. What are the Single-File Components of Vue.js?
The SFCs are the recommended way to create Vue components. The file extension for such files is ```*.vue```.  
A Vue SFC contains the component's logic (JS), template (HTML) and styles (CSS) all in a single file.  

Example of a SFC:

```html
<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>

<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
```

### 13. Vue.js Options API
```html
<script>
export default {
  // Properties returned from data() become reactive state
  // and will be exposed on `this`.
  data() {
    return {
      count: 0
    }
  },

  // Methods are functions that mutate state and trigger updates.
  // They can be bound as event listeners in templates.
  methods: {
    increment() {
      this.count++
    }
  },

  // Lifecycle hooks are called at different stages
  // of a component's lifecycle.
  // This function will be called when the component is mounted.
  mounted() {
    console.log(`The initial count is ${this.count}.`)
  }
}
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>
```

### 14. Vue.js Composition API
The Composition API allows to use less boilerplate because e.g. imports and top-level variables / functions declared in ```<script setup>``` are directly usable in the template.
Here is the same component, with the exact same template, but using Composition API and ```<script setup>``` instead

```html
<script setup>
import { ref, onMounted } from 'vue'

// reactive state
const count = ref(0)

// functions that mutate state and trigger updates
function increment() {
  count.value++
}

// lifecycle hooks
onMounted(() => {
  console.log(`The initial count is ${count.value}.`)
})
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>
```

### 15. What are Directives?
Directives are instructions for VueJS to do things in a certain way. Examples of built-in directives are: 
    
    v-if
    v-else
    v-else-if
    v-for
    v-bind
    v-model
    v-on

Custom directives can be implemented as well:
```js
Vue.directive('nameofthedirective', {
    bind(e1, binding, vnode) {
        
    }
})
```
```html
<div v-nameofthedirective>VueJS Directive</div>
```


### 16. Vue.js Conditionals & Loops (Directives)?
```html
<!-- We can render content conditionally or in a loop with the v-if and v-for directives. -->

<script setup>
import { ref } from 'vue'

const show = ref(true)
const list = ref([1, 2, 3])
</script>

<template>
  <button @click="show = !show">Toggle List</button>
  <button @click="list.push(list.length + 1)">Push Number</button>
  <button @click="list.pop()">Pop Number</button>
  <button @click="list.reverse()">Reverse List</button>

  <ul v-if="show && list.length">
    <li v-for="item of list">{{ item }}</li>
  </ul>
  <p v-else-if="list.length">List is not empty, but hidden.</p>
  <p v-else>List is empty.</p>
</template>
```


### 17. What is the DOM (Document Object Model) ?
A programming interface for web documents. It represents the page so that programs can change the document structure, 
style, and content. The DOM represents the document as nodes and objects; that way, programming languages can interact 
with the page.


### 18. What is a singleton?
The singleton pattern is a software design pattern that restricts the instantiation of a class 
to one "single" instance.


### 19. What is tree shaking?
Tree shaking means to eliminate code that isn't in use ("dead-code").


### 20. What is Shadow Dom?
Shadow DOM is a sublevel of the standard Document Object Model (DOM).  this type of DOM doesn’t apply to the entire
web project, only to the project component(s) expressed within it. In addition, shadow DOMs separate the elements
they contain from any default styling and structuring instructions that apply across projects, such as certain CSS statements.


### 21. What is the :host property in CSS for?
The :host property is used to select a custom element from inside its shadow DOM.


