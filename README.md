# Vue.js 

### Introduction
Vue.js is a front end javascript framework for building websites and user interfaces.
- Vue is generally used to create single page applications that run on the client, but can also
be used to create full stack applications by making http requests to a backend server. Vue is 
popular with Nodejs and Express (MEVN Stack).
- Vue can also run on server side using by using SSR (Server Side Rendering) frameworks like Nuxt.

### Why use Vue?
- Create dynamic frontend applications and websites.
- Has a relatively easy learning curve.
- Easy to integrate with other projects.
- Fast and lightweight.
- Virtual DOM (It only updates part of the page, no refreshing) .
- Has a great community.

### Basic Layout of a Vue Component
Components include a template for markup, logic including any state/data/methods as well as the
styling for that component.

```
<template>
    <header>
        <h1>{{title}}</h1>
    </header>
</template>

<script>
    export default {
        props: {
            title: String,
        },
    }
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottm: 20px;
}
</style>
```

### Working with state/data
Components can have their own state which can determine how a specific component behaves and 
what data is displayed.

Some state may be local to a specific component and some may be "global" or "app"
level state that needs to be shared with multiple components.

Vuex is state manager for global state in larger applications (similar to redux in Reactjs)

### Options API vs Composition API
Vue 3 has a new composition API, which aims to address code reusability
and reading in Vue 3, especially in larger applications. Traditionally components use the 
options API.

### VUE CLI
Vue CLI is the standard tooling for Vue.js development.
- It is the command line interface for creating vue apps.
- It has GUI for managing vue apps
- It has a dev server and easy production build tool
- It has integrated testing, Typescript support, ESLint etc

To install Vue.js cli globally:

```
    npm install -g @vue/cli
```

To create a new project

```
    vue create my-project
```

To use vue UI

```
    vue ui
```

### Project setup
```
npm install
```

#### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Project Structure
The index.html file in the public folder is the single page loaded in the browser which has div with id app in it's body. All vue components are rendered in this div tag.

In the src folder, there is a main.js file. This is the entry point to a vue.js app.
We mount App to the div with id #app inside the main.js file.
App.vue is the root component.
Other components used in the app will be declared in the components part in App.vue
