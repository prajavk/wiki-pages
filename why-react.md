# Why React?
```
-------------------------------------------------------
Choose          |    REACT        |   ANGULAR
-------------------------------------------------------
Components      | in-built        |   in-built
Testing         | Jest, Mocha     |   in-built
HTTP library    | Fetch, Axios    |   in-built
Routing         | React Router    |   in-built
I18n            | react-inlt      |   in-built
Animation       | react-motion    |   in-built
Form Validation | react-forms     |   in-built
CLI             | create-react-app|   in-built
------------------------------------------------------
```

## Basic npm packages
1. react
2. react-dom
3. react-redux router
4. react-thunk
5. react-axios
6. redux
7. react-bootstrap

## Must Know Topics
ES6, Promise, Axios, React basics, Redux

## ESlint cmds
https://eslint.org/docs/user-guide/command-line-interface

## How to use npm scripts better than gulp, grunt?
https://medium.freecodecamp.org/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8

## Search for npm packages
https://libraries.io/

Example of npm scripts- The scripts below will run in order based on their prefix.
```
{
"name": "npm-scripts-example",
"version": "1.0.0",
"description": "npm scripts example",
"scripts": {
"prebuild": "echo I run before the build script",
"build": "cross-env NODE_ENV=production webpack",
"postbuild": "echo I run after the build script"
	}
}
```
```
{
  "name": "npm-scripts-example",
  "version": "1.0.0",
  "description": "npm scripts example",
  "scripts": {
    "clean": "rimraf ./dist && mkdir dist",
    "prebuild": "npm run clean",
    "build": "cross-env NODE_ENV=production webpack"
  }
}

// you can always call a separate file
  "scripts": {
    "build": "node build.js"
  }

```

## Key notes about REACT

1. Capitalization:
The component name must be capitalized, both in JSX as well as when you define them
If you get the capitalization wrong, React will not render your content properly. The component will not be found. Trying to identify capitalization issues is probably the last thing you’ll think about when things aren’t working, so keep this little tip in mind.

2. JSX: JSX is not HTML. It looks like HTML and behaves like it in many common scenarios, but it is ultimately designed to be translated into JavaScript. 
- Can't use Javascript reserved keywords as properties in JSX
  That can be difficult when certain really popular keywords like class are commonly used in HTML despite also being in JavaScript’s reserved keywords list.
- Attributes are camelcase
- No inline CSS
- Expect single DOM
 
3. Synthetic Event
Your event handlers don’t get native event arguments of type MouseEvent, KeyboardEvent, etc. They always get event arguments of type SyntheticEvent that wrap your browser’s native event instead. Don’t refer to traditional DOM event documentation when using Synthetic events and their properties.
Because the SyntheticEvent wraps your native DOM event, events and their properties may not map one-to-one. Some DOM events don’t even exist in React.
- synthetic events can't listen directly in components.

4. Improved Performance in React
In complex UIs, the more event handlers you have, the more memory your app takes up. Manually dealing with that isn’t difficult, but it is a bit tedious as you try to group events under a common parent. Sometimes, that just isn’t possible. Sometimes, the hassle doesn’t outweigh the benefits. What React does is pretty clever. React never attaches event handlers to the DOM elements directly. It uses one event handler at the root of your document that is responsible for listening to all events and calling the appropriate event handler as necessary 

Handling events with React elements is very similar to handling events on DOM elements

```
//HTML
<button onclick="greet()">  
  Say Hello!
</button>

//JSX 
<button onClick={greet}>  
  Say Hello!
</button>
```
Camelcase the event listener. i.e. onClick, onSubmit, onChange etc

For Class Based Components
Call the function with the keyword this. 
``` ex: <button onClick={this.handleClick}>```

For Function Based Components
Call the function with just the function name. 
``` ex: <button onClick={handleClick}>```

Passing arguments as,
``` 
<button onClick={this.handleClick.bind(this, id)}>Click Me
</button>
```
## Lifecycle methods
These methods can be overridden for each component, to run code during a specific lifecycle phase.
1. https://blog.codecentric.de/en/2017/11/developing-modern-offline-apps-reactjs-redux-electron-part-2-reactjs-basics/

```
Mounting:
constructor()
componentWillMount()
render()
componentDidMount()
Updating:
componentWillReceiveProps()
shouldComponentUpdate()
componentWillUpdate()
render()
componentDidUpdate()
Unmounting:
componentWillUnmount()
Error handling (since React 16 – released September 2017):
componentDidCatch()

Stateless Functional components:
const counter = ({ counter }) => (
   <div>
        <h3>Count: {counter}</h3>
   </div>
);
```

## Functional (stateless) vs class-based (stateful) Components
Functional (stateless)
- receive props as argu
- No internal state
- No life cycle methods
- use as often as possible.

```
import React from 'react'
const MyComponent = props => {
  return <p>I'm a functional component!</p>
}
```

class-based alternative:(use mininum)
-Access props via this.props
-Manage internal state this.state
-Uses Life cycle methods
-use only as containers (which pass state to its stateless cmps) 
-Use use this when cmp need to manage state
```
import React, { Component } from 'react'
class MyComponent extends Component {
  render() {
    return <p>I'm a class-based component!</p>
  }
}
```

## HOC
1. HOC should always be a pure function. That means that the same enhanced component should always be returned with the same base component passed as a parameter.
2. Don’t use HOCs inside the render method. This makes React's reconciliation algorithm think that a new component is redeclared within each render, causing the whole subtree to be unmounted rather than just checked for differences.
3. Static methods do not get copied implicitly. This needs to be done explicitl. A good way to do it is with hoist-non-react-statics package.
4. Refs don’t get passed through.

## Contents
- What is React?
- what is JSX? ES6?
- Complex components - start break down complex page into pieces
- Data-driven components - setup components to be driven by data to them access to external data.
- State - How Stateful components work in React
- Lifecycle Hooks to use in React
- Packaging and PropTypes
- Styles - Different methods we use to style cmps from traditional css to inline styling.
- Interactivity - Build dynamic components to engage with application
- Pure Components - React offers different methods to create components. How to create cmps, functoins stateless pure component.
- Repeating Elements - How to display multiple cmps by pulling in external data into our app.
- Intro APIs - How to make external request to fecth data. make call to an external API.
- Promises - Understand Promises from a high level, build our applications using this concept.
- Displaying Remote Data - start requesting remote data and get it integrated into our app.
- Client-side Routing - If application has multiple views in our single-page app. how to create multile views using React Router.

- Redux - Data Management becomes easy with Redux Integration across app.
- Redux actions - How we actually modify the Redux state from within our apps.
- Redux Middleware - Redux method of managing complex state changes in our code using Redux middleware.

## Testing
- Implementing different types of tests that we write in React.
- Install the dependencies required to setup tests.
- Components testing with React- Testing tools like JEST
- Open source library maintained by Airbnb called "Enzyme" that makes testing fun and easy
- Integration Testing - how to write tests to simulate how user interact with our app.and will test the entire flow of our app in a live browser.

## Deployment
- Different pieces involved in deploying our React app 
- Integration Solutions available in marketplace to run tests when app in the cloud.


## Key Features of React Component
Props
- Props are the "arguments" to your components

Event Handlers
- onClick specifies a function that we can call when an element is clicked

Nested Components
- Components can be used by other components. A React app is a tree of nested components

Dynamic Attributes
- By mixing code and markup, we're able to easily change the view based on state

- State in a component is intended to be completely internal to the Component and it's children
