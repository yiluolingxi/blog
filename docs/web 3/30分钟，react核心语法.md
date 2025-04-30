![](Pasted%20image%2020250212211144.png)

# 创建一个基于 React 的项目

## 一、创建 React 项目的两种方式

### 1.1 引入核心文件
- 直接引入核心库文件  
    示例：`react.js`
### 1.2 使用 React 脚手架（推荐方案）
- 通过官方脚手架工具创建项目  
    （项目中常用的还是直接通过脚手架的方式来创建）
#### 1.2.1 脚手架创建步骤演示
1. **开发环境准备**
    - 下载 Visual Studio Code（VS Code）   
2. **操作流程**
    - 打开终端  
        快捷键：<code>Ctrl + `</code>
    - 创建项目命令：
    ```bash
    npx create-react-app 项目英文名称
    ```  
   > 说明：`npx` 是 **npm**（Node Package Manager）的命令行工具，用于执行 npm 包中的可执行文件而无需全局安装，避免版本冲突 ，这时脚手架工具就会帮助我们进行项目的搭建以及项目依赖的安装，几分钟的时间，空格后再加项目名称

		示例：
    ```bash
    npx creat-react-app my-creat-app   
	```
    - 进入项目目录：
   ```bash
     cd 项目名
     ```
		示例：
	 ```bash
	 cd my-creat-app
	 ```
    - 启动项目：
	 ```bash
	 npm start
	 ```
    - 打开浏览器查看（可查看页面的呈现效果）
## 二、React 项目文件结构说明

![示意图](Pasted%20image%2020250215111315.png)
（根据附图补充说明）
```
my-react-app/
├── public/        # 静态资源
│   ├── index.html
│   └── favicon.ico
├── src/           # 核心代码目录
│   ├── App.js
│   ├── index.js
│   └── styles/
└── package.json   # 项目配置依赖
```
最重要的两个文件：
根文件：App.js
入口文件：index.js

[具体见：](obsidian://open?vault=blog&file=docs%2Fweb%203%2FReact%20%E9%A1%B9%E7%9B%AE%E4%B8%AD%E7%9A%84%E6%96%87%E4%BB%B6%E7%BB%93%E6%9E%84%E4%B8%8E%E8%B5%84%E6%BA%90%E7%AE%A1%E7%90%86)
### 2.1 核心目录

- **源码目录**：`src/`
- **静态资源**：`public/`
    
### 2.2 资源管理

- 开发代码集中存放在 `src` 目录
- 图片/字体等静态文件建议放在 `public` 目录
## 创建一个基于 react 的项目
### 创建 react 项目的两种方式
#### 引入核心文件
比如：react.js
#### 用 react 提供的脚手架
直接通过 react 提供的脚手架来进行项目的创建。（项目中常用的还是直接通过脚手架的方式来创建）
##### 通过脚手架来演示关键步骤：
- 下载 Visual Studio Code（VS Code）
- 打开终端 
```md
Ctrl + `
```
- 输入 npx create-react-app 项目英文名称 （ 空格后再加项目名称，`npx` 是 **npm**（Node Package Manager）的一个命令行工具。用于执行 **npm** 包中的可执行文件，而无需全局安装这些包，避免版本冲突，这时脚手架工具就会帮助我们进行项目的搭建以及项目依赖的安装，几分钟的时间）
  比如：npx creat-react-app my-creat-app
- cd 项目名 进入项目目录
  比如：cd my-creat-app
- 通过 npm start 启动项目
- 打开浏览器查看（可以查看页面的呈现效果）

### 演示 React 项目中的文件结构与资源管理
具体见：
![](Pasted%20image%2020250215111315.png)
- 源码放在 `src` 目录下
- `public` 目录下是一些静态资源
 



### 标签渲染
### 条件渲染

### 列表渲染
### 状态渲染
### 
### 
