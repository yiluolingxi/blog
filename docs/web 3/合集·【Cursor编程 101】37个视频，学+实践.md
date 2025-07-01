先创建一个新文件，命名后用cursor打开
![](Pasted%20image%2020250701151159.png)
安装中文插件
![](Pasted%20image%2020250701151127.png)
设置规则，在Rules for AI设置下面内容：
# Always respond in Chinese-simplified
# 使用 MCP mcp-context7 查询文档

# MCP Interactive Feedback 规则
1. 在任何流程、任务、对话进行时，无论是询问、回复、或完成阶段性任务，皆必须调用 MCP mcp-feedback-enhanced。
2. 每当收到用户反馈，若反馈内容非空，必须再次调用 MCP mcp-feedback-enhanced，并根据反馈内容调整行为。
3. 仅当用户明确表示「结束」或「不再需要交互」时，才可停止调用 MCP mcp-feedback-enhanced，流程才算结束。
4. 除非收到结束指令，否则所有步骤都必须重复调用 MCP mcp-feedback-enhanced。
5. 完成任务前，必须使用 MCP mcp-feedback-enhanced 工具向用户询问反馈。
6. 当反馈超时后，需要重新使用 MCP mcp-feedback-enhanced 工具向用户询问反馈。

![](Pasted%20image%2020250701151423.png)
在Add context（添加上下文）这个地方输入提示词：
用Python 帮我写一个贫吃蛇游戏。 但我没有任何相关的编程经验， 我的NoteBook电脑上除了安装了Cursor代码编辑器外，也没有任何相关环境， 请详细的一步一步的告诉我应该怎么做, 我做完一步告诉你我做完了， 你再告诉我下一步应该干什么。
![](Pasted%20image%2020250701152007.png)
![](Pasted%20image%2020250701152111.png)
复制指令到终端运行
![](Pasted%20image%2020250701152244.png)
复制保存内容+运行报错了，发给cursor

![](Pasted%20image%2020250701144648.png)
![](Pasted%20image%2020250701144738.png)
![](Pasted%20image%2020250701144922.png)
右上角运行或
![](Pasted%20image%2020250701145001.png)
终端输入运行指令
![](Pasted%20image%2020250701152709.png)
![](Pasted%20image%2020250701145141.png)
增加一个游戏开始界面和结束界面，以及游戏界面增加一个暂停按钮。
![](Pasted%20image%2020250701152935.png)
点击左边复制代码后到中间文件里更新代码
![](Pasted%20image%2020250701145544.png)
![](Pasted%20image%2020250701145626.png)
再次点击运行
![](Pasted%20image%2020250701145727.png)
当前游戏界面的中文字体不显示，我这里可以提供相关的本地字体。
![](Pasted%20image%2020250701145902.png)
![](Pasted%20image%2020250701150040.png)
依然报错
![](Pasted%20image%2020250701150320.png)
点运行


