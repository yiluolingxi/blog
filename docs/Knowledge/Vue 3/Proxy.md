### 总结
`Proxy` 是一种ES6中的特性，可以理解成在目标对象之前架设一层“拦截”，外界对该对象的访问，都必须先通过这层拦截，  
因此提供了一种机制，可以对外界的访问进行过滤和改写。    
`Proxy` 这个词的原意是代理，用在这里表示由它来“代理”某些操作，可以译为“代理器”。  

在使用Proxy时，需要注意以下几点：      

-   Proxy的构造函数接受两个参数，分别是target和handler，两个参数的类型必须是object。  
-   Proxy的handler中有很多方法，根据具体需求选择不同的方法来拦截不同的操作。  
-   如果直接操作目标对象，则会绕过代理定义的各种拦截行为，因此一般需要用代理对象来操作。  

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

Proxy提供了很多不同的捕获器方法，可以根据具体需求选择不同的方法来拦截不同的操作。  


在使用Proxy时，如果直接操作目标对象，则会绕过代理定义的各种拦截行为，因此一般需要用代理对象来操作。  

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

通过以上例子，我们可以得出以下结论：  

-   代理对象不等于目标对象，他是目标对象的包装品。
-   目标对象既可以直接操作，也可以被代理对象操作，且两者相互关联。  

Proxy可以用于很多地方，比如Vue3数据响应式系统。     

---

### 追根究底

- 在使用Proxy时，如果直接操作目标对象，则会绕过代理定义的各种拦截行为，因此一般需要用代理对象来操作  

也就是说，我们无法通过代理对象来拦截这些操作。因此，我们一般使用代理对象来操作目标对象，这样就可以通过代理对象来拦截操作，并且对操作进行过滤和改写。举个例子，如果我们直接给目标对象的属性赋值，那么就不会触发代理对象中定义的set方法，而如果我们通过代理对象来给属性赋值，那么就会触发代理对象中定义的set方法，从而实现拦截和过滤操作。

当我们使用Proxy时，可以通过代理对象来拦截目标对象的操作，并对操作进行过滤和改写。举个例子，我们可以使用Proxy来实现一个简单的数据校验器，当我们给对象的属性赋值时，会先进行一些校验，如果校验通过，则将值赋给属性，否则抛出一个错误。以下是一个例子：  

```js
let validator = {
  set: function(obj, prop, value) {
    if (prop === 'age') {
      if (!Number.isInteger(value)) {
        throw new TypeError('Age is not an integer');
      }
      if (value < 0) {
        throw new TypeError('Age is invalid');
      }
    }
    obj[prop] = value;
  }
};
let person = new Proxy({}, validator);
person.age = 18;
console.log(person.age); // 18
person.age = '18'; // 抛出一个错误：Age is not an integer
person.age = -1; // 抛出一个错误：Age is invalid
```

在这个例子中，我们定义了一个validator对象，它是一个Proxy的handler，用来拦截目标对象的set操作。当我们给对象的age属性赋值时，会先进行一些校验，如果校验通过，则将值赋给属性，否则抛出一个错误。这样就可以确保对象的age属性只能是整数，并且不能小于0。


- 如果我们直接操作目标对象

在Proxy中，如果我们直接操作目标对象，就是指我们直接对目标对象进行赋值、调用方法等操作，而不是通过代理对象来进行操作。此时，我们无法通过代理对象来拦截这些操作，因为这些操作会直接绕过代理对象定义的各种拦截行为。以下是一个例子：  

```js
var target = {
    name: "Alice"
};
var proxy = new Proxy(target, {
    set(target, propKey, value, receiver) {
        console.log(`设置 \${target} 的\${propKey} 属性，值为\${value}`);
        target[propKey] = value
    }
});        
target.age = 18
```

上面的代码定义了一个 `person` 对象，然后创建了一个代理对象 `proxy`。这个代理对象通过 `new Proxy(target, handler)` 的方式创建，其中 `target` 参数是被代理的对象，也就是 `person` 对象，`handler` 参数是用来自定义代理行为的对象。

在 `handler` 中，我们定义了 `set` 方法，它会在代理对象设置属性值时被调用。方法中输出了一条设置属性的日志，并将属性值设置到了被代理的对象上。

最后，我们通过 `proxy.age = 18` 的方式向代理对象 `proxy` 中添加了 `age` 属性，并将其值设置为 `18`。此时，代理对象中的 `set` 方法被触发，输出了设置属性的日志，并将属性值设置到了被代理的对象 `person` 上。因此，最终 `person` 对象中也拥有了 `age` 属性。  

在这个例子中，我们直接给目标对象target的属性赋值，而不是通过代理对象proxy来操作，因此不会触发代理对象中定义的set方法，也就无法通过代理对象来拦截这个操作。   

需要注意的是，如果我们直接操作目标对象，可能会导致代理对象和目标对象不一致。因此，我们一般使用代理对象来操作目标对象，这样就可以通过代理对象来拦截操作，并且对操作进行过滤和改写。  


- 
```js
 console.log(`设置 \${target} 的\${propKey} 属性，值为\${value}`) 里面的反引号表示什么
```

这里使用的是模板字符串（Template literals），它们用反引号`` ` ``而不是单引号或双引号来包含文本。在模板字符串中，可以插入变量的值，使用 `${}` 语法将变量括起来。  
这样，在输出日志的时候，就可以直接将变量的值嵌入到字符串中。例如，上面代码中的模板字符串就可以根据属性的名称和值，动态地输出每一次设置属性的操作日志。  


- 
```js
    set(target, propKey, value, receiver) {
        console.log(`设置 \${target} 的\${propKey} 属性，值为\${value}`);
        target[propKey] = value
    }
```

上面这段代码定义了一个代理对象的 `handler` 对象，其中包含了一个 `set` 方法。`set` 方法是当代理对象设置属性值时被调用的回调函数。

`set` 方法接受四个参数：

-   `target`：被代理的目标对象。
-   `propKey`：要设置或修改的属性名称。
-   `value`：要设置或修改的属性值。
-   `receiver`：最初被调用的代理对象，通常是代理对象本身。

在上面的代码中，`set` 方法输出了一条日志，描述了正在设置的属性名称和值，然后将属性值设置到了被代理的目标对象上。这样，当代理对象设置属性值时，就会触发 `set` 方法，并在控制台输出一条日志。   

`propKey` 是代理对象中要设置或修改的属性名称，它作为 `set` 方法的第二个参数传入。

在上面的代码中，我们使用 `target[propKey] = value` 将属性值设置到了被代理的目标对象上。这行代码实际上是给被代理的目标对象动态添加一个新的属性，属性名由 `propKey` 决定，属性值由 `value` 决定。例如，在下面这个语句中：

```js
proxy.age = 18;
```

`propKey` 的值是 `age`，`value` 的值是 `18`。因此，代码会将 `18` 这个值赋给 `person` 对象的 `age` 属性。