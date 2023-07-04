Certainly! Here are the relevant code snippets from the script:

1. Installing and importing React Router:
```bash
# Installation
npm install react-router-dom
```

```javascript
// Importing BrowserRouter and Route
import { BrowserRouter, Route } from 'react-router-dom';
```

2. Setting up the BrowserRouter and defining routes:
```javascript
// Wrap your app content in BrowserRouter
ReactDOM.render(
  <BrowserRouter>
    <App />
  </BrowserRouter>,
  document.getElementById('root')
);

// Defining routes with Route component
<BrowserRouter>
  <Route exact path="/" component={Home} />
  <Route exact path="/eat" component={Eat} />
  <Route exact path="/drink" component={Drink} />
</BrowserRouter>
```

3. Using exact and path props in Route:
```javascript
// Example of exact and path usage
<Route exact path="/" component={Home} />
<Route exact path="/eat" component={Eat} />
<Route exact path="/drink" component={Drink} />
```

These snippets demonstrate the installation and usage of React Router in a React application. The BrowserRouter component is used to wrap the app, and the Route component is used to define the routes and corresponding components. The `exact` prop ensures an exact match for the specified path, and the `path` prop defines the path to be matched.