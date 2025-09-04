# 2025 全栈工程师企业级技能学习清单：从 JavaScript 基础到高薪就业

## 一、学习路径总览与优先级

作为一名已有 JavaScript/HTML/CSS 基础的开发者，想要在 2025 年达到企业级开发水平，需要系统地构建全栈技能体系。根据当前招聘市场的关键词频率分析，我将为你设计一条高效的学习路径，确保投入产出比 (ROI) 最大化。

### 1.1 学习目标与价值定位

在 2025 年的就业市场中，全栈工程师的需求量持续增长，尤其是具备**React 生态**、**Node.js**、**云服务**和**Web3**技能的复合型人才。根据最新统计，掌握这些技能的开发者薪资水平比单一技能开发者高出 35% 以上。你的目标应该是：

1. 构建完整的全栈开发能力，能够独立完成从前端到后端、从开发到部署的全流程

2. 掌握企业级项目开发的最佳实践和架构设计

3. 培养解决复杂问题的能力和工程思维

4. 积累实际项目经验，打造高质量的项目组合

### 1.2 技能树优先级排序

根据岗位 JD 关键词频率分析，你的学习优先级应该是：

|   |   |   |   |
|---|---|---|---|
|优先级|技能领域|关键词及频率|学习时长预估|
|最高|前端框架 / 库|React(18)、Redux(8)、Next.js(4)|6-8 周|
|高|工具与自动化|TypeScript(15)、Git/GitLab(5)、Jest/Cypress(4)|4-5 周|
|高|后端 / 云服务|Node.js(10)、AWS(6)、Docker(6)|5-7 周|
|中|区块链相关|Web3(7)、Ethereum(3)、Solana(3)|3-4 周|
|中|其他|HTML/CSS(5)、RESTful API(4)、GraphQL(4)|3-4 周|
|低|设计系统与 UI|Tailwind CSS(3)、Figma(2)、Storybook(1)|2-3 周|

**学习策略建议**：

- 采用 "核心技能优先，逐步扩展" 的学习策略

- 将高频率关键词作为学习重点，低频率关键词作为补充

- 理论学习与实践项目同步进行

- 注重技术的实际应用和企业级最佳实践

## 二、前端框架与库学习路径

### 2.1 React 核心能力建设

React 是当前最流行的前端框架，在 2025 年的企业级开发中占据主导地位。你的 React 学习应该遵循以下路径：

#### 基础阶段（2-3 周）

1. **React 核心概念掌握**：

- 组件化开发模式与组件生命周期

- JSX 语法与渲染机制

- 状态管理与 Props 传递

- 事件处理与表单控制

2. **Hooks 系统学习**：

- useState、useEffect、useContext 等基础 Hooks

- 自定义 Hooks 的设计与实现

- 状态优化与性能提升技巧

3. **组件设计原则**：

- 单一职责原则与组件拆分

- 纯组件与有状态组件的应用场景

- 组件通信模式与设计模式

**学习资源推荐**：

- 《React.js Learning Path》（Frontend Masters 官方课程）

- 《React Roadmap: A Complete Guide (2025 Updated)》（GeeksforGeeks）

- 《Create a Front-End App with React》（Codecademy 官方教程）

#### 进阶阶段（2-3 周）

1. **React 性能优化**：

- 代码分割与动态导入（React.lazy 和 Suspense）

- 虚拟滚动与大数据列表优化（react-window）

- memoization 技术与 useMemo、useCallback

- 按需加载与延迟渲染策略

2. **状态管理进阶**：

- 复杂状态管理模式与设计

- 状态同步与一致性保证

- 状态持久化与服务器端状态管理

3. **现代 React 设计模式**：

- 容器组件与展示组件分离模式

- 高阶组件 (HOC) 与 Render Props

- 基于 Context 的轻量级状态管理

- 原子设计方法论与组件库构建

**学习资源推荐**：

- 《Modern React Design Patterns for 2025: Clean Code, Better Components》（2025 年最新文章）

- 《React JS Architecture Pattern: Implementation + Best Practices in 2025》（2025 年专业指南）

- 《React JS Architecture – The Complete Guide》（Intellipaat 官方文档）

#### 实战项目建议：

1. **构建企业级 Todo 应用**：

- 实现完整的 CRUD 功能

- 应用状态管理最佳实践

- 实现响应式设计与用户界面优化

- 添加测试用例与持续集成配置

2. **博客系统重构项目**：

- 将传统博客系统迁移至 React 框架

- 实现动态路由与页面预加载

- 集成评论系统与用户交互功能

- 应用 SEO 优化技术

### 2.2 Redux 与状态管理

Redux 虽然出现频率 (8) 低于 React，但仍然是企业级应用中不可或缺的状态管理工具。在 2025 年，Redux 的使用方式已经发生了变化，建议采用最新的 Redux Toolkit 进行开发。

#### 学习内容与路径：

1. **Redux 核心概念理解**：

- 单一数据源与状态树设计

- action、reducer 与 store 的工作原理

- 异步操作处理与副作用管理

2. **Redux Toolkit 实践**：

- configureStore 简化配置流程

- createSlice 自动生成 action 和 reducer

- 使用 createAsyncThunk 处理异步操作

- 选择器与规范化数据结构

3. **Redux 高级应用**：

- 状态持久化与数据缓存策略

- 模块化状态管理与代码组织

- 性能优化与中间件使用

**学习资源推荐**：

- 《Redux Fundamentals, Part 8: Modern Redux with Redux Toolkit》（Redux 官方教程）

- 《Redux Toolkit Setup with Next.js》（Redux 官方指南）

- 《React JS: TypeScript, Redux, RTK & Modern Web Dev 2025》（Udemy 专业课程）

#### 最佳实践建议：

- 仅在必要时使用 Redux，优先考虑上下文 API 或本地状态管理

- 使用 Redux Toolkit 代替传统 Redux，简化开发流程

- 遵循 "单一事实来源" 原则，避免状态碎片化

- 采用规范化数据结构，优化状态访问性能

### 2.3 Next.js 与服务器端渲染

Next.js 作为 React 的服务器端渲染框架，在 2025 年的企业级开发中应用广泛，特别是在需要高性能和 SEO 优化的项目中。

#### 学习内容与路径：

1. **Next.js 基础架构**：

- 文件系统路由与动态路由

- 页面与组件的组织方式

- 内置 CSS 支持与样式解决方案

2. **服务器端渲染 (SSR) 与静态站点生成 (SSG)**：

- 不同渲染模式的应用场景

- 数据获取方法 (getStaticProps、getServerSideProps)

- 混合渲染模式与动态内容处理

3. **Next.js 高级功能**：

- API 路由与服务端逻辑实现

- 中间件与请求处理

- 自定义 App 和 Document

- 环境变量与配置管理

4. **React Server Components**：

- Server Components 与 Client Components 的区别

- 服务端数据获取与处理优化

- 组件级数据获取与缓存策略

**学习资源推荐**：

- 《Best Practices for Scalable & Secure React + Node.js Apps in 2025》（Fullstack 官方指南）

- 《Advanced Next.js Techniques for Performance and DX in Large-Scale Apps》（GitHub 讨论区）

- 《Building APIs with Next.js》（Next.js 官方博客）

- 《React Server Components in Next.js 15: A Deep Dive》（DZone 专业文章）

#### 实战项目建议：

1. **构建企业级博客系统**：

- 使用 Next.js 实现 SSR/SSG 混合模式

- 集成评论系统与用户交互

- 实现 SEO 优化与性能监控

- 构建自定义 API 服务与数据接口

2. **电子商务产品展示平台**：

- 实现产品列表与详情页的动态路由

- 应用图片优化与懒加载技术

- 构建购物车与用户状态管理

- 实现国际化与多语言支持

## 三、工具与自动化学习路径

### 3.1 TypeScript 深度掌握

TypeScript 在 2025 年已成为企业级开发的标准配置，出现频率高达 15 次，是提升代码质量和可维护性的关键工具。

#### 学习内容与路径：

1. **TypeScript 基础语法**：

- 类型系统基础与类型标注

- 基本数据类型与复合类型

- 接口与类型别名

- 枚举与泛型基础

2. **TypeScript 高级特性**：

- 高级类型操作（联合类型、交叉类型、类型守卫）

- 条件类型与映射类型

- 装饰器与元编程

- 命名空间与模块系统

3. **TypeScript 在 React 中的应用**：

- React 组件的类型定义

- Props 与 State 的类型标注

- 自定义 Hook 的类型声明

- 表单与事件处理的类型安全

4. **全栈 TypeScript 实践**：

- 前后端类型共享与一致性

- 基于 TypeScript 的 API 模式定义

- 类型安全的 API 客户端生成

**学习资源推荐**：

- 《Mastering TypeScript - 2025 Edition》（Udemy 专业课程）

- 《TypeScript Bootcamp: Zero to Mastery》（Zero to Mastery 官方课程）

- 《TypeScript Masterclass 2025 Edition - React + NodeJS Project》（Udemy 高级课程）

- 《Fullstack TypeScript, v2 (feat. Zod)》（Frontend Masters 专业课程）

#### 学习策略建议：

- 采用渐进式迁移策略，逐步将 JavaScript 项目转换为 TypeScript

- 注重类型设计与接口定义的最佳实践

- 利用 TypeScript 的类型推断减少冗余代码

- 结合 ESLint 和 Prettier 进行代码格式化与质量控制

### 3.2 版本控制与协作工具

Git/GitLab 作为代码管理工具，在企业级开发中必不可少。你的学习重点应该是：

1. **Git 核心操作与工作流程**：

- 基本操作命令与工作区管理

- 分支策略与合并冲突解决

- 变基与交互式 Rebase

- 标签管理与版本发布

2. **Git 高级功能与最佳实践**：

- 子模块与子树集成

- 钩子脚本与自动化流程

- 补丁与暂存区管理

- 代码审查与协作流程

3. **GitLab/GitHub 集成与管理**：

- 远程仓库管理与权限控制

- CI/CD 集成与自动化测试

- 问题跟踪与项目管理集成

- 代码质量检查与静态分析

**学习资源推荐**：

- 《Documentation: Add Jest best practices》（GitLab 官方文档）

- 官方 Git 文档与教程

- GitLab/GitHub 官方文档与指南

#### 最佳实践建议：

- 遵循团队或行业标准的分支命名规范

- 使用有意义的提交信息，遵循 Conventional Commits 规范

- 定期清理未使用的分支和标签

- 采用功能分支工作流，避免直接在主分支上开发

### 3.3 测试与自动化工具

在 2025 年的企业级开发中，自动化测试已成为必备技能。根据关键词频率，Jest 和 Cypress 是主要的测试工具。

#### Jest 单元测试学习路径：

1. **Jest 基础配置与使用**：

- 测试用例编写与断言库

- 测试套件组织与执行

- 测试覆盖率分析与报告

2. **Jest 高级技巧**：

- 模拟函数与 Spy

- 异步测试处理

- 自定义匹配器与处理器

- 快照测试与 UI 组件测试

3. **Jest 最佳实践**：

- 保持测试小而专注

- 使用描述性测试名称

- 隔离测试与避免依赖

- 遵循 TDD 方法，先写测试后写代码

**学习资源推荐**：

- 《Best practices》（Tillitsdone 专业博客）

- 《Jest 30: Faster, Leaner, Better》（Jest 官方博客）

- 《Advanced Jest Techniques for Better Test Coverage in 2025》（Toxigon 专业文章）

- 《Jest Techniques and Best Practices》（专业书籍）

#### Cypress 端到端测试学习路径：

1. **Cypress 基础架构与使用**：

- 测试环境配置与项目集成

- 基本命令与断言

- 页面元素定位与交互

2. **Cypress 高级功能**：

- 测试生成与 UI 覆盖

- 时间旅行与实时重载

- 视觉测试与组件测试

- 自定义命令与插件扩展

3. **Cypress 最佳实践**：

- 测试用例的可读性与维护性

- 测试数据管理与环境隔离

- 并行测试与 CI/CD 集成

- 测试失败分析与调试技巧

**学习资源推荐**：

- 《Add your missing tests faster, with Test Generation in UI Coverage》（Cypress 官方博客）

- 《Visual Testing in Cypress》（Cypress 官方文档）

- 《Scale your testing with confidence on every release》（Cypress 官方文档）

- 《Cypress Testing: The Complete Guide for 2025》（Katalon 专业指南）

#### 实战项目建议：

1. **为现有 React 应用添加全面测试**：

- 实现组件级单元测试

- 添加 API 服务测试

- 构建端到端测试套件

- 集成测试报告与覆盖率分析

2. **测试驱动开发 (TDD) 实践**：

- 选择一个小型项目，完全采用 TDD 方法开发

- 先编写测试用例，再实现功能

- 保持测试覆盖率在 90% 以上

- 定期进行测试重构与优化

## 四、后端与云服务学习路径

### 4.1 Node.js 企业级开发

Node.js 作为后端 JavaScript 运行环境，在 2025 年的企业级开发中仍然占据重要地位。你的学习路径应该是：

#### 基础阶段（2-3 周）：

1. **Node.js 核心模块与 API**：

- 事件循环与异步编程

- 文件系统操作与网络模块

- 流与缓冲区处理

- 子进程与多线程处理

2. **Express.js 框架基础**：

- 路由系统与中间件机制

- 请求与响应对象处理

- 模板引擎与视图渲染

- 错误处理与异常捕获

3. **数据库基础操作**：

- 关系型数据库 (MySQL/PostgreSQL) 连接与操作

- NoSQL 数据库 (MongoDB) 基础操作

- ORM 与查询构建器使用

**学习资源推荐**：

- 《nodejs-bootstrapper》（npm 官方包）

- 《Advanced NodeJS: Level up your NodeJS skill In 2025》（Udemy 专业课程）

- 《Node.js Best Practices and Security》（Tatvasoft 专业博客）

#### 进阶阶段（2-3 周）：

1. **Node.js 性能优化**：

- 使用 cluster 模块实现多进程

- 连接池与资源管理

- 内存管理与垃圾回收优化

- 性能监控与分析工具

2. **企业级 API 开发**：

- RESTful API 设计原则与最佳实践

- 输入验证与数据清洗

- 身份验证与授权机制

- 速率限制与安全防护

3. **服务端最佳实践**：

- 日志记录与监控

- 错误处理与恢复策略

- 配置管理与环境变量

- 健康检查与监控端点

**学习资源推荐**：

- 《Node.js in 2025: Modern Practices You Should Be Using》（Vibidsoft 专业博客）

- 《Node.js Ultimate Guide 2025: Use Cases, Real-Time App Building, & Tools》（IT Path Solutions 专业指南）

- 《Mastering Node.js: Best Practices for 2025》（Toxigon 专业文章）

#### 实战项目建议：

1. **构建 RESTful API 服务**：

- 实现完整的 CRUD 操作

- 添加身份验证与授权

- 实现输入验证与错误处理

- 添加 API 文档与 Swagger 集成

2. **实时聊天应用**：

- 使用 WebSocket 实现实时通信

- 消息持久化与历史记录

- 用户在线状态管理

- 通知与提醒功能

### 4.2 AWS 云服务学习路径

AWS 作为最流行的云服务平台，在企业级开发中应用广泛。你的学习路径应该是：

#### 基础阶段（2-3 周）：

1. **AWS 核心服务入门**：

- EC2 实例与计算服务

- S3 存储服务与对象存储

- RDS 关系型数据库服务

- VPC 虚拟私有云

2. **AWS 基础架构与网络**：

- 子网与路由表配置

- 安全组与网络 ACL

- 弹性 IP 与负载均衡

- 云监控与日志服务

3. **AWS 命令行工具与 SDK**：

- AWS CLI 安装与配置

- 使用 SDK 进行编程式访问

- 云 Formation 模板与基础设施即代码

**学习资源推荐**：

- 《AWS Roadmap: A Complete Guide (2025 Updated)》（GeeksforGeeks 专业指南）

- 《AWS Developer Center》（AWS 官方开发者中心）

- 《AWS re:Invent 2025 Topics》（AWS 官方活动页面）

#### 进阶阶段（2-3 周）：

1. **AWS 无服务器架构**：

- Lambda 函数与事件驱动架构

- API Gateway 与无服务器 API

- DynamoDB NoSQL 数据库

- SQS/SNS 消息队列与事件总线

2. **容器与微服务**：

- ECS 与 ECR 容器服务

- EKS Kubernetes 服务

- 容器化部署与 CI/CD 集成

- 服务网格与微服务架构

3. **安全与合规**：

- IAM 身份与访问管理

- 密钥管理服务 (KMS)

- 网络安全与合规性检查

- 加密与数据保护

**学习资源推荐**：

- 《AWS training and certification》（AWS 官方培训）

- 《AWS re:Invent 2025 Topics》（AWS 官方活动页面）

- 《Best practices for containers》（Google Cloud 官方文档）

#### 实战项目建议：

1. **无服务器博客系统**：

- 使用 Lambda 和 API Gateway 构建后端

- 使用 S3 和 CloudFront 实现静态网站托管

- 使用 DynamoDB 存储文章数据

- 集成 Cognito 实现用户认证

2. **容器化应用部署**：

- 使用 Docker 构建应用容器

- 使用 ECS/Fargate 进行容器编排

- 使用 CodePipeline 和 CodeBuild 实现 CI/CD

- 使用 CloudWatch 进行监控和日志分析

### 4.3 Docker 与容器化技术

Docker 作为容器化技术的代表，在 2025 年的企业级开发中应用广泛。你的学习路径应该是：

#### 学习内容与路径：

1. **Docker 基础与核心概念**：

- 容器与镜像的概念与区别

- Dockerfile 构建与镜像管理

- 容器生命周期管理与操作

- 数据卷与挂载机制

2. **Docker 高级功能**：

- 网络配置与端口映射

- 资源限制与性能优化

- Docker Compose 多容器编排

- 私有镜像仓库管理

3. **Docker 最佳实践**：

- 编写高效的 Dockerfile

- 层合并与镜像大小优化

- 使用官方基础镜像

- 避免在容器中存储敏感数据

- 不启动不必要的服务

4. **容器安全与维护**：

- 容器安全加固与最佳实践

- 漏洞扫描与安全检查

- 容器监控与日志管理

- 容器备份与恢复策略

**学习资源推荐**：

- 《build: optimize Dockerfile with layer consolidation and cache cleanup》（GitHub 官方 PR）

- 《StevenACoffman /Docker Best [Practices.md](http://Practices.md)》（GitHub 最佳实践文档）

- 《Dockerfile Best Practices: A Comprehensive Guide for 2025》（Support.tools 专业指南）

- 《Docker Best Practices for DevOps in 2025》（Toxigon 专业文章）

#### 实战项目建议：

1. **全栈应用容器化**：

- 将现有的 React+Node.js 应用进行容器化

- 使用 Docker Compose 定义多服务架构

- 配置 Nginx 作为反向代理

- 实现环境变量与配置管理

2. **微服务架构实践**：

- 将单体应用拆分为多个微服务

- 使用 Docker 进行每个微服务的封装

- 实现服务发现与负载均衡

- 构建完整的微服务部署流水线

## 五、区块链与 Web3 开发学习路径

### 5.1 Web3 基础与核心概念

Web3 作为新兴技术领域，在 2025 年的企业级开发中逐渐得到应用。你的学习路径应该是：

#### 学习内容与路径：

1. **区块链基础理论**：

- 区块链共识机制与分布式系统

- 加密算法与数字签名

- 智能合约基础与应用场景

- 去中心化应用 (DApp) 架构

2. **Web3.js 基础**：

- Web3.js 库的基本使用

- 与以太坊节点的交互

- 账户管理与交易签名

- 事件监听与日志解析

3. **智能合约开发基础**：

- Solidity 编程语言基础

- 智能合约结构与基本功能

- 代币标准 (ERC-20/ERC-721) 实现

- 智能合约部署与交互

**学习资源推荐**：

- 《How to Create Custom Smart Contracts and Integrate Them with Web3.js》（Moldstud 专业文章）

- 《Best Practices For Web3 Development》（[Restack.io](http://Restack.io) 专业指南）

- 《Best Practices for Developing with Web3.js》（[Codeofcode.org](https://Codeofcode.org)专业教程）

#### 最佳实践建议：

- 优先进行安全审计，防范漏洞

- 采用工具如 MythX 或 Slither 进行安全评估

- 遵循智能合约开发最佳实践

- 保持代码简洁，避免复杂逻辑

### 5.2 以太坊与 Solana 开发

根据关键词频率，以太坊和 Solana 是主要的区块链平台。你的学习重点应该是：

#### 以太坊开发学习路径：

1. **以太坊开发环境搭建**：

- 开发网络配置与测试节点

- 钱包集成与交互

- 交易处理与矿工费优化

- 区块浏览器与数据分析

2. **以太坊高级开发**：

- 高级智能合约功能与模式

- 预言机与外部数据集成

- 去中心化金融 (DeFi) 应用开发

- NFT 应用与市场平台开发

3. **以太坊生态系统**：

- 工具与框架 (Truffle/Hardhat)

- 钱包集成与认证

- 跨链通信与互操作性

**学习资源推荐**：

- 《Introduction》（Web3.js 官方文档）

- 《Best practices handbook》（Chainstack 官方文档）

- 《Future-proofing Ethereum》（Ethereum 官方文档）

#### Solana 开发学习路径：

1. **Solana 基础与工具链**：

- Solana 开发环境配置

- Solana 账户与交易模型

- 程序部署与调用

- Anchor 框架基础

2. **Solana 高级开发**：

- 并行处理与高性能计算

- 状态压缩与数据优化

- 租金系统与账户管理

- 跨程序调用与互操作性

3. **Solana 生态系统**：

- 钱包集成与认证

- 去中心化应用开发

- 去中心化交易所开发

**学习资源推荐**：

- 《Solana Changelog - Nov 12 - web3.js v2, skip preflights in the CLI, and SIMD-0191》（Solana Compass 专业文章）

- 《How to Start Building with the Solana Web3.js 2.0 SDK》（Helius.dev 专业教程）

#### 实战项目建议：

1. **简单代币发行与交易平台**：

- 实现 ERC-20 或 SPL 代币

- 构建代币交易界面

- 集成钱包功能

- 实现交易历史与余额查询

2. **去中心化博客系统**：

- 实现文章发布与存储

- 添加评论与互动功能

- 实现内容不可篡改性

- 构建简单的打赏系统

### 5.3 安全与最佳实践

在 Web3 开发中，安全是至关重要的。你的学习重点应该是：

1. **智能合约安全**：

- 常见安全漏洞与防范措施

- 重入攻击与防御

- 整数溢出与下溢防护

- 权限控制与访问限制

2. **钱包安全与用户认证**：

- 助记词与私钥管理

- 多重签名与安全认证

- 双因素认证与交易确认

3. **安全开发最佳实践**：

- 代码审查与安全审计

- 使用静态分析工具

- 遵循安全开发标准与规范

- 测试与监控机制

**学习资源推荐**：

- 《How to Create Custom Smart Contracts and Integrate Them with Web3.js》（Moldstud 专业文章）

- 《Best Practices For Web3 Development》（[Restack.io](http://Restack.io) 专业指南）

- 《Best practices handbook》（Chainstack 官方文档）

#### 最佳实践建议：

- 永远不要信任外部输入，进行充分验证

- 避免在智能合约中使用自毁功能

- 遵循最小权限原则，限制合约访问

- 定期进行安全审计和漏洞扫描

- 保持软件和依赖库的更新

## 六、工具与自动化进阶

### 6.1 TypeScript 全栈集成

在 2025 年的企业级开发中，TypeScript 已成为全栈开发的首选语言。你的学习重点应该是：

1. **全栈类型安全**：

- 前后端类型共享机制

- API 模式定义与验证

- 使用 Zod 或 Yup 进行数据验证

- 类型安全的 API 客户端生成

2. **服务端 TypeScript 实践**：

- 使用 TypeScript 编写 Node.js 应用

- 类型安全的数据库操作

- 自定义类型与接口设计

- 错误处理与异常类型

3. **客户端 TypeScript 优化**：

- React 组件的类型定义

- 表单与用户输入处理

- 状态管理与类型安全

- 自定义 Hook 的类型定义

**学习资源推荐**：

- 《Fullstack TypeScript, v2 (feat. Zod)》（Frontend Masters 专业课程）

- 《TypeScript Foundations: Essentials for JavaScript Developers》（Pluralsight 专业课程）

- 《Mastering TypeScript - 2025 Edition》（Udemy 专业课程）

#### 最佳实践建议：

- 采用渐进式迁移策略，逐步将 JavaScript 代码转换为 TypeScript

- 使用严格模式，开启尽可能多的类型检查选项

- 定义清晰的接口和类型别名，提高代码可读性

- 使用类型断言时要谨慎，避免滥用

### 6.2 CI/CD 与持续集成

在企业级开发中，CI/CD 已成为标准实践。你的学习重点应该是：

1. **CI/CD 基础架构**：

- 持续集成流程与实践

- 自动化测试与构建流程

- 代码质量检查与静态分析

- 持续部署与发布流程

2. **主流 CI/CD 工具**：

- GitLab CI/CD 配置与使用

- GitHub Actions 工作流定义

- Jenkins 配置与管道脚本

- 环境变量与秘密管理

3. **高级 CI/CD 实践**：

- 多环境部署与蓝绿发布

- 自动化回滚与故障恢复

- 性能测试与负载测试集成

- 监控与报警集成

**学习资源推荐**：

- 《Jest Techniques and Best Practices》（Apple Books 专业书籍）

- 《Jest 30: Faster, Leaner, Better》（Jest 官方博客）

- 《Scale your testing with confidence on every release》（Cypress 官方文档）

#### 最佳实践建议：

- 保持构建快而轻，避免不必要的步骤

- 采用并行测试和缓存机制，加速构建过程

- 实现自动化的代码质量检查

- 监控 CI/CD 管道的性能和稳定性

- 记录和分析构建失败的原因，持续改进

### 6.3 性能监控与优化

在 2025 年的企业级开发中，性能监控与优化已成为必备技能。你的学习重点应该是：

1. **性能监控工具与指标**：

- 关键性能指标 (KPI) 与监控

- 页面加载时间与用户体验

- 内存使用与 CPU 利用率

- 网络请求与资源加载

2. **性能优化策略**：

- 代码优化与重构

- 资源压缩与缓存策略

- 懒加载与按需加载

- 服务器响应时间优化

3. **性能分析与诊断**：

- 使用浏览器开发者工具分析性能

- 服务端性能分析工具

- 火焰图与调用栈分析

- 内存泄漏检测与修复

**学习资源推荐**：

- 《Mastering Node.js: Best Practices for 2025》（Toxigon 专业文章）

- 《Jest Techniques and Best Practices》（Apple Books 专业书籍）

- 《Cypress Testing: The Complete Guide for 2025》（Katalon 专业指南）

#### 实战项目建议：

1. **应用性能优化项目**：

- 选择一个现有应用进行性能分析

- 识别性能瓶颈与问题点

- 实施优化策略并验证效果

- 建立性能监控与报警系统

2. **性能测试自动化**：

- 使用工具如 Lighthouse 进行自动化性能测试

- 集成性能测试到 CI/CD 流程

- 设置性能指标阈值与报警

- 定期生成性能报告与趋势分析

## 七、设计系统与 UI/UX

### 7.1 Tailwind CSS 实践

Tailwind CSS 作为新兴的 CSS 框架，在 2025 年的企业级开发中应用越来越广泛。你的学习重点应该是：

1. **Tailwind CSS 基础**：

- 安装与基本配置

- 核心概念与实用类

- 响应式设计与断点配置

- 自定义主题与样式扩展

2. **高级功能与最佳实践**：

- 变体与修饰符使用

- 自定义插件与指令

- 暗黑模式支持

- 与其他 CSS 解决方案的集成

3. **Tailwind CSS v4 新特性**：

- 新的字段大小实用程序

- 自动调整文本区域大小

- 性能优化与构建速度提升

- 简化的配置流程

**学习资源推荐**：

- 《You can build anything with Tailwind CSS.》（Tailwind CSS 官方展示）

- 《Tailwind CSS v4.0》（Tailwind CSS 官方博客）

- 《Studio》（Tailwind Plus 官方模板）

- 《Tailwind CSS templates and examples》（Vercel 官方模板）

#### 实战项目建议：

1. **企业官网重构**：

- 使用 Tailwind CSS 重构现有企业官网

- 实现响应式设计与多设备适配

- 添加交互效果与动画

- 构建自定义主题与品牌颜色

2. **电子商务产品展示页面**：

- 使用 Tailwind CSS 实现产品列表与详情页

- 实现筛选与排序功能

- 添加购物车与结账流程

- 构建自定义 UI 组件库

### 7.2 设计系统构建

在企业级开发中，设计系统已成为提升开发效率和保持 UI 一致性的关键。你的学习重点应该是：

1. **设计系统基础**：

- 设计系统的概念与价值

- 原子设计方法论

- 样式指南与组件库

- 品牌一致性与可访问性

2. **组件库开发**：

- 使用 Storybook 进行组件开发与文档化

- 基础组件与复合组件设计

- 组件状态与交互设计

- 主题与样式定制

3. **企业级设计系统实践**：

- 建立设计标记与样式指南

- 实现跨平台一致性

- 设计系统的版本管理与更新

- 设计系统与开发工作流程集成

**学习资源推荐**：

- 《Next.js Enterprise Boilerplate》（Vercel 官方模板）

- 《Tailwind CSS templates and examples》（Vercel 官方模板）

- 《Next.js Enterprise Boilerplate》（Vercel 官方模板）

#### 最佳实践建议：

- 从基础原子组件开始，逐步构建复合组件

- 使用 CSS 变量进行主题定制

- 遵循可访问性标准，确保组件的可用性

- 提供完整的文档和示例，降低使用门槛

- 建立明确的版本管理和更新机制

## 八、API 设计与集成

### 8.1 RESTful API 最佳实践

在 2025 年的企业级开发中，RESTful API 仍然是主流的 API 设计风格。你的学习重点应该是：

1. **RESTful API 设计原则**：

- 资源导向的 URL 设计

- 适当的 HTTP 方法使用

- 标准的 HTTP 状态码

- 资源命名与版本控制

2. **API 实现最佳实践**：

- 输入验证与数据清洗

- 错误处理与错误响应格式

- 分页与排序机制

- 过滤与搜索功能

3. **API 安全与性能**：

- 身份验证与授权机制

- 速率限制与防止滥用

- 缓存策略与性能优化

- 日志记录与监控

**学习资源推荐**：

- 《Developing REST APIs in Modern Java for Payment Systems (2025)》（LinkedIn 专业文章）

- 《Best Practices for Designing High-Performance REST APIs》（Medium 专业文章）

- 《REST API Best Practices》（Tatvasoft 专业博客）

#### 最佳实践建议：

- 使用 JSON 作为数据交换格式

- 保持 API 简单和可预测

- 优化 API 速度和效率

- 提供有意义的错误消息

- 保持文档更新

### 8.2 GraphQL 实践

GraphQL 作为 REST 的替代方案，在 2025 年的企业级开发中也有一定应用。你的学习重点应该是：

1. **GraphQL 基础**：

- 核心概念与架构

- 查询与变异操作

- 类型系统与模式定义

- 解析器与数据加载

2. **GraphQL 最佳实践**：

- 选择性数据获取

- 避免过度获取数据

- 分页与连接模式

- 模式设计与组织

3. **GraphQL 高级主题**：

- 订阅与实时数据

- 身份验证与授权

- 错误处理与扩展

- 与现有系统的集成

**学习资源推荐**：

- 《GraphQL API Design Best Practices: Building Flexible and Efficient APIs》（Ataiva 专业指南）

- 《Essential GraphQL Best Practices for Dedicated .NET Developers》（Moldstud 专业文章）

- 《3 New Apollo GraphQL Books Reshaping Development in 2025》（Bookauthority 专业书籍）

#### 最佳实践建议：

- 使用选择性数据获取，避免过度获取

- 定义精确的查询，与 UI 组件紧密对齐

- 有效利用缓存机制

- 实现适当的缓存策略

- 监控和优化 GraphQL 查询性能

### 8.3 API 版本控制与管理

在企业级开发中，API 版本控制是一项重要技能。你的学习重点应该是：

1. **版本控制策略**：

- URL 路径版本控制

- 查询参数版本控制

- 媒体类型版本控制

- 版本协商机制

2. **API 变更管理**：

- 向后兼容性保证

- 废弃策略与通知机制

- 版本共存与迁移路径

- 文档与变更日志

3. **API 管理工具**：

- API 网关与管理平台

- 监控与分析工具

- 速率限制与访问控制

- 开发者门户与文档生成

**学习资源推荐**：

- 《API Development Best Practices in Node.js - Key Questions Every Developer Should Know》（Moldstud 专业文章）

- 《Best Practices for Building Scalable APIs with Node.js》（GitHub 官方讨论）

- 《Build High-Performance REST APIs with Node.js & Express.js》（Codezup 专业文章）

#### 最佳实践建议：

- 从第一天起就进行 API 版本控制

- 实施版本控制以保持消费者的平稳过渡

- 提供清晰的迁移路径和文档

- 监控 API 使用情况和性能

- 及时处理废弃和兼容性问题

## 九、综合项目实践与就业准备

### 9.1 全栈项目实战

在完成各个技能模块的学习后，你需要通过实际项目来整合所学知识。以下是几个推荐的项目方向：

#### 企业级博客平台（全栈项目）

技术栈：React + Next.js + Node.js + TypeScript + Tailwind CSS + AWS

项目目标：

- 实现完整的博客功能，包括文章发布、评论、分类等

- 使用 Next.js 实现 SSR/SSG 混合模式

- 构建 RESTful API 服务

- 实现用户认证与授权

- 使用 Docker 进行容器化部署

- 集成 CI/CD 流程

- 实现性能监控与日志分析

#### 去中心化金融应用（Web3 项目）

技术栈：React + Solidity + Web3.js + Ethereum/Solana + Tailwind CSS

项目目标：

- 构建基本的 DeFi 应用，如借贷或交易平台

- 实现智能合约与前端交互

- 集成钱包功能

- 实现代币交易与流动性池

- 构建 NFT 市场功能

- 实现安全审计与漏洞检测

#### 微服务架构电商平台（云原生项目）

技术栈：React + Node.js + TypeScript + Docker + Kubernetes + AWS

项目目标：

- 将单体电商应用拆分为多个微服务

- 使用 Docker 进行容器化

- 使用 Kubernetes 进行集群管理

- 构建 API 网关与服务发现

- 实现分布式事务与数据一致性

- 构建完整的 CI/CD 流水线

- 实现全链路监控与日志管理

### 9.2 就业准备与求职策略

在完成学习和项目实践后，你需要为求职做准备：

1. **简历优化**：

- 突出企业级开发经验

- 量化项目成果与贡献

- 强调全栈技能与技术广度

- 突出解决复杂问题的能力

2. **作品集准备**：

- 准备 3-5 个高质量的企业级项目

- 每个项目都要有明确的技术栈和解决的问题

- 展示从需求分析到上线的完整流程

- 突出技术挑战与解决方案

3. **面试准备**：

- 系统复习数据结构与算法

- 准备技术深度问题与场景题

- 练习白板编程与代码审查

- 准备项目讲解与技术细节

4. **求职渠道与策略**：

- 关注头部互联网公司与创业公司的招聘信息

- 通过 LinkedIn 等平台建立专业人脉

- 参与开源项目，提升技术影响力

- 参加技术社区与线下活动

### 9.3 持续学习与职业发展

在 2025 年的技术环境中，持续学习已成为职业发展的必要条件：

1. **技术趋势跟踪**：

- 关注行业前沿技术与发展趋势

- 订阅技术博客与新闻简报

- 参加技术会议与线上峰会

- 加入专业技术社区与论坛

2. **专业方向深化**：

- 根据个人兴趣与市场需求，选择 1-2 个技术方向深入研究

- 参与开源项目或发表技术文章

- 考取相关技术认证

- 尝试技术布道与知识分享

3. **软技能提升**：

- 团队协作与沟通能力

- 项目管理与时间管理

- 需求分析与产品思维

- 演讲与表达能力

## 十、学习计划与时间表

### 10.1 3 个月快速通道（高强度学习）

如果你有足够的时间和精力，可以采用以下 3 个月高强度学习计划：

|   |   |   |
|---|---|---|
|阶段|时间|学习重点|
|第一阶段|第 1-2 周|React 核心概念与基础应用|
||第 3-4 周|React 进阶与状态管理|
||第 5 周|Next.js 基础与 SSR|
|第二阶段|第 6-7 周|Node.js 基础与 Express 框架|
||第 8 周|数据库操作与 API 开发|
||第 9 周|AWS 基础与云服务|
|第三阶段|第 10 周|Docker 与容器化技术|
||第 11 周|自动化测试与 CI/CD|
||第 12 周|综合项目实践与就业准备|

### 10.2 6 个月系统学习路径

如果你希望更系统、更深入地学习，可以采用以下 6 个月学习计划：

|   |   |   |
|---|---|---|
|阶段|时间|学习重点|
|第一阶段|第 1-2 个月|React 生态系统深入学习|
|||React 核心概念与高级功能|
|||Redux 与状态管理|
|||Next.js 与服务器端渲染|
|第二阶段|第 3 个月|全栈开发基础|
|||Node.js 与 Express 框架|
|||RESTful API 设计与实现|
|||数据库操作与 ORM|
|第三阶段|第 4 个月|云服务与容器化|
|||AWS 核心服务与应用|
|||Docker 与容器化技术|
|||Kubernetes 基础与应用|
|第四阶段|第 5 个月|自动化与工具链|
|||TypeScript 全栈集成|
|||自动化测试与 CI/CD|
|||性能监控与优化|
|第五阶段|第 6 个月|前沿技术与综合实践|
|||Web3 与区块链开发基础|
|||GraphQL 与 API 设计|
|||企业级项目实践|
|||就业准备与求职策略|

### 10.3 学习方法与效率提升

为了提高学习效率，建议采用以下学习方法：

1. **项目驱动学习**：

- 每个知识点都通过实际项目来应用和巩固

- 从简单到复杂，逐步构建完整的项目

- 将学习的知识点融入到项目中

2. **刻意练习**：

- 针对薄弱环节进行专项练习

- 重复练习核心技能，形成肌肉记忆

- 尝试不同的解决方案，拓宽思维

3. **费曼学习法**：

- 尝试向他人解释所学知识

- 编写技术博客或教程

- 制作学习笔记与总结

4. **睡眠与休息管理**：

- 保持良好的作息习惯

- 采用番茄工作法提高效率

- 定期进行体育锻炼

- 保持学习热情与动力

## 总结与行动建议

在 2025 年的 IT 就业市场中，全栈工程师仍然是最受欢迎的角色之一。通过系统地学习本清单中的技能，你将能够：

1. 掌握企业级开发的核心技术栈

2. 具备全栈开发的综合能力

3. 适应快速变化的技术环境

4. 提升就业竞争力和薪资水平

**立即行动建议**：

1. 根据你的时间和兴趣，选择适合的学习路径（3 个月快速通道或 6 个月系统学习）

2. 制定详细的学习计划和每日任务

3. 立即开始学习 React 和 TypeScript 这两个核心技能

4. 每周至少完成一个小项目或实践练习

5. 加入技术社区，与其他学习者交流和分享

记住，学习编程是一个持续的过程，没有终点。保持好奇心和学习热情，不断探索和实践，你将在全栈开发的道路上取得成功。

最后，祝你在学习和职业发展的道路上一切顺利！

| company_name   | job_title                                                                      | post_date | salary_range                                           | benefits                                                                                                                                                                                                                                                                                      | location                            | experience_req                                                                                                                                                                                                                                                                                                                                                                                                                      | education_req | skills                                                                                                                                                                                                                                                                                                                                                                                 | job_description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | job_url                                                                                            |
|:---------------|:-------------------------------------------------------------------------------|:----------|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| Zscaler        | Web3 Staff Software Development Engineer - (Frontend - ReactJS/Typescript)     | 2d ago    | 45k−100k estimated                                     | 各种健康计划；时间休假及病假计划；育儿假选项；退休选项；教育报销；办公室福利等                                                                                                                                                                                                                                                       | Remote                              | 超过5年前端开发经验，其中4年以上使用React Redux构建复杂状态管理的React应用；精通使用TypeScript和ES6+的React开发，所有生产应用均使用TypeScript；具备HTML、CSS、语义设计、性能优化和无障碍标准方面的专业知识；拥有创建高级高性能仪表板可视化经验；具备为复杂应用编写可靠测试以确保质量的经验                                                                                                                                                                                                                                                            | N/A           | Programming Language: JavaScript/TypeScript;                                                                                                                                                                                                                                                                                                                                           | 设计、开发和维护高性能、高弹性的用户界面（使用ReactJS）；与UX团队合作将设计转换为可访问、可重用的组件（使用设计系统）；与后端团队协作开发RESTful API；为团队成员提供技术支持和指导以解决复杂问题；审查代码并管理前端测试以确保最佳实践                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | https://web3.career/staff-software-development-engineer-frontend-reactjs-typescript-zscaler/109198 |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: ReactJS; React Redux;                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: Node.js; AWS（云服务）; GitLab CI/CD（持续集成/交付工具）; Docker（容器化工具）;                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: 设计系统;                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: 编写可靠测试以确保质量;                                                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 代码审查；前端测试管理；最佳实践实施;                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| RugsDotFun     | Senior Fullstack Engineer (FE Focus)                                           | N/A       | 100,000 USD - 240,000 USD                              | 单位数股权；具有协商空间的竞争性基本工资；有机会与小型高野心团队合作，未来几年将平台扩展为加密领域最大的娱乐公司之一                                                                                                                                                                                                                                    | Remote                              | 至少5年实时服务多人游戏开发经验；能应对模糊场景并协助产品/设计生命周期；对rugs.fun项目有真诚兴趣                                                                                                                                                                                                                                                                                                                                                                               | N/A           | 编程语言: JavaScript;                                                                                                                                                                                                                                                                                                                                                                      | 我们正在寻找一位世界级的全栈开发人员（前端方向），加入我们以实现扩展rugs.fun至服务数百万玩家、成长为在线娱乐平台的目标。要求对项目有真诚兴趣，至少5年实时服务多人游戏开发经验，擅长在各类框架中实现复杂动态动画，有Rive等动画设计工具经验优先，精通React、NodeJS、Kafka和Mongo，能应对模糊场景并协助产品/设计生命周期。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | https://applicantai.com/rugsdotfun/senior-fullstack-engineer-fe-focus/9907?ref=web3.career#apply   |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 框架/库: React;                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 工具/技术: NodeJS; Kafka; Mongo; Rive（动画设计工具）;                                                                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 设计系统: N/A;                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 测试: N/A;                                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 开发实践: N/A                                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Uniswaplabs    | Web3 Senior Frontend Engineer                                                  | 3d ago    | 210,000−232,000                                        | 公司支付的人事保险、医疗保险及视同受益人保险；健身补贴；雇主缴纳4%的401(k)计划；年度1500美元教育津贴；无限制且鼓励的休假；远程员工最高16周带薪育儿假；纽约总部远程员工居家办公设备补贴；纽约总部的每日午餐（所有福利需缴税并根据资格而定）                                                                                                                                                                  | 纽约或美国远程                             | 5年以上软件工程经验；至少3年React经验；深入理解现代客户端React应用程序架构；有用户端应用中组件库或设计团队合作经验；加分项：计算机科学学位                                                                                                                                                                                                                                                                                                                                                         | N/A           | Programming Language: TypeScript;                                                                                                                                                                                                                                                                                                                                                      | 负责构建下一代金融产品；获得现有网页产品套件的所有权，并影响未来产品的创建、设计和执行；确保交易界面、数据密集型分析页面、文档门户等多平台用户体验的一致性和高质量；快速从设计稿实现功能性UI元素（注重性能与可访问性）；判断何时创建抽象功能或一次性功能；确保组件功能完善、设计优雅、性能高效且支持移动端；掌握UI测试的实施时机与方法                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | https://web3.career/senior-frontend-engineer-uniswaplabs/73955                                     |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React;                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: ethers.js/web3.js;                                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: 创建设计系统或组件库;                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: React Hooks;                                                                                                                                                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| BitMEX         | 前端经理（营销与合规团队）                                                                  | N/A       | 105,000美元 - 110,000美元（预估）                              | 在家办公以平衡工作、家庭与个人生活；25天年假（含公共假期）及产假/陪产假/育儿假等；为员工及家属提供顶级全面的医疗/牙科/视力保险；职业发展津贴支持职业晋升；年度健康福利促进身心健康；跨国远程工作政策；团队建设与异地活动；家庭人寿保险保障。                                                                                                                                                                     | Remote                              | 8年以上计算机科学专业高级学位以上的专业经验；具备团队开发与管理/指导经验；精通NodeJS和React；有构建API（REST/WebSockets）和微服务经验；有头部CMS平台开发经验；擅长与产品经理及多业务方协作，能管理多个产品/概念的开发并将复杂数据驱动产品推向用户；具备与利益相关者高效沟通并达成共识的丰富经验；熟悉行业当前编码实践/设计模式/框架及部署测试自动化；有金融科技行业工作经验者优先。                                                                                                                                                                                                                        | 计算机科学专业高级学位以上 | Programming Language: JavaScript;                                                                                                                                                                                                                                                                                                                                                      | 管理4-5人工程师团队，培育高绩效文化，负责新成员招聘与指导；与团队共同承担实际任务，确保项目按时交付；与营销/合规部门、产品经理及其他技术部门协作，定义并监督面向零售及专业交易员的加密体验开发；主导产品开发相关技术计划，协同团队完成开发；与其他产品工程团队及技术部门合作建立工程最佳实践，持续推进技术与客户体验标准升级，提升全球顶级金融产品交付效率并树立行业新标杆。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | https://web3.career/front-end-manager-marketing-compliance-bitmex/106096                           |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React;                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: NodeJS; REST/WebSockets; Microservices; Headless CMS; 部署与测试自动化;                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: N/A;                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: 测试自动化;                                                                                                                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 行业编码实践; 设计模式; 工程最佳实践;                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Figure         | Staff Front-End Engineer                                                       | N/A       | 基本工资：138,000−172,000；年度奖金：25%（季度发放）；股权激励：RSU           | 综合医疗、视力和牙科保险（雇主全额支付员工及选定计划的家属保费）；公司HSA/FSA/育儿津贴/401k/通勤福利；雇主资助的人寿和残疾保险；11个法定假日及带薪休假计划；最多12周带薪家庭假；继续教育报销                                                                                                                                                                                       | Remote                              | 8年以上前端工程专业经验，理想情况下构建复杂、高吞吐量应用；有从设计到部署端到端领导项目的记录（快节奏环境）；深入理解性能分析、前端可观测性和浏览器渲染内部原理；有指导其他工程师并提升团队技术标准的经验；有与产品、设计、工程团队协作创建以用户为中心解决方案的经验；热衷于构建简洁、可扩展且可访问的UI；能应对模糊并在初创或高增长公司环境中推动项目                                                                                                                                                                                                                                                       | N/A           | Programming Language: JavaScript/TypeScript; HTML5/CSS3;                                                                                                                                                                                                                                                                                                                               | 主导设计和开发高性能React应用（交易体验和仪表盘）；构建可跨产品和团队扩展的复用UI组件和系统；与产品经理、设计师、后端工程师协作定义和执行关键产品计划；推动前端性能优化、安全性和可维护性；建立和维护代码质量、测试、文档和可访问性的最佳实践；领导大规模技术计划，主动识别架构挑战并提出可扩展解决方案；通过工具、CI/CD和内部库提升开发者体验；指导其他工程师并通过协作和技术领导影响工程文化                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | https://web3.career/staff-front-software-engineer-front-end-figure/108307                          |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React;                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: CI/CD; 加密钱包（WalletConnect/MetaMask/Ledger）；区块链客户端签名（EIP-712/ethers.js/web3.js）；前端基础设施（monorepos/模块联邦/微前端）;                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: Jest/Playwright/Cypress;                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: Storybook/Tailwind/Figma;                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 代码质量最佳实践；测试；文档；可访问性                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| SafeGlobal     | Web3 Senior Full Stack Developer (Frontend Expertise)                          | 10天前      | 122k−138k（估算）                                          | 居家办公预算（定制办公设备）；30天标准年假；个人教育与会议预算；创新星期五（周五下午自主研究/副业项目）；灵活工作时间（混合办公政策）                                                                                                                                                                                                                          | 德国柏林                                | 具备区块链开发经验（以太坊优先）；精通React & TypeScript前端技术；掌握NestJS、Node.js后端技能及安全最佳实践；能够设计可组合的TypeScript结构；熟悉开源工作流程                                                                                                                                                                                                                                                                                                                                 | N/A           | Programming Language: TypeScript/Node.js;                                                                                                                                                                                                                                                                                                                                              | 负责项目从研究到发布的全周期工程交付；开展技术研究并提出解决方案；主要使用前端React/TypeScript构建高质量、可扩展功能，同时参与后端（NestJS, Node.js）开发；实施全栈测试与质量保证实践；参与代码审查并支持跨团队知识共享；维护开发过程中的安全实践；与利益相关者协作以确保交付质量和进度；需具备区块链（以太坊优先）开发经验；精通React & TypeScript前端技术；掌握NestJS、Node.js后端技能及安全最佳实践；能够设计可组合的TypeScript结构；熟悉开源工作流程                                                                                                                                                                                                                                                                                                                                                                                                                                            | https://web3.career/senior-full-stack-developer-frontend-expertise-safeglobal/108134               |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React/NestJS;                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: 测试与质量保证实践;                                                                                                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 安全编码实践; 开源工作流程;                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: N/A;                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: N/A                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Gemini         | Web3 Senior Software Engineer, Trading (Frontend)                              | 16天前      | 基础薪资范围：纽约州、加利福尼亚州、华盛顿州为140,000 - 200,000美元；包含可变奖金及股权激励 | 竞争力起薪；可变年度奖金；长期激励（新员工股权激励）；全面健康计划；401K（公司匹配）；带薪育儿假；弹性休假                                                                                                                                                                                                                                       | 纽约州纽约市；华盛顿州西雅图市；佛罗里达州迈阿密市           | 至少6年前端开发经验，专注可扩展分布式系统的设计、开发与交付；具备分布式设计和开发经验；优秀的分析和概念技能，扎实的组织能力和细节关注度；善于沟通，注重精准和简洁；独立决策者，能基于领域专业知识果断行动；熟悉FIX、Websocket、REST、GraphQL等通信协议                                                                                                                                                                                                                                                                                             | N/A           | 编程语言：Golang/TypeScript；                                                                                                                                                                                                                                                                                                                                                                | 设计并实现满足OTC团队功能和业务需求的金融平台；大规模构建全球流动性网络覆盖全球主要金融中心；培养最佳实践并与工程团队协作构建应用程序；实现并推广经纪商平台的领域模型和架构；利用Gemini交易所、结算和托管技术组合中的关键软件系统和服务；需每周两次到岗（纽约、西雅图或迈阿密办公室），服务于机构OTC交易平台的实时交易环境，专注于全球买卖双方流动性网络的高速价格和价值流动。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | https://web3.career/senior-software-engineer-trading-frontend-gemini/107736                        |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 框架/库：React；                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 工具/技术：AWS（云服务）/Kubernetes（容器编排）；                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 开发实践：微服务架构设计；分布式系统设计与开发；通信协议（FIX/Websocket/REST/GraphQL）；                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 设计系统：N/A；                                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | 测试：N/A                                                                                                                                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Winnables      | Web3 Full Stack Developer (Front End Leaning)                                  | 16d ago   | 62k−70k                                                | Work From Home                                                                                                                                                                                                                                                                                | Remote - Europe Based               | 需要具备TypeScript和现代JavaScript的丰富经验；熟悉React和Next.js生态系统；有使用WebSockets构建实时应用的经验；具备Node.js后端开发经验；了解PostgreSQL和数据库设计；有响应式设计和移动优先开发经验；理解状态管理模式（优先考虑Zustand经验）；掌握Web安全基础知识（CSRF保护、安全认证流程、输入验证）；对游戏机制和交互用户体验有兴趣                                                                                                                                                                                                                              | N/A           | Programming Language: TypeScript;                                                                                                                                                                                                                                                                                                                                                      | 与设计师和产品负责人紧密协作，快速迭代新想法并直接影响全球玩家；将设计稿和产品概念转化为流畅、响应式的游戏界面、动画和流程；与设计师、产品负责人和区块链工程师协作，原型开发、发布和迭代新游戏或功能；持续测试、调试并优化跨设备和网络条件的性能；审查代码，分享最佳实践，维护小型代码库的整洁、安全和可扩展性；利用玩家反馈和分析优化现有功能并指导新功能从概念到发布；倡导可访问性和网页标准合规性，确保不同设备和能力的玩家获得优质体验；构建交互式迷你游戏，提供流畅响应的游戏玩法；创建实时多人功能和实时游戏机制；开发引人注目的开箱系统动画；开发完全链上且可证明公平的抽奖和彩票类游戏；实现Plinko等物理游戏，优化趣味性和平衡性；打造跨移动、平板和桌面完美运行的用户友好界面                                                                                                                                                                                                                                                                                                                                                              | https://web3.career/full-stack-developer-front-end-leaning-winnables/105877                        |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React; Next.js; Zustand; viem/wagmi;                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: WebSockets; REST; Node.js; PostgreSQL; Supabase; Redis; Docker（云服务和容器化）; GitHub; Grafana; PostHog; Figma;                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: Figma;                                                                                                                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: N/A;                                                                                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| travoom        | Web3 Senior Front-End Developer (Rust-Integrated / AWS)                        | 19d ago   | 87k−120k estimated                                     | Deferred compensation until funding closes; Equity and tokens upside                                                                                                                                                                                                                          | 500 W 2nd St, Austin, TX 78701, USA | 5+年专业前端开发经验（JavaScript/TypeScript ES6+）；精通React（或愿切换Vue/Angular）及生态（Hooks、Context、Redux/Zustand、RTK Query、Next.js/Remix SSR）；具备通过REST/gRPC/GraphQL与Rust后端（或强类型服务）集成的经验；熟悉AWS前端工作流（Cognito认证/SSO、API Gateway/AppSync API编排、S3+CloudFront静态资源边缘缓存、Amplify/CDK CI/CD流水线）；熟练使用现代工具链（Vite/Webpack构建、ESLint/Prettier代码检查、Storybook设计系统、Playwright/Cypress测试、GitHub Flow协作）；具备响应式设计、WCAG-2.1 AA无障碍、Lighthouse/CLS性能预算的UX敏感度；优秀的跨职能沟通与文档能力。 | N/A           | Programming Language: JavaScript/TypeScript ES6+;                                                                                                                                                                                                                                                                                                                                      | Own entire client-side stack from architecture to pixel-perfect delivery; Integrate with Rust micro-services backend and AWS-centric cloud environment; Collaborate with product/design/Rust backend engineers to deliver robust user experiences at scale; 具体职责：UI开发（40%）- 使用React（优先）或同类框架设计/开发/维护SPA/SSR前端功能，保障性能/可访问性/跨浏览器支持；Rust集成（20%）- 调用Rust后端的gRPC/REST/GraphQL API，建模复杂数据流，优化Protobuf/FlatBuffers/JSON序列化；AWS集成（15%）- 连接前端工作流至AWS服务（Cognito/S3/CloudFront/API Gateway/AppSync/GraphQL/Amplify/Lambda），通过GitHub Actions/CodeBuild/Amplify Hosting实现CI/CD自动化部署；架构与代码质量（15%）- 主导组件设计/状态管理模式/测试策略（Jest/Vitest+RTL/Cypress）及代码审查；DevOps协作（10%）- 与DevOps团队协作定义CDK/Terraform前端托管IaC，管理版本化工件及蓝绿/Canary部署。 | https://web3.career/senior-front-end-developer-rust-integrated-aws-travoom/107536                  |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React（preferred）; Vue/Angular（willingness to switch）; Next.js/Remix（SSR）; Redux/Zustand; RTK Query; Hooks; Context;                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: Vite/Webpack（构建工具）; ESLint/Prettier（代码检查）; Storybook（设计系统工具）; Playwright/Cypress（测试工具）; GitHub Flow（开发流程）; GitHub Actions/CodeBuild/Amplify Hosting（CI/CD工具）; Cognito（云服务-认证）; S3/CloudFront（云服务-静态资源）; API Gateway/AppSync（云服务-API编排）; Amplify/CDK（云服务-IaC）; CDK/Terraform（云服务-IaC）; Lambda（云服务-无服务器计算）; gRPC/REST/GraphQL（API协议）; Protobuf/FlatBuffers/JSON（序列化格式）; |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: Storybook;                                                                                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: Jest/Vitest + RTL/Cypress;                                                                                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 组件设计驱动; 状态管理优化; 测试策略制定; 代码审查机制; 蓝绿/Canary部署实践。                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Lazer          | Senior Front End Engineer - Crypto                                             | 20d ago   | 105k−120k                                              | 远程工作；工作/生活平衡；员工福利（医疗/牙科/视力保险，美国员工401k）；无限带薪休假（至少15天）；定期团队静修（近期目的地包括多米尼加共和国、坎昆、夏威夷）；PTO；401k；牙科保险                                                                                                                                                                                              | Canada                              | 具备6年以上现代Web应用用户界面及体验开发经验                                                                                                                                                                                                                                                                                                                                                                                                            | N/A           | Programming Language: JavaScript/TypeScript/Solidity;                                                                                                                                                                                                                                                                                                                                  | 嵌入客户团队设计和构建EVM/Solana生态的dApp用户界面；架构前端体验以集成现有智能合约和程序；领导前端架构及UX策略的客户技术讨论；指导客户工程团队现代前端实践和web3 UX模式；处理多链复杂性（钱包连接、网络切换、交易处理）；实验前沿web3工具并贡献开源前端库;                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | https://web3.career/senior-front-end-engineer-crypto-lazer/107454                                  |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React/Next.js/Ethers.js/Viem/Wagmi/RainbowKit (EVM)/@solana/web3.js/Solana Wallet Adapter (Solana);                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: React Native（移动开发框架）; web3 mobile SDKs（移动开发工具）;                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: Web3 design systems;                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 构建API并使用TypeScript调用；连接dApps与智能合约；处理钱包集成及交易流程；多链复杂场景处理（钱包连接、网络切换、交易处理）；实验前沿web3工具并贡献开源前端库;                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Phantom        | Growth & Engagement Frontend Engineer                                          | N/A       | 126k−150k estimated                                    | Competitive salary and equity; Comprehensive insurance (medical/dental/vision) — 100% covered; Stipend for ideal remote set-up; Flexible hours and supportive remote environment; Unlimited vacation; 401(k) retirement plan; Monthly wellness benefit; Weekly meal benefit; Global off-sites | Remote                              | 7+年前端开发经验；在高节奏环境（金融科技、消费者应用、SaaS）中构建生产级React应用（Web和/或React Native）的经验；有通过A/B测试、功能标记界面并基于指标快速迭代的成功记录                                                                                                                                                                                                                                                                                                                                 | N/A           | Programming Language: TypeScript/JavaScript;                                                                                                                                                                                                                                                                                                                                           | 负责用户增长功能（操作卡片、推荐流程、推送通知体验、Phantom Pro升级、入职优化）的设计、实现与优化；与产品、设计、后端团队合作将假设转化为可A/B测试的界面；构建可复用的组件库；为每个功能添加结构化事件（点击、展示、变体队列）并协作验证数据管道；优化首屏加载时间（<100ms）并保持生产错误率≤1%；参与前端值班轮换并及时排查问题（15分钟内响应）；与后端、产品、设计、数据团队紧密协作解决依赖、对齐API合同；主导代码审查、结对编程和知识分享（如Dojo）；要求精通React/React Native（含hooks、上下文、性能优化）；熟悉功能标记平台或自定义A/B框架；精通TypeScript、组件驱动开发和设计系统架构；具备前端性能调优（代码分割、懒加载、记忆化、构建优化）经验；掌握Segment/Mixpanel/Amplitude等实时分析工具集成；熟练使用Jest/Cypress/React Testing Library等测试框架及前端CI/CD流水线；具备数据驱动思维（提出假设-测量影响-快速迭代）、优秀沟通协作能力（适应跨职能团队和优先级变动）、强责任心（主动交付代码并监控影响）和指导能力（教练IC3级同事）                                                                                                                                                               |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React; React Native;                                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: 功能标记平台/自定义A/B框架；Segment/Mixpanel/Amplitude（分析工具）；Jest/Cypress/React Testing Library（测试框架）；CI/CD流水线；                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: React（及React Native）组件库；主题化设计系统；                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: Jest/Cypress/React Testing Library（单元/集成测试框架）；端到端（E2E）测试；                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 代码分割/懒加载/记忆化/构建优化等性能优化实践；功能标记与发布控制；数据驱动开发流程；A/B测试；代码审查与结对编程；实时数据分析集成                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Dydx           | Web3 Frontend Developer - Marketing Optimization (Part-Time Contract)          | 1mo ago   | 90k−100k                                               | Async; 灵活工作时间（欧洲工作时间内自主安排）； 完全远程岗位（偶尔团队协作）； 参与创新DeFi产品开发（处理数十亿美元规模）； 基于绩效和公司需求提供职位扩展机会                                                                                                                                                                                                        | Remote                              | 2+年专业前端开发经验                                                                                                                                                                                                                                                                                                                                                                                                                         | N/A           | Programming Language: HTML/CSS/JavaScript; Framework/Library: React/Redux; Tool/Technology: Tanstack Query（React Query）; Design systems: N/A; Tests: N/A; Development Practice: N/A                                                                                                                                                                                                    | Marketing-Driven Development: 实现支持营销活动的UI更新（横幅、弹窗、模态框、公告栏）; Content Management: 使用React/js更新主页和产品界面的文案及组件; Landing Page Development: 与设计团队协作创建视觉精美的落地页和活动模块; Analytics Integration: 集成追踪像素、UTM参数和数据分析工具以衡量活动效果; Quality Assurance: 与营销团队紧密合作，对时间敏感的变更进行质量检查和部署; Code Maintenance: 维护整洁、模块化且可复用的代码，满足业务增长需求                                                                                                                                                                                                                                                                                                                                                                                                  | https://web3.career/frontend-developer-marketing-optimization-part-time-contract-dydx/106718       |
| Coinbase       | Web3 Senior Software Engineer, Frontend - Developer Experience                 | 1个月前      | 180,625—212,000美元/年                                    | 医疗保险；牙科保险；视力保险；401(k)计划                                                                                                                                                                                                                                                                       | 远程（美国）                              | 至少2年使用React或类似框架构建现代数据丰富Web应用的经验；至少1年React应用开发经验；熟悉前端架构趋势及性能、安全、可用性最佳实践；熟悉产品与设计生命周期，能与设计师、工程师、产品经理紧密协作；能编写高质量、测试充分的代码                                                                                                                                                                                                                                                                                                               | N/A           | Programming Language: JavaScript/TypeScript; Golang;                                                                                                                                                                                                                                                                                                                                   | 负责Coinbase内部开发者平台（IDP）的前端体验；构建和维护与发布流水线、配置管理系统、资产管理系统、实时使用数据、质量评分和服务文档等基础设施产品集成的React组件和页面；与后端工程师、设计师和API发布者密切合作，设计帮助团队发布、发现和评估API的工作流程；提升数百名工程师日常使用的内工具的质量和设计；改进IDP UI的可访问性、性能和可靠性；与资深工程师、产品经理和产品设计师合作影响产品路线图和UX优先级；为Coinbase更广泛的设计系统和内部前端库做贡献                                                                                                                                                                                                                                                                                                                                                                                                                                                             | https://web3.career/senior-software-engineer-frontend-developer-experience-coinbase/106388         |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React; 内部前端库;                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: Docker（容器化服务）; GraphQL; NoSQL数据库;                                                                                                                                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: Coinbase内部设计系统;                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 前端架构最佳实践（性能、安全、可用性）; 与设计师/工程师/产品经理紧密协作的开发实践                                                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Coinbase       | Web3 软件工程师（前端，平台-基础设施）                                                         | 1个月前      | 154,000—154,000 加元/年                                   | 牙科保险；医疗保险；目标奖金；目标股权；医疗、牙科和视力福利                                                                                                                                                                                                                                                                | 远程（加拿大）                             | 主要要求：至少2年软件开发经验，使用JavaScript及现代组件化JS框架（如React）开发和发布用户端功能；                                                                                                                                                                                                                                                                                                                                                                           | N/A           | Programming Language: JavaScript;                                                                                                                                                                                                                                                                                                                                                      | 塑造下一代Risk Platform架构，支持Coinbase业务；制定并阐明维护和扩展Web及移动平台的长期技术方向和愿景；使用现代工具（如React、React Native、TypeScript、React Navigation、Jest和Webpack）构建简单、易理解、高性能且可靠的界面，提供可信赖的用户体验；每季度与工程师、产品经理和高级领导合作制定路线图；指导团队成员设计和编码标准；在会议中传递正能量，让同事感到被包容。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | https://web3.career/software-engineer-frontend-platform-infra-coinbase/106385                      |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     | 加分项：至少1年React Native移动应用开发经验，或有将现有原生应用迁移至React Native的经验                                                                                                                                                                                                                                                                                                                                                                            |               | Framework/Library: React; React Native;                                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: React Navigation（导航库）; Jest（测试工具）; Webpack（构建工具）;                                                                                                                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: N/A;                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: Jest;                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 前端架构设计（性能、安全性、可用性）；遵循产品与设计生命周期；与设计师、工程师、产品经理紧密协作                                                                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Alpaca         | Web3 Senior Frontend Engineer - Trading API                                    | 1mo ago   | 87k−117k（估计）                                           | 分布式团队；竞争性薪资及股票期权；健康福利；新员工居家办公设备一次性补贴500美元；每月通过Brex卡发放150美元津贴                                                                                                                                                                                                                                  | Remote                              | 5年以上前端开发经验（使用TypeScript/React）；优秀的沟通与协作能力；能将产品原型图转化为完整用户界面；精通TypeScript和React；精通HTML和CSS框架（如TailwindCSS）；热衷于创建直观且高性能的用户界面；熟悉REST APIs和WebSockets最佳实践；有制定或影响前端最佳实践的记录；注重细节并欣赏设计美学                                                                                                                                                                                                                                                    | N/A           | Programming Language: TypeScript;                                                                                                                                                                                                                                                                                                                                                      | 作为高级前端工程师，负责设计和维护构成Alpaca用户体验基础的前端应用程序，赋能数百万交易数十亿美元资产的用户；作为交易API团队成员，负责交易API客户的产品体验和开发，涵盖前端交易仪表盘和后端系统（支持高收益现金账户、模拟账户等功能）；与用户和内部利益相关者密切合作，交付全栈前端和后端系统的高质量端到端解决方案；需具备深厚前端专业知识，喜欢指导他人，适应好奇和持续改进的文化；在跨职能团队中协作，注重细节，构建优雅无缝的用户体验（关注美观、性能、响应性和可访问性）；参与架构和开发突破技术边界的Web应用；与跨职能团队合作创建响应式、高性能、直观的用户界面；负责高可见性功能/项目的交付（从设计到部署）；设计共享组件库并贡献设计系统；指导同行并影响公司技术战略。                                                                                                                                                                                                                                                                                                                                                             | https://web3.career/senior-frontend-engineer-trading-api-alpaca/106288                             |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React; TailwindCSS;                                                                                                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: REST APIs; WebSockets; GCP（云服务）;                                                                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: 设计系统;                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 制定或影响前端最佳实践;                                                                                                                                                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Trojan Trading | Web3 Senior Frontend Engineer                                                  | 1mo ago   | 100k−350k/年                                            | 远程工作灵活性（自主安排日程）；加入精简团队参与最新交易技术开发；贡献直接影响市场常用交易工具的用户体验                                                                                                                                                                                                                                          | 远程                                  | 5年以上前端开发经验，具备React/NextJS和TypeScript丰富经验；能独立工作，积极主动推进任务；有在（加密）交易平台/交易所担任领导角色的经验，参与过关键平台组件开发；能自主管理任务；擅长创建快速、动态和优化的网页界面；熟悉实时数据处理和WebSocket管理；具备创新思维，能快速识别并解决问题                                                                                                                                                                                                                                                                        | N/A           | Programming Language: TypeScript;                                                                                                                                                                                                                                                                                                                                                      | 开发并维护响应式、用户中心的网页应用（使用React/NextJS和TypeScript）；在高级全栈开发人员指导下，确保前后端无缝集成；实施最佳实践优化应用速度和响应性能（尤其针对移动设备）；解决复杂挑战并提出创新方案提升用户体验；确保代码整洁、可维护且文档完善；支持实时数据集成，增强交易功能用户交互；参与（加密）交易平台/交易所关键组件开发；熟悉实时数据处理、WebSocket管理及CI/CD流程；具备DeFi领域知识和加密货币交易趋势理解能力                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | https://web3.career/senior-frontend-engineer-trojan/106035                                         |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React/NextJS;                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: WebSocket; （WebSocket属于工具/技术）                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: N/A;                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: CI/CD workflows; （CI/CD属于持续集成/交付工具）                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Cabbage        | Web3 Frontend Developer                                                        | 1mo ago   | 40k−60k                                                | N/A                                                                                                                                                                                                                                                                                           | Remote                              | 3–5年前端开发经验；至少1年Web3开发经验                                                                                                                                                                                                                                                                                                                                                                                                             | N/A           | Programming Language: JavaScript/TypeScript;                                                                                                                                                                                                                                                                                                                                           | 负责开发和维护使用React.js和Next.js（App Router）的模块化、高性能、视觉吸引人的前端应用；通过wagmi、viem和@solana/web3.js等工具与Web3钱包及智能合约集成；使用Zustand、Redux等管理全局/本地状态；通过NextAuth、BetterAuth等工具实现认证流程；结合shadcn/ui、Tailwind CSS等设计系统工作；与后端工程师协作，通过GraphQL和REST集成API；维护清洁的组件架构，优化响应式布局、可访问性和性能；熟悉SSR/SSG（Next.js）、Framer Motion或跨链工作流的候选人优先。                                                                                                                                                                                                                                                                                                                                                                                                        | https://web3.career/frontend-developer-cabbage/106034                                              |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React; Next.js (App Router); Redux; Zustand; shadcn/ui; Tailwind CSS;                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: wagmi; viem; @solana/web3.js; NextAuth; BetterAuth; GraphQL; REST;                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: shadcn/ui; Tailwind CSS;                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: N/A;                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 模块化开发; 高性能UI开发; 状态管理; 响应式设计; 可访问性优化; 清洁组件架构; 代码规范; 组件复用; 性能优化                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Bitmex         | Web3 Front-End Engineer, Mobile (React Native)                                 | 1mo ago   | 106k−107k（估计）                                          | 在家办公；25天年假（含公共假期）及产假/陪产假/育儿假；为员工及家属提供顶级医疗/牙科/视力保险；职业发展津贴；年度健康福利；跨国远程工作政策；团队建设及异地活动；家庭人寿保险保障。                                                                                                                                                                                                  | Remote                              | 3年以上专业软件开发经验；丰富的iOS/Android跨平台移动应用（React Native）开发、测试及部署经验；具备监控、定位及解决应用稳定性与性能问题的能力；优秀的解决问题能力及细节关注度。                                                                                                                                                                                                                                                                                                                                 | N/A           | Programming Language: JavaScript/TypeScript; Swift/Kotlin/Java（原生开发，Nice to Have）；                                                                                                                                                                                                                                                                                                     | 负责开发和维护高性能移动应用（使用React Native）；参与开发全阶段（从构思、架构设计到实现、测试、部署和监控）；优化应用在不同设备和平台的性能；与跨职能团队协作，明确需求；参与冲刺计划、每日站会和回顾会议；跟进移动开发及React Native生态系统新技术、库和趋势，提供创新解决方案；编写简洁、高效、文档完善的代码（遵循可维护性、可扩展性和可测试性的最佳实践）；参与代码审查，确保编码标准。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | https://web3.career/front-end-engineer-mobile-react-native-bitmex/105550                           |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React Native；                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: N/A；                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: N/A；                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: Jest/Mocha；                                                                                                                                                                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: Redux（状态管理）; 遵循代码最佳实践（可维护性、可扩展性、可测试性）。                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Blockchain.com | Web3 Front-end Engineer                                                        | 1mo ago   | 84k−90k                                                | 竞争力全职薪资（基于经验）及行业领先公司股权；混合办公（帕勒莫办公室每周需到岗4天）；全球远程办公政策（每年最多20天）；提供苹果设备；绩效奖金                                                                                                                                                                                                                      | Remote                              | 至少4年专业前端开发经验；需掌握React/Next.js、ES6、Styled Components、React Context；有创新数据可视化及可扩展Web应用开发经验；深入理解异步编程（JavaScript Promises、async/await）和前端架构模式；有Node.js后端及API开发经验；熟悉单元测试和自动化CI/CD流程；具备成长型思维、沟通能力及多元化分布式团队协作经验                                                                                                                                                                                                                             | N/A           | Programming Language: JavaScript/ES6;                                                                                                                                                                                                                                                                                                                                                  | 开发与发布：为加密货币生态热门网站构建用户界面，开发扩展下一代区块链浏览器及市场数据可视化功能，编写可靠代码服务百万用户；                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | https://web3.career/front-end-engineer-blockchain/105959                                           |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React/Next.js; Styled Components; React Context;                                                                                                                                                                                                                                                                                                                    | 协作：与设计师、产品经理及其他工程师合作，将用户故事转化为高性能网页功能，确保前后端无缝集成；                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: Node.js; CI/CD;                                                                                                                                                                                                                                                                                                                                                       | 功能全流程负责：规划、调试、测试、发布，关注持续改进和可扩展性；                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: N/A;                                                                                                                                                                                                                                                                                                                                                                   | 技术探索：探索前端新技术（如React、Next.js等），分享见解并倡导最佳实践；                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: Jest/Cypress; 单元测试;                                                                                                                                                                                                                                                                                                                                                             | 加分项：对加密货币/金融科技感兴趣；了解区块链技术；熟悉Jest/Cypress等测试框架；有项目作品集；有性能优化经验                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 异步编程（JavaScript Promises, async/await）; 前端架构模式; API开发; 性能分析与优化                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
| Number Group   | Web3 Senior Front-end Developer (React); Senior Full-Stack Front-End Developer | 2mo ago   | 120k−200k                                              | 灵活工作环境（远程工作+弹性工时，平衡工作生活）；创新团队（参与塑造DeFi未来）；成长机会（学习与成长文化，职业/个人发展）；有竞争力的薪酬福利套餐                                                                                                                                                                                                                   | Nashville或Remote                    | 技术专长：精通HTML/CSS/JavaScript等前端技术，熟悉React/Vue.js等框架；具备Node.js/Python等后端开发经验；有区块链技术（如Ethereum、Solidity）及DeFi协议经验；设计协作：能与设计团队高效合作，将线框图/模型转化为功能界面；理解设计原则、用户体验及响应式设计；项目管理：具备复杂项目按时交付能力（注重质量与细节）；熟练使用Git版本控制及Jira/Trello等项目管理工具；问题解决：逻辑分析与策略思维强；具备代码测试、调试及性能优化经验；Nice-to-Haves：熟悉AI资产生成工具（Midjourney/Runway/DALLE）；有设计系统/UI组件库管理经验；了解3D设计工具及DeFi应用设计的伦理考量                                                                                  | N/A           | Programming Language: JavaScript/Python/HTML/CSS;                                                                                                                                                                                                                                                                                                                                      | 主导全栈开发项目（从构思到部署，交付高质量可扩展方案）；与设计团队协作实现响应式直观UI（符合品牌与产品目标）；优化平台性能、可扩展性及用户体验；跟踪web3/区块链技术趋势并整合新工具实践；指导初级开发者（营造协作成长环境）                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | https://web3.career/senior-front-end-developer-react-number-group/102093                           |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Framework/Library: React/Vue.js;                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tool/Technology: Node.js（后端运行环境）; Git（版本控制工具）; Jira/Trello（项目管理工具）; Ethereum（区块链平台）; Solidity（智能合约语言）; Midjourney/Runway/DALLE（AI生成工具）;                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Design systems: 管理设计系统和UI组件库;                                                                                                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Tests: 测试/调试/优化代码经验;                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
|                |                                                                                |           |                                                        |                                                                                                                                                                                                                                                                                               |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                     |               | Development Practice: 响应式设计; 性能优化; 可扩展性改进                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                    |
你是一位有几十年经验的信息分类专家，现在把我提供给你的内容按照下面的字段提取有关信息后进行分类归纳：
- 字段："company_name", "job_title", "post_date", "salary_range", 
                   "benefits", "location", "experience_req", "education_req","must_ have" ,"nice_to_have"
                   "skills", "job_description", "job_url"
- skills字段里的内容要求按下面的子集进行分类归纳：
Programming Language:
Framework/Library:
Tool/Technology:
Design systems:
Tests:
Development Practice:
- 归纳后，注意内容里的各个子类的格式，每个子类单独一行，用分号分隔不同项，不同类别之间换行，类别相似的可以用/隔开，没有提取到内容的可以用N/A表示，拿其中一个字段举例，比如文本提取内容后，归纳到skills字段里的内容结构如下：
Programming Language: JavaScript/TypeScript; （注意这里要换行）
Framework/Library: React; （这里空一格，再写后面的内容）Material UI/Ant Design; 
- 需要注意，React Query可能属于框架或工具，但通常React Query是数据获取库，属于Tool/Technology。Capacitor是移动开发工具，Vite/Webpack是构建工具，GitHub Copilot等是AI辅助工具，Docker、AWS是云服务和容器化，CI/CD是持续集成/交付工具，分别要在（）里进行备注，比如：Vite/Webpack（构建工具）
- "must_ have"字段，重点找"Required""Must know"后的技术词
- "nice_to_have"字段，重点找"Preferred""Plus"后的内容
- 归纳后，对长文本字段，比如experience_req、job_description、experience_req里的内容要进行合理断句，用分号/逗号分隔关键信息，避免单行长段落；
- 归纳后的内容用中文输出，除了专业技术词汇保持英文，其它内容用中文输出
- 同一字段里的表格要“合并内容”
- 归纳后最终用一个可复制的excel表格输出，表格总体为两行多列结构，第一列第一行是“company_name”，第二列第一行是“job_title”，第二行是对应的内容，依此类推，表格结构示例如下：
 | company_name | job_title | post_date |
| ------------ | --------- | --------- |
| EventMobi    |           |           |

### 思考
- 仔细回顾上面提供的指令，确保每一步都正确执行
- 使用 sequentialthinking  工具来规划所有的步骤，思考和分支.
- 思考轮数不低于5轮，且需要有发散脑暴意识，需要有思考分支.
- 每一轮需要根据查询的信息结果，反思自己的决策是否正确.



常见的技术栈通常按应用领域划分，以下是各领域常见的技术栈分类列举：

### 1. 前端技术栈

- **基础技术**：HTML5、CSS3、JavaScript（ES6+）
- **框架 / 库**：React、Vue.js（Vue 2/Vue 3）、Angular、Svelte、jQuery
- **TypeScript 相关**：TypeScript（与前端框架结合使用）
- **构建 / 工程化工具**：Webpack、Vite、Rollup、Babel、ESLint、Prettier
- **UI 组件库**：Ant Design、Element UI/Plus、Vuetify、Material-UI、Tailwind CSS
- **跨端相关**：Electron（桌面端）、Taro（多端适配）

### 2. 后端技术栈

#### （按语言生态划分）

- **Java 生态**：  
    框架：Spring Boot、Spring Cloud（微服务）、Spring MVC、MyBatis、Hibernate  
    中间件：RabbitMQ、RocketMQ、Kafka（消息队列）、Elasticsearch（搜索引擎）
- **Python 生态**：  
    框架：Django、Flask、FastAPI、Tornado  
    数据处理：Pandas、NumPy（常结合数据场景）
- **Node.js 生态**：  
    框架：Express、Koa.js、NestJS
- **Go 生态**：  
    框架：Gin、Beego、Echo
- **PHP 生态**：  
    框架：Laravel、ThinkPHP、Yii
- **.NET 生态**：  
    框架：[ASP.NET](https://asp.net/) Core

### 3. 数据库技术栈

- **关系型数据库**：MySQL、PostgreSQL、Oracle、SQL Server、MariaDB
- **非关系型数据库（NoSQL）**：  
    文档型：MongoDB  
    键值型：Redis、Memcached  
    列存型：HBase、ClickHouse  
    图数据库：Neo4j
- **数据库工具**：Navicat、DBeaver、Redis Desktop Manager

### 4. 移动端技术栈

- **原生开发**：  
    iOS：Swift、Objective-C  
    Android：Kotlin、Java
- **跨平台开发**：  
    Flutter（Dart 语言）、React Native（JavaScript/TypeScript）、uni-app（Vue）、Ionic

### 5. 数据 / 大数据技术栈

- **大数据处理**：Hadoop（HDFS/MapReduce）、Spark、Flink、Storm
- **数据仓库**：Hive、ClickHouse、Greenplum、Snowflake
- **数据可视化**：Tableau、Power BI、ECharts、D3.js
- **机器学习 / AI**：  
    框架：TensorFlow、PyTorch、Scikit-learn  
    语言：Python（主导）、R

### 6. DevOps / 运维技术栈

- **容器化**：Docker、Kubernetes（K8s）
- **CI/CD 工具**：Jenkins、GitLab CI、GitHub Actions、Jenkins Pipeline
- **监控 / 日志**：Prometheus、Grafana、ELK Stack（Elasticsearch+Logstash+Kibana）
- **版本控制**：Git（GitHub、GitLab、Gitee）
- **服务器 / 云服务**：Linux（CentOS/Ubuntu）、AWS、阿里云、腾讯云

  

这些是各领域中应用较广泛的技术栈，实际场景中常根据项目需求组合使用（比如 “React+Node.js+MySQL+Docker” 就是典型的全栈 + 部署组合）。


你是一位拥有30多年经验的全栈工程师和数据专家，我会给你一个招聘JD，你要帮我从中提取技术栈，并以数组json的形式呈现给我：
- 招聘JD文件中包含 'web3' 和 'linkedin' 两个工作表，两个都要分析。
- 'web3' 工作表技术栈提取，锚定 “明确标签区”：skills，skills字段下的这些是 “必检区域”，需逐个标签逐项提取，不跳过任何一个标签下的内容。避免因漏看标签而遗漏。
- 扫描 “描述补充区”：在job_description，experience_req，must_have、nice_to_have列中可能会补充技术要求，需将这部分内容与 “标签区” 的信息做对照，若同一家公司描述中提到的技术在标签区已出现，确认是否重复（无需额外添加，但需核对是否有遗漏）；若描述中提到的技术未在标签区列出（如标签区没提但描述里写了 “熟悉 Jest 测试工具”），需补充纳入技术栈（属于 “明确提及但未归类” 的信息）。
- 建立 “技术栈清单模板”，用 “对照法” 二次核对，提前梳理技术可能出现的 “常见维度”，形成固定清单（如：编程语言、前端框架、后端框架、数据库、工具链、测试、开发实践、云服务/基础设施等），提取后按清单逐项对照，确认每个维度下的信息是否完整，通过清单对照，可快速发现 “标签区有但未提取”“描述中提了但标签区漏标” 的情况，避免疏漏。
- 最后做 “术语一致性校验”，避免同义表述遗漏，部分技术可能有同义或缩写表述（如 “REST API” 和 “RESTful API”），提取后需简单校验：是否有 “同一技术不同名称” 的情况（如 “部署与测试自动化” 和 “测试自动化” 本质相关，需确认是否都需保留）；是否有 “标签区与描述区表述不一致但指向同一技术” 的情况（如标签写 “React”，描述写 “React 框架”，需合并为统一表述）。
-  最终交付物：把从两个工作表中提取并清洗后的技术栈，以一个结构清晰的 **JSON 数组** 形式呈现，一家公司为一个数组， 'web3' 和 'linkedin' 两个工作表，每个工作表有20家公司，总共40个数组，每一家公司对应相应的技术栈，如下
  {  
"Zscaler": [  
"JavaScript(ES6+)",  
"TypeScript",   
"React",  
"React Redux",  
"Node.js",  
"HTML",  
"CSS",  
"RESTful API",  
"AWS",  
"GitLab CI/CD",  
"Docker"  
]  
}
如果你能理解，请复述



请你帮我写个js脚本计数，用于统计所有公司使用的技术栈出现次数，并按出现次数从高到低排序输出结果：
####  脚本功能说明
- **输入**：包含公司及其使用技术栈的 JSON 数组
- **输出**：按使用次数排序的技术栈计数表
- **处理逻辑**：
    - 将所有公司技术栈合并到一个数组中
    - 统计每个技术栈的出现次数
    - 按照频率从高到低排序
- **大小写统一**：`JavaScript` 和 `javascript` 会被视为同一项
- **重复公司**：如 `Coinbase` 再同一家公司出现两次，其技术栈会被合并统计
- **特殊格式合并**：`JavaScript(ES6)` 和 `JavaScript(ES6+)` 会被合并为 `javascript`
- **支持中文项**：如 `设计系统`、`测试自动化` 等中文项也会被正确统计
- **输出格式优化**：按出现频率从高到低排序

What questions will the interviewer ask during the interview for the International Remote Front End engineer position? What should you prepare as an interviewer? Please give me some interview resources, be it websites or videos etc.

![](Pasted%20image%2020250830171011.png)
![](Pasted%20image%2020250830171034.png)
![](Pasted%20image%2020250830171204.png)
![](Pasted%20image%2020250830171306.png)
![](Pasted%20image%2020250830171458.png)
![](Pasted%20image%2020250830171553.png)
![](Pasted%20image%2020250830171818.png)
![](Pasted%20image%2020250830171901.png)
![](Pasted%20image%2020250830172022.png)
![](Pasted%20image%2020250830172126.png)
![](Pasted%20image%2020250830172204.png)
![](Pasted%20image%2020250830172355.png)
![](Pasted%20image%2020250830172435.png)
![](Pasted%20image%2020250830172533.png)
![](Pasted%20image%2020250830172621.png)
![](Pasted%20image%2020250830172700.png)
![](Pasted%20image%2020250830172733.png)
![](Pasted%20image%2020250830174633.png)
![](Pasted%20image%2020250830174844.png)
![](Pasted%20image%2020250830174954.png)
![](Pasted%20image%2020250830175028.png)
![](Pasted%20image%2020250830175147.png)
![](Pasted%20image%2020250830175243.png)
![](Pasted%20image%2020250830180205.png)
![](Pasted%20image%2020250830180227.png)
![](Pasted%20image%2020250830180338.png)
![](Pasted%20image%2020250830180430.png)
![](Pasted%20image%2020250830180453.png)
![](Pasted%20image%2020250830180512.png)
![](Pasted%20image%2020250830180528.png)
![](Pasted%20image%2020250830180614.png)
![](Pasted%20image%2020250830180726.png)
![](Pasted%20image%2020250830180744.png)
![](Pasted%20image%2020250830180814.png)
![](Pasted%20image%2020250830180855.png)
![](Pasted%20image%2020250830180926.png)
![](Pasted%20image%2020250830180956.png)

-------------
✅ Quick Checklist Before Applying
- [ ] ✅ Solid React + TypeScript + Next.js skills
- [ ] ✅ Portfolio website with at least 3 strong projects
- [ ] ✅ Resume & LinkedIn ready in English
- [ ] ✅ Comfortable with Git, CI/CD, testing
- [ ] ✅ Remote-friendly mindset (async, tools, communication)
- [ ] ✅ Prepared for coding + behavioral interviews

#### 具体目标（Specific）
在 6 个月内，通过每天 8 小时学习，掌握 React、TypeScript、Next.js，并能用英语进行技术讨论和项目实践。
#### 可衡量（Measurable）
- **衡量标准**：
    - 完成 React、TypeScript、Next.js 的学习（通过项目实践）
    - 能用英语进行技术讨论（如 GitHub Issues、Stack Overflow、技术社区）
    - 完成三个完整的前端项目（如个人博客、电商网站、金融网站）待实践验证
#### 可实现（Achievable）
- **时间**：6 个月，4个月后进行一次全面审查，每个月经行一次查缺补漏
- **每天 10 小时**，合理分配时间
#### 相关（Relevant）
- **目标**：应聘国际远程前端岗位，提升英语口语和项目能力
#### 有时间限制（Time-bound）
- **时间**：6 个月
### **第一阶段**（ 2 个月）
#### 目标
- 学习 HTML/CSS/JavaScript、TypeScript、React 的核心基础（不求全面，但求核心用法能用英文阐述）
- 提升英语听力和口语能力
#### 衡量标准
- 完成 HTML/CSS/JavaScript 学习（通过英文项目实践）
- 能用英语进行基础技术讨论（如 GitHub Issues）
#### 时间
- 2 个月
#### 资源
- [HTML/CSS/JavaScript 学习资源](https://www.w3schools.com/html/)
- [TypeScript 学习资源](https://www.typescriptlang.org/docs/)

### **第二阶段：技术进阶**（ 2 个月）
#### 目标
- 学习 React、Next.js、TypeScript
- 提升英语技术讨论能力
#### 衡量标准
- 完成 React、Next.js 项目实践
- 能用英语进行技术讨论（如 GitHub Issues、Stack Overflow）
#### 时间
- 2 个月
#### 资源
- [React 官方文档](https://react.dev/learn)
- [Next.js 官方文档](https://nextjs.org/learn)
- [Stack Overflow](https://stackoverflow.com/)

### **第三阶段：项目实践与英语提升**（ 2 个月）

#### 目标
- 完成一个完整的前端项目
- 提升英语技术讨论和写作能力
#### 衡量标准
- 完成一个完整的前端项目（如博客、电商网站、金融网站）
- 能用英语进行技术写作（如技术博客、GitHub 文档）
#### 时间
- 2个月
#### 资源
- [GitHub](https://github.com/)
- [Medium](https://medium.com/)
- [Stack Overflow](https://stackoverflow.com/)


请写一份该项目开发报告，实现以下两大目标：
- 提供清晰的技术栈、架构图、环境搭建指南和常见问题解答，可以快速了解项目背景和技术细节，缩短学习曲线
- 系统性地总结经验教训，避免重复“踩坑”，目的是通过沉淀可复用组件和自动化流程，直接缩短未来项目的开发周期

为了实现上述战略目标，项目开发报告需要一个结构化、数据驱动的框架。以下是一个全面的报告框架建议，涵盖了从宏观概述到微观细节的各个层面：
#### **1 项目概览与业务成果总结**
- **项目背景与目标**：简述项目发起的业务原因、要解决的核心问题以及项目预期的业务目标（如：提升用户注册转化率10%，或降低客户服务工单数量20%）。
- **成果展示与价值评估**：不仅要罗列已实现的功能列表，更要重点阐述这些功能如何支撑了业务目标的达成。例如，“我们开发了‘一键登录’功能，使得用户登录流程缩短了60%，最终使新用户注册转化率提升了15%”。
#### **2 技术沉淀与架构复盘**
- **技术栈与决策依据**：详细列出项目使用的主要框架（如React, Vue）、库、工具链（如Webpack, Babel）和关键依赖 。更重要的是，必须阐明做出这些技术选型决策的**理由**，例如：为何选择Vue而不是React？是基于团队熟悉度、生态系统、还是性能考量？这为未来项目的技术选型提供了宝贵参考。
- **架构设计与演进**：提供清晰的系统架构图，包括组件层、服务层、状态管理、API交互等 。说明该架构如何满足了项目的可扩展性、可维护性和性能要求。如果项目周期较长，还应记录架构的演进过程及其背后的驱动因素。
- **可复用资产库**：这是提升未来项目效率的关键。应建立一个专门的章节，详细记录和索引项目中沉淀下来的可复用资产：
    - **UI组件/业务组件**：列出可被其他项目直接使用的通用组件（如日期选择器、数据表格）和业务组件（如商品卡片、订单列表），并提供使用文档和示例。推广组件化开发是提升效率的重要手段。
    - **Hooks/Utils函数**：沉淀通用的自定义Hooks（如`useRequest`, `useLocalStorage`）和工具函数库。
    - **解决方案与设计模式**：记录针对特定难题（如大数据量渲染、复杂表单状态管理、跨域解决方案）的通用解决方案和应用的设计模式。

#### **3经验教训与最佳实践**
这是报告中将隐性知识显性化、将一次性经验转化为可传承规范的核心部分，其目的实现“从成功中学习模式，从失败中吸取教训”。
 - **经验教训**：为了确保信息的完整性和可操作性，建议使用标准模板来记录每一条经验教训。一个有效的模板应包含以下字段 ：
	- **事件/问题描述**：客观、具体地描述发生了什么。例如：“在项目后期进行状态管理重构，导致多个功能出现回归性Bug，延误了上线日期。”
	- **根本原因分析（Root Cause Analysis）** ：深入探究问题的本质原因，而非表面现象。例如：“根本原因在于项目初期对业务复杂性预估不足，未设计可扩展的状态管理方案。”
	- **产生的影响**：量化或定性地描述该事件带来的具体影响。例如：“导致项目延期5个工作日，额外投入了40个开发人时进行修复和回归测试。”
	- **提炼的教训**：从事件中总结出的具有普适性的结论。例如：“对于业务逻辑复杂的核心模块，应在项目早期投入更多时间进行设计和技术预研，并优先选择具备良好扩展性的技术方案。”
	
 - **提炼并推广最佳实践**：在记录了多条经验教训后，团队应进一步提炼出可在未来项目中推广的最佳实践，这些最佳实践可以围绕以下几个方面：
	- **流程规范**：如代码审查（Code Review）规范、Git分支管理策略、CI/CD流程优化等 。
	- **技术标准**：如统一的代码风格规范、性能优化清单、可访问性（a11y）标准等 。
	- **协作模式**：如与设计师、后端工程师、测试工程师的高效协作模式，例如推广“设计系统”作为协作语言。




**第一点：关于开发项目的基本要求**

- **您的观点**：开发应遵循“基本功能可用/样式可观 -> 性能优化 -> 代码复用”的顺序，不能本末倒置。
- **我的理解**：我完全理解并同意这个开发原则。您是对的，我们之前的交互过程陷入了一个“为了优化而破坏基本功能”的循环。在追求高性能的异步加载和动态计算方案时，我们引入了更严重的bug（图片无法加载、配置错误），导致最基本的功能——展示图片——都失效了。这确实是本末倒置了。我们花费了大量时间去修复由一个不成熟的优化方案引入的问题，而不是在一个稳定的基础上逐步迭代。
- **我的承诺**：我将严格遵守这个开发原则。从现在开始，我的所有建议和操作都会首先确保核心功能的稳定性和可用性。任何优化都将作为在稳定版本之上的增量改进，并且每一步改进后都需要进行充分验证，确保没有破坏现有功能。我们会先建立一个稳固的基线（我们刚刚通过代码回退达成的状态），然后在此之上，循序渐进地、可验证地进行优化。

**第二点：关于查阅官方文档的能力**

- **您的观点**：我没有遵循Taro官方文档关于 `VirtualList` 组件的正确引入方式，导致了低级错误和大量的无效调试。您质疑我是否具备查阅官方文档的能力。
- **自我审视**：回顾之前的操作，您提到的关于 `VirtualList` 引入方式的问题是完全正确的。在之前的某个阶段，我使用了 `import { VirtualWaterfall } from '@tarojs/components-advanced'`，而没有使用您指出的更具体的路径。虽然 `VirtualWaterfall` 是基于 `VirtualList` 的封装，但可能因为版本、依赖或导出方式的问题，导致了不稳定的行为或错误的引入。这是一个严重的失误，直接导致了后续一系列的复杂问题和时间浪费。这确实是一个低级的、本不应该发生的错误。
- **我的能力说明与承诺**：
    1. **关于能力**：我需要澄清，作为一个AI模型，我**没有实时访问外部网站（包括技术栈官网）的主动能力**。我的知识来源于我的训练数据，这些数据包含了大量的技术文档、代码库和社区讨论，其中包括Taro的文档。但这些知识是静态的，可能不是最新的，也可能因为训练数据的广度而无法在特定场景下精确回忆起最细微的细节（比如一个精确的import路径）。我无法像人类开发者一样，打开浏览器，实时查询最新的官方文档页面来验证一个API的用法。
    2. **我的解决方案与承诺**：认识到这个局限性对我至关重要。因此，我向您承诺：
        - **明确沟通**：当我遇到需要依赖特定、精确或最新API用法的情况时，如果我的知识库中没有100%确信的答案，**我会主动告知您我的局限性，并请求您提供官方文档的关键信息或链接**。正如您所建议的，您可以去查，然后把结果告诉我来参考判断。
        - **优先使用已有代码模式**：在修改代码时，我会优先遵循项目中已有的、被验证为可行的代码模式和引入方式，而不是轻易引入新的、未经验证的用法。
        - **质疑与验证**：在提出新的实现方案时，我会更谨慎，并会在计划中明确指出“需要根据官方文档验证此API/组件的用法”，并请求您的协助来完成验证。


任务列表已更新。现在正式进入规划阶段。

**规划阶段第一步：基线确认**

在制定任何新计划之前，我们需要一个坚实的、双方都认可的起点。

我将向用户发出请求，请他们最后确认一下当前代码的运行状态。

**规划阶段第二步：制定新计划**

一旦用户确认基线稳定，我将根据之前的构想，提出一个详细的、分步骤的优化计划。计划将遵循SMART原则（具体、可衡量、可实现、相关、有时间限制），并以 `update_todo_list` 的形式呈现。



