
[https://github.com/vuejs/vue-next](https://github.com/vuejs/vue-next)

最显著的变化是引入了 TypeScript。Vue 3 的源码主要分为以下几个部分：

1.  compiler-core`：编译器的核心部分，用于将 Vue 模板编译成渲染函数。如虚拟 DOM 的生成和渲染、组件的创建和更新、指令的解析和执行等。
2.  reactivity`：响应式系统的核心部分，用于实现数据的双向绑定。包括了数据劫持、依赖追踪、派发更新等功能。它定义了响应式数据的基本结构和方法。
3.  runtime-core`：Vue 运行时的核心部分，包括虚拟 DOM 的实现和渲染函数的执行。包括虚拟 DOM 的实现、组件的渲染逻辑、事件处理等。
4.  runtime-dom ：
5.  server-renderer``：用于服务器端渲染的相关代码。
6.  shared`：Vue 内部共享的一些工具函数和类型定义。包含了 Vue 3 中的一些共享代码，包括常量、错误类型、工具函数等。

一些辅助模块，如 compiler-core、compiler-dom 等，用于将模板编译成渲染函数或者将标记字符串解析成虚拟 DOM。
-  compiler-core``:  这个模块包含了 Vue 3 的编译器的核心代码，它将模板转换为渲染函数，以便在运行时进行渲染。
-  vue`: 这个文件是 Vue 3 的入口文件，它包含了一些全局的配置和方法，同时也导入了其他模块。

除了以上几个主要部分外，Vue 3 的源码还包括一些辅助工具和插件，例如`@vue/reactivity`、`@vue/runtime-core`、`@vue/server-renderer`等。这些工具和插件主要用于支持 Vue 3 的生态系统和构建过程。




Vue 3 的源码采用 TypeScript 编写，其中包括许多核心功能，例如虚拟 DOM、响应式系统、组件化等。

Vue 3 的源码是使用 TypeScript 编写的，其中包括了 Vue 3 的核心模块、编译器、响应式系统、虚拟 DOM 等重要模块。这些模块都是相互依赖的，构成了 Vue 3 的整个框架。

在源码中，可以看到 Vue 3 使用了新的响应式系统，即使用了 Proxy 对象来代替 Object.defineProperty，从而更好地支持动态添加和删除属性，并且避免了一些 Object.defineProperty 存在的限制。

此外，Vue 3 还引入了一些新的 API，例如 Composition API，用于更好地组织代码，提高代码的可读性和可维护性。Vue 3 的编译器也进行了重构，从而更好地支持了模板中的指令、组件和插槽等特性。