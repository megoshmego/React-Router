Certainly! Here are the relevant code snippets from the script:

1. Importing and using the `useHistory` hook to access the history object:
```javascript
import { useHistory } from 'react-router-dom';

// Inside a component or function
const history = useHistory();
```

2. Using the `push` method of the `history` object to programmatically redirect:
```javascript
import { useHistory } from 'react-router-dom';

// Inside a component or function
const history = useHistory();

// Redirect to a specific route
history.push('/about');
```

These code snippets demonstrate how to use the `useHistory` hook from React Router to access the `history` object. By invoking `useHistory`, we get access to the `history` object, which contains methods such as `push`. Calling `history.push('/about')` redirects the user to the specified route.

Using the `push` method differs from using the `Redirect` component in that it adds the new route to the browser history, allowing the user to navigate back and forward. The `Redirect` component, on the other hand, does not add any history entry and is more like a quick redirection without tracking the user's visit.

These techniques provide you with different ways to handle redirects programmatically in your React Router application.