Certainly! Here are the relevant code snippets from the script:

1. Importing the NavLink component:
```javascript
// Importing the NavLink component
import { NavLink } from 'react-router-dom';
```

2. Adding NavLink components:
```javascript
// Example of using NavLink components
<NavLink to="/drink">Drink</NavLink>
<NavLink to="/eat">Eat</NavLink>
<NavLink to="/">Home</NavLink>
```

3. Adding an "active" class to the NavLink:
```javascript
// Adding an "active" class to NavLink
<NavLink to="/drink" activeClassName="active">Drink</NavLink>
<NavLink to="/eat" activeClassName="active">Eat</NavLink>
<NavLink to="/" activeClassName="active">Home</NavLink>
```

4. Styling the active NavLink:
```css
/* Styling the active NavLink */
.navbar a.active {
  color: black;
  /* Additional styles for the active NavLink */
}
```

These snippets illustrate how to use the NavLink component from React Router. It functions similarly to the Link component, but it adds an "active" class to the NavLink when the corresponding route is active. This allows for styling of the active NavLink, such as changing its color or applying different CSS styles. The `activeClassName` prop is used to specify the class name to be added when the NavLink is active.