React –
1.	React Concepts
2.	React Hooks.
3.	React Router
4.	React Redux
5.	React Devtool
6.	Formix
7.	React Query
8.	Axios
9.	Material UI
10.	 Storybook
11.	 Apollo Client
12.	 React Testing Library
13.	 TypeScript
14.	 React Virtualized
15.	React Sprint (Animations)
16.	React Native
17.	Nextjs
Join React Community.










React Concepts -
The library for web and native user interfaces.
React is a free and open-source front-end JavaScript library for building user interfaces based on components.
It was developed by Jordan Walke a software engineer at Facebook and released first in 2013, It is maintained by Meta (formerly Facebook).
On March 16, 2023 by Dan Abramov and Rachel Nabors introduced react.dev.
•	The new React site (react.dev) teaches modern React with function components and Hooks.
•	We’ve included diagrams, illustrations, challenges, and over 600 new interactive examples.
•	The previous React documentation site has now moved to legacy.reactjs.org.
The new docs teach React with Hooks from the beginning. The docs are divided in two main sections:
•	Learn React is a self-paced course that teaches React from scratch.
•	API Reference provides the details and usage examples for every React API.
Components – 
React apps are made out of components. A component is a piece of the UI (user interface) that has its own logic and appearance. A component can be as small as a button, or as large as an entire page. React components are JavaScript functions that return markup.
Note - Components can render other components, but you must never nest their definitions, Without parentheses, any code on the lines after return will be ignored!
Note - React component names must always start with a capital letter, while HTML tags must be lowercase. you specify a CSS class with className.
style={{}} is not a special syntax, but a regular {} object inside the style={ } JSX curly braces. You can use the style attribute when your styles depend on JavaScript variables.
Inline style properties are written in camelCase. For example, HTML <ul style="background-color: black"> would be written as <ul style={{ backgroundColor: 'black' }}> in your component.
React projects use JSX for its convenience
JavaScript XML JSX is stricter than HTML. You have to close tags like <br />. Your component also can’t return multiple JSX tags. You have to wrap them into a shared parent, like a <div>...</div> or an empty <>...</> wrapper

Writing Markup with JSX –
JSX is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file. Although there are other ways to write components, most React developers prefer the conciseness of JSX, and most codebases use it.
JSX and React are two separate things. They’re often used together, but you can use them independently of each other.
The Rules of JSX 
1. Return a single root element 
2. Close all the tags 
3. camelCase all most of the things!
This empty tag is called a Fragment. Fragments let you group things without leaving any trace in the browser HTML tree.
JSX is very minimal as a templating language because it lets you organize data and logic using JavaScript.

State and Props –
There are two types of “model” data in React: props and state. The two are very different:
Props are like arguments you pass to a function. They let a parent component pass data to a child component and customize its appearance. Props are immutable(unchangeable).
State is like a component’s memory. It lets a component keep track of some information and change it in response to interactions. State are mutable(changeable)
Props and state are different, but they work together. A parent component will often keep some information in state (so that it can change it), and pass it down to child components as their props.
Which of these are state? Identify the ones that are not:
•	Does it remain unchanged over time? If so, it isn’t state.
•	Is it passed in from a parent via props? If so, it isn’t state.
•	Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!
Installation –
You need to install Node.js for local development – 
Production-grade React frameworks -
•	Next.js is a full-stack React framework.
•	Remix is a full-stack React framework with nested routing.
•	Gatsby is a React framework for fast CMS-backed websites.
•	Expo is a React framework that lets you create universal Android, iOS, and web apps with truly native UIs. 
•	Next.js’s App Router is a redesign of the Next.js APIs aiming to fulfill the React team’s full-stack architecture vision. Next.js’s App Router bundler fully implements the official React Server Components specification. This lets you mix build-time, server-only, and interactive components in a single React tree.
Editor -
•	VS Code.
•	WebStorm
•	Sublime Text
•	Vim
Linting -
Code linters find problems in your code as you write, helping you fix them early. ESLint is a popular, open source linter for JavaScript.
Formatting -
Fortunately, Prettier will clean up your code by reformatting it to conform to preset, configurable rules.
TypeScript -
Every file containing JSX must use the .tsx file extension. This is a TypeScript-specific extension that tells TypeScript that this file contains JSX.

React Developer Tools -
Use React Developer Tools to inspect React components, edit props and state, and identify performance problems.
Import and Exports –
You may encounter files that leave off the .js file extension while importing component
Example - import Gallery from './Gallery';
Either './Gallery.js' or './Gallery' will work with React, though the former is closer to how native ES Modules work.
There are two primary ways to export values with JavaScript: default exports and named exports.
A file can have no more than one default export, but it can have as many named exports as you like.
 
 

When you write a default import, you can put any name you want after import. For example, you could write import Banana from './Button.js' instead and it would still provide you with the same default export. In contrast, with named imports, the name has to match on both sides. That’s why they are called named imports!

People often use default exports if the file exports only one component, and use named exports if it exports multiple components and values. Regardless of which coding style you prefer, always give meaningful names to your component functions and the files that contain them. Components without names, like export default () => {}, are discouraged because they make debugging harder.

For historical reasons, aria-* and data-* attributes are written as in HTML with dashes.
Reference - https://transform.tools/html-to-jsx

Conditional Rendering -
In React, you can conditionally render JSX using JavaScript syntax like if statements, &&, and ? : operators.
Conditionally returning nothing with null

Pitfall - 
Don’t put numbers on the left side of &&.
To test the condition, JavaScript converts the left side to a boolean automatically. However, if the left side is 0, then the whole expression gets that value (0), and React will happily render 0 rather than nothing.
For example, a common mistake is to write code like messageCount && <p>New messages</p>. It’s easy to assume that it renders nothing when messageCount is 0, but it really renders the 0 itself!
To fix it, make the left side a boolean: messageCount > 0 && <p>New messages</p>.

 

Components Pure -
A component must be pure, meaning:
It minds its own business. It should not change any objects or variables that existed before rendering.
Same inputs, same output. Given the same inputs, a component should always return the same JSX.

State as a Snapshot –
State behaves more like a snapshot. Setting it does not change the state variable you already have, but instead triggers a re-render You can fix this by passing an updater function when setting state. Notice how replacing setScore(score + 1) with setScore(s => s + 1) fixes the “+3” button

Responding to Events –
 
 

Note
Make sure that you use the appropriate HTML tags for your event handlers. For example, to handle clicks, use <button onClick={handleClick}> instead of <div onClick={handleClick}>. Using a real browser <button> enables built-in browser behaviors like keyboard navigation. If you don’t like the default browser styling of a button and want to make it look more like a link or a different UI element, you can achieve it with CSS.

Event propagation -
Event handlers will also catch events from any children your component might have. We say that an event “bubbles” or “propagates” up the tree: it starts with where the event happened, and then goes up the tree. 
If you want to prevent an event from reaching parent components, you need to call e.stopPropagation()
Note : All events propagate in React except onScroll, which only works on the JSX tag you attach it to.





Capture phase events – 

 

Preventing default behavior - e.preventDefault()
Don’t confuse e.stopPropagation() and e.preventDefault(). They are both useful, but are unrelated:

e.stopPropagation() stops the event handlers attached to the tags above from firing.
e.preventDefault() prevents the default browser behavior for the few events that have it.

State: A Component's Memory - 
Two things prevent local variable change from being visible:

1.	Local variables don’t persist between renders. When React renders this component a second time, it renders it from scratch—it doesn’t consider any changes to the local variables.
2.	Changes to local variables won’t trigger renders. React doesn’t realize it needs to render the component again with the new data.
To update a component with new data, two things need to happen:

1.	Retain the data between renders.
2.	Trigger React to render the component with new data (re-rendering).

The useState Hook provides those two things:
A state variable to retain the data between renders.
A state setter function to update the variable and trigger React to render the component again.
State is isolated and private - 
State is local to a component instance on the screen. In other words, if you render the same component twice, each copy will have completely isolated state! Changing one of them will not affect the other. Unlike props, state is fully private to the component declaring it

Render and Commit - 
Before your components are displayed on screen, they must be rendered by React. 
Triggering a render.
Rendering the component.
Committing to the DOM.
React only changes the DOM nodes if there’s a difference between renders.
You can use Strict Mode to find mistakes in your components

A state variable’s value never changes within a render, even if its event handler’s code is asynchronous. Inside that render’s onClick, the value of number continues to be 0 even after setNumber(number + 5) was called. Its value was “fixed” when React “took the snapshot” of the UI by calling your component.

<button onClick={() => {
  setNumber(number + 1);
  setNumber(number + 1);
  setNumber(number + 1);
}}>+3</button>	<button onClick={() => {
  setNumber(0 + 1);
  setNumber(0 + 1);
  setNumber(0 + 1);
}}>+3</button>


React waits until all code in the event handlers has run before processing your state updates.

This lets you update multiple state variables—even from multiple components—without triggering too many re-renders. But this also means that the UI won’t be updated until after your event handler, and any code in it, completes. This behavior, also known as batching, makes your React app run much faster. It also avoids dealing with confusing “half-finished” renders where only some of the variables have been updated.



Updating Objects in State
Although objects in React state are technically mutable, you should treat them as if they were immutable—like numbers, booleans, and strings. Instead of mutating them, you should always replace them.
In React, you treat state as immutable!

Local mutation is fine - 
Code like this is a problem because it modifies an existing object in state:
position.x = e.clientX;
position.y = e.clientY;

But code like this is absolutely fine because you’re mutating a fresh object you have just created:

const nextPosition = {};
nextPosition.x = e.clientX;
nextPosition.y = e.clientY;
setPosition(nextPosition);
In fact, it is completely equivalent to writing this:

setPosition({
  x: e.clientX,
  y: e.clientY
});
Mutation is only a problem when you change existing objects that are already in state. Mutating an object you’ve just created is okay because no other code references it yet. Changing it isn’t going to accidentally impact something that depends on it. This is called a “local mutation”. You can even do local mutation while rendering. Very convenient and completely okay!

Note that the ... spread syntax is “shallow”—it only copies things one level deep. This makes it fast, but it also means that if you want to update a nested property, you’ll have to use it more than once.

Note –
Hooks—functions starting with use—can only be called at the top level of your components or your own Hooks. You can’t call Hooks inside conditions, loops, or other nested functions. Hooks are functions, but it’s helpful to think of them as unconditional declarations about your component’s needs. You “use” React features at the top of your component similar to how you “import” modules at the top of your file.

How does Immer work?
The draft provided by Immer is a special type of object, called a Proxy, that “records” what you do with it. This is why you can mutate it freely as much as you like! Under the hood, Immer figures out which parts of the draft have been changed, and produces a completely new object that contains your edits.

Updating Arrays in State - 
Arrays are mutable in JavaScript, but you should treat them as immutable when you store them in state. Just like with objects, when you want to update an array stored in state, you need to create a new one (or make a copy of an existing one), and then set state to use the new array.

 

 
Arrow functions implicitly return the expression right after =>, so you didn’t need a return statement:
const listItems = chemists.map(person =>
  <li>...</li> // Implicit return!
);
However, you must write return explicitly if your => is followed by a { curly brace!
const listItems = chemists.map(person => { // Curly brace
  return <li>...</li>;
});
Arrow functions containing => { are said to have a “block body”. They let you write more than a single line of code, but you have to write a return statement yourself. If you forget it, nothing gets returned!

Reacting to Input with State –
•	Declarative programming means describing the UI for each visual state rather than micromanaging the UI (imperative).
•	When developing a component:
1.	Identify all its visual states.
2.	Determine the human and computer triggers for state changes.
3.	Model the state with useState.
4.	Remove non-essential state to avoid bugs and paradoxes.
5.	Connect the event handlers to set state.

Principles for structuring state - 
1.	Group related state
2.	Avoid contradictions in state. 
3.	Avoid redundant state. 
4.	Avoid duplication in state. 
5.	Avoid deeply nested state.
Make your state as simple as it can be—but no simpler.

Group related state -
You might sometimes be unsure between using a single or multiple state variables.
Technically, you can use either of these approaches. But if some two state variables always change together, it might be a good idea to unify them into a single state variable. Then you won’t forget to always keep them in sync.
Lifting state up state -
To “lift their state up” to a parent component in three steps:

1.	Remove state from the child components.
2.	Pass hardcoded data from the common parent.
3.	Add state to the common parent and pass it down together with the event handlers.
It’s useful to consider components as “controlled” (driven by props) or “uncontrolled” (driven by state).

A single source of truth for each state 
In a React application, many components will have their own state. Some state may “live” close to the leaf components (components at the bottom of the tree) like inputs. Other state may “live” closer to the top of the app. For example, even client-side routing libraries are usually implemented by storing the current route in the React state, and passing it down by props!

For each unique piece of state, you will choose the component that “owns” it. This principle is also known as having a “single source of truth”. It doesn’t mean that all state lives in one place—but that for each piece of state, there is a specific component that holds that piece of information. Instead of duplicating shared state between components, lift it up to their common shared parent, and pass it down to the children that need it.

Note - CSSOM The CSS Object Model is a set of APIs allowing the manipulation of CSS from JavaScript. It is much like the DOM, but for the CSS rather than the HTML. It allows users to read and modify CSS style dynamically. The values of CSS are represented untyped, that is using String objects.

Preserving and Resetting State – 

React preserves a component’s state for as long as it’s being rendered at its position in the UI tree. If it gets removed, or a different component gets rendered at the same position, React discards its state.



The UI tree -
Browsers use many tree structures to model UI. The DOM represents HTML elements, the CSSOM does the same for CSS. There’s even an Accessibility tree!

React also uses tree structures to manage and model the UI you make. React makes UI trees from your JSX. Then React DOM updates the browser DOM elements to match that UI tree. (React Native translates these trees into elements specific to mobile platforms.)

 

Note – 
Remember that it’s the position in the UI tree—not in the JSX markup—that matters to React! This component has two return clauses with different <Counter /> JSX tags inside and outside the if:
You might expect the state to reset when you tick checkbox, but it doesn’t! This is because both of these <Counter /> tags are rendered at the same position. React doesn’t know where you place the conditions in your function. All it “sees” is the tree you return.

In both cases, the App component returns a <div> with <Counter /> as a first child. To React, these two counters have the same “address”: the first child of the first child of the root. This is how React matches them up between the previous and next renders, regardless of how you structure your logic.
Also, when you render a different component in the same position, it resets the state of its entire subtree.

As a rule of thumb, if you want to preserve the state between re-renders, the structure of your tree needs to “match up” from one render to another. If the structure is different, the state gets destroyed because React destroys state when it removes a component from the tree.
•	React keeps state for as long as the same component is rendered at the same position.
•	State is not kept in JSX tags. It’s associated with the tree position in which you put that JSX.
•	You can force a subtree to reset its state by giving it a different key.
•	Don’t nest component definitions, or you’ll reset state by accident.
Passing Data Deeply with Context -
Usually, you will pass information from a parent component to a child component via props. But passing props can become verbose and inconvenient if you have to pass them through many components in the middle, or if many components in your app need the same information. Context lets the parent component make some information available to any component in the tree below it—no matter how deep—without passing it explicitly through props.

Props drilling -
Prop drilling occurs when a parent component passes data down to its children and then those children pass the same data down to their own children.

Avoiding Prop Drilling in the React Ecosystem - 
Three ways to avoid prop drilling in React: using useContext, component composition, and the Zustand library for advanced state management.
The React context API is a fast way of avoiding prop drilling and ensuring your data is managed globally without using a huge third-party state management.

 


Three steps to use Context :-
Create and export it with export const MyContext = createContext(defaultValue).
Pass it to the useContext(MyContext) Hook to read it in any child component, no matter how deep.
Wrap children into <MyContext.Provider value={...}> to provide it from a parent.

Escape Hatches -
Some of your components may need to control and synchronize with systems outside of React. For example, you might need to focus an input using the browser API, play and pause a video player implemented without React, or connect and listen to messages from a remote server.
Referencing values with refs 
When you want a component to “remember” some information, but you don’t want that information to trigger new renders, you can use a ref:

const ref = useRef(0);
Like state, refs are retained by React between re-renders. However, setting state re-renders a component. Changing a ref does not! You can access the current value of that ref through the ref.current property.
A ref is like a secret pocket of your component that React doesn’t track. For example, you can use refs to store timeout IDs, DOM elements, and other objects that don’t impact the component’s rendering output.

Lifecycle of reactive effects 
Effects have a different lifecycle from components. Components may mount, update, or unmount. An Effect can only do two things: to start synchronizing something, and later to stop synchronizing it. This cycle can happen multiple times if your Effect depends on props and state that change over time.

Referencing Values with Refs -

When you want a component to “remember” some information, but you don’t want that information to trigger new renders, you can use a ref.
import { useRef } from 'react';
const ref = useRef(0);
useRef returns an object like this:

{ 
  current: 0 // The value you passed to useRef
}
ref.current // give ref value

This value is intentionally mutable, meaning you can both read and write to it. It’s like a secret pocket of your component that React doesn’t track.

Differences between refs and state -
Perhaps you’re thinking refs seem less “strict” than state—you can mutate them instead of always having to use a state setting function, for instance. But in most cases, you’ll want to use state. Refs are an “escape hatch” you won’t need often. Here’s how state and refs compare:

refs	state
useRef(initialValue) returns { current: initialValue }	useState(initialValue) returns the current value of a state variable and a state setter function ( [value, setValue])
Doesn’t trigger re-render when you change it.	Triggers re-render when you change it.
Mutable—you can modify and update current’s value outside of the rendering process.	“Immutable”—you must use the state setting function to modify state variables to queue a re-render.
You shouldn’t read (or write) the current value during rendering.	You can read state at any time. However, each render has its own snapshot of state which does not change.

A ref is a plain JavaScript object with a single property called current, which you can read or set.




When to use refs -
Typically, you will use a ref when your component needs to “step outside” React and communicate with external APIs—often a browser API that won’t impact the appearance of the component. Here are a few of these rare situations:

Storing timeout IDs -
Storing and manipulating DOM elements, which we cover on the next page
Storing other objects that aren’t necessary to calculate the JSX.
If your component needs to store some value, but it doesn’t impact the rendering logic, choose refs.

Best practices for refs -
Treat refs as an escape hatch. 
Don’t read or write ref.current during rendering.

// You can use any browser APIs, for example:
myRef.current.scrollIntoView();

Accessing another component’s DOM nodes -
When you put a ref on a built-in component that outputs a browser element like <input />, React will set that ref’s current property to the corresponding DOM node (such as the actual <input /> in the browser).

However, if you try to put a ref on your own component, like <MyInput />, by default you will get null.
A component doesn’t expose its DOM nodes by default. You can opt into exposing a DOM node by using forwardRef and passing the second ref argument down to a specific node.

Synchronizing with Effects -
Every time your component renders, React will update the screen and then run the code inside useEffect. In other words, useEffect “delays” a piece of code from running until that render is reflected on the screen.
By default, Effects run after every render (including the initial one).




import { useEffect } from 'react';
useEffect(() => {
  // This runs after every render
});
useEffect(() => {
  // This runs only on mount (when the component appears first time)
}, []);
useEffect(() => {
  // This runs on mount *and also* if either a or b have changed since the last render
}, [a, b]);

If your Effect breaks because of remounting, you need to implement a cleanup function.
React will call your cleanup function each time before the Effect runs again, and one final time when the component unmounts (gets removed).
useEffect(() => {
    const connection = createConnection();
    connection.connect();
    return () => {
      connection.disconnect();
    };
  }, []);

To cache expensive calculations, add useMemo instead of useEffect.
// 🔴 Avoid: Resetting state on prop change in an Effect
  useEffect(() => {
    setComment('');
  }, [userId]);
  // ...

 // 🔴 Avoid: Event-specific logic inside an Effect
  useEffect(() => {
    if (product.isInCart) {
      showNotification(`Added ${product.name} to the shopping cart!`);
    }
  }, [product]);
 // ...

 // 🔴 Avoid: The onChange handler runs too late
  useEffect(() => {
    onChange(isOn);
  }, [isOn, onChange])
 // ...

// 🔴 Avoid: Passing data to the parent in an Effect
  useEffect(() => {
    if (data) {
      onFetched(data);
    }
  }, [onFetched, data]);
  // ...

Lifecycle of Reactive Effects -
Effects have a different lifecycle from components. Components may mount, update, or unmount. An Effect can only do two things: to start synchronizing something, and later to stop synchronizing it. This cycle can happen multiple times if your Effect depends on props and state that change over time. React provides a linter rule to check that you’ve specified your Effect’s dependencies correctly. This keeps your Effect synchronized to the latest props and state.

The lifecycle of an Effect -
Every React component goes through the same lifecycle:

A component mounts when it’s added to the screen.
A component updates when it receives new props or state, usually in response to an interaction.
A component unmounts when it’s removed from the screen.
It’s a good way to think about components, but not about Effects.

Note -
Some Effects don’t return a cleanup function at all. More often than not, you’ll want to return one—but if you don’t, React will behave as if you returned an empty cleanup function.

If your linter is configured for React, it will check that every reactive value used by your Effect’s code is declared as its dependency.
The linter is your friend, but its powers are limited. The linter only knows when the dependencies are wrong. It doesn’t know the best way to solve each case. If the linter suggests a dependency, but adding it causes a loop, it doesn’t mean the linter should be ignored. You need to change the code inside (or outside) the Effect so that that value isn’t reactive and doesn’t need to be a dependency.
useEffect(() => {
  // ...
  // 🔴 Avoid suppressing the linter like this:
  // eslint-ignore-next-line react-hooks/exhaustive-deps
}, []);

Reusing Logic with Custom Hooks -
Custom Hooks let you share logic between components.
Custom Hooks must be named starting with use followed by a capital letter.
Custom Hooks only share stateful logic, not state itself.
You can pass reactive values from one Hook to another, and they stay up-to-date.
All Hooks re-run every time your component re-renders.
The code of your custom Hooks should be pure, like your component’s code.
Wrap event handlers received by custom Hooks into Effect Events.
Don’t create custom Hooks like useMount. Keep their purpose specific.

Note – 
•	JavaScript supports closures which means an inner function.
•	Make sure that you’ve enabled all the eslint-plugin-react-hooks rules for your project. They are essential and catch the most severe bugs early. The recommended eslint-config-react-app preset already includes them.
•	TypeScript is a popular way to add type definitions to JavaScript codebases. Out of the box, TypeScript supports JSX and you can get full React Web support
•	Every file containing JSX must use the .tsx file extension. This is a TypeScript-specific extension that tells TypeScript that this file contains JSX.


Cover it later –
Extracting State Logic into a Reducer

