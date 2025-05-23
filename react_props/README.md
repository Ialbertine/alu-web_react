# React Props
## How to create basic React components using functions
This is actually really easy, you just need to create functions that return html+css, known as .jsx or with TypeScript, .tsx

Here's an example of this App.js, with a couple of custom component imported in. You just need a parent tag as a div, or a React.Fragment, shown here as '<>'
```
function App() {
  return (
    <>
      <Notifications />
      <div className="App">
        <Header />
        <Login />
        <Footer />
      </div>
    </>
  );
}
```

## How to reuse components
Components are react functions and classes that are *reusable* which means that you can import them and place them anywhere in your project! They act like standalone HTML tags, but with custom definitions! In my previous example, 'Notifications', 'Header', 'Login', & 'Footer' are custom components.

## How to pass properties to components
All components can take properties, known as props, downstream from parent components. In a functional component, you pass these props like parameters, and in a class component, you must call these props in a constructor.

Here's what that looks like in my CourseListRow functional component from task_4
```function CourseListRow({ isHeader, textFirstCell, textSecondCell }) {```
And then you can use these properties like variables!

In a class component, this looks more like this
```
class App extends React.Component {
  constructor(props) {
    super(props);
  }
```

## How to define types for components
Well you can use PropTypes from the 'prop-types' library for js, or this is a natural feature of typescript :triumph:
It's as simple as defining an App's prop "types" and "default" props, let me show you what I mean.
```
// For an example App.js with a boolean isLogggedIn
App.propTypes = {
  isLoggedIn: PropTypes.bool,
};

App.defaultProps = {
  isLoggedIn: false
};
```