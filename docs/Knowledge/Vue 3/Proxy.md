### 总结
`Proxy` 是一种ES6中的特性，可以理解成在目标对象之前架设一层“拦截”，外界对该对象的访问，都必须先通过这层拦截，因此提供了一种机制，可以对外界的访问进行过滤和改写。  
`Proxy` 这个词的原意是代理，用在这里表示由它来“代理”某些操作，可以译为“代理器”。

### 概念
Proxy是一种代理机制，可以在目标对象之前加一层“拦截”，来对外界的访问进行过滤和改写。可以理解为代理器，用于代理某些操作。
使用Proxy的核心优点是可以交由它来处理一些非核心逻辑，如读取或设置对象的某些属性前记录日志、设置对象的某些属性值前需要验证、某些属性的访问控制等。从而可以让对象只需关注于核心逻辑，达到关注点分离，降低对象复杂度等目的。[[1]](https://zhuanlan.zhihu.com/p/450344790)

### 定义
Proxy的构造函数接受两个参数，分别是target和handler。target表示要拦截的目标对象，handler是用来定制拦截行为的。

handler中有很多方法，这些方法都被称为捕获器，分别捕获对象不同的操作行为。以下是几个常用的捕获器：[[0]](https://juejin.cn/post/6975858843729264653)

-   get方法：拦截某个属性的读取操作，比如proxy.foo和proxy['foo']。
-   set方法：拦截某个属性的赋值操作，比如proxy.foo = 'bar'或proxy['foo'] = 'bar'。
-   has方法：拦截propKey in proxy的操作，返回一个布尔值。
-   deleteProperty方法：拦截delete proxy[propKey]的操作，返回一个布尔值。
-   apply方法：拦截函数的调用、call和apply操作。
-   construct方法：拦截new操作符。
-   getPrototypeOf方法：拦截获取对象原型。
-   setPrototypeOf方法：拦截设置对象原型。
-   defineProperty方法：拦截Object.defineProperty操作。
-   getOwnPropertyDescriptor方法：拦截Object.getOwnPropertyDescriptor操作。
-   isExtensible方法：拦截Object.isExtensible操作。
-   preventExtensions方法：拦截Object.preventExtensions操作。
-   getOwnPropertyNames方法：拦截Object.getOwnPropertyNames操作。
-   getOwnPropertySymbols方法：拦截Object.getOwnPropertySymbols操作。
-   ownKeys方法：拦截Object.keys操作。

Proxy提供了很多不同的捕获器方法，可以根据具体需求选择不同的方法来拦截不同的操作。[[0]](https://juejin.cn/post/6975858843729264653)

在使用Proxy时，如果直接操作目标对象，则会绕过代理定义的各种拦截行为，因此一般需要用代理对象来操作。[[0]](https://juejin.cn/post/6975858843729264653)

一个例子：
```js
var person = {
    name: "Alice"
};
var proxy = new Proxy(person, {
    set(target, propKey, value, receiver) {
        console.log(`设置 \${target} 的\${propKey} 属性，值为\${value}`);
        target[propKey] = value
    }
});        
proxy.age = 18
```

