Certainly! Here are the relevant code snippets from the script:

1. Creating a class-based component:
```javascript
import React from 'react';

class Counter extends React.Component {
  render() {
    return (
      <div>
        <h1>I am counter</h1>
      </div>
    );
  }
}

export default Counter;
```

In this example, a class-based component named `Counter` is created by extending the `React.Component` class. The `render` method is defined within the class, and it returns JSX that represents the component's UI. The `Counter` component can be exported and used in other parts of the application.

2. Accessing props in a class component:
```javascript
import React from 'react';

class Counter extends React.Component {
  constructor(props) {
    super(props);
    console.log(this.props);
  }

  render() {
    const { color } = this.props;
    return (
      <div>
        <h1 style={{ color }}>I am counter</h1>
      </div>
    );
  }
}

export default Counter;
```

In this example, the `constructor` method is added to the class component to access the `props` passed to the component. By calling `super(props)`, the parent class's constructor is invoked with the `props` argument. The `props` can then be accessed using `this.props`. In the `render` method, the `color` prop is used to style the `<h1>` element.

These code snippets illustrate the process of creating and using class-based components in React. They demonstrate how to define a class component, access and use props within the component, and render JSX to represent the component's UI.