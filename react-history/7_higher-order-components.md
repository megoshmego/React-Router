Certainly! Here are the relevant code snippets from the script:

1. Higher-Order Functions and Higher-Order Components:
```javascript
// Higher-Order Function example
function withLogging(func) {
  return function wrapperFunc(...args) {
    const results = func(...args);
    console.log(results);
    return results;
  };
}

// Higher-Order Component example
function withCounter(Component) {
  return class extends React.Component {
    state = {
      count: 0
    };

    increaseCount = () => {
      this.setState(prevState => ({
        count: prevState.count + 1
      }));
    };

    decreaseCount = () => {
      this.setState(prevState => ({
        count: prevState.count - 1
      }));
    };

    render() {
      return (
        <Component
          count={this.state.count}
          onIncrease={this.increaseCount}
          onDecrease={this.decreaseCount}
          {...this.props}
        />
      );
    }
  };
}
```
In the script, higher-order functions and higher-order components are introduced as alternative solutions to sharing code between components. The higher-order function example `withLogging` takes a regular function as an argument and returns a new function that adds logging functionality. The higher-order component example `withCounter` takes a React component as an argument and returns a new component that adds a count state and methods to increase and decrease the count.

2. Using Higher-Order Components:
```javascript
class Counter extends React.Component {
  render() {
    const { count, onIncrease, onDecrease } = this.props;
    return (
      <div>
        <p>Count: {count}</p>
        <button onClick={onIncrease}>Increase</button>
        <button onClick={onDecrease}>Decrease</button>
      </div>
    );
  }
}

const CounterWithLogging = withLogging(Counter);
const CounterWithCounter = withCounter(Counter);
```
In this example, the `Counter` component is a regular class-based component that displays the count and provides buttons to increase and decrease it. The `CounterWithLogging` and `CounterWithCounter` components are created by applying the higher-order functions `withLogging` and `withCounter` to the `Counter` component, respectively. These higher-order components enhance the `Counter` component with additional functionality, such as logging and count state management.

These code snippets demonstrate how higher-order functions and higher-order components can be used to share code and functionality between components in React. Higher-order functions allow us to enhance regular functions, while higher-order components enable us to enhance React components. They provide a way to abstract and reuse common logic, making our code more modular and reusable.