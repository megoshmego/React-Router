Certainly! Here are the relevant code snippets from the script:

1. Using the `Redirect` component to redirect to a specific route:
```javascript
import { Redirect } from 'react-router-dom';

// Inside a component or a route
<Redirect to="/about" />
```

2. Placing a `Redirect` component directly inside a component:
```javascript
import { Redirect } from 'react-router-dom';

// Inside a component
return (
  isAdmin ? (
    <h1>Welcome back, admin</h1>
  ) : (
    <Redirect to="/" />
  )
);
```

3. Importing and using the `history` object to programmatically redirect:
```javascript
import { useHistory } from 'react-router-dom';

// Inside a component or a function
const history = useHistory();
history.push('/about');
```

These code snippets demonstrate different approaches to implementing redirects using React Router. The first method utilizes the `Redirect` component, which is rendered and redirects the browser to the specified route when it is rendered. The second method shows how a `Redirect` component can be placed directly inside a component and conditionally rendered based on some logic.

The third method involves using the `useHistory` hook from React Router. By invoking `useHistory`, we get access to the `history` object, which provides a `push` method. Calling `history.push('/about')` programmatically redirects the user to the specified route.

These redirect techniques allow you to control the flow of navigation in your application based on certain conditions or events.