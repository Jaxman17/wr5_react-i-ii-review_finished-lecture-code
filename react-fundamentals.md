### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
    - A library
    - Uses javascript/JSX
    - JSX ultimately compiles into JS
    - Create apps 
    - Created by Facebook
    - Component based
    - Front-end development
    - Unidirectional data flow

2.  What is create-react-app?
    - Is a command
    - Sets up boilerplate of react
    - It sets up our development environment in which we can run our app (npm start), which includes auto-refresh (hot reloading)

3.  What is Component Based Architecture?
    - Encapsulates certain functionalities or individual pieces of code
    - Highly reusable 
    - Makes our code much easier to debug

4.  What is JSX?
    - JavaScript XML
    - Makes it easier to write HTML in react while also include JS functionality
    - It's the syntax React uses to describe a UI.
    - Looks like HTML, but eventually transpiles into regular JS

5.  What is the virtual DOM?
    - A representation of the actual DOM
    - A lightweight copy, more efficient version of the browser's DOM
    - React uses this virtual DOM to decide what parts of the actual DOM to change

6.  What is unidirectional (one-way) data flow?
    - Data has one way to be passed to other components
    - The way to get around this is to pass data up through events
    - Parent to child
    - We use props for this

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
    - create-react-app creates a new folder called my-app that contains all the boilerplate code for a new React application. 
    - It creates a git repository and also creates a package.json file so that other libraries can be incorporated into the project.

8.  Explain what this code does:
    - This creates a functional, stateless Mentor component that display's a person's information. 
    - It is expecting a title prop to be passed in. If that prop has a value of "Lead Mentor" then React applies a class of lead. Otherwise, there is no class.

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.
    - By using props

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?
    - Benefits
      - We can throw together a React app quickly
      - We don't install the individual pieces separately required in a React app
      - Most of the setup (think config files, etc) is already done for us
    - Drawbacks
      - It could potentially install something that we don't need leading to a bigger app size
        - Though, this is not really a concern

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue
    - Feel free to research in your own time :)

14. Compare and contrast one-way data flow with two-way data binding.
    - One-way = unidirectional
    - Two-way = bidirectional
