# `new-component`
### Simple utility for creating new React components.

<br />

**Note :** Based on original code developed by Joshua Comeau at https://github.com/joshwcomeau/new-component 

I did modify Joshua Comeau's version (1.0.1) to match with my coding style. The purpose of modification is for my personal development on local machine. What i did modified from Joshua's version are

- change logic to create component under **current directory** instead of under **src/components**. This will be more flexible in case you want to create child component under any component's folder.
- create an empty stylesheet file + add link into a component. 
- modify default Component coding template (add default Constructor & change default coding style)
- reduce amount of logs display on screen.

<br />

Anyone else sick of writing the same component boilerplate, over and over?

This project is based on code developed by a Joshua Comeau. It's very simple to use, and requires no configuration. You can visit the original version of Joshua Comeau here --> https://github.com/joshwcomeau/new-component

<br />

## Features
- Simple CLI interface for adding Component, PureComponent, or Stateless Functional components.
- Colourful terminal output!

<br />

## Quickstart

Option 1: Install my modified version (via GitHub repository):

```bash
$ npm i -g git+https://github.com/8columns/new-component.git
```

Option 2 : Install original version developed by Joshua Comeau

```bash
$ npm i -g new-component
```


`cd` into your project's directory, then cd into src folder, and try creating a new component:

```bash
$ cd your-project
$ cd src
$ new-component Button
```

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

> `index.js` will allows you to `import` from the directory (eg. `import Button from 'components/Button'`), otherwise you have to import like this `import Button from 'components/Button/Button'` (a little wiered!)
>
