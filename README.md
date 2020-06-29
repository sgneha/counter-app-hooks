We had used class components for following reasons:

1. to keep data in state
2. to use lifecycle methods
3. to pass props from classes to function components

   However by using hooks we can do all these without class components.

Hooks are functions which let us use states and other react features without writing class components.

In function components we cannot use states but with the use of hooks we can use states in function component as well.
Here is just demonstration of 2 hooks

1. useState() we can use state
2. useEffect() we can handle sideeffects means now no need to use all lifecycle methods like componentDidMount(),componentWillMount() if we use useeffect hook.

We have written counter using class component.Lets rewrite the counter in function components using hooks:

1. useState
   Import useState `import React, { Component, useState } from "react";`
   useState(0) returns 2 things first current state value and function that lets us update the state.
   so 0 is default value of count state.

   Now we have same couneter in function component.
   Let's next make use of useEffect to avoid using lifecycle methods.

2. useEffect
   As soon as state changes or updates useEffect will run.
   Let's write a simple app which lets us update Document title.
   Will make use of same class component as above with lifecycle methods then rewrite the same using useEffect hook.
   Bring back class component:
   Add two life cycle methods.
   1. componenetDidMount(): when the component mounts it will set the document title to equal to how many counts we have, which is 0 now.
   2. componenetDidUpdate(): when the state updates it changes the value of title as well.

Rewrite above using UseEffect hook:
Bring back the function component.
useEffect is a function which takes another function as argument
Add this

```
useEffect(() => {
    document.title = `Clicked ${count} times`;
  });
```

useEffect runs everytime there is change in state.
Its works perfectly.

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `yarn build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
