# Learning React with create-react-app
Documentation

# Table of Content

|Topics|
|----------|
|[Introduction](#introduction)|
|[Installation and Setup](#installation-and-setup)|
|[Start a new React Project](#start-a-new-react-project)|
|[Code Structure](#code-structure)|
|[JSX](#jsx)|
|[Components](#components)|
|[Props](#props)|
|[State](#state)|
|[List Rendering](#list-rendering)|
|[Conditional Rendering](#conditional-rendering)|
|[Hooks](#hooks)|
|[Routing](#routing)|
|[Installation of other Libraries](#installation-of-other-libraries)|
|[Context API](#context-api)|
|[Redux](#redux)|
|[Axios](#axios)|

---



# Introduction
React is an open-source front-end JavaScript library created by META (formerly facebook). React is used for building userinterfaces  web and mobile applications by creating UI components. React can be used to create
- Single page applications
- Mobile applications
- Web applications
- Server-rendered applications
React also have support powerful framework's support like Next.js

[Back to the Top](#table-of-content)

---
# Installation and Setup
To start a react project you must have *nodeJS* installed in your PC. To install NodeJS, go to the official website of nodejs https://nodejs.org/en
Here as shown in the picture below. Download and install the **LTS verstion** not the Current. You might have a different version from mine at that time when you are going through.
![nodejs](resources/nodejs_installation.png)

[Back to the Top](#table-of-content)

---

# Start a new React Project

[Back to the Top](#table-of-content)

---
# Code Structure

[Back to the Top](#table-of-content)

---
# JSX

[Back to the Top](#table-of-content)

---
# Components

[Back to the Top](#table-of-content)

---

# Props

[Back to the Top](#table-of-content)

---

# State

[Back to the Top](#table-of-content)

---
# List Rendering

[Back to the Top](#table-of-content)

---

# Conditional Rendering

[Back to the Top](#table-of-content)

---
# Hooks

## React.memo
###### App.js
```
//--App.js--
import './App.css';
import Button from './components/Button';
import { useState } from 'react';

function App() {
  const [counter, setCounter] = useState(0);
  return (
    <>
      <Button />
      <br />
      <h1>{counter}</h1>
      <br />
      <br />
      <button onClick={() => { setCounter(counter + 1) }}>Increment</button>
    </>
  );
}
export default App;
```
###### componenets/Button/index.js
```
//--components/Button/index.js--

function Button () {
    console.log("Button Component");
    return (
        <button>Click</button>
    )
}
export default Button;
```
But, if we don't want to render the button component every time. So, we use the *React Hook* **React.memo**. It memorises the component and do not let them to be rendered, every time when state changes but, only once at first time render.
Here, look the variation in the code of Button component.
to use **React.memo**, we have to first import. So, added the line

`import React from "react";`

Then, we use React.memo exactly where we are exporting the component like this

`export default React.memo(Button)`

See the complete code with changes.
```
//--components/Button/index.js--
import React from "react";
function Button () {
    console.log("Button Component");
    return (
        <button>Click</button>
    )
}
export default React.memo("Button");
```
Here is the glimpse of the working code.
![An example of React.memo (hook)](resources/React-memo.gif)

## useRef
### Example 1
using useRef hook get the value from input field.
###### App jsx
```
//--App.js--
import {useRef} from 'react';

function App() {
  const inputRef = useRef(null);

  return (
    <>
      <input ref={inputRef}/>
      <button onClick={()=>{console.log(inputRef.current.value)}}>Get input value</button>
    </>
  )
}

export default App;
```

# useRef
### Example 1
using useRef hook get the value from input field.
###### App jsx
```
//--App.js--
import {useRef} from 'react';

function App() {
  const inputRef = useRef(null);

  return (
    <>
      <input ref={inputRef}/>
      <button onClick={()=>{console.log(inputRef.current.value)}}>Get input value</button>
    </>
  )
}

export default App;
```



[Back to the Top](#table-of-content)

---

# Routing

[Back to the Top](#table-of-content)

---

# Installation of Other Libraries

[Back to the Top](#table-of-content)

---

# Context API

[Back to the Top](#table-of-content)

---

# Redux

[Back to the Top](#table-of-content)

---

# Axios

[Back to the Top](#table-of-content)

---
