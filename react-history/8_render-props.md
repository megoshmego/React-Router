Certainly! Here are some code snippets to illustrate the concepts mentioned in the feedback:

1. Higher-Order Components (HOCs):
```jsx
// Example of a higher-order component
const withRouter = (Component) => {
  // Wrapper component that provides router functionality
  return class extends React.Component {
    // ... logic to handle router functionality

    render() {
      // Render the wrapped component with additional props
      return <Component {...this.props} />;
    }
  };
};

// Usage of the higher-order component
const MyComponent = (props) => {
  // ... component logic
};

// Wrap MyComponent with the withRouter higher-order component
const WrappedComponent = withRouter(MyComponent);
```

2. Render Props:
```jsx
// Example of a component using render props
class CounterWrapper extends React.Component {
  state = {
    count: 0,
  };

  increment = () => {
    this.setState((prevState) => ({
      count: prevState.count + 1,
    }));
  };

  decrement = () => {
    this.setState((prevState) => ({
      count: prevState.count - 1,
    }));
  };

  render() {
    return (
      <div>
        {/* Call the render prop function with necessary data */}
        {this.props.render({
          count: this.state.count,
          increment: this.increment,
          decrement: this.decrement,
        })}
      </div>
    );
  }
}

// Usage of the CounterWrapper component
const Counter = () => {
  return (
    <CounterWrapper
      render={({ count, increment, decrement }) => (
        <div>
          <div>Count: {count}</div>
          <button onClick={increment}>Increment</button>
          <button onClick={decrement}>Decrement</button>
        </div>
      )}
    />
  );
};
```

3. Hooks:
```jsx
// Example of a functional component using hooks
const Counter = () => {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount((prevCount) => prevCount + 1);
  };

  const decrement = () => {
    setCount((prevCount) => prevCount - 1);
  };

  return (
    <div>
      <div>Count: {count}</div>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
    </div>
  );
};
```

These snippets showcase the usage of higher-order components, render props, and hooks in React.