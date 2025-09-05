![](Pasted%20image%2020250905131436.png)![](Pasted%20image%2020250905132803.png)
![](Pasted%20image%2020250905132936.png)
![](Pasted%20image%2020250905133104.png)
 ![](Pasted%20image%2020250905151526.png)
 that can notify developers of any issues integrating their changes 
 when a repo evolves in small steps
 like this it prevents what's known as merge Hell
 imagine Mary you're back and developer builds a new API for your product
 
![](Pasted%20image%2020250905152138.png)

{
  "name": "devops",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "jest",
    "build": "webpack src/app.js -o public/bundle.js",
    "deploy": "firebase deploy --token \"$FIREBASE_TOKEN\" --only hosting"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "jest": "^25.1.0",
    "webpack": "^4.42.0",
    "webpack-cli": "^3.3.11"
  },
  "dependencies": {
    "firebase-tools": "^7.14.0",
    "terser": "^4.6.6"
  }
}
I have a node.js web app in order to deliver this out to my customers 
I need to run three commands test, build and deploy

![](Pasted%20image%2020250905135455.png)
![](Pasted%20image%2020250905161829.png)
name: Firebase Continuous Deployment

on:
  push:
    branches: [ master ]


jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@master
      - uses: actions/setup-node@master
        with:
          node-version: 12
      - run: npm ci
      - run: npm run build
      - uses: w9jds/firebase-action@master
        with:
          args: deploy --only hosting
        env:
          FIREBASE_TOKEN: ${{ secrets.FIREBASE_TOKEN }}
          
I can automate this entire process in the cloud by using a CI service like github actions
first I create a workflow
and then I tell it to run on every push to the master branch
the event triggers a job that runs on a Linux container in the cloud and we tell the container what to do as a series of steps
first it checks out the code in this github repo 
then sets up nodejs 
installs my dependencies 
and runs my tests 
build and deploy commands 
now anytime we commit code to the master branch in this repo it will run this workflow
if any of the steps fail, the bad software won't be delivered to our customers and will automatically know there's an issue that needs to be addressed at the end of the day
CI CD offers two main benefits it helps you automate things that would
otherwise have to be done manually by developers that will increase your velocity 
but it also detects small problems early before they can grow into major disasters
and that results in higher code quality this has been CI/CD or DevOps
![](deepseek_mermaid_20250905_264925.png)
**1. 事件触发 (Event Trigger)**
- `on every push to the master branch`：这是管道的**触发器**。任何推送到主分支的代码提交都会自动启动整个流程。这是一种非常常见的模式，确保了主分支的每次更新都经过验证。

**2. 环境准备 (Environment Preparation)**
- `run on a Linux container in the cloud`：这是 CI/CD 的**关键优势**之一。GitHub Actions 会为每次运行都提供一个**全新的、干净的、标准化**的虚拟环境（称为 Runner）。这保证了： 
    - **环境一致性**：不会出现“在我电脑上是好的”这种问题，因为每次测试和构建的环境完全相同。        
    - **隔离性**：不同项目的依赖不会相互冲突。    
    - **安全性**：在隔离的容器中运行代码更安全。    

**3. 执行步骤 (Execution Steps)**  
您定义的步骤是管道逻辑的核心：
- `checkout the code`：第一步，容器需要从仓库获取最新的代码。    
- `set up node.js`：配置项目所需的运行时环境。GitHub Actions 有丰富的预置操作，可以轻松安装任何版本的 Node.js、Java、Python 等。   
- `install my dependencies`：安装项目依赖（如 `npm install`）。这确保了所有需要的库都已就位。   
- `run my tests`：**这是持续集成的核心**。运行自动化测试套件，确保新代码没有破坏任何现有功能。   
- `build and deploy commands`：**这是持续部署/交付的核心**。将测试通过的代码编译、打包，并部署到服务器或发布环境。    

**4. 质量门禁 (Quality Gate)**
- `if any of the steps fail, the bad software won't be delivered`：这是**最重要的保障**。整个管道中的任何一步失败（比如测试用例失败、构建出错），后续步骤都会停止。这形成了一个**自动化的质量门禁**，防止有缺陷的代码交付给用户。  

**5. 即时反馈 (Immediate Feedback)**
- `automatically know there's an issue`：开发者会立即收到通知（邮件、Slack 消息等），知道这次提交导致了问题，可以立刻着手修复。这实现了快速的反馈循环。
### 总结的两大好处

1. **提高效率，增加开发速度 (Increase Velocity)**
    - 将重复性工作（测试、构建、部署）自动化，解放开发者，让他们专注于编写代码。    
    - 自动化流程远比手动操作更快、更可靠。     
2. **提前发现问题，提高代码质量 (Higher Code Quality)**    
    - “在问题变成重大灾难之前就发现它们”。这正是“左移”理念的体现——在开发的最早期阶段就进行质量和安全测试，其修复成本远低于在生产环境中发现问题。
### 关于“CI/CD or DevOps”

- **CI/CD** 是实现 **DevOps** 文化和实践的一系列**具体工具和流程**。    
- **DevOps** 是一种旨在打破开发（Development）和运维（Operations）之间隔阂的**文化、哲学和一套实践原则**。它强调自动化、协作和快速迭代。  
- 可以说，**CI/CD 是 DevOps 的技术基础和核心引擎**。没有自动化的 CI/CD 管道，就很难真正实践 DevOps。

![](Pasted%20image%2020250905164058.png)![](Pasted%20image%2020250905165853.png)
![](Pasted%20image%2020250905170208.png)