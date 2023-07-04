Certainly! Here are the relevant code snippets from the script:

1. Repeating code and logic in lifecycle methods of class-based components:
```javascript
class TodoList extends React.Component {
  // ...

  componentDidMount() {
    this.fetchTodos();
  }

  componentDidUpdate(prevProps) {
    if (prevProps.todoId !== this.props.todoId) {
      this.fetchTodos();
    }
  }

  fetchTodos() {
    // Axios request to fetch todos
    // Set state with the response
  }

  // ...
}
```

In this example, the `TodoList` class component demonstrates the problem of repeating code and logic in lifecycle methods. The `componentDidMount` and `componentDidUpdate` methods both call the `fetchTodos` function to fetch todos from an API. The logic for fetching todos is duplicated in both methods, which can lead to code redundancy and maintenance issues.

2. Difficulty sharing logic or functionality between class-based components:
```javascript
class ComponentA extends React.Component {
  // ...

  handleButtonClick() {
    // Handle button click logic specific to ComponentA
  }

  render() {
    return (
      <div>
        {/* JSX for ComponentA */}
        <button onClick={this.handleButtonClick}>Click me</button>
      </div>
    );
  }
}

class ComponentB extends React.Component {
  // ...

  handleButtonClick() {
    // Handle button click logic specific to ComponentB
  }

  render() {
    return (
      <div>
        {/* JSX for ComponentB */}
        <button onClick={this.handleButtonClick}>Click me</button>
      </div>
    );
  }
}
```

In this example, there are two class components, `ComponentA` and `ComponentB`, that share similar functionality of handling a button click event. However, in class-based components, it's difficult to extract and share this logic between components because it often relies on `this.state` and `this.props` specific to each component. This can result in code duplication and make it challenging to reuse or maintain the shared logic.

These code snippets highlight the challenges faced in class-based components, such as repeating code and logic in lifecycle methods and difficulty sharing logic or functionality between components. These challenges have motivated the creation of hooks in React to provide a more streamlined and reusable approach to managing component behavior and state in functional components.