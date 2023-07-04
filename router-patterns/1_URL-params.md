Certainly! Here are the relevant code snippets from the script:

1. Setting up a route with URL parameter:
```javascript
// Defining a route with URL parameter
<Route path="/food/:name" component={Food} />
```

2. Using useParams to access URL parameters in a component:
```javascript
// Importing useParams hook
import { useParams } from 'react-router-dom';

// Inside the component
const params = useParams();
const name = params.name;
// OR
const { name } = useParams();
```

3. Accessing URL parameters for multiple variables:
```javascript
// Defining a route with multiple URL parameters
<Route path="/food/:foodName/:drinkName" component={Food} />

// Inside the component
const params = useParams();
const foodName = params.foodName;
const drinkName = params.drinkName;
// OR
const { foodName, drinkName } = useParams();
```

These snippets illustrate how to use URL parameters with React Router. By defining a route with a colon followed by the parameter name, you can capture dynamic values from the URL. The useParams hook allows you to access these parameters in your component. You can either assign the parameters to separate variables or destructure them directly. This enables you to create dynamic routes and handle different scenarios based on the URL parameters.