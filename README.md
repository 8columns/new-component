<p align="center">
  <img src="https://github.com/joshwcomeau/new-component/blob/master/docs/logo@2x.png?raw=true" width="285" height="285" alt="new-component logo">
  <br>
  <a href="https://www.npmjs.org/package/new-component"><img src="https://img.shields.io/npm/v/new-component.svg?style=flat" alt="npm"></a>
</p>

# `new-component`
### Simple utility for creating new React components.

<br />

**Note :** Based on original code developed by Joshua Comeau at https://github.com/joshwcomeau/new-component 

I did modify Joshua Comeau's version to match with my coding style. The purpose of modification is for using in my local development. What i did modified from Joshua's version are

- add default component stylesheet 
- modify default Component coding template (add Constructor & default stylesheet)

<br />

Anyone else sick of writing the same component boilerplate, over and over?

This project is based on code developed by a Joshua Comeau. It's very simple to use, and requires no configuration. You can visit the original version of Joshua Comeau here --> https://github.com/joshwcomeau/new-component

<br />

## Features
- Simple CLI interface for adding Component, PureComponent, or Stateless Functional components.
- Colourful terminal output!

<br />

## Quickstart

Install via my GitHub repository:

```bash
$ npm i -g git+[URL]
```

`cd` into your project's directory, and try creating a new component:

<p align="center">
  <img src="https://github.com/joshwcomeau/new-component/blob/master/docs/demo.gif?raw=true" width="888" height="369" alt="demo of CLI functionality">
</p>

Your project will now have a new directory at `src/components/Button`. This directory has two files:

```jsx
// `Button/index.js`
export { default } from './Button';
```

```jsx
// `Button/Button.js`
import React, { Component } from 'react';

class Button extends Component {
  render() {
    return <div />;
  }
}

export default Button;
```

> This structure might appear odd to you, with an `index.js` that points to a named file. I've found this to be an optimal way to set up components; the `index.js` allows you to `import` from the directory (eg. `import Button from 'components/Button'`), while having `Button.js` means that you're never lost in a sea of `index.js` files in your editor.
>
> This structure is not currently configurable, but I'm happy to consider implementing alternatives!
