---
layout: post
title:  "React is a global variable"
date:   2018-05-09 1:00:00 -0700
categories: react
---
Learning any new library can be challenging.  With React, it can be hard peer through the opaque ecosystem of transpilers, linters, test runners and bundlers and see the library for what it is.  I'll be using [codepen][codepen] to give myself a rapid prototyping environment.  I'm going to use the React library without using JSX syntax to demonstrate that the React library is really just a simple global variable.

## Creating Components using `React.createElement()`

`createElement()` is a core part of the [React API][react-api], and will be key to how we avoid using the JSX syntax to create React Elements.

Here is how one might create a button element using JSX:
```JSX
const button = (props) => (<button {...props}>Button Text</button>);
```

And here is how the equivalent is written _without_ JSX:
```JS
const button = (props) => React.createElement('button', props, 'Button Text');
```

[react-api]: https://reactjs.org/docs/react-api.html
[react-without-jsx]: https://reactjs.org/docs/react-without-jsx.html
[react-component-api]: https://reactjs.org/docs/react-component.html
[codepen]: https://codepen.io/
