# React Redux Webpack
Getting started with React Redux and Webpack... Coming soon!

[Complete Intro to React](https://btholt.github.io/complete-intro-to-react/all.html)

[Playlist](https://www.youtube.com/playlist?list=PLQDnxXqV213JJFtDaG0aE9vqvp6Wm7nBg)

[Full Stack Redux Tutorail](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)

[Encapsulation in Redux](http://blog.javascripting.com/2016/02/02/encapsulation-in-redux/)

[A Detailed Introduction To Webpack](https://www.smashingmagazine.com/2017/02/a-detailed-introduction-to-webpack/)

[Webpack: Core Concepts](https://opbeat.com/community/posts/webpack-the-core-concepts-by-sean-larkin/)

[Webpack and React](http://survivejs.com/webpack_react/introduction/)

[React Higher Order Components](http://www.darul.io/post/2016-01-05_react-higher-order-components)

[Practical Redux Series](http://blog.isquaredsoftware.com/series/practical-redux/)

[Redux FAQ](http://redux.js.org/docs/FAQ.html)

[Redux without profanity](https://tonyhb.gitbooks.io/redux-without-profanity/content/architecture.html)

[Best Practices for Writing React Components](https://medium.com/code-life/our-best-practices-for-writing-react-components-dec3eb5c3fc8)

[A Visual Guide to State in React](https://daveceddia.com/visual-guide-to-state-in-react/)

### Redux

The whole state of your app is stored in an object tree inside a single store.
The only way to change the state tree is to emit an action, an object describing what happened.
To specify how the actions transform the state tree, you write pure reducers.

#### Principles

Single source of truth: The state of your whole application is stored in an object tree within a single store.

State is read-only: The only way to mutate the state is to emit an action, an object describing what happened.

Changes are made with pure functions: To specify how the state tree is transformed by actions, you write pure reducers.

#### Basics

**Actions** 

Are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using store.dispatch().

**Action Creators**

Action creators are exactly that—functions that create actions. It's easy to conflate the terms “action” and “action creator,” so do your best to use the proper term.

```javascript
function addTodo(text) {
  return {
    type: ADD_TODO,
    text
  }
}
```

**Bound Action Creators**

You can create a bound action creator that automatically dispatches:

```javascript
const boundAddTodo = (text) => dispatch(addTodo(text))
const boundCompleteTodo = (index) => dispatch(completeTodo(index))
```

Now you’ll be able to call them directly:

```javascript
boundAddTodo(text)
boundCompleteTodo(index)
```

**Reducers**

Actions describe the fact that something happened, but don’t specify how the application’s state changes in response. This is the job of a reducer.

Things you should never do inside a reducer:

Mutate its arguments;

Perform side effects like API calls and routing transitions;

Call non-pure functions, e.g. Date.now() or Math.random().

[Build yourself a Redux](https://zapier.com/engineering/how-to-build-redux/)

[Code Redux Guide](http://blog.jakoblind.no/code-redux-guide/)

[Learn Redux Video series](https://learnredux.com/)

[How to dispatch a Redux action with a timeout?](http://stackoverflow.com/questions/34570758/why-do-we-need-middleware-for-async-flow-in-redux)

###  Redux Middleware

Redux middleware basically provides a third-party extension point between dispatching an action, and the moment it reaches the reducer. It is designed by creating functions that can be composed together before the main dispatch method is invoked. The dispatch function is responsible for sending actions to one or many reducer functions for state changes. The composed specialized functions around the original dispatch method creates the new middleware capable dispatch method.

[Understanding Redux Middleware](https://medium.com/@meagle/understanding-87566abcfb7a#.yrivjv7ma)

[Exploring Redux Middleware](http://blog.krawaller.se/posts/exploring-redux-middleware/)

[Why do we need middleware for async flow in Redux?](http://stackoverflow.com/questions/34570758/why-do-we-need-middleware-for-async-flow-in-redux)

[Redux Thunk](http://nojaf.com/2015/12/06/redux-thunk/)

[Redux Middleware](http://jonnyreeves.co.uk/2016/redux-middleware/)

[Redux Middleware - Behind the scenes](http://briantroncone.com/?p=529)

[Redux Middlware - Mayakumar](https://vmayakumar.wordpress.com/2016/12/27/redux-middleware/)

### React-Redux links

[`react-redux` source code walk through](https://www.youtube.com/watch?v=VJ38wSFbM3A)

### React Router

[React Router - Declarative Routing for React](https://react-router.now.sh/)

[Leveling up with React Router](https://css-tricks.com/learning-react-router/)

### Redux Form

[Abstracting Form State with Redux Form](https://www.youtube.com/watch?v=eDTi7lYR1VU)

[Adding A Robust Form Validation To React Redux Apps](https://medium.com/@rajaraodv/adding-a-robust-form-validation-to-react-redux-apps-616ca240c124#.6cfwgnhs6)

### Redux Thunk

[What the heck is a thunk](https://daveceddia.com/what-is-a-thunk/)

### Redux Sagas

[Master complex Redux workflows with sagas](http://konkle.us/master-complex-redux-workflows-with-sagas/)

### Testing

[Getting Started with TDD in React](https://semaphoreci.com/community/tutorials/getting-started-with-tdd-in-react)

[UI Testing in React](https://voice.kadira.io/ui-testing-in-react-74fd90a5d58b#.qdkc78scl)

[Test Driven React Tutorial](http://spencerdixon.com/blog/test-driven-react-tutorial.html)

[Testing in React: Getting Off The Ground](https://medium.com/javascript-inside/testing-in-react-getting-off-the-ground-5f569f3088a#.u7mn8bihu)

[Testing React Components Using Shallow Rendering](http://www.randomjavascript.com/2016/01/testing-react-components-using-testing.html)

[Testing Redux Applications](http://randycoulman.com/blog/2016/03/15/testing-redux-applications/)

### Concepts

[Thoughts on Thunks](https://blog.getify.com/thoughts-on-thunks/)

### Server Rendering

[Should I use Server Side Rendering?](http://andrewhfarmer.com/server-side-render/)

### Redux Discussions

#### Connecting Redux to React

[How should I use redux with nested subcomponents that won't be reused?](http://stackoverflow.com/questions/34425741/how-should-i-use-redux-with-nested-subcomponents-that-wont-be-reused)

[How to handle global state data into deeply nested components in Redux?](http://stackoverflow.com/questions/34299460/how-to-handle-global-state-data-into-deeply-nested-components-in-redux)

[Redux + React with only stateless functions](https://github.com/reactjs/redux/issues/1176#issuecomment-167015145)

### Redux Ecosystem Libraries

[Reselect](https://github.com/reactjs/reselect)

Simple “selector” library for Redux

* Selectors can compute derived data, allowing Redux to store the minimal possible state.

* Selectors are efficient. A selector is not recomputed unless one of its arguments change.

* Selectors are composable. They can be used as input to other selectors.

[Redux Actions](https://github.com/acdlite/redux-actions)

Flux Standard Action utilities for Redux.

[Reduce Reducers](https://github.com/acdlite/reduce-reducers)

Reduce multiple reducers into one from left to right.

### Code Splitting

[Code Splitting for React Router with Webpack and HMR](https://hackernoon.com/code-splitting-for-react-router-with-webpack-and-hmr-bb509968e86f)

[Webpack: Code Splitting](https://survivejs.com/webpack/building/code-splitting/)

[Webpack v1: Code splitting](https://webpack.github.io/docs/code-splitting.html)

[Webpack v2: Code splitting](https://webpack.js.org/guides/code-splitting-async/)

[Webpack: Bundle Splitting](https://survivejs.com/webpack/building/bundle-splitting/)

[Vendor and code splitting in webpack 2](https://medium.com/@adamrackis/vendor-and-code-splitting-in-webpack-2-6376358f1923)

[Code Splitting for React Router with ES6 Imports](http://moduscreate.com/code-splitting-for-react-router-with-es6-imports/)

[Webpack: Code Splitting by Routes](https://medium.com/@puppybits/webpack-code-splitting-by-routes-92f96cf733f2)

[Code Cracked for Code-Splitting + SSR in Reactlandia: React Loadable + Webpack Flush Chunks and more](https://hackernoon.com/code-cracked-for-code-splitting-ssr-in-reactlandia-react-loadable-webpack-flush-chunks-and-1a6b0112a8b8)

