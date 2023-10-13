# Nuxt.js - The Intuitive Web Framework

## Overview

Nuxt.js is an open source JavaScript framework built on top of Vue.js, a JavaScript library. It is a powerful, high-level front-end framwork that simplifies the development of single-page Vue.js applications.<br>"Nuxt.js is the most intuitive Vue framework available today. It combines the power of Vue.js with server-side rendering features to make it more powerful." [[1]](#ref1)

### Purpose
Nuxt.js provides clean and useful solutions for many challanges that modern day web developers face:

1. **Universal/Server-Side Rendering:** In modern day, many web applications render content client-side, which is great for complex and dynamic applications, but can negatively impact SEO and performance. "Nuxt provides server-side rendering (SSR) out-of-the-box, delivering a rendered page to the client, improving SEO, and ensuring content is visible even if JavaScript fails or is disabled." [[2]](#ref2)

2. **Automatic File-Based Routing:** In web development, a very prevalent task is managing routes within your application. Essentially routing your application to various endpoints that allow you to navigate from page to page. Nuxt automates this by generating the Vue router configuration based on Vue files in the "pages" directory which removes much inital setup and avoids manual errors.

3. **Vuex Store Integration:** Nuxt works together with Vuex, a state management pattern/library for Vue.js. By placing files in the store directory, they are automatically integrated into a centralized store, tremendously aiding state management. [[3]](#ref3)

4. **Enhanced Developer Experience:** Nuxt abstracts common and repetitive tasks involved for the developer. Features like module management, out-of-box structure, and automatic routing allow developers to focus on building features without having to worry about manual setup and configuration.

### Using Nuxt.js
1. **Installation:** To start a new project, you can use the create-nuxt-app:
```
$ npx create-nuxt-app <project-name>
```
There will be a series of questions in setting up the Nuxt project such as choosing UI frameworks, testing utilities, etc. that help to personalize the framework to your needs.

3. **Project Directory:** After the initial setup, navigate to the project directory:
```
$ cd <project-name>
```

5. **Directory Structure:** A Nuxt project includes directories like assets, components, layouts, pages, store, and middleware, each with a specific purpose in the application's structure.

6. **Development:** Nuxt.js is friendly and out of the box functional as you can start your Nuxt app locally instantly by simply running:
```
$ npm run dev
```

8. **Production:** To prepare the application for production, you build it by running:
```
$ npm run build
```
Which will build all assets for production. 
Then you can run your application at production level using: 
```
$ npm run start
```

## Functionality
Nuxt.js provides a plethora of functionality that can not all be covered in one study. However, I will outline some of the features that stuck out to me the most.

### Directory Structure
<img width="383" alt="Screen Shot 2023-10-12 at 1 31 44 AM" src="https://github.com/CS2613-FA23/explorationactivity1-matthew-collett/assets/97645707/c24d077d-f640-4299-b5b6-72ee98700664">


### State Management with Vuex Store
- State: This is the data being passed around in the application. In my app, the state has a count property.

- Mutations: Functions that directly modify the state. In Vuex, the only way to change the state is by committing a mutation as shown below.
```
export const state = () => ({
  count: 0
})

export const mutations = {
  increment(state) {
    state.count++
  },
  decrement(state) {
    state.count--
  }
}
```

### Component: **nuxt-link**
Optimized for Nuxt's capabilities, especially for SSR, it can preload linked pages when they're visible in the viewport, leading to faster navigation experiences.
```
<nuxt-link to="/endpoint">Endpoint Link</nuxt-link>
```

### Directives: 
Special characters that tell the library to do something. They are prefixed with v- or @, below see the directive that corresponds to JavaScript's onClick listener
```
<button @click="increment">Click me!</button>
```

### Nuxt Configuration for Modules, Plugins, and Add-ons
```
export default {
  // Global page headers
  head: { ... },

  // Global CSS
  css: ['~/assets/main.css'],

  // Plugins to run before rendering page
  plugins: [...],

  // Auto import components
  components: true,

  // Modules for dev and build 
  buildModules: ['@nuxtjs/tailwindcss'],

  // Modules
  modules: [...],

  // Build Configuration
  build: { ... }
}
```

## Origin of Nuxt.js
Nuxt.js was created by 2 brothers named Alexandre Chopin and Sébastien Chopin on October 26th, 2016.

"The first commit for Nuxt.js on Github was made on October 26th, 2016." [[4]](#ref4) 

## Why Nuxt.js?
I chose to research and explore Nuxt.js as recently I worked on a website that used very basic and vanilla JavaScript and other web technologies. It was a great experience, however I definitely experienced some of the headache involved with working with JavaScript in a web development environment on a lower level. I knew that there were popular libraries/frameworks available that streamlined and simplified many components of what I was doing, but never had the time to explore them. Nuxt.js stuck out to me because of my interest in learning Vue, and I quickly learned that it provided a an extra layer of simplication and structure to your Vue project, which is a concept I focus on and try my best to adhere to when building software in general. 

## Influence
Having worked with JavaScript and various libraries in the past for web developement, using Nuxt.js proved to add another level of simplicity and overall ease of development. As a very structured and organized individual, seeing the structure and modularity of Nuxt.js upon project creation was breath-taking. Experiencing this framework in action allowed me to visualize and experience a much higher level of Javascript implementation and enabled me to understand what some of the modern libraries and frameworks have to offer in terms of simplistic design and usage. Moving forward, I feel as though I will focus on researching some of the newer and more modern packages available for JavaScript.

## Overall Experience
My overall experience with learing about and exploring Nuxt.js was very positive. I really enjoyed learning about some of the basics of Nuxt and would be ecstatic use it in future projects. I would recommend this framework to an individual that maybe has experience with the usage of JavaScript in web development and has maybe already explored libraries like React or others of the like. For those people, I believe they would instantly see the overall added simplicity that Nuxt provides to the developer. I would continue to use this framework as I feel as though it would tremendously expedite the development process when building a web application, as well as I enjoy the added structure of the project as I eluded to before.

## References
<a id="ref1"></a>[1] [What Is Nuxt.js? Learn More About the Intuitive Vue Framework](https://kinsta.com/knowledgebase/nuxt-js/)
<br>
<a id="ref2"></a>[2] [Server-Side Rendering (SSR)](https://vuejs.org/guide/scaling-up/ssr.html)
<br>
<a id="ref3"></a>[3] [Vuex Store Integration](https://v2.nuxt.com/docs/directory-structure/store/)
<br>
<a id="ref4"></a>[4] [How we use Nuxt at The NuxtJS Company](https://devblogs.microsoft.com/startups/nuxt/)
<br>
[5] [Nuxt.js Fundementals](https://vueschool.io/lessons/what-is-nuxtjs)
<br>
[6] [Nuxt Documentation](https://nuxt.com/docs)
<br>
[7] [OpenAI. "ChatGPT."](https://openai.com/)
