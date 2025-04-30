一，科学寻找开源的方法：
**工具**
GitHub代码活跃度 + Dune链上采用率 ≈ 判断项目的真实热度与健康度
[Dune — Crypto Analytics Powered by Community.](https://dune.com/home)

Dune无法直接追踪代码开源性，需手动验证GitHub仓库
部分项目可能伪装开源（如仅开放部分模块），需检查代码提交历史。
高交易量可能由刷量导致（如低Gas链上的Farm项目）
避免被表面数据（如高TVL、GitHub Star数）误导
**多维度交叉验证**
结合链上数据（Dune）+代码活跃度（GitHub）+社区讨论（Discord/Twitter）或外部榜单（如 DappRadar）

方法1：
**搜索词汇**
**技术栈相关**：`web3`, `blockchain`, `ethereum`, `solidity`, `rust`, `substrate`, `ipfs`, `nft`, `defi`, `dao`, `smart contract`, `dapp`

方法2：
**GitHub Trending**：访问 [GitHub Trending](https://github.com/trending)，选择语言（如 `Solidity`）或时间段（日/周/月）查看热门项目
**为什么要在 Trending 页面搜索 Web3 关键词？**
- **发现新兴项目**：Trending 页面能快速捕捉到最近流行的 Web3 项目（例如新发布的工具、协议或框架），而传统按 Stars 排序可能遗漏短期爆款。
    
- **避免过时信息**：Web3 领域技术迭代快，Trending 能优先展示近期活跃项目。

方法3：
 **第三方 GitHub Trending 客户端**
#### **(1) GitHubPopular** 

- **功能**：基于 React Native 开发的跨平台应用，支持订阅 **50+ 种编程语言**（如 Solidity、Rust），可自定义关键词（如 `web3`、`blockchain`）过滤 Trending 项目。
    
- **优势**：
    
    - 自动聚合 GitHub 热门项目，支持按时间范围（日/周/月）筛选。
        
    - 提供收藏、搜索、分享功能，适合长期追踪 Web3 领域动态。
        
- **安装**：支持 Android 和 iOS，需自行编译或下载预构建版本。
    

 **(2) Gitter（微信小程序）** 
- **功能**：高颜值 GitHub 客户端，内置 **Trending 模块**，可查看每日 Star 增长最快的项目。
    
- **优势**：
    
    - 直接通过微信使用，无需安装额外应用。
        
    - 支持关键词搜索 Trending 列表（需手动输入 `web3` 或 `blockchain`）。

今天完成任务：
多方查找，验证了GitHub关键词的可行性，但是效率低
GitHub Trending关键词的可行性，但是效率低

待完成任务：
1. 验证Dune
2. 试用第三方工具GitHub Trending 客户端

