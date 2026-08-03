# Vue 3 Recap

This section highlights the key topics I learned about Vue 3 while working on the commercial web team.

## What is Vue 3
Vue 3 is a third-party framework used to create code components, allowing for more reusable code and adding functionality with less code involved.

## V-Directives
V-Directives are special attributes that help make code reactive and give it additional functionality. Some have shorthands 
I've listed some of the common directives that I was introduced to.

| Directive | Shorthand | Function  | Example
| ----------- | ----------- | ----------- | ----------- |
| v-bind |  : | Binds attributes to a reference variable, automatically updating the attribute when the reference value changes | ```<img :src = 'imgSrc'>```
| v-on | @| Handles user interactions bu attaching event listeners to elements| ```<button @click="openModal"></button>```|
| v-if | *None* | Conditional renders elements by adding/removing them from DOM| ```<p v-if="showText"></p>```|
| v-show | *None* | Similar to v-if but toggles visibility using CSS display attribute instead of removing from DOM| ```<h1 v-show="header"></h1>```|
| v-for | *None* | Acts as a loop to render a list of elements | ```<td v-for="object in objects"></td>```|
| v-model | *None* | Creates two-way data binding on form inputs, meaning data can be changed through ref variable or through user input | ```<select v-model="userSelection"></select>```|

## Consts vs. Functions 

### Constants

- Constants are used to store values, refs, objects, or even functions  
- Constants are consistent and can't be changed (accidentally or not)  

### Functions 

- Functions contain behavior (actions) 
- Functions are hoisted meaning they can be used before it's called  

### When to use  
Use **const** for reactive state, when wanting to change values internal state, but keep reference  

```Vue 3
const openDeleteModal = (project: Project) => {
    selectedProject.value = project
    showDeleteModal.value = true
}
```
Use **function** when performing actions and wanting to access them before function is declared  

```Vue 3
function confirmDelete(id: number) {
    store.deleteProject(id)
    closeDeleteModal()
    showToast.value = true
    toastMessage.value = 'Project successfully deleted!'
}
```
## Computed Properties 

Computed properties create derived reactive state from other reactive state. So you use them for a value that you want to update when a different ref value is changed.

```Vue 3
const firstName = ref('John')
const lastName = ref('Doe')

const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`
}) 
```