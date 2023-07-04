Certainly! Here are the relevant code snippets from the script:

1. Using the `componentDidMount` method in a class component:
```javascript
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
      isHiding: false
    };
  }

  componentDidMount() {
    console.log('Component mounted');
  }

  render() {
    console.log('Component rendering');
    // ...
  }
}
```

In this example, the `componentDidMount` method is added to the class component. It runs after the component has been initially rendered. Here, we simply log a message to the console to indicate that the component has mounted. The method is called only once during the component's lifecycle.

2. Using the `componentDidUpdate` method in a class component:
```javascript
class Counter extends React.Component {
  // ...

  componentDidUpdate() {
    console.log('Component updated');
  }

  // ...
}
```

In this example, the `componentDidUpdate` method is added to the class component. It runs after the component has been updated due to a change in props or state. Here, we log a message to the console to indicate that the component has been updated. The method can be used to perform additional actions or side effects after an update.

3. Using the `componentWillUnmount` method in a class component:
```javascript
class Counter extends React.Component {
  // ...

  componentWillUnmount() {
    console.log('About to go bye-bye');
  }

  // ...
}
```

In this example, the `componentWillUnmount` method is added to the class component. It runs right before the component is about to be removed from the DOM. Here, we log a message to the console to indicate that the component is about to be unmounted. The method can be used to clean up any resources or subscriptions before the component is removed.

These code snippets demonstrate how to use lifecycle methods in class-based components. Each method serves a specific purpose and is called at a particular point in the component's lifecycle. These methods provide hooks to perform actions such as data fetching, updating, or cleanup in class-based components.