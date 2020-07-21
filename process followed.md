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

1. useState()
   Import useState `import React, { Component, useState } from "react";`
   useState(0) returns 2 things first current state value and function that lets us update the state.
   so 0 is default value of count state.

   Now we have same counter in function component.
   Let's next make use of useEffect to avoid using lifecycle methods.

2. useEffect()
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
