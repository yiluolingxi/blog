### 总结

1. **创建项目文件夹并初始化 npm 项目。**
2. **安装 `ethers` 库。**
3. **创建 `index.js` 文件并编写代码。**
4. **配置 `package.json` 以支持 ES Modules。**
5. **运行代码。**

要在 VSCode 中运行这个简单的 Ethers.js 程序，查询 Vitalik 的 ETH 余额并输出到控制台，请按照以下步骤操作：

1. **确保已经安装 Node.js 和 npm：**
    
    - 如果还没有安装，请前往 [Node.js 官方网站](https://nodejs.org/) 下载并安装 Node.js。安装 Node.js 时会自动安装 npm（Node Package Manager）。
2. **打开 VSCode 并创建项目文件夹：**
    
    - 在你的文件系统中创建一个新的文件夹，比如 `hello-vitalik`。
    - 启动 VSCode，选择 `File` -> `Open Folder...`，然后选择刚刚创建的文件夹。
3. **初始化 npm 项目：**
    
    - 打开 VSCode 内置终端，选择 `Terminal` -> `New Terminal`，或者使用快捷键 `Ctrl+`（或 `Cmd+` on macOS）。
    - 在终端中运行以下命令初始化一个新的 npm 项目：
    ```sh
    npm init -y
    ```
    
4. **安装 ethers 库：**
    
    - 在 VSCode 的终端中运行以下命令来安装 `ethers` 库：
```sh
npm install ethers --save
```

5. **创建并编写 JavaScript 文件：**
    
    - 在 VSCode 中创建一个新的 JavaScript 文件，例如 `index.js`。
    - 将以下代码粘贴到 `index.js` 文件中：
```js
import { ethers } from "ethers";

const provider = ethers.getDefaultProvider();

const main = async () => {
    const balance = await provider.getBalance(`vitalik.eth`);
    console.log(`ETH Balance of vitalik: ${ethers.formatEther(balance)} ETH`);
}

main();
```

6. **配置 Node.js 支持 ES Modules：**
    
    - 默认情况下，Node.js 使用 CommonJS 模块（`require` 和 `module.exports`），而不是 ES Modules（`import` 和 `export`）。
    - 要使用 ES Modules，需要在 `package.json` 文件中添加 `"type": "module"`：
```json
{
  "name": "hello-vitalik",
  "version": "1.0.0",
  "main": "index.js",
  "type": "module",  // 添加这一行
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "ethers": "^5.0.0"  // 这里会显示你安装的 ethers 版本
  }
}

```

7. **运行代码：**
    
    - 在终端中运行以下命令来执行你的 `index.js` 文件：
```sh
node index.js
```

这样，你的程序就会连接到以太坊网络，查询 Vitalik 的 ETH 余额，并将结果输出到控制台。

## 用`ethers`编写第一个程序`HelloVitalik`
查询Vitalik的`ETH`余额，并输出在`console`中。整个程序只需要6行

### 1. 导入`ethers`
```js
import { ethers } from "ethers";
```
### 2. 连接以太坊
```js
const provider = ethers.getDefaultProvider();
```
是使用 Ethers.js 库来创建一个默认的提供者（provider），用于与以太坊区块链进行交互。

1. **`ethers.getDefaultProvider()`：**
    
    - `getDefaultProvider()` 是 Ethers.js 库中的一个方法，用于创建一个默认的 `Provider` 实例。
    - 这个默认的提供者会自动连接到以太坊主网，并使用多个第三方服务（例如 Infura、Etherscan、Alchemy 等）来提供冗余和容错功能。
    - 默认提供者会根据网络的负载和性能自动选择最佳的服务提供者来响应请求。
2. **`provider`：**
    
    - `provider` 是一个 `Provider` 实例，代表了与以太坊区块链的连接。
    - 你可以使用 `provider` 来执行各种读取操作，比如查询区块链状态、读取合约数据、获取账户余额等。

### 3. 声明`async`函数
由于和区块链交互不是实时的我们需要用到js的`async/await`语法糖。  
每次和链交互的调用需要用到`await`，再把这些用`async`函数包裹起来，最后再调用这个函数。
```js
const main = async () => {
    //...
}
main()
```
尤其是在使用异步操作时。  
代码的作用是定义并立即执行一个异步函数。以下是详细解释：
#### 解释代码的每个部分

1. **定义异步函数 `main`：**
```js
const main = async () => {
    // ...
}
```
这段代码使用箭头函数（Arrow Function）语法定义了一个名为 `main` 的异步函数。`async` 关键字表明这个函数是异步的，意味着它内部可以使用 `await` 来等待异步操作完成。

2. **调用函数 `main`：**
```js
main();
```
这行代码立即调用了前面定义的 `main` 函数。因为 `main` 是异步函数，它会返回一个 Promise。  

#### 异步函数和 `await` 关键字

- **异步函数**：通过在函数前面加上 `async` 关键字，函数内部就可以使用 `await` 关键字来等待异步操作的完成，而不会阻塞程序的执行。
- **`await` 关键字**：只能在异步函数中使用，它会暂停函数的执行，直到 `await` 后面的 Promise 完成，然后继续执行函数并返回结果。

#### 示例代码

以下是一个使用 `main` 函数查询 Vitalik 的 ETH 余额并输出到控制台的示例：
```js
import { ethers } from "ethers";

const provider = ethers.getDefaultProvider();

const main = async () => {
    try {
        const balance = await provider.getBalance('vitalik.eth');
        console.log(`ETH Balance of vitalik: ${ethers.formatEther(balance)} ETH`);
    } catch (error) {
        console.error('Error fetching balance:', error);
    }
}

main();
```

#### 代码的工作原理

1. **定义 `provider`**：
```js
const provider = ethers.getDefaultProvider();
```
2. **定义 `main` 函数**：
```js
const main = async () => {
    try {
        const balance = await provider.getBalance('vitalik.eth');
        console.log(`ETH Balance of vitalik: ${ethers.formatEther(balance)} ETH`);
    } catch (error) {
        console.error('Error fetching balance:', error);
    }
}
```
这个异步函数使用 `await` 关键字等待 `provider.getBalance` 返回的 Promise 解析，并输出 Vitalik 的 ETH 余额。如果获取余额时发生错误，会捕获并输出错误信息。
3. **调用 `main` 函数**：
```js
main();
```
立即调用 `main` 函数，开始执行异步操作。

#### 为什么使用这种模式？

- **简洁性**：这种模式将异步操作封装在一个函数中，使代码结构更加清晰。
- **立即执行**：定义并立即调用异步函数，使其像同步代码一样顺序执行，而不需要在全局作用域中使用 `await`（因为在顶层作用域中直接使用 `await` 需要特定环境支持，如模块化的顶层 `await`）。
- **错误处理**：可以在异步函数内部使用 `try-catch` 块来处理错误，提高代码的健壮性。

这种模式在处理异步操作（如网络请求、文件读取等）时非常常见

### 4. 获取Vitalik地址的`ETH`余额
利用`Provider`类的`getBalance()`函数来查询某个地址的`ETH`余额。  
由于`ethers`原生支持`ENS`域名，我们不需要知道具体地址，用`ENS`域名`vitalik.eth`就可以查询到以太坊创始人豚林-vitalik的余额。  
```js
const balance = await provider.getBalance(`vitalik.eth`);
```
### 5. 转换单位后在`console`中输出
从链上获取的以太坊余额以`wei`为单位，而`1 ETH = 10^18 wei`。  
我们打印在`console`之前，需要进行单位转换。    
`ethers`提供了功能函数`formatEther`，我们可以利用它将`wei`转换为`ETH`。 
```js
console.log(`ETH Balance of vitalik: ${ethers.formatEther(balance)} ETH`);
```

#### 总结

- `ethers.formatEther(balance)` 将以 Wei 为单位的余额转换为以太单位。
- 模板字符串 `${ethers.formatEther(balance)} ETH` 会插入转换后的余额。
- `console.log` 将格式化后的余额打印到控制台。

通过这种方式，可以轻松读取并输出以太坊地址的余额，便于查看和调试。

代码用于将 Vitalik 的 ETH 余额转换为人类可读的格式，并将其打印到控制台。具体来说，`ethers.formatEther(balance)` 会将 `balance`（以 Wei 为单位的余额）转换为 Ether（ETH），然后通过模板字符串将结果格式化并输出。以下是详细解释和示例输出。  

#### 详细解释

- **`balance`**: 这是一个包含以太坊余额的 `BigNumber` 对象，单位是 Wei（以太坊的最小单位）。
- **`ethers.formatEther(balance)`**: 这个函数将 `balance` 从 Wei 转换为 Ether。1 Ether 等于 10^18 Wei。
- **模板字符串**: 使用反引号（`` ` ``）和 `${}` 语法，可以在字符串中插入表达式的值。

### 假设输出

假设 Vitalik 的 ETH 余额是 1000000000000000000 Wei（即 1 ETH），则输出如下：

```js
const { ethers } = require("ethers");

const provider = ethers.getDefaultProvider();

const main = async () => {
    const balance = await provider.getBalance('vitalik.eth');
    console.log(`ETH Balance of vitalik: ${ethers.formatEther(balance)} ETH`);
}

main();
```

在这种情况下，假设 `balance` 为 `BigNumber` 对象，其值为 `1000000000000000000`（1 ETH），则：

```js
console.log(`ETH Balance of vitalik: ${ethers.utils.formatEther(balance)} ETH`);
```
#### 示例输出
```plaintext
ETH Balance of vitalik: 1.0 ETH
```

####  `BigNumber` 
从 `ethers` 库中的 `getBalance` 方法可以看出，`balance` 是一个 `BigNumber` 对象。`getBalance` 方法返回的是一个表示账户余额的 `BigNumber` 实例。`BigNumber` 是 `ethers` 库用来处理大数的类，尤其是在处理以太坊中的金额（Wei）时。  

- `provider.getBalance(address)` 方法返回一个 `Promise`，解析为一个 `BigNumber` 对象，表示给定地址的以太坊余额（以 Wei 为单位）。
- 因此，`balance` 变量是一个 `BigNumber` 实例。