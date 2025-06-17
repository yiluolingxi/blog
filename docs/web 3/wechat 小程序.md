1. **安装 Node.js 和 npm**：Taro 依赖于 Node.js 和 npm，需先安装它们。可在 Node.js 官网下载适合操作系统的安装包，并按照安装向导完成安装。
2. **安装 Taro CLI**：使用以下命令全局安装 Taro 开发工具：

```bash
npm install -g @tarojs/cli
```
-  **​Windows​**​：按 `Win + R` 输入 `cmd` 或 `powershell` 打开命令提示符/PowerShell。
- ​**​切换到用户主目录**
```bash
 # Windows
 cd %USERPROFILE%
```
先切换到用户主目录，再全局安装 Taro 开发工具，此目录权限宽松，避免因系统路径权限导致安装失败。​**​系统目录（如 System32\）​**，权限严格，可能触发安全拦截；环境变量冲突易导致命令失效，**环境变量优先级问题​**，若`system32`在环境变量`PATH`中的顺序优先于Node.js路径，系统会错误解析命令，导致安装失败。正确操作步骤：打开命令提示符（CMD）或PowerShell，切换到​**​非系统目录​**​（如用户目录）。

​**​为什么在用户目录操作？​**​  
全局安装的命令（如 `npm install -g`）会将工具安装到系统环境变量指向的全局路径（如 `C:\Users\你的用户名\AppData\Roaming\npm`），与具体项目无关。在用户目录执行可避免因系统目录（如 `C:\Windows\System32\`）权限不足导致的安装失败。

​**​操作步骤：**
```bash
cd %USERPROFILE%       # 切换到用户目录
npm install -g @tarojs/cli  # 安装全局工具
taro -v                # 验证安装（显示版本号即成功）
```

