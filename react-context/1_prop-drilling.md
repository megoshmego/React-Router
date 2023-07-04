Certainly! Here are some code snippets that illustrate the concepts discussed in the video:

1. Prop Drilling:
   - Prop drilling refers to the practice of passing data down from a parent component as a prop to a child component, and potentially to deeper levels of nested components.
   - It can become cumbersome and repetitive when sharing data between multiple components.
   - Here's an example of prop drilling in the code:

```jsx
// Child component
const Child = () => {
  // ...
  return (
    <div>
      <p>I am the child</p>
      <GrandChild count={count} />
    </div>
  );
};

// GrandChild component
const GrandChild = ({ count }) => {
  // ...
  return (
    <div>
      <p>I am the grandchild</p>
      <GreatGrandChild count={count} />
    </div>
  );
};

// GreatGrandChild component
const GreatGrandChild = ({ count }) => {
  // ...
  return <p>Count is {count}</p>;
};
```

2. Introduction to Context:
   - Context is an API in React that helps solve the prop drilling problem by providing a way to share data without explicitly passing it through props.
   - It allows for the creation of a "context" that can be accessed by nested components.
   - Here's a basic example of creating a context and using it:

```jsx
import React, { createContext, useContext } from 'react';

// Create a context
const CountContext = createContext();

// Parent component
const Parent = () => {
  // Set up the context provider
  return (
    <CountContext.Provider value={count}>
      <Child />
    </CountContext.Provider>
  );
};

// Child component
const Child = () => {
  // Consume the context using useContext
  const count = useContext(CountContext);
  // ...
};

// GrandChild component
const GrandChild = () => {
  // Consume the context using useContext
  const count = useContext(CountContext);
  // ...
};

// GreatGrandChild component
const GreatGrandChild = () => {
  // Consume the context using useContext
  const count = useContext(CountContext);
  // ...
};
```

3. Updating Context Value:
   - Context can also be used to update shared data by providing a mechanism to modify the context value.
   - In this example, a button in the `GreatGrandChild` component triggers a function in the `Child` component to update the context value.

```jsx
// Child component
const Child = () => {
  const [count, setCount] = useState(0);
  const addToCount = () => {
    setCount(count + 1);
  };

  return (
    <CountContext.Provider value={{ count, addToCount }}>
      {/* ... */}
    </CountContext.Provider>
  );
};

// GreatGrandChild component
const GreatGrandChild = () => {
  const { count, addToCount } = useContext(CountContext);

  return (
    <div>
      <p>Count is {count}</p>
      <button onClick={addToCount}>Increment Count</button>
    </div>
  );
};
```

These code snippets demonstrate the concept of prop drilling and how React's context API can be used to alleviate the need for excessive prop passing and enable sharing data between components more efficiently.