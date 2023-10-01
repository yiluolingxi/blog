在Vue项目中，常见的目录结构如下：

```
.
├── public/                     # 静态资源如 logo 等
├── src/                        # 源代码
│   ├── assets/                 # 模块资源（由 webpack 处理）
│   ├── components/             # 全局 UI 组件
│   ├── views/                  # 所有页面
│   ├── router/                 # 路由
│   ├── store/                  # 全局 state 管理
│   ├── App.vue                 # 主应用组件
│   ├── main.js                 # 应用入口文件
├── .env                        # 环境变量
├── .gitignore                  # 忽略的文件
├── package.json                # 包说明文件
└── README.md                   # 项目说明文件
```

对于大型项目，我们需要更细致的划分结构和组件：

1. `src/components/`目录下可以按功能划分子目录，比如`Header/`、`Footer/`、`Sidebar/`等。
    
2. `src/views/`目录下可以按业务模块划分子目录，比如`User/`、`Product/`、`Order/`等。
    
3. 对于复杂的业务逻辑，可以使用`vuex`进行状态管理，`src/store/`目录下可以按模块划分子目录。
    
4. 对于复杂的路由配置，可以将路由配置拆分到`src/router/`目录下的多个文件中。
    
5. 对于大型项目，可能还需要`src/api/`目录来管理所有的API请求。
    
6. 对于复用性高的功能，可以抽象为插件或工具函数，放在`src/plugins/`或`src/utils/`目录下。
    

在划分组件时，我们通常会将组件划分为全局组件和业务组件。全局组件通常是一些通用的UI组件，如按钮、输入框、表格等，放在`src/components/`目录下。业务组件通常是一些和业务逻辑紧密相关的组件，放在`src/views/`目录下的对应业务模块目录中。