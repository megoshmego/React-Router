Certainly! Here are the relevant code snippets from the script:

1. Adding a catch-all route at the bottom of the Switch component:
```javascript
<Switch>
  {/* Existing routes */}
  <Route component={NotFound} />
</Switch>
```

2. Creating a catch-all component to display when no route is matched:
```javascript
// Example catch-all component
const NotFound = () => {
  return <h1>Not Found</h1>;
};
```

3. Using a Switch component to ensure exclusive routing:
```javascript
<Switch>
  {/* Existing routes */}
  <Route component={NotFound} />
</Switch>
```

These snippets demonstrate how to add a catch-all route at the bottom of the Switch component to handle cases where no route is matched. By specifying a route without a path, it acts as a catch-all or a fallback option. In this example, the NotFound component is rendered when no other route is matched. The Switch component ensures that only the first matching route is rendered, providing exclusive routing. It's important to place the catch-all route at the end of the Switch component to prevent it from matching every page or route.

Note: In a real-world scenario, the NotFound component would typically be more complex than just a hard-coded `<h1>Not Found</h1>`. It can be a dedicated component with a custom design and additional content to indicate that the requested route was not found.