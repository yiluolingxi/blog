### **分支命名规范（主流策略）​**​ 

#### ​**​1. 核心前缀 + 描述（全小写，短横线连接）​**​

|​**​分支类型​**​|​**​命名格式​**​|​**​示例​**​|​**​生命周期​**​|
|---|---|---|---|
|功能开发分支|`feature/[功能描述]`|`feature/user-auth`|合并后删除|
|缺陷修复分支|`bugfix/[问题简述]`|`bugfix/login-timeout`|修复后删除|
|紧急热修复分支|`hotfix/[问题简述]`|`hotfix/payment-error`|生产修复后删除|
|版本预发布分支|`release/[语义化版本号]`|`release/v1.2.0`|版本发布后保留|
|实验性分支|`experiment/[实验内容]`|`experiment/new-ui`|根据结果决定保留与否|
|文档分支|`docs/[修改内容]`|`docs/api-refactor`|合并后删除|
#### ​**​2. 关键原则​**
#### **关键原则​**​

- ​**​前缀统一性​**​：优先使用 `feature/` 而非缩写 `feat/`（避免歧义）
- ​**​语义关联​**​：集成任务追踪系统（如 Jira）
```bash
git checkout -b feature/PROJ-123-search-optimization  # 关联问题ID
```
- **​避免冗余​**​：禁用特殊字符（`@`、`#`）、空格或大写字母

### ​**​二、提交信息规范（Conventional Commits）**
#### **1. 结构化格式​**
```plaintext
<类型>(<作用域>): <主题>
<空行>
<正文>
<空行>
<页脚>  # 关联Issue或PR
```
**示例​**​：
```bash
git commit -m "feat(auth): add OAuth2 support" \
-m "- Implement Google & GitHub OAuth" \
-m "- Add token refresh mechanism" \
-m "Closes #123, Refs #45"
```
### **完整提交信息效果​**​

在 Git 历史或 PR 中会显示为：
```
feat(auth): add OAuth2 support

- Implement Google & GitHub OAuth
- Add token refresh mechanism

Closes #123, Refs #45
```

###  ​**​为何这样写？​**​

#### ​**​1. 标准化优势​**​

- ​**​自动化生成变更日志​**​（如 `standard-version` 工具）
- ​**​快速定位历史修改​**​（通过 `git log --grep="feat(auth)"`）
- ​**​触发语义化版本升级​**​（`feat` → 次版本号+1）

#### ​**​2. 团队协作价值​**​

- ​**​清晰的作用域​**​：`(auth)` 让团队知道影响范围
- ​**​任务可追溯性​**​：通过 `#123` 直接跳转到原始需求
- ​**​代码审查效率​**​：正文详细说明减少沟通成本


### Git 常用命令行详解

Git 命令按功能分为以下类别，覆盖日常开发全流程：

#### 1. ​**​仓库与配置​**​

| 命令                                             | 说明      |
| ---------------------------------------------- | ------- |
| `git init`                                     | 初始化本地仓库 |
| `git clone <url>`                              | 克隆远程仓库  |
| `git config --global user.name "xxx"`          | 设置全局用户名 |
| `git config --global user.email "xxx@xxx.com"` | 设置全局邮箱  |

#### 2. ​**​分支管理​**​

| 命令                         | 说明                |
| -------------------------- | ----------------- |
| `git branch`               | 查看本地分支（`*`标记当前分支） |
| `git checkout -b <branch>` | 创建并切换到新分支         |
| `git merge <branch>`       | 将指定分支合并到当前分支      |
| `git branch -d <branch>`   | 删除已合并的分支          |
| `git push origin <branch>` | 推送分支到远程仓库         |

#### 3. ​**​提交与撤销​**​

| 命令                          | 说明                             |
| --------------------------- | ------------------------------ |
| `git add .`                 | 添加所有修改到暂存区                     |
| `git commit -m "msg"`       | 提交暂存区内容                        |
| `git reset --hard <commit>` | 彻底回退到指定提交（​**​危险​**​：丢失未提交的修改） |
| `git restore <file>`        | 恢复工作区文件到最近提交状态                 |
| `git stash`                 | 临时保存未提交的修改（用于紧急切换任务）           |

#### 4. ​**​远程协作​**​

| 命令                            | 说明                         |
| ----------------------------- | -------------------------- |
| `git fetch`                   | 拉取远程更新（不自动合并）              |
| `git pull`                    | 拉取并合并远程分支（`fetch + merge`） |
| `git push --force`            | 强制推送（覆盖远程提交，​**​慎用​**​）    |
| `git remote add <name> <url>` | 添加远程仓库别名                   |

#### 5. ​**​高级操作​**​

| 命令                          | 说明              |
| --------------------------- | --------------- |
| `git rebase <branch>`       | 变基（重写提交历史，保持线性） |
| `git cherry-pick <commit>`  | 应用指定提交到当前分支     |
| `git tag v1.0 -m "Release"` | 创建版本标签          |
| `git log --oneline --graph` | 图形化查看提交历史       |

> ⚠️ ​**​注意事项​**​：
> 
> - ​**​强制操作风险​**​：`git reset --hard` 和 `git push --force` 可能导致数据丢失，需谨慎使用

> - ​**​分支保护​**​：团队协作中建议启用分支保护规则（如禁止直接推送主分支）




以下是为 Windows 10 64 位系统配置和使用 GitHub 的完整指南，结合最新稳定版工具（截至 2025 年）和高效实践，包含避坑指南、风险提示及详细操作步骤。所有步骤均经实战验证，兼顾安全性和开发效率。

---

### **一、Git 安装与环境配置（最新稳定版 v2.45.0）**
#### **安装步骤**
1. **下载安装包**  
   - 进入 [Git 官网](https://git-scm.com/download/win) → 下载 Windows 64-bit 安装包（自动识别系统）。
   - ⚠️ 避坑提示：勿从第三方渠道下载，避免捆绑恶意软件。

2. **安装关键选项配置**  
   - **编辑器选择**：推荐 `Visual Studio Code`（未来趋势，集成度高）  
   - **PATH 环境**：勾选 *Git from the command line and also from 3rd-party software*（确保全局调用）  
   - **换行符处理**：选 *Checkout as-is, commit as-is*（避免跨平台换行符问题）  
   - 其他选项按默认即可。

3. **验证安装**  
   打开命令提示符（Win+R → 输入 `cmd`）执行：  
   ```bash
   git --version
   ```
   ✅ 成功提示：显示 `git version 2.45.0.windows.1` 类似信息。

---

### **二、GitHub 连接与 SSH 密钥配置**
#### **1. 注册 GitHub 账户**
- 访问 [GitHub 官网](https://github.com/) → 点击 `Sign Up`  
- 邮箱建议使用工作邮箱（后续需验证）。

#### **2. 生成 SSH 密钥（更安全的 Ed25519 算法）**
1. 打开 **Git Bash**（桌面右键或开始菜单搜索）  
2. 执行（替换为你的邮箱）：
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
   - 提示保存路径：按 Enter 使用默认 `C:\Users\你的用户名\.ssh\id_ed25519`  
   - 设置密码（可选但推荐，增加私钥安全性）。  
3. ✅ 成功提示：显示 `Your public key has been saved in ...` 并生成随机艺术图案。

#### **3. 添加公钥到 GitHub**
1. 复制公钥内容：
   ```bash
   cat ~/.ssh/id_ed25519.pub | clip  # 自动复制到剪贴板
   ```
2. 登录 GitHub → 点击右上角头像 → `Settings` → `SSH and GPG Keys` → `New SSH Key`  
   - **Title**：输入标识（如 `My Windows PC`）  
   - **Key type**：保持 `Authentication Key`  
   - **Key**：粘贴剪贴板内容（以 `ssh-ed25519` 开头）。  
3. ✅ 成功验证：
   ```bash
   ssh -T git@github.com
   ```
   显示 `Hi 用户名! You've successfully authenticated...`。

#### **4. 配置全局用户信息（关联提交记录）**
```bash
git config --global user.name "YourGitHubUsername"
git config --global user.email "your_email@example.com"
```
⚠️ **风险提示**：确保邮箱与 GitHub 设置的 **Primary Email** 一致，否则提交不计入贡献图。

---

### **三、GitHub 基础工作流程与高效实践**
#### **1. 克隆仓库（Clone）**
```bash
git clone git@github.com:用户名/仓库名.git  # 使用 SSH 避免重复输密码
```
- 📍 输入位置：在 Git Bash 中进入目标目录（如 `cd /d/projects`）后执行。

#### **2. 本地修改与提交**
```bash
git add .                          # 添加所有更改到暂存区（Staging Area）
git commit -m "修复登录页样式"     # 提交到本地仓库，注释清晰
```
- 💡 高效技巧：用 `git add -p` 交互式选择部分更改，避免提交无关代码。

#### **3. 推送到远程仓库（Push）**
```bash
git push origin main               # 推送到 main 分支（原 master）
```
✅ 成功提示：显示 `Writing objects: 100%...` 并在 GitHub 仓库页面实时刷新。

#### **4. 高级效率工具**
- **GitHub CLI（命令行管理 Issue/PR）**  
  安装：`winget install --id GitHub.cli` → 执行 `gh auth login` 按提示关联。  
- **GitHub Desktop**：图形化操作分支和合并。  
- **GitHub Mobile App**：支持 iOS/Android，实时接收代码审查通知。  

---

### **四、避坑指南与风险提示**
| **常见问题**               | **解决方案**                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **SSH 连接超时**          | 在 `~/.ssh/config` 添加：<br>`Host github.com`<br>`Hostname ssh.github.com`<br>`Port 443` |
| **换行符导致文件修改**     | 执行 `git config --global core.autocrlf false`（关闭自动转换）     |
| **误提交敏感信息**         | 立即撤销：`git reset HEAD^` → 使用 `git rm --cached 文件` → 重提交并 force push |
| **权限不足错误**           | 检查 SSH 密钥是否绑定 GitHub 账户，勿用 HTTPS 协议克隆              |

⚠️ **安全风险提示：**
- **私钥泄露**：勿上传 `.ssh/id_ed25519` 文件（公钥可分享）。  
- **敏感数据提交**：避免将 `.env`、`API Keys` 推送到仓库，使用 `.gitignore` 文件过滤。  
- **启用 2FA**：在 GitHub 设置 → `Security` → `Enable two-factor authentication`。  

---

### **五、常用命令速查表**
| **命令**                     | **参数示例**                  | **说明**                                  | **使用场景**                     |
|-----------------------------|-----------------------------|-----------------------------------------|--------------------------------|
| `git clone`                 | `git@github.com:user/repo.git` | 克隆远程仓库到本地                      | 首次获取项目代码               |
| `git status`                | `-s`（简化输出）              | 查看工作区和暂存区状态                  | 修改后检查变动                 |
| `git add`                   | `.`（所有文件）、`文件名`      | 添加文件到暂存区                        | 准备提交前                     |
| `git commit`                | `-m "提交描述"`               | 提交更改到本地仓库                      | 阶段性保存代码                 |
| `git push`                  | `origin main`               | 推送本地提交到远程仓库                  | 本地修改后同步到 GitHub        |
| `git pull`                  | `origin feature`            | 拉取远程分支更新到本地                  | 多人协作前更新代码             |
| `git branch`                | `-a`（查看所有分支）          | 分支管理                                | 切换/创建分支                 |
| `git checkout`              | `-b new-feature`            | 创建并切换到新分支                      | 开发新功能隔离环境             |
| `git merge`                 | `feature/login`             | 合并指定分支到当前分支                  | 功能完成后的集成               |
| `git log`                   | `--oneline --graph`         | 查看提交历史（图形化精简版）            | 回溯变更记录                   |
| `git restore`               | `--staged 文件`             | 撤销暂存区的修改（Git 2.23+）           | 误 add 后回退                 |

> 💡 **未来趋势适配**：  
> - 优先使用 `main` 而非 `master` 作为默认分支名（GitHub 2020 年已更改）。  
> - 结合 GitHub Actions 实现 CI/CD（免费配额支持自动化测试/部署）。

此指南覆盖从环境搭建到高效协作的全流程，严格遵循最新安全标准和开发实践。建议定期执行 `git update-git-for-windows` 保持工具更新。



### 一、个人项目的分支策略

1. ​**​简单项目（推荐方案）​**​
    
    - 直接使用 `main` 分支开发
    - 每次修改后提交：
    
    `git add . git commit -m "feat: 实现用户登录功能" git push origin main`
    
    - ​**​优势​**​：简单直接，适合小型项目或实验性代码
2. ​**​中等复杂度项目​**​
    
    - 保留 `main` 分支作为稳定版本
    - 创建 `dev` 分支用于日常开发：
    
    `git checkout -b dev # 进行开发后... git checkout main git merge dev`
    

### 二、修改定位方案（无分支时）

即使只有 `main` 分支，仍可通过以下方式精确定位修改：

1. ​**​提交哈希值定位​**​
    
    `git log --oneline # 输出示例：a1b2c3d feat: 添加用户模块 git show a1b2c3d`
    
2. ​**​按时间范围查询​**​
    
    `git log --since="2024-07-01" --until="2024-07-20"`
    
3. ​**​文件修改历史​**​
    
    `git log -p src/user.js  # 查看指定文件变更历史`
    
4. ​**​关键词搜索​**​
    
    `git log --grep="登录"  # 搜索包含"登录"的提交`
### 实用技巧

1. ​**​临时保存修改​**​
    
    `git stash  # 保存当前修改 git stash pop  # 恢复修改`
    
2. ​**​修改最后一次提交​**​
    
    `git add . git commit --amend  # 修改提交信息或内容`
    
3. ​**​后悔药机制​**​
    
    `git reflog  # 查看所有操作记录 git reset --hard [commit-hash]  # 回退到指定状态`