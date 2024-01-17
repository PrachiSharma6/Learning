React API Reference –
Built-in React Hooks –
1.	useState - 
useState is a React Hook that lets you add a state variable to your component.
import { useState } from 'react';
const [state, setState] = useState(initialState);
useState returns an array with exactly two values: initialState and set function,

Caveats -
•	useState is a Hook, so you can only call it at the top level of your component or your own Hooks. You can’t call it inside loops or conditions.
•	In Strict Mode, React will call your initializer function twice in order to help you find accidental impurities.
•	You can’t put a function into state

Updating state based on the previous state
Here, a => a + 1 is your updater function. It takes the pending state and calculates the next state from it.
setAge(a => a + 1)

2.	useEffect -
useEffect is a React Hook that lets you synchronize a component with an external system. useEffect returns undefined.

import { useEffect } from 'react';
useEffect(() => {
    const connection = createConnection(serverUrl, roomId);
    connection.connect();
    return () => {
      connection.disconnect();
    };
  }, [serverUrl, roomId]);

My Effect does something visual, and I see a flicker before it runs - 
If your Effect must block the browser from painting the screen, replace useEffect with useLayoutEffect. Note that this shouldn’t be needed for the vast majority of Effects. You’ll only need this if it’s crucial to run your Effect before the browser paint: for example, to measure and position a tooltip before the user sees it.

useContext - 

Context provide us a way to avoid props drilling. useContext store data to pass down to childrens in a parent tree.
useContext is a React Hook that lets you read and subscribe to context from your component. useContext returns the context value for the context you passed.
To determine the context value, React searches the component tree and finds the closest context provider above for that particular context. It searches upwards and does not consider providers in the component from which you’re calling useContext().
Specifying a fallback default value 
If React can’t find any providers of that particular context in the parent tree, the context value returned by useContext() will be equal to the default value that you specified when you created that context:

testContext.ts
import { createContext } from 'react';
interface User = {
name: string,
}
export const DashboardContext = createContext<User | undefined>(undefined);

index.ts
import { DashboardContext } from './context';
return (
<div>
<DashboardContext.Provider value={ name: 'John' }>
<Dashboard />
</DashboardContext.Provider>
</div>
);

sidebarProps.ts 
import { useContext } from 'react';
import { DashboardContext } from './context';

export function Sidebar({}: SidebarProps) {
const user = useContext(DashboardContext);

return (
<div>{user.name}</div>
);
}
Context with custom hook –
 

Overriding context for a part of the tree -
You can override the context for a part of the tree by wrapping that part in a provider with a different value.

useReducer -
useReducer is a React Hook that lets you add a reducer to your component.
const [state, dispatch] = useReducer(reducer, initialArg, init?);



import { useReducer } from 'react';
function reducer(state, action) {
  // ...
}
function MyComponent() {
  const [state, dispatch] = useReducer(reducer, { age: 42 });
  // ...

Returns 
useReducer returns an array with exactly two values:
- The current state.
- dispatch function

function reducer(state, action) {
  switch (action.type) {
    case 'incremented_age': {
      return {
        name: state.name,
        age: state.age + 1
      };
    }
    case 'changed_name': {
      return {
        name: action.nextName,
        age: state.age
      };
    }
  }
  throw Error('Unknown action: ' + action.type);
}

function handleButtonClick() {
    dispatch({ type: 'incremented_age' });
  }
 function handleInputChange(e) {
    dispatch({
      type: 'changed_name',
      nextName: e.target.value
    });
  }

useRef -
useRef is a React Hook that lets you reference a value that’s not needed for rendering.
const ref = useRef(initialValue);
useRef returns a ref object with a single current property initially set to the initial value you provided.

On the next renders, useRef will return the same object. You can change its current property to store information and read it later. This might remind you of state, but there is an important difference.

Changing a ref does not trigger a re-render. This means refs are perfect for storing information that doesn’t affect the visual output of your component. For example, if you need to store an interval ID and retrieve it later, you can put it in a ref. To update the value inside the ref, you need to manually change its current property:

By using a ref, you ensure that:
- store information
- it does not trigger a re-render
-  information is local

Do not write or read ref.current during rendering.
function MyComponent() {
  // ...
  // 🚩 Don't write a ref during rendering
  myRef.current = 123;
  // ...
  // 🚩 Don't read a ref during rendering
  return <h1>{myOtherRef.current}</h1>;
}

You can read or write refs from event handlers or effects instead.
function MyComponent() {
  // ...
  useEffect(() => {
    // ✅ You can read or write refs in effects
    myRef.current = 123;
  });
  // ...
  function handleClick() {
    // ✅ You can read or write refs in event handlers
    doSomething(myOtherRef.current);
  }
  // ...
}

Package details - 
add "analyze:contactless": "source-map-explorer 'dist/apps/mi-contactless-renderer/.next/static/chunks/pages/*.js'", in script. it shows bundle details 


Reference - 
5 Custom React Hooks You Need In Every Project
https://www.youtube.com/watch?v=0c6znExIqRw
