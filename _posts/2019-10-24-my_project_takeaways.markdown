---
layout: post
title:      "My React Project Takeaways"
date:       2019-10-24 22:34:52 -0400
permalink:  my_project_takeaways
---

While working on my final project, I had to create both Functional as well as Class components. In the following sections, I have attempted to highlight some of the major differences and some thoughts on when they are relevant to use in an application.

**Functional Components vs Class Components**

 Functional components by definition are presentational components- i.e. their function is merely to present/render data that is provided to the function via props. They are simple in terms of code and look like normal functions with parameters and a return. The parameter, if provided, is the prop object and the function returns a React element which is rendered on the page. Functional components do not maintain any state and they do not interface with the Redux Store. Hence, we cannot use the SetState inside a functional component. Functional components also do not have access to any of the React lifecycle methods.

 The lack of access to state behooves the need for a Class component. A class component is basically what it is named- a class. The class can have its own methods and also the React lifecycle methods, of which the ComponentDidMount and render methods are the most frequently used. In fact, the render method is mandatory in a class component. Render method returns the React elements that is displayed on the page. Class components can maintain state and interface with the Redux store. Any application that need to fetch data via an API will require access to the Redux store and state. Class components are also re-rendered whenever there is a change in its state. When using multiple fetches in a component, the promise is fulfilled in an asynchronous mode and hence it is required for the component to re-render every time a fetch promise is fulfilled. Since functional components do not deal with state, this does not apply to them. Like in any object oriented programming, a class component creates instances and is referred to by *this*. So ,within the class, you would refer to its props and state using this.props. and this.state. This leads to an interesting situation in that the props may be implicitly mutated due to the this.props changing on a re-render. This would not happen in the case of a functional component since it does not have the render life cycle method.

 
There are differing views on whether class components perform better than functional components or vice-versa( since functional components have less code) but no firm proof of this has been established.


Here are some rules that I have applied when building my project.
																							
| --------------------------| Functional Components | Class Components|
| Need State                        |                                                   |            X                         |
| Fetch Data                         |                                                   |            X                         |
| Connect to Redux Store|                                                 |             X                         | 
|Only Displaying Data      |                     X                           |                                        |
 

Newer versions of react have provided utilities like Hooks to be able to maintain state within a functional component – but that is a subject by itself which I am trying to understand more details on. 

**Arrow functions(ES6) vs Regular functions**

Arrow functions, also called fat arrow functions, is a ES6 feature that was basically created to amend quirks in earlier versions of Javascript( ES5). With ES5, we could only the regular function and the keyword this  required special handling using the bind function. This was cumbersome and not very elegant. The arrow function in ES6 solved the issue.

This project gave me an opportunity to examine the differences between arrow functions and regular functions. One of my components uses an arrow function to handle a button click. I changed the arrow function into a regular function to see if I’d get the same output. However, I ran into an error. I did some research on arrow functions and regular functions. From what I read and understood, in a regular function, the keyword ’this’, (this.handleClick) points to the window object since the function goes out of scope. I even added a debugger and an ‘alert(this)’ within my handleClick function. When I hit the debugger, I got an alert message on my browser saying ‘[object, Object]’. Indeed, ‘this’ within a standalone function points to the window object. I could still use a standalone function for my handleClick, However, I would need to bind the keyword ‘this’ to the parent object, which in my case, would be the component - a JS class. I added the following code to the constructor of my component to make the standalone function work.

```
constructor(){
     super()
       this.state = {
         renderedData: [],
         sortClicked: false
       }
     this.handleClick = this.handleClick.bind(this);
 }
```

While this works, it’s also extra code and considered less elegant. I understand that this is bad practice. Arrow functions, on the other hand, solve this issue. I wouldn’t need to bind the keyword this to the parent object. Arrow functions take care of this internally. Arrow function is an ES6/ES2015 feature and considered more elegant. I changed the regular function back to an arrow function. This time, I added a console.log(this) within my handleClick arrow function. I saw this on my console. 

`this CompareCard {props: {…}, context: {…}, refs: {…}, updater: {…}, handleClick: ƒ, …}`

The keyword this, points to the parent object which is the CompareCard component. 


Sources Used:

https://tylermcginnis.com/arrow-functions/
https://stackoverflow.com/questions/22939130/when-should-i-use-arrow-functions-in-ecmascript-6/28135120
https://www.freecodecamp.org/news/learn-es6-the-dope-way-part-ii-arrow-functions-and-the-this-keyword-381ac7a32881/
https://alligator.io/react/constructors-with-react-components/
https://stackoverflow.com/questions/52862027/onclick-action-not-triggered-using-regular-function-in-react





