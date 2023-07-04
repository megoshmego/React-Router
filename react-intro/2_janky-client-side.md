Certainly! Here are the relevant code snippets from the script:

1. Setting up the components and initial state:
```javascript
// Components: Home, Eat, Drink
const Home = () => (
  <>
    <img src="home.jpg" alt="Home" />
    <h1>Home</h1>
  </>
);

const Eat = () => (
  <>
    <img src="eat.jpg" alt="Eat" />
    <h1>Eat</h1>
  </>
);

const Drink = () => (
  <>
    <img src="drink.jpg" alt="Drink" />
    <h1>Drink</h1>
  </>
);

// App component
const App = () => {
  const [page, setPage] = useState('home');

  // Conditional rendering based on page state
  const showPage = () => {
    if (page === 'home') return <Home />;
    if (page === 'eat') return <Eat />;
    if (page === 'drink') return <Drink />;
  };

  return (
    <>
      <nav>
        <a onClick={() => setPage('home')}>Home</a>
        <a onClick={() => setPage('eat')}>Eat</a>
        <a onClick={() => setPage('drink')}>Drink</a>
      </nav>
      {showPage()}
    </>
  );
};
```

2. Limitations of the janky version of Client-Side Routing:
- The URL bar does not change when navigating between components.
- Bookmarks or direct URLs to specific pages do not work.
- The back button does not navigate to the previous page.

3. Using `window.history` for navigation:
```javascript
// Navigating back using window.history
const goBack = () => {
  window.history.back();
};
```

These snippets demonstrate the implementation of a basic version of Client-Side Routing without using React Router. It shows how to conditionally render components based on the `page` state and how to handle navigation using `onClick` events. The limitations of this approach are also highlighted, such as the lack of URL changes and the inability to handle back button navigation.