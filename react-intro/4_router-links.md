Certainly! Here are the relevant code snippets from the script:

1. Importing the Link component:
```javascript
// Importing the Link component
import { Link } from 'react-router-dom';
```

2. Adding links using the Link component:
```javascript
// Example of adding links using Link component
<Link to="/drink">Drink</Link>
<Link to="/eat">Eat</Link>
<Link to="/">Home</Link>
```

3. Wrapping links in a `<nav>` element:
```javascript
// Wrapping links in a <nav> element
<nav>
  <Link to="/drink">Drink</Link>
  <Link to="/eat">Eat</Link>
  <Link to="/">Home</Link>
</nav>
```

4. Styling the links using CSS:
```css
/* Adding margin to anchor tags inside .app class */
.app nav a {
  margin-right: 10px;
}
```

These snippets illustrate how to add links using the Link component from React Router. The `to` prop is used to specify the destination path, and the link text is placed between the opening and closing `<Link>` tags. The links are wrapped in a `<nav>` element for semantic purposes and styling is applied using CSS.