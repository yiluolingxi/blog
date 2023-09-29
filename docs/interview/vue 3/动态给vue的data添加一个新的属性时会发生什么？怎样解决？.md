在Vue中，如果你在组件的`data`函数返回的对象之外动态添加一个新的属性，Vue将无法跟踪这个新属性的变化，也就是说，这个新属性不是响应式的。

这是因为Vue在初始化组件时，会遍历`data`函数返回的对象的所有属性，并使用Object.defineProperty将它们转换为getter/setter，以便于跟踪它们的变化。如果你在之后添加新的属性，Vue将无法跟踪这个新属性的变化。

解决这个问题的方法是使用Vue的`Vue.set`方法或者`this.$set`方法来添加新的属性。这两个方法都可以将新属性添加到响应式对象，并确保新属性也是响应式的。

例如：  
```js
this.$set(this.someObject, 'newProperty', 'newValue')
```
或者：  
```js
Vue.set(this.someObject, 'newProperty', 'newValue')
```
这样，`newProperty`就会成为响应式的，当它的值改变时，Vue将能够检测到这个变化，并更新视图。  

