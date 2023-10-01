在Vue中，权限管理通常涉及到以下几个方面：

1. 路由权限：通过vue-router的导航守卫，我们可以在跳转路由前进行权限检查，如果用户没有权限，我们可以重定向到错误页面或者登录页面。
    
2. 视图权限：在渲染视图时，我们可以使用v-if指令来根据用户的权限决定是否渲染某个视图。
    
3. 请求权限：在发送请求时，我们可以在请求拦截器中添加权限校验，如果用户没有权限，我们可以拒绝发送请求。
    

对于按钮级别的权限，我们可以使用自定义指令来实现。首先，我们可以创建一个权限列表，然后在自定义指令中检查用户是否具有该权限，如果用户没有权限，我们可以隐藏或禁用该按钮。

例如，我们可以创建一个权限指令如下：
```js
Vue.directive('permission', {
  inserted: function (el, binding) {
    const permissionList = store.state.user.permissionList
    if (!permissionList.includes(binding.value)) {
      el.parentNode.removeChild(el)
    }
  }
})
```
然后在模板中使用这个指令：
```html
<button v-permission="'edit'">编辑</button>
```
这样，只有当用户具有'edit'权限时，才会显示编辑按钮。
