### 当新入职一家公司时，如何快速搭建开发环境并让应用跑起来
先阅读公司提供的开发文档，安装代码编辑器、Node.js、Git等必要的软件，然后用Git克隆项目代码到本地，进入项目目录，使用包管理工具（如npm或yarn）安装项目依赖。根据项目需要，配置本地的环境变量。运行项目，项目运行后，了解项目文件结构及主要组件。

### 了解 React 中的 ErrorBoundary 吗，它有那些使用场景
ErrorBoundary是React 16中的一个功能，用于捕获UI中的JavaScript错误，展示备用UI，报告错误。
在一些大型应用中，组件比较复杂，不可避免就会有组件抛除意外错误，使用ErrorBoundary可以将不可预测的错误捕获，并向用户展示友好的降级 UI，而不是整个应用崩溃。
比如为支付页面、登录页面这些关键组件设置错误边界。确保即使其他组件出现错误，关键组件也能够正常工作。

### 有没有使用过 react hooks，它带来了那些便利
useState提供了在函数组件中管理本地状态的方式。
useEffect允许组件执行副作用操作，如数据获取、订阅或手动修改DOM。
useContext使得在函数组件中消费上下文更加方便。
useReducer常用于复杂组件中，或需要多个子组件共享状态的场景。

### 如何使用 react hooks 实现一个计数器的组件
用`useState`这个Hook来创建一个数字状态，这个数字就是计数器的当前值。然后，定义两个函数，一个用来加一，一个用来减一，这两个函数都会用到`setCount`来更新计数器状态。
用`useEffect`这个Hook来添加一些额外的功能，比如每次计数器更新后打印当前的计数值到控制台。`useEffect`只需要在计数器值变化的时候才运行，所以把它依赖的变量设置为计数器的值。
然后，只需要在组件里返回一个简单的界面，显示当前的计数值，并且放两个按钮，一个按钮绑上加一的函数，另一个绑上减一的函数。这样，每次点击按钮，计数器的值就会更新，界面也会跟着变化。
简单来说，就是用`useState`来保存计数器的状态，用`useEffect`来处理一些额外的事情，然后用函数来改变状态，并在界面上显示出来。

### React 中，cloneElement 与 createElement 各是什么，有什么区别
**createElement** 用来创建一个React元素。需要指定元素类型（标签名、组件名等）及属性和子元素。
**cloneElement** 是以一个已存在的元素为原型，创建该元素的一个副本，并可以添加/替换属性和子元素。
他们的区别是，createElement用于从零开始创建元素。
cloneElement用于修改或扩展一个已存在的元素（通常是通过另一个React元素返回的组件）。

### 使用 react 实现一个通用的 message 组件
创建一个通用的消息组件，它可以用来显示不同类型的消息（如提示信息、警告信息、错误信息等）。这个组件将会使用一些基本的样式，并且可以通过传递不同的props来定制其外观和行为。
`Message`组件接收两个props，type 和 children，
 `type`：默认为`info`，可以是`info`, `success`, `warning`, `error`中的任意一个，用来指定消息的类型。
`children`：实际要显示的消息文本。

### 如何使用 react hooks 实现 useFetch 请求数据
创建一个函数，它内部使用`useState`来管理请求的数据和加载状态，以及`useEffect`来执行数据获取。
使用`useState`来定义`data`、`loading`、和`error`这三个状态变量，分别用于存储获取到的数据、是否处于加载中的状态以及请求过程中可能发生的错误。
使用`useEffect`来监听URL和选项的变化，并在变化时执行数据获取逻辑。
在请求过程中设置`isLoading`为`true`，请求完成后（无论成功还是失败）将其设置为`false`。
处理请求可能发生的错误，并将错误信息存储在`error`状态中。
返回一个对象，包含了请求的数据、加载状态和错误信息。
接下来，在组件中使用这个Hook
通过`useFetch`获取数据，并根据请求的状态来显示不同的内容。如果正在加载数据，则显示“Loading...”。如果请求失败，则显示错误信息。如果请求成功，则显示获取到的数据。
### react 如何使用 render prop component 请求数据
使用render prop模式来请求数据是一种将数据获取逻辑与UI渲染逻辑分离的方法。Render prop组件会提供一个prop，通常命名为`render`或者`children`，这个prop是一个函数，可以在其中定义如何渲染组件。
创建一个`DataFetcher`组件，它会负责数据的获取，并通过一个prop传递给它的子组件：
可以在其他组件中使用`DataFetcher`，通过`render` prop来定义如何渲染数据：
`DataFetcher`组件负责发起网络请求，并管理数据、加载状态和错误状态。它接收一个`render` prop，这个prop是一个函数，接收当前的状态（`data`, `isLoading`, `error`）作为参数，并返回你希望渲染的JSX。
`MyComponent`使用`DataFetcher`，并提供一个函数来定义当数据加载完成时如何渲染。这个函数根据`DataFetcher`提供的状态来决定渲染什么内容。
这种方式的好处是将数据获取的逻辑与UI渲染逻辑分离，使得组件更加灵活和可重用。同时，它也支持更复杂的场景，比如在数据加载过程中显示加载指示器，或者在出现错误时显示错误信息。
### React Portal 有哪些使用场景
**弹出层**：如模态框，需要阻塞页面交互的元素。
**通知和提示**：在父级组件之外显示通知和提示。
**置顶样式**：创建置顶的样式效果，如全局提示条。
### 什么是 virtual DOM，它的引入带了什么好处
虚拟DOM是一棵与真实DOM相对应的树形数据结构，是一个轻量级的JavaScript对象，在内存中模拟真实DOM，当应用程序的状态发生变化时，React会创建一个新的虚拟DOM树，并与之前的虚拟DOM树进行比较（这个过程称为“diffing”），然后计算出最小化变更所需的DOM操作，最终将这些变更应用到实际的DOM上。
### react 与 vue 数组中 key 的作用是什么
- **React和Vue**都使用`key`来唯一标识列表中的每个元素，助于框架在渲染列表时跟踪每个元素的身份。  
- 当列表发生变化时，React和Vue会使用`key`来识别哪些元素被添加、删除或移动，而不是重新渲染整个列表。    

- 两者都使用虚拟DOM来优化渲染过程，当列表发生变化时，框架会比较新旧虚拟DOM树。如果没有`key`，框架可能会错误地认为元素被重新排序或修改，从而导致不必要的DOM操作。  
- 通过使用`key`，React和Vue 可以准确地识别哪些元素发生了变化，从而只更新那些实际需要更新的部分。**最小化DOM操作**，提高了渲染效率。   

- React和Vue使用`key`能够正确地保持组件的状态，如果你有一个带有输入框的列表项，使用`key`可以确保在列表重新排序时，输入框中的内容不会丢失。 

- 如果没有为列表项提供唯一的`key`，列表项可能会被错误地重新排序，或者组件的状态可能会丢失。

- 在实践运行用中，通常使用数据库中的唯一ID作为`key`，而不是数组的索引。因为数组索引可能会在列表发生变化时改变，导致渲染问题。要**避免使用索引作为`key`**：除非列表项是静态的且不会改变顺序。
### react 中 ref 是干什么用的，有哪些使用场景
直接访问DOM元素或在组件中访问实例

使用场景：  
**管理焦点、文本选择或媒体播放**  
**触发动画**  
**测量DOM元素的尺寸和位置**   
**管理第三方库或插件**  
**访问子组件的方法或状态**  
### 如何使用 react/vue 实现一个 message API
- React 中实现 `message` API    
先创建 `Message` 组件，用于显示消息内容，这个组件可以接收消息文本、类型（如成功、错误、警告等）以及一个关闭回调函数。  
再创建一个 `MessageContainer` 组件，用于管理消息的显示和隐藏。这个组件将使用 React 的 `useState` 来管理消息列表。  
再创建一个 `message` API，用于在应用的任何地方显示消息。这个 API 可以是一个简单的函数，调用 `MessageContainer` 中的 `addMessage` 方法。  
最后在应用中使用 `message` API，只需要在应用的根组件中包裹 `MessageProvider`，然后在任何子组件中调用 `useMessage` 钩子来显示消息。   

-  Vue 中实现 `message` API  
先创建 `Message` 组件，用来显示消息内容。  
再创建 `MessageContainer` 组件，用于管理消息的显示和隐藏。
再创建 `message` API，用于在应用的任何地方显示消息。  
最后在应用中使用 `message` API，只需要在应用的根组件中包裹 `MessageContainer`，然后在任何子组件中调用 `useMessage` 方法来显示消息。  

总结：React和Vue中实现一个通用的 `message` API 都需要创建一个消息组件和一个管理消息状态的容器组件。通过这种方式，可以在应用的任何地方调用 `message` API 来显示提示信息。

### react hooks 中如何模拟 componentDidMount
在函数组件中，React Hooks可以使用 `useEffect` 钩子来模拟 `componentDidMount`。  
`useEffect`钩子用于处理副作用，如数据获取、订阅或手动更改React组件中的DOM。它在每次渲染后都会执行，但可以通过传递一个空的依赖数组`[]`来模拟`componentDidMount`的行为，即仅在组件挂载时执行一次。  

`componentDidMount`是类组件生命周期方法之一，用于在组件挂载（插入到DOM树中）后立即执行一些操作。
### 如果使用 SSR，可以在 created/componentWillMount 中访问 localStorage 吗
不可以，因为`localStorage`是浏览器提供的API，它允许你在用户的浏览器中存储数据对象，而服务器端并不具备浏览器的环境，因此无法访问这些API。

正确的做法是在组件挂载到客户端后，再访问`localStorage`。这可以通过条件渲染、自定义Hook或状态管理库来实现。这样可以确保代码只在浏览器环境中执行，避免在服务器端出现错误或安全问题。

### react hooks 如何替代或部分替代 redux 功能
1. **使用`useState`和`useReducer`进行状态管理**：分别适用于简单和复杂状态逻辑。  
2. **自定义Hooks实现跨组件状态共享**：提取状态逻辑以实现状态共享。   
3. **Context API结合Hooks**：构建轻量级状态管理解决方案，适用于中小型应用或特定模块。  
4. **使用状态管理库如Recoil或Zustand**：提供更简洁的API来管理状态。

### 如何实现一个 react hook，你有没有自己写过一个
实现自定义Hook的步骤如下：

1.**确定需求**：首先明确你想要复用的逻辑。例如，管理表单输入、跟踪窗口大小、处理异步数据等。

2.**使用内置 Hook**：在自定义Hook中使用React的内置Hook来实现所需的功能。

3.**暴露必要的接口**：通过返回值将状态和操作函数暴露给使用该Hook的组件。

示例：
1.**`useLocalStorage` Hook**：

- **初始化状态**：使用`useState`的函数式初始化方式，从`localStorage`中读取初始值。如果`localStorage`中没有对应的键，则使用提供的`initialValue`。
- **更新`localStorage`**：在`useEffect`中监听`state`的变化，每当`state`变化时，将新的状态序列化并保存到`localStorage`中。
- **错误处理**：在读取和写入`localStorage`时，加入了错误处理，以便在出现问题时记录错误日志。

2.**使用 Hook 的组件**：

- `MyComponent`使用`useLocalStorage`来管理`name`的状态。初始值为`张三`，并且当用户在输入框中输入新的名字时，`localStorage`中的值也会同步更新。

### 在 react/vue 中数组是否可以以在数组中的次序为 key
不推荐，数组中的`key`属性用于帮助框架识别每个元素的身份，从而高效地更新和渲染列表。
虽然在列表内容固定且渲染简单组件时（比如列表是静态的，不会重新排序、添加或删除项。
或者列表项的内容不会改变），使用索引作为key是可以接受的，但通常是不推荐。

1. **避免使用数组索引作为key**：  
- **重新排序问题**：可能导致不必要的DOM操作和组件重新挂载。  
- **添加/删除问题**：添加或删除项时，后续所有元素的key变化，引发不必要的更新。   

2. **推荐的key选择**：  
- **唯一且稳定的标识符**：如数据库ID，确保元素有唯一身份。   
- **稳定的唯一属性**：如果没有唯一ID，可以使用其他稳定的唯一属性。

### React 中 fiber 是用来做什么的
**Fiber**是React 16引入的一种新的协调（reconciliation）引擎，旨在提高React应用的性能和响应性。Fiber的主要目标是将React的协调过程分解为更小的单元，从而实现更细粒度的控制，包括任务调度、暂停、恢复和中止等操作。
Fiber 的主要作用：
1. 增量渲染（Incremental Rendering）
2. 任务调度（Task Scheduling）
3. 暂停、恢复和中止任务的能力 
4. 并发模式（Concurrent Mode）的支持
### React hooks 中 useCallback 的使用场景是什么
`useCallback` 是 React Hooks 中用于优化性能的一个钩子。它的主要作用是 **缓存一个函数**，确保在组件重新渲染时，只有在依赖项发生变化时才会生成新的函数实例。
使用场景：
避免子组件不必要的重新渲染、在依赖数组中使用函数、优化高阶组件（HOC）或渲染属性（Render Props）以及性能关键型组件

示例：
- 当你在父组件中定义一个函数并将其作为 prop 传递给子组件时，每次父组件重新渲染时，这个函数都会创建一个新的实例。这会导致子组件接收到新的 prop，从而触发子组件的重新渲染，即使子组件的其他 props 没有变化。
  使用 `useCallback` 可以确保只有在依赖项变化时，函数才会重新创建，从而避免不必要的子组件重新渲染。
- 在 `useEffect`、`useMemo` 或其他依赖数组中使用了函数时，使用 `useCallback` 可以确保这些函数的引用是稳定的，避免因为函数引用变化而导致不必要的副作用或重新计算。   
-  在使用高阶组件或渲染属性模式时，`useCallback` 可以帮助缓存传递给子组件的函数，避免因为函数引用变化而导致子组件重新渲染。  
- 在性能关键的组件中，减少不必要的重新渲染和计算是非常重要的。`useCallback` 可以通过缓存函数来优化性能，尤其是在函数被频繁调用或传递给多个子组件时。

### useEffect 中如何使用 async/await
在`useEffect`中使用`async/await`，需要通过内部定义`async`函数或使用IIFE来实现。这确保了`useEffect`的回调函数不会返回Promise，从而避免React的警告。

因为在React的`useEffect`钩子中使用`async/await`进行异步操作时，需要注意一些事项，因为`useEffect`的回调函数不能直接声明为`async`。这是因为`async`函数会返回一个隐式的Promise，而`useEffect`期望返回一个清理函数（可选）或`undefined`，而不是一个Promise。

可以
-  定义一个内部的 `async` 函数
-  使用立即执行的异步函数表达式（IIFE）
-  使用 `then` 链式调用

### react hooks 的原理是什么
React Hooks 通过提供一系列钩子函数，使得函数组件能够拥有状态、处理副作用和复用逻辑。其核心原理依赖于 Fiber 架构和调用顺序的严格管理。

React Hooks 是 React 16.8 引入的一种新特性，它允许我们在函数组件中使用状态和其他 React 特性，而无需编写类组件。  
在 Hooks 出现之前，函数组件（也称为无状态组件）只能用于展示数据，无法拥有自己的状态。Hooks 通过 `useState` 等钩子，使得函数组件能够拥有和管理自己的状态。  

 `useState` 的工作原理：

- **状态单元**：每个调用 `useState` 的地方都会创建一个独立的状态单元。React 通过调用顺序（调用链）来跟踪每个状态单元。
- **初始值和更新函数**：`useState` 返回一个包含当前状态值和更新函数的数组。例如，`const [count, setCount] = useState(0);`。
- **状态更新**：调用更新函数（如 `setCount`）会触发组件重新渲染，并使用最新的状态值。  

`useEffect` 来处理副作用，如数据获取、订阅、手动更改 DOM 等。`useEffect` 允许你在函数组件中执行副作用操作，并在必要时进行清理。

 `useEffect` 的工作原理：

- **副作用函数**：`useEffect` 接受一个函数作为参数，这个函数可以包含副作用逻辑。
- **依赖数组**：第二个参数是一个依赖数组，React 会根据这个数组来决定何时重新执行副作用函数。如果依赖数组为空，副作用函数只会在组件挂载和卸载时执行一次。
- **清理函数**：副作用函数可以返回一个清理函数，React 会在组件卸载或依赖项变化时调用这个清理函数。
  
 **Hooks 必须按相同的顺序在组件的每次渲染中被调用**。这意味着：

- **不要在条件语句、循环或嵌套函数中调用 Hooks**。这会导致 Hooks 的调用顺序不一致，从而引发错误。
- **React 通过调用顺序来跟踪每个 Hook 的状态**。例如，第一次调用 `useState` 对应第一个状态，第二次调用对应第二个状态，以此类推。  

React Hooks 的内部实现依赖于 **Fiber 架构**。Fiber 是 React 的协调引擎，它将组件的更新过程分解为更小的单元（称为 fibers），从而实现更细粒度的控制。

 **常见 Hooks 的实现机制**

- **`useState`**：管理组件的状态，返回当前状态和一个更新函数。
- **`useEffect`**：处理副作用，如数据获取、订阅等，接受一个副作用函数和一个依赖数组。
- **`useContext`**：访问 React 的 Context，返回当前 Context 的值。
- **`useReducer`**：类似于 Redux 的 reducer，用于管理复杂的状态逻辑。
- **`useCallback`**：缓存函数，避免不必要的重新创建。
- **`useMemo`**：缓存计算结果，避免不必要的重新计算。
### redux 解决什么问题，还有什么其他方案
Redux 是一个用于 JavaScript 应用的状态管理库，通常与 React 或其他视图层库一起使用。它主要解决的是在复杂应用中状态管理的难题。
Redux 通过引入集中式存储（Store）、Actions、Reducers 、 Dispatch 和Selectors等核心概念，来进行状态管理。

除了 Redux，还有其他一些状态管理方案，它们各自具有不同的特点和适用场景：
1. **MobX**：基于观察者模式，适合需要快速开发和灵活状态管理的中小型项目。
2. **Recoil**：Facebook 开发，专门为 React 设计，适合需要高性能和复杂数据流的应用。
3. **Vuex**：为 Vue.js 设计的状态管理库，与 Vue 的响应式系统紧密集成。
4. **Zustand**：轻量级库，基于 React Hooks，适合需要简单、高效状态管理的 React 项目。
5. **Context API + Hooks**：React 内置方案，适合简单到中等复杂度的 React 应用。 
6. **XState**：专注于状态机管理，适合需要复杂状态管理和状态机逻辑的应用。
7. **Apollo Client**：适合主要依赖于 GraphQL API 的应用，同时处理数据获取和本地状态管理。

Redux 的核心概念：

1.**Store**：一个集中式的存储，包含应用的所有状态。

2.**Actions**：描述状态变化的普通对象，必须有一个 `type` 属性。

3.**Reducers**：纯函数，接收当前状态和 action，返回新的状态。

4.**Dispatch**：用于分发 actions 到 store，从而触发状态更新。

5.**Selectors**：用于从 store 中提取特定的状态。
### 为什么不能在表达式里面定义 react hooks
在React中，不能在表达式里面定义Hooks
是因为React需要保证Hooks的调用顺序在组件的每次渲染中都保持一致。这是由于React通过调用顺序来跟踪每个Hook的状态和副作用。如果在表达式（如条件语句、循环或嵌套函数）内部定义Hooks，会导致调用顺序不一致，从而引发错误或不可预期的行为。
### redux 和 mobx 有什么不同
 **核心理念** 
- **Redux** 使用单一状态树和纯函数（Reducers）来管理状态，采用严格的单向数据流。
- **MobX** 基于响应式编程，使用可观察的状态和自动追踪的状态变化，允许直接修改状态。 
 **状态管理方式**
- **Redux** 强调状态的不可变性和纯函数Reducers，需要手动订阅状态变化。
- **MobX** 允许状态的可变性，自动追踪状态变化和依赖关系，执行副作用更灵活。 
 **API和使用方式** 
- **Redux** 有明确的Action Creators、Reducers和Store结构，通过react-redux库与React集成。 
- **MobX** 使用Observables、Actions和Reactions，通过mobx-react-lite库与React集成。 
 **性能** - **Redux** 由于不可变性可能带来性能开销，但可以通过选择器优化。
- **MobX** 通过细粒度的响应式更新提高性能，自动追踪减少手动管理订阅的开销。 
 **社区和生态系统**
- **Redux** 在React社区中非常流行，有庞大的生态系统和丰富的工具。
- **MobX** 社区相对较小，但逐渐受到关注，尤其在需要灵活状态管理的项目中。
 **适用场景** 
- **Redux** 适合大型、复杂应用，需要时间旅行调试或严格不可变性管理。
- **MobX** 适合中小型应用或快速开发项目，需要更灵活、可变的状态管理。
### 关于 React hooks 的 caputre value，以下输出多少
在`useEffect`中设置的定时器，由于闭包的特性，捕获了`count`的初始值。这意味着，无论`count`在组件的其他部分更新多少次，定时器内部的`count`值始终是第一次捕获的值，即初始值0。
为了解决这个问题，有两种方法：
- 使用 `useEffect` 的依赖数组，将`count`添加到`useEffect`的依赖数组中，这样每次`count`变化时，定时器都会被重新创建，从而捕获最新的`count`值。
- 使用函数式更新，如果不想重新创建定时器，可以使用函数式更新来确保回调函数使用最新的`count`值。

### 在 React 项目中 immutable 是优化性能的
是的，在React项目中，**不可变性（Immutability**是优化性能的一种重要策略，尤其是在使用像**Redux**这样的状态管理库或进行**浅层比较（Shallow Comparison**时，通过确保状态和props的不可变性，React可以更有效地判断何时需要重新渲染组件，从而提高应用的性能和响应性。还能带来其他好处，如简化状态管理和增强代码的可预测性。

不可变性如何优化React性能：
- **浅层比较（Shallow Comparison）**：
- **PureComponent 和 memo**：
- **Redux 中的不可变性**：
- **避免不必要的渲染**：

 实现不可变性的方法:
 使用展开运算符（Spread Operator）、
 不可变数据结构的库（如Immutable.js和Immer），
 以及函数式编程方法（如map, filter, reduce）来实现不可变性。

### 在 redux 中如何发送请求
在Redux中使用Redux Thunk中间件来处理异步请求。
安装中间件、配置Store、定义Action Types、创建异步Action Creators、编写Reducers处理动作，以及在组件中发起请求。

### 在 redux 中如何写一个记录状态变更的日志插件
创建一个记录状态变更的日志插件可以通过编写一个自定义中间件（Middleware）来实现。中间件允许你在Action被分发到Reducer之前、之后或前后执行一些自定义逻辑。在本例中，我们将创建一个中间件，用于在每次状态变更时记录日志。
创建一个日志中间件,
配置 Redux Store 使用中间件, 
可选：在生产环境中禁用日志中间件,

使用现成的第三方库，如`redux-logger`。这是一个功能强大的日志中间件，提供了更多的配置选项和功能。
- 安装 `redux-logger`：
-  配置 Store：  


什么是 Redux 中间件？
Redux中间件提供了一种第三方扩展点，用于拦截、修改或响应所有通过`dispatch`发送的Action。它在Action被分发到Reducer之前执行，允许你添加日志记录、异步处理等功能。
### React 在 setState 时发生了什么
在React中，`setState`（在类组件中）和`useState`（在函数组件中）是用于更新组件状态的主要方法。当调用这些方法时，React会执行一系列操作来更新UI并保持应用的一致性。

 类组件中的 `setState`
1.**调用 `setState`**时：
- React会将传入的状态更新请求放入一个更新队列中。

2.**批量更新（Batching）**：
- React会将多个状态更新请求进行批量处理，以优化性能。这意味着在一次事件处理过程中，多个`setState`调用可能会被合并，以减少重新渲染的次数。

3.**触发重新渲染（Reconciliation）**：
- 一旦状态更新完成，React会进入协调阶段，比较前后虚拟DOM的差异（Diffing）。
- React会生成一个新的虚拟DOM树，并将其与之前的虚拟DOM树进行比较，找出需要更新的部分。

4.**应用DOM更新**：

- 根据协调阶段的差异，React会计算出最小化的DOM操作集，并将其应用到真实的DOM上。这包括添加、删除或修改DOM节点。

5.**生命周期方法**：

- 在重新渲染过程中，相关的生命周期方法会被调用，例如`shouldComponentUpdate`、`componentDidUpdate`等。这些方法允许你在状态更新前后执行自定义逻辑。

6.**更新UI**：

- 最终，UI会根据新的状态进行更新，用户可以看到最新的界面变化。

### 函数组件中的 `useState`

1.**调用 `setState`（实际上是 `setState` 的替代品，如 `setCount`）**：
- 在函数组件中，使用`useState`返回的更新函数（如`setCount`）来更新状态。

2.**触发重新渲染**：
- 与类组件类似，调用更新函数会触发组件的重新渲染。React会重新执行函数组件的函数体，以生成新的虚拟DOM。

3.**状态更新**：
- `useState`钩子会返回最新的状态值，确保在重新渲染时组件能够访问到最新的状态。

4.**协调和DOM更新**：
- React会进行协调，比较前后虚拟DOM的差异，并应用必要的DOM更新。

5.**Hooks 的调用顺序**：
- 在函数组件中，Hooks（如`useState`、`useEffect`等）必须按照相同的顺序在每次渲染中被调用。React通过调用顺序来跟踪每个Hook的状态和副作用。
  
### 注意事项

- **异步更新**：
    - `setState`和`useState`的更新是异步的。这意味着在调用更新函数后，状态可能不会立即更新。如果需要在状态更新后执行某些操作，可以使用`componentDidUpdate`（类组件）或`useEffect`（函数组件）来监听状态变化。
- **函数式更新**：
    - 在某些情况下，使用函数式更新可以确保你获取到最新的状态。例如：
    ```jsx
        setCount(prevCount => prevCount + 1);
    ```
- **性能优化**：
    - 为了优化性能，避免在`render`方法或函数组件的函数体内进行昂贵的计算。可以使用`React.PureComponent`或`React.memo`来避免不必要的重新渲染。

### 如何设计一个UI组件库
明确UI组件库的目标和需求，看目标客户是内部使用还是开源，
看是用在web、移动端，还是特定框架（如React、Vue、Angular），
需要哪些类型的组件（基础组件、布局组件、表单组件、导航组件、数据展示组件等），
是遵循哪个设计系统（如Material Design、Ant Design），还是自定义风格，

**竞品分析**：研究现有的UI组件库（如Ant Design、Material-UI、Element UI等），了解它们的优缺点。
与团队成员或潜在用户沟通，收集他们对组件库的需求和期望。
选择适合的技术栈和框架。例如，如果目标是React，可以选择TypeScript、Rollup或Webpack作为打包工具。

**样式**：
定义组件库的设计原则，如一致性、可访问性、可定制性等。
制定详细的样式指南，包括颜色、字体、间距、布局等。
将组件分类，如基础组件（按钮、图标）、布局组件（栅格、容器）、表单组件（输入框、选择框）、导航组件（菜单、面包屑）、数据展示组件（表格、卡片）等。
为每个组件制定详细的设计规范，包括尺寸、状态（正常、悬停、激活、禁用）、交互行为等。

**组件结构**：
每个组件应具有单一的职责，避免功能过于复杂。
组件应易于组合和嵌套，以适应不同的使用场景。
提供足够的props和slots，让用户能够自定义组件的外观和行为。

 **类型检查**：使用TypeScript或其他类型检查工具，确保代码的类型安全。
 遵循一致的代码风格和命名规范，可以使用ESLint和Prettier进行代码格式化。
 为每个组件编写单元测试，确保其功能和行为的正确性。可以使用Jest、React Testing Library等工具。
 
使用CSS-in-JS解决方案（如Styled-Components、Emotion）来编写样式，方便样式的动态生成和主题定制。
如果使用CSS Modules，可以将样式与组件分离，增强样式的模块化和可维护性。
实现一个主题系统，让用户能够轻松地切换主题（如浅色模式、深色模式）

**语义化HTML**，提升组件的可访问性。
使用ARIA属性来增强组件的可访问性。
**键盘导航**：确保组件可以通过键盘进行操作。
### React 中的 dom diff 算法如何从 O(n3) 优化到 O(n) 的
React 的 DOM diff 算法，也称为协调算法（Reconciliation Algorithm），在早期实现中确实面临着较高的时间复杂度问题。最初的算法复杂度为 O(n^3)，这对于大规模的应用来说是不可接受的。为了优化性能，React 团队对算法进行了改进，使其复杂度降低到了 O(n)。

 从 O(n^3) 到 O(n) 的优化：
 1. **树级别的比较**：不再逐个比较所有节点，采用更高效的方式进行树级别比较。 
 2. **假设同层级下的元素类型不会改变**：如果元素类型变化，则直接替换整个子树。 
 3. **使用key属性**：通过key属性高效追踪和重用元素。当 React 比较两个树时，它首先根据 `key` 来判断哪些节点是可以复用的，提高算法效率。
 4. **双端比较策略**：在比较新旧两棵树的过程中，它是同时从头到尾及从尾到头比较节点，快速识别不变部分。 
 5. **Fiber架构的支持**：自 React 16 引入 Fiber 架构以来，React 能够中断和恢复渲染工作，提供更精细的控制粒度，支持异步渲染和优先级调度。

### 在 React 应用中如何排查性能问题
使用 React Developer Tools，可以帮助我分析组件的渲染时间和层级结构。
使用内置的 Profiler 功能，可以记录用户交互期间的渲染行为。
启用**Highlight Updates**，每当组件重新渲染时，页面上会高亮显示对应的区域，有助于发现不必要的重新渲染。

分析 Re-renders：
函数组件，可以使用 `React.memo` 来阻止不必要的重新渲染；
类组件，可以使用 `shouldComponentUpdate` 方法进行更精细的控制。

检查大型列表渲染：考虑以下优化策略：
- **虚拟滚动（Virtual Scrolling）**：仅渲染当前可见区域的数据项，而不是一次性加载所有数据。
- **Windowing**：类似于虚拟滚动的概念，但更具体地指只加载部分数据到DOM中，例如使用 `react-window` 或 `react-virtualized` 等库。

利用 Code Splitting:
通过动态导入（Dynamic Imports）实现代码分割，可以让应用按需加载所需的模块，减少初始加载时间。

使用 Web Vitals,衡量网页质量的核心指标集合，包括 Largest Contentful Paint (LCP), First Input Delay (FID), Cumulative Layout Shift (CLS) 等，帮助你了解用户的实际体验并针对性地优化。

集成如 Sentry、New Relic 或者 Datadog 等服务，持续监控生产环境下的性能表现，收集错误报告和性能指标，以便及时发现潜在的问题。

Lighthouse 测试,开源自动化工具，用于改进网页的质量。它可以运行针对性能、可访问性、SEO 等方面的审计，并给出改进建议。

### React 17.0 有什么变化
**无新特性发布**,它不会添加很多新的开发者可见的功能，而是专注于底层架构的改进。

**逐步升级支持**,允许在同一应用中同时使用 React 17 和旧版本的 React,这对于大型应用来说非常重要，因为它使得可以一部分一部分地迁移至新版本，而不需要一次性完成整个应用的升级。

**事件委托机制的更改**,不再将所有事件监听器附加到 `document` 上，而是直接附加到渲染 React 树的根 DOM 容器上。这一改变有助于解决某些与浏览器插件或其他脚本冲突的问题，并提高了与外部代码集成的能力。

**废弃不安全的生命周期方法警告**,React 17 加强了对不推荐使用的生命周期方法（如 `componentWillMount`, `componentWillReceiveProps`, 和 `componentWillUpdate`）的警告。鼓励开发者转向更安全的替代方案（例如 `getDerivedStateFromProps` 或者完全重构以使用 Hooks）。

**改进错误边界处理**,确保如果一个错误发生在事件处理器、效果（effects）、计时器或回调中，这个错误现在会被正确地传递给最近的错误边界（如果有的话），而不是默认情况下导致整个应用程序崩溃。

**其他小改进和修复**,对 JSX 转换的改进，使得编译后的代码更加简洁；以及一些针对特定场景下的 bug 修复。
### 现代框架如 React、Vue 相比原生开发有什么优势
1. **组件化开发**：复用性和模块化。
2. **虚拟DOM与高效的更新机制**：优化性能和减少手动操作DOM。
3. **双向数据绑定 vs 单向数据流**：Vue的双向绑定和React的单向数据流。 
4. **状态管理和响应式系统**：集中式状态管理和响应式编程。
5. **工具链和支持生态系统**：插件、工具和CLI工具。
### React/Vue 中的 router 实现原理如何
共同点
1. **HTML5 History API**：两者都依赖HTML5的History API（`pushState`, `replaceState`, `popstate`事件）来管理URL的变化，实现无刷新页面跳转。 
2. **路径匹配**：都通过定义的路由配置，匹配当前URL到相应的组件/视图。 
3. **组件渲染**：根据路由匹配结果，动态渲染对应的组件或视图。 
4. **导航控制**：提供编程式导航和声明式导航（如链接）的手段，以及管理浏览器历史记录的能力。

差异点
1. **路由配置**：React Router的路由配置通常更倾向于组件化和声明式，而Vue Router提供了更加灵活的配置方式，既可以是声明式的，也可以通过JavaScript配置路由。
2. **集成与响应式**：Vue Router与Vue框架的集成更紧密，可以更直接地利用Vue的响应式系统，例如通过`$route`对象访问路由信息。而React Router则更多地依赖React的Context和Hooks API来实现类似的功能。 
3. **导航守卫**：Vue Router提供了更为丰富和细粒度的导航守卫机制，包括全局守卫、路由独享守卫、组件内守卫等。React Router的导航守卫功能通常通过组件生命周期方法或Hooks实现。

### 在 SSR 项目中如何判断当前环境时服务器端还是浏览器端
1. **使用 `typeof window === 'undefined'`**：
- **优点**：简单有效，适用于大多数情况。
- **缺点**：需要谨慎使用，避免在服务器端访问 `window` 或 `document` 导致错误。
2. **使用环境变量**：
- **优点**：可以区分不同的运行环境，如生产环境和开发环境。
- **缺点**：需要正确设置和管理环境变量。
3. **使用框架提供的 API**：
- **优点**：与框架的其他功能紧密集成，简化开发。 
- **缺点**：依赖于特定框架的实现，可能不适用于其他项目。

### React.setState 是同步还是异步的
在React中，`setState`（在类组件中）和`useState`（在函数组件中）的更新行为在不同的上下文中表现不同。
- **异步更新**：在React的事件处理函数中，`setState`和`useState`的更新函数是异步的，React会批量处理多个状态更新以优化性能。
- **同步更新**：在非React事件处理函数（如`setTimeout`、`Promise`回调）中，`setState`和`useState`的更新函数可能表现为同步更新。
- **函数式更新**：为了确保基于前一个状态进行更新，应该使用函数式更新形式（如`setCount(prevCount => prevCount + 1)`）。

### 什么是服务器渲染 (SSR)
服务器渲染（Server-Side Rendering，SSR）是一种在服务器上生成完整的HTML页面并将其发送给客户端的技术。与之对应的客户端渲染（Client-Side Rendering，CSR）是在浏览器中通过JavaScript动态生成和操作DOM。
### 在 React 中如何实现代码分割 (code splitting)
使用 React.lazy 和 Suspense 实现懒加载组件

`React.lazy` 函数允许你定义一个动态导入作为常规组件一样渲染。结合 `Suspense` 组件，可以在加载新组件时显示一个备用 UI（例如加载指示器）。
如果使用 React Router，可以直接对路由配置中的组件应用懒加载。

除了通过 `React.lazy` 实现懒加载之外，你也可以手动创建异步加载的模块，并根据需要动态地加载它们。

### 在 React 中如何做好性能优化
1. **使用钩子（useMemo, useCallback, React.memo）**,来避免不必要的渲染和计算.
2. **使用代码分割（Code Splitting）和懒加载（Lazy Loading）,通过React.lazy和Suspense实现按需加载组件，而不是一次性加载所有资源，这有助于减少初始加载时间。
3. **服务器端渲染（SSR）和静态站点生成（SSG）**，更符合当前的Web开发趋势，特别是随着Jamstack架构的流行和静态网站生成器（如Next.js, Gatsby等）的广泛应用。
4. **虚拟滚动**：处理大量数据时，虚拟滚动技术的使用是一个重要的优化手段

### 在 React 中发现状态更新时卡顿，此时应该如何定位及优化
1. 使用 React Developer Tools 定位问题，使用内置的 Profiler 功能记录用户交互期间的渲染行为。
2. 如果某些组件在父组件的状态变化时被不必要地重新渲染了，可能会导致性能下降。
   对于函数组件，可以使用 `React.memo` 来包裹组件，避免不必要的重新渲染。
   类组件则可以继承自 `PureComponent`。
   **`useMemo` 和 `useCallback`**：利用这些 Hooks 可以缓存计算结果或回调函数，防止因父组件重新渲染而导致的子组件不必要的重新渲染。
3. 有时，复杂的计算或大量的 DOM 操作会导致渲染过程变慢。
- **懒加载组件**：使用 `React.lazy` 结合 `Suspense` 实现代码分割和按需加载，减少初始加载时间。  
- **虚拟滚动**：当处理大量数据时，考虑使用虚拟滚动技术（例如 react-window 或 react-virtualized），只渲染当前可见的部分内容。
4. （如 Redux、MobX），确保状态管理逻辑高效且必要。
- **最小化状态树的复杂度**：保持状态树尽可能简单和平坦，减少深层嵌套的状态结构。
- **选择合适的中间件**：比如在 Redux 中合理使用 `redux-thunk` 或者 `redux-saga` 来管理异步操作，避免不必要的同步阻塞。
5. 集成性能监控服务（如 Sentry, New Relic 或 Datadog），持续监控生产环境下的性能表现，收集错误报告和性能指标，以便及时发现潜在的问题。
6. Google 提供的 **Web Vitals** 是一组衡量网页质量的核心指标集合，包括 Largest Contentful Paint (LCP), First Input Delay (FID), Cumulative Layout Shift (CLS) 等，可以帮助你了解用户的实际体验并针对性地优化。
7. 运行 Google 的 **Lighthouse** 工具进行审计，它可以提供关于性能、可访问性、SEO 等方面的改进建议。
8. 对于频繁触发的事件（如滚动、鼠标移动），考虑使用节流（throttling）或防抖（debouncing）技术来限制事件处理器的调用频率。


### 当多次重复点击按钮时，以下三个 Heading 是如何渲染的
```
import React, { memo, useMemo, useState } from "react"; const Heading = memo(({ style, title }) => { console.log("Rendered:", title); return <h1 style={style}>{title}</h1>; }); export default function App() { const [count, setCount] = useState(0); const normalStyle = { backgroundColor: "teal", color: "white", }; const memoizedStyle = useMemo(() => { return { backgroundColor: "red", color: "white", }; }, []); return ( <> <button onClick={() => { setCount(count + 1); }} > Increment {count} </button> <Heading style={memoizedStyle} title="Memoized" /> <Heading style={normalStyle} title="Normal" /> <Heading title="React.memo Normal" /> </> ); }
```

- **第一个 `Heading`（带有 `memoizedStyle`）**：
    
    - 这个组件接收了一个通过 `useMemo` 创建的 `style` 对象，因为 `useMemo` 的依赖数组为空 (`[]`)，所以这个 `style` 对象在整个生命周期内都不会改变。
    - 因此，只要 `title` 不变，无论 `count` 如何变化，这个 `Heading` 组件都不会重新渲染，除非 `title` 被修改。
- **第二个 `Heading`（带有 `normalStyle`）**：
    
    - 每次 `App` 组件重新渲染时，都会重新计算 `normalStyle`，即使它的值没有实际变化。
    - 因为 `style` 是一个新的对象引用，即使内容相同，`Heading` 组件也会认为这是一个新的属性，并触发重新渲染。
- **第三个 `Heading`（没有传递 `style` 属性）**：
    
    - 只传递了 `title` 属性，且 `title` 值固定不变。
    - 由于 `React.memo` 的存在，只要 `title` 没有改变，即便父组件重新渲染，这个 `Heading` 组件也不会重新渲染。

### Javascript 数组中有那些方法可以改变自身，那些不可以

### 关于 setState 以下代码的输出

### React 中什么是合成事件

### 前端项目中有哪些副作用

### React/Vue 中受控组件与不受控组件的区别

### React 中监听 input 的 onChange 事件的原生事件是什么

### 在 React hooks 中如何模拟 forceUpdate

### React/Vue 中兄弟组件如何进行通信

### React.memo 中是如何实现性能优化的

### immer 的原理是什么，为什么它的性能更高

### React.useMemo 与 React.useCallback 是如何进行性能优化的

### 同一页面三个组件请求同一个 API 发送了三次请求，如何优化

### 如何优化 React 项目的性能

### useLayoutEffect 和 useEffect 有什么区别

### 在 React Hooks 中实现 usePreviouseValue 取上次渲染的值

### 在虚拟 DOM 中进行 diff 算法时，介绍当根据 key 对数组进行重用时的算法

### 在 react 中，以下父子组件的 useEffect/useLayoutEffect 顺序如何

### React18 有哪些新特性

### React19 有哪些新特性