### Inspecting the starter code

#### `App.js`
App.js 的代码创建了一个 **组件**。  
![](Pasted%20image%2020240607142701.png)
在 React 中，组件是一段可重用代码，作为 UI 界面的一部分。  
组件用于渲染、管理和更新应用中的 UI 元素。  


```jsx
export default function Square() {  

return <button className="square">X</button>;  

}
```
第一行定义了一个名为 `Square` 的函数。    
JS 的 `export` 关键字使此函数可以在此文件之外访问。    
`default` 关键字表明它是文件中的主要函数。  
第二行返回一个按钮。  

JS 的 `return` 关键字意味着后面的内容都作为值返回给函数的调用者。
`<button>` 是一个 JSX 元素。  
JSX 元素是 JS 代码和 HTML 标签的组合，用于描述要显示的内容。  
`className="square"` 是一个 button 属性，它决定 CSS 如何设置按钮的样式。  
`X` 是按钮内显示的文本，  
`</button>` 闭合 JSX 元素以表示不应将任何后续内容放置在按钮内。    

#### `styles.css`
定义了 React 应用的样式。  
![](Pasted%20image%2020240607144843.png)
前两个 **CSS 选择器**（`*` 和 `body`）定义了应用大部分的样式 。
![](Pasted%20image%2020240607144959.png)
`.square` 选择器定义了 `className` 属性设置为 `square` 的组件的样式。  
这与 `App.js` 文件中的 `Square` 组件中的按钮是相匹配的。    

#### `index.js`
它是 `App.js` 文件中创建的组件与 Web 浏览器之间的桥梁。  
```jsx
import { StrictMode } from 'react';  

import { createRoot } from 'react-dom/client';  

import './styles.css';  

  

import App from './App';
```
- React
- React 与 Web 浏览器对话的库（React DOM）
- 组件的样式
- `App.js` 里面创建的组件    

```jsx
const root = createRoot(document.getElementById("root"));

root.render(

  <StrictMode>

    <App />

  </StrictMode>

);
```
- 简阅：   
1. `import React, { StrictMode } from "react";`: 这里导入了 React 库以及其中的 StrictMode 组件。StrictMode 是 React 提供的一个组件，用于帮助发现代码中的潜在问题，并标识出不安全的生命周期方法和过时的 API 使用。
    
2. `import { createRoot } from "react-dom/client";`: 这里从 React DOM 中导入了 createRoot 方法。createRoot 是一个用于启动 React 渲染的函数，它接受一个 DOM 元素作为参数，并返回一个根渲染器对象，用于将 React 组件渲染到该 DOM 元素中。
    
3. `import "./styles.css";`: 这里导入了样式表，用于给组件添加样式。
    
4. `import App from "./App";`: 这里导入了名为 App 的组件，通常是整个应用的主组件。
    
5. `const root = createRoot(document.getElementById("root"));`: 这行代码创建了一个根渲染器对象，将其赋值给名为 root 的变量。根据代码中的参数，这个根渲染器将渲染到 id 为 "root" 的 DOM 元素中。
    
6. `root.render(...)`: 这里调用了根渲染器对象的 render 方法，将一个 JSX 元素渲染到根元素中。在这个例子中，使用了 StrictMode 组件将 App 组件包裹起来，以启用严格模式下的渲染。这样可以帮助检测潜在的问题。
    
总体而言，这段代码的作用是将应用的根组件 App 渲染到 HTML 文档中具有 id 为 "root" 的 DOM 元素中，并在渲染过程中启用了 React 的严格模式。

### Building the board
Let’s get back to `App.js`.      
`<button>` is a _JSX element_.
React components need to return a single JSX element.
#### _Fragments_ (**`<>` and `</>`**) can wrap multiple adjacent JSX elements.
```jsx
export default function Square() {  
  return (  
	<>  
	  <button className="square">X</button>  
      <button className="square">X</button>  
	</>  
  );  
}
```
you should see:  
![](Pasted%20image%2020240607154231.png)

#### Creating a Grid Layout with `Divs` and **CSS Classes**
Using divs to group the squares into rows       
and adding some CSS classes can arrange the squares into a grid.   

While you’re at it, you’ll give each square a number to make sure you know where each square is displayed.

In the `App.js` file, update the `Square` component to look like this:    
```jsx
export default function Board() {
  return (
    <>
      <div className="board-row">
        <button className="square">1</button>
        <button className="square">2</button>
        <button className="square">3</button>
      </div>
      <div className="board-row">
        <button className="square">4</button>
        <button className="square">5</button>
        <button className="square">6</button>
      </div>
      <div className="board-row">
        <button className="square">7</button>
        <button className="square">8</button>
        <button className="square">9</button>
      </div>
    </>
  );
}
```
Note:  
在HTML和React中，`<button>` 是一个内置的HTML元素，用于创建一个按钮。它不是JavaScript代码，而是HTML标签，用于在网页上创建一个可交互的按钮。

`className` 是一个属性，它在HTML和React中用于指定元素的CSS类名。在HTML中，`class` 是标准的属性名，但在JavaScript中，由于 `class` 是一个保留字，所以React使用 `className` 作为替代，以避免与JavaScript的类定义语法冲突。

在React中，`className` 是一个标准的属性，用于指定组件的CSS类名。例如：
```jsx
function MyButton() { return <button className="my-button">Click Me</button>; }
```
在上面的React组件中，`className="my-button"` 指定了按钮的CSS类名，这样就可以在CSS文件中定义 `.my-button` 的样式。

总结来说，`<button>` 是HTML和React中的一个内置元素，而 `className` 是一个属性，用于指定元素的CSS类名。在React中，由于JavaScript的限制，使用 `className` 代替了HTML中的 `class` 属性。   
  
### Passing data through props
you’ll want to change the value of a square from empty to “X” when the user clicks on the square.   

React’s component architecture allows you to create a reusable component to avoid messy, duplicated code.  

- First, you are going to copy the line defining your first square (`<button className="square">1</button>`) from your `Board` component into a new `Square` component:  
```jsx
function Square() {  
  return <button className="square">1</button>;  
}  


export default function Board() {  
  // ...  
}
```


- Then you’ll update the Board component to render that `Square` component using JSX syntax:    
- components `Board` and `Square` must start with a capital letter.
- `div`s must start with a lowercase letter.
```jsx
// ...  

export default function Board() {  
  return (  
    <>  
	  <div className="board-row">  
		<Square />  
		<Square />  
		<Square />  
	  </div>  
	  <div className="board-row">  
		<Square />  
		<Square />  
		<Square />  
	  </div>  	 
	  <div className="board-row">  
		<Square />  
		<Square />  
		<Square />  
	  </div>    
    </>  
  );  
}
```
note:  
`<Square />`是在JSX语法中用于表示一个React组件的实例。这里`<Square />`代表了一个`Square`组件的实例，它会被渲染成一个按钮元素。   
`<Square />`是一个自闭合标签，它代表对`Square`组件的引用，而不是一个React Fragment。  
在React中，自闭合标签（self-closing tag）用于表示一个组件，这个组件没有子元素。自闭合标签的语法是`<ComponentName />`，其中`ComponentName`是组件的名称。在您提供的代码中，`Square`是一个组件，而`<Square />`表示在`Board`组件中创建了一个`Square`组件的实例。  
在`Board()`函数的返回值中，有多次使用`<Square />`这个语法，它表示调用了`Square()`函数。每次使用`<Square />`都会创建一个`Square`组件的实例.   
因为`Board()`函数内部调用了`Square()`函数，并将多个`Square`组件组合在一起，形成了一个完整的游戏板。  
所以`Square()`函数是子组件，而`Board()`函数是父组件。  
`board-row`是一个自定义的CSS类名，用于样式化游戏板的行。  
`className`是React中用于指定CSS类的属性。  
`<div>`是HTML中的一个元素，用于在页面上创建一个块级容器。  
在React 16.2版本之前，React Fragment是通过`<React.Fragment>`标签来表示的。从React 16.2版本开始，引入了简写语法`<>...</>`

- you will use _props_ to pass the value each square should have from the parent component (`Board`) to its child (`Square`).  
- Update the `Square` component to read the `value` prop that you’ll pass from the `Board`:   
```jsx
function Square({ value }) {  
  return <button className="square">1</button>;  
}
```

- `function Square({ value })` indicates the Square component can be passed a prop called `value`.  
- you want to display that `value` instead of `1` inside every square. Try doing it like this:  
```jsx
function Square({ value }) {  
  return <button className="square">value</button>;  
}
```

- To “escape into JavaScript” from JSX, you need curly braces.
- Bs you wanted to render the JavaScript variable called `value` from your component, not the word “value”.
```jsx
function Square({ value }) {  
  return <button className="square">{value}</button>;  
}
```
you should see an empty board:  
![](Pasted%20image%2020240608160343.png)

- you’ll add the `value` prop to each `Square` component rendered by the `Board` component, bs the `Board` component hasn’t passed the `value` prop to each `Square` component it renders yet.
```jsx
export default function Board() {  
  return (  
    <>  
	  <div className="board-row">  
		<Square value="1" />  
		<Square value="2"/>  
		<Square value="3"/>  
	  </div>  
	  <div className="board-row">  
		<Square value="4"/>  
		<Square value="5"/>  
		<Square value="6"/>  
	  </div>  	 
	  <div className="board-row">  
		<Square value="7"/>  
		<Square value="8"/>  
		<Square value="9"/>  
	  </div>    
    </>  
  );  
}
```
you should see a grid of numbers again:
![](Pasted%20image%2020240608161336.png)

Your updated code should look like this:
```jsx
function Square({ value }) {
  return <button className="square">{value}</button>;
}

export default function Board() {  
  return (  
    <>  
	  <div className="board-row">  
		<Square value="1" />  
		<Square value="2" />  
		<Square value="3" />  
	  </div>  
	  <div className="board-row">  
		<Square value="4" />  
		<Square value="5" />  
		<Square value="6" />  
	  </div>  	 
	  <div className="board-row">  
		<Square value="7" />  
		<Square value="8" />  
		<Square value="9" />  
	  </div>    
    </>  
  );  
}
```

### Making an interactive component
- Let’s fill the `Square` component with an `X` when you click it. Declare a function called `handleClick` inside of the `Square`. Then, add `onClick` to the props of the button JSX element returned from the `Square`:  
```jsx
function Square({ value }) { 
// 定义一个点击处理函数
  function handleClick() {  
	console.log('clicked!');  
}  

  return ( 
  // 将点击处理函数关联到按钮的onClick属性 
    <button  
	  className="square"  
	  onClick={handleClick}  
    > 
	  {value}  
	</button>  
  );  
}
```
note：
- 当用户点击这个按钮时，React会触发`onClick`事件，并调用`handleClick`函数。
- `handleClick`函数执行后，会在控制台输出"clicked!"，表明按钮被点击了。
这个机制允许开发者在React组件中定义和处理用户交互事件，使组件具有交互性和动态行为。  
1. `handleClick`：
    
    - `handleClick`是一个定义在`Square`组件内部的函数。
    - 它的作用是在按钮被点击时执行一些操作，这里它只是简单地在控制台打印了"clicked!"。
    - 它是JavaScript中的一个普通函数，由开发者在组件内定义。
2. `onClick`：
    
    - `onClick`是React中用于处理点击事件的属性。
    - 它的作用是将点击事件与处理函数关联起来。当用户点击按钮时，React会调用与`onClick`属性关联的函数，在这个例子中就是`handleClick`。
    - `onClick`来自于React，它是React事件处理系统的一部分，与HTML中的`onclick`类似，但React的事件系统是合成事件（Synthetic Event），提供了跨浏览器的一致性。  


- As a next step, you want the Square component to “remember” that it got clicked, and fill it with an “X” mark. To “remember” things, components use _state_.

- React provides a special function called `useState` that you can call from your component to let it “remember” things. Let’s store the current value of the `Square` in state, and change it when the `Square` is clicked.

- Import `useState` at the top of the file. Remove the `value` prop from the `Square` component. Instead, add a new line at the start of the `Square` that calls `useState`. Have it return a state variable called `value`:
```jsx
import { useState } from 'react';

function Square() {
  const [value, setValue] = useState(null);

  function handleClick() {
  }
}
```
note:  
1. `useState`：
    
    - `useState` 是 React 中的一个 Hook，用于在函数组件中添加状态管理能力。
    - 它来自于 React 库，允许函数组件在不使用类组件的情况下管理状态。
    - `useState` 函数接受一个初始状态值作为参数，并返回一个包含状态值和更新状态值的数组。
2. `const [value, setValue] = useState(null);`：
    
    - 这行代码使用了解构赋值和 `useState` Hook。
    - `value` 是状态值，而 `setValue` 是更新状态值的函数。
    - 初始状态值为 `null`。
    - 当调用 `setValue` 函数时，`value` 的值会更新，并触发组件的重新渲染。

这段代码中的 `useState` 和 `const [value, setValue]` 使得 `Square` 组件具有了内部状态管理的能力，可以在用户与组件交互时更新其状态，并根据状态的变化重新渲染。  

- `value` stores the value 
- `setValue` is a function that can be used to change the value. 
- The `null` passed to `useState` is used as the initial value for this state variable, so `value` here starts off equal to `null`.

- The `Square` component no longer accepts props anymore bs it uses the useState hook to manage internal state, allowing the component to manage its own state internally without relying on external props.
- you’ll remove the `value` prop from all nine of the Square components created by the Board component:  
```jsx
// ...  

export default function Board() {  
  return (  
	<>  
	  <div className="board-row">  
		<Square />  
		<Square />  
		<Square />  
	  </div>  
	  <div className="board-row">  
		<Square />  
		<Square />  
		<Square />  
	  </div>  
	  <div className="board-row">  
		<Square />  
		<Square />  
		<Square />  
	  </div>  
	</>  
  );  
}
```

- Now you’ll change `Square` to display an “X” when clicked. Replace the `console.log("clicked!");` 
- event handler with `setValue('X');`. Now your `Square` component looks like this:  
```jsx
function Square() {  
  const [value, setValue] = useState(null);    

  function handleClick() {  
    setValue('X');  
}  

  return (  
	<button  
	  className="square"  
	  onClick={handleClick}  
    >  
      {value}  
	</button>  
  );  
}
```
- By calling this `set` function from an `onClick` handler, you’re telling React to re-render that `Square` whenever its `<button>` is clicked. After the update, the `Square`’s `value` will be `'X'`, so you’ll see the “X” on the game board. Click on any Square, and “X” should show up:
![](Pasted%20image%2020240608192442.png)

- Each Square has its own state: the `value` stored in each Square is completely independent of the others.
- When you call a `set` function in a component, React automatically updates the child components inside too.

After you’ve made the above changes, your code will look like this:
```jsx
import { useState } from "react";

function Square() {
  const [value, setValue] = useState(null);

  function handleClick() {
    setValue("x");
  }

  return (
    <
      button className="square" 
      onClick={handleClick}
    >
      {value}
    </button>
  );
}
 
export default function Broad() {
  return (
    <>
      <div className="board-row">
        <Square />
        <Square />
        <Square />
      </div>
      <div className="board-row">
        <Square />
        <Square />
        <Square />
      </div>
      <div className="board-row">
        <Square />
        <Square />
        <Square />
      </div>
    </>
  );
}
```
从组件内部逻辑（Square）到外部结构（Board），逐步构建应用的整体结构，有助于保证代码的清晰和可维护性。
### React Developer Tools

### Lifting state up
Currently, each `Square` component maintains a part of the game’s state. To check for a winner in a tic-tac-toe game, the `Board` would need to somehow know the state of each of the 9 `Square` components.

- the best approach is to store the game’s state in the parent `Board` component instead of in each `Square`. The `Board` component can tell each `Square` what to display by passing a prop, like you did when you passed a number to each Square.
- **To collect data from multiple children, or to have two child components communicate with each other, declare the shared state in their parent component instead. The parent component can pass that state back down to the children via props. This keeps the child components in sync with each other and with their parent.**
- Lifting state into a parent component is common when React components are refactored.
- 
How would you approach that? At first, you might guess that the `Board` needs to “ask” each `Square` for that `Square`’s state. Although this approach is technically possible in React, we discourage it because the code becomes difficult to understand, susceptible to bugs, and hard to refactor.

- Edit the `Board` component so that it declares a state variable named `squares` that defaults to an array of 9 nulls corresponding to the 9 squares:  
```js
export default function Board() {
  const [squares, setSquares] = useState(Array(9).fill(null))
  return(
  //...
  );
}
```
- `Array(9).fill(null)` creates an array with nine elements and sets each of them to `null`. 
- The `useState()` call around it declares a `squares` state variable that’s initially set to that array. 
- Each entry in the array corresponds to the value of a square. When you fill the board in later, the `squares` array will look like this:
```jsx
['O', null, 'X', 'X', 'X', 'O', 'O', null, null]
```

- your `Board` component needs to pass the `value` prop down to each `Square` that it renders:  
```jsx
export default function board() {
  const [squares, setSquares] = useState(Array(9).fill(null));
  return (
    <>
      <div className="board-row">
        <square value={squares[0]} />
        <square value={squares[1]} />
        <square value={squares[2]} />
      </div>
      <div className="board-row">
        <square value={squares[3]} />
        <square value={squares[4]} />
        <square value={squares[5]} />
      </div>
      <div className="board-row">
        <square value={squares[6]} />
        <square value={squares[7]} />
        <square value={squares[8]} />
      </div>            
    </>   
  );
}
```

-  you’ll edit the `Square` component to receive the `value` prop from the Board component. 
- This will require removing the Square component’s own stateful tracking of `value` and the button’s `onClick` prop:
```jsx
import { useState } from "react";

function Square({ value }) {
  return <button className="square">{value}</button>;
}
  
export default function board() {
  const [squares, setSquares] = useState(Array(9).fill(null));
  return (
    <>
      <div className="board-row">
        <square value={squares[0]} />
        <square value={squares[1]} />
        <square value={squares[2]} />
      </div>
      <div className="board-row">
        <square value={squares[3]} />
        <square value={squares[4]} />
        <square value={squares[5]} />
      </div>
      <div className="board-row">
        <square value={squares[6]} />
        <square value={squares[7]} />
        <square value={squares[8]} />
      </div>            
    </>   
  );
}
```

- Each Square will now receive a `value` prop that will either be `'X'`, `'O'`, or `null` for empty squares.
- you need to change what happens when a `Square` is clicked. The `Board` component now maintains which squares are filled.
- You’ll need to create a way for the `Square` to update the `Board`’s state. Since state is private to a component that defines it, you cannot update the `Board`’s state directly from `Square`.

- you’ll pass down a function from the `Board` component to the `Square` component, and you’ll have `Square` call that function when a square is clicked.
- you’ll pass down a function from the `Board` component to the `Square` component, and you’ll have `Square` call that function when a square is clicked.
- You’ll call that function `onSquareClick`:  
note:指的是从 Board 组件传递给 Square 组件的函数。也就是说，当 Square 被点击时，Square 组件将调用传递给它的函数，这个函数被命名为 "onSquareClick"。
```jsx
function Square({ value }) {
  return (
    <button className="square" onClick={onSquareClick}>
      {value}
    </button>  
  );  
}
```

- you’ll add the `onSquareClick` function to the `Square` component’s props:
```jsx
function Square({ value, onSquareClick }) {
  return (
    <button className="square" onClick={onSquareClick}>
      {value}
    </button>  
  );
}
```

- Now you’ll connect the `onSquareClick` prop to a function in the `Board` component that you’ll name `handleClick`. 
- To connect `onSquareClick` to `handleClick` you’ll pass a function to the `onSquareClick` prop of the first `Square` component:
```jsx
export default function Board() {
  const [squares, setSquares] = useState(Array(9).fill(unll));

  return (
    <>
      <div className="board-row">
        <Square value={square[0]} onSquareClick={handleClick} />
        //...
    </>
  )
}
```

- you will define the `handleClick` function inside the Board component to update the `squares` array holding your board’s state:  
```jsx
export default function Board() {
  const [squares, setSquares] = useState(Array(9).fill(unll));

  function handleClick() {
    const nextSquares = square.slice();
    nextSquares[0] = "X"
    setSquares(nextSquares);
  }

  return (
  //...
  )
```
- The `handleClick` function creates a copy of the `squares` array (`nextSquares`) with the JavaScript `slice()` Array method.
- `handleClick` updates the `nextSquares` array to add `X` to the first (`[0]` index) square.
- Calling the `setSquares` function lets React know the state of the component has changed.
- This will trigger a re-render of the components that use the `squares` state (`Board`) as well as its child components (the `Square` components that make up the board).  
- Note:  JavaScript supports [closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures) which means an inner function (e.g. `handleClick`) has access to variables and functions defined in a outer function (e.g. `Board`). The `handleClick` function can read the `squares` state and call the `setSquares` method because they are both defined inside of the `Board` function.  

- Now you can add X’s to the board… but only to the upper left square.
- Your `handleClick` function is hardcoded to update the index for the upper left square (`0`).
- Let’s update `handleClick` to be able to update any square.
- Add an argument `i` to the `handleClick` function that takes the index of the square to update:
```jsx
export default function Board() {  
  const [squares, setSquares] = useState(Array(9).fill(null));  

  function handleClick(i) {  
    const nextSquares = squares.slice();  
    nextSquares[i] = "X";  
	setSquares(nextSquares);  
}  

  return (  
	// ...  
  )  
}
```

- Next, you will need to pass that `i` to `handleClick`.
- You could try to set the `onSquareClick` prop of square to be `handleClick(0)` directly in the JSX like this, but it won’t work:
```jsx
<square value={square[0]} onSquareClick={handleClick(0)} />
```
- Here is why this doesn’t work. The `handleClick(0)` call will be a part of rendering the board component.
- Because `handleClick(0)` alters the state of the board component by calling `setSquares`,your entire board component will be re-rendered again.
- But this runs `handleClick(0)` again, leading to an infinite loop:

- Note:Too many re-renders. React limits the number of renders to prevent an infinite loop.  



