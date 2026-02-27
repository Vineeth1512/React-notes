# React-notes

---

# 📘 Core React

## Part 1 (Questions 1 – 10)

---

# Core React

---

## 1. What is React?

React (aka React.js or ReactJS) is an **open-source front-end JavaScript library** that is used for building composable user interfaces, especially for single-page applications. It is used for handling view layer for web and mobile apps based on components in a declarative approach. 

React was created by [Jordan Walke](https://github.com/jordwalke), a software engineer working for Facebook. React was first deployed on Facebook's News Feed in 2011 and on Instagram in 2012.

**[⬆ Back to Top](#core-react)**

---

## 2. What is the history behind React evolution?

The history of ReactJS started in 2010 with the creation of **XHP**. XHP is a PHP extension which improved the syntax of the language such that XML document fragments become valid PHP expressions and the primary purpose was used to create custom and reusable HTML elements. 

The main principle of this extension was to make front-end code easier to understand and to help avoid cross-site scripting attacks. The project was successful to prevent the malicious content submitted by the scrubbing user.

But there was a different problem with XHP in which dynamic web applications require many roundtrips to the server, and XHP did not solve this problem. Also, the whole UI was re-rendered for small change in the application. Later, the initial prototype of React is created with the name **FaxJS** by Jordan inspired from XHP. Finally after sometime React has been introduced as a new library into JavaScript world.

**Note:** JSX comes from the idea of XHP

**[⬆ Back to Top](#core-react)**

---

## 3. What are the major features of React?

The major features of React are:

- Uses **JSX** syntax.
- Uses **Virtual DOM** instead of Real DOM.
- Supports **server-side rendering** (SEO friendly).
- Follows **one-way data flow**.
- Uses **reusable/composable components**.

**[⬆ Back to Top](#core-react)**

---

## 4. What is JSX?

JSX stands for **JavaScript XML** and it is an XML-like syntax extension to ECMAScript. It provides syntactic sugar for the `React.createElement(type, props, ...children)` function.

### Example:

```jsx
export default function App() {
  return (
    <h1 className="greeting">
      {"Hello, this is a JSX Code!"}
    </h1>
  );
}
```

Without JSX:

```javascript
import { createElement } from 'react';

export default function App() {
  return createElement(
    'h1',
    { className: 'greeting' },
    'Hello, this is a JSX Code!'
  );
}
```

**Note:** JSX is stricter than HTML.

**[⬆ Back to Top](#core-react)**

---

## 5. What is the difference between Element and Component?

### Element

An Element is a plain object describing what you want to appear on the screen.

```javascript
const element = React.createElement("div", { id: "login-btn" }, "Login");
```

Equivalent JSX:

```html
<div id="login-btn">Login</div>
```

### Component

A component can be a function or class that returns JSX.

```javascript
const Button = ({ handleLogin }) => (
  <div id="login-btn" onClick={handleLogin}>
    Login
  </div>
);
```

**[⬆ Back to Top](#core-react)**

---

## 6. How to create components in React?

### 1. Function Components

```jsx
function Greeting({ message }) {
  return <h1>{`Hello, ${message}`}</h1>;
}
```

### 2. Class Components

```jsx
class Greeting extends React.Component {
  render() {
    return <h1>{`Hello, ${this.props.message}`}</h1>;
  }
}
```

**[⬆ Back to Top](#core-react)**

---

## 7. When to use Class Component over Function Component?

After Hooks (React 16.8+), Function components are preferred.

Use Class Components when:

1. Using Error Boundaries.
2. Working in older React versions.

**[⬆ Back to Top](#core-react)**

---

## 8. What are Pure Components?

Pure components render the same output for the same props and state.

In Function components:

```jsx
const MemoizedComponent = React.memo(SomeComponent);
```

In Class components:
Extend `React.PureComponent`.

**[⬆ Back to Top](#core-react)**

---

## 9. What is state in React?

State is an object that holds information that may change over time.

```jsx
import React, { useState } from "react";

function User() {
  const [message, setMessage] = useState("Welcome to React world");

  return <h1>{message}</h1>;
}
```

State is private and controlled by the component.

**[⬆ Back to Top](#core-react)**

---

## 10. What are props in React?

Props are inputs to components. They are read-only and passed from parent to child.

```jsx
const ChildComponent = ({ name, age }) => (
  <div>
    <p>{name}</p>
    <p>{age}</p>
  </div>
);
```

**[⬆ Back to Top](#core-react)**



---


