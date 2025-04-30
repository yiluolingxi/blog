###  MetaMask (and other injected providers)
这段代码的功能是根据用户是否安装了 MetaMask 来选择合适的以太坊提供者。如果没有安装 MetaMask，则使用默认的只读提供者；如果安装了 MetaMask，则使用 MetaMask 提供的提供者，并请求签名者以便进行写操作。

**定义变量：**
```js
let signer = null;
let provider;
```

**检查 MetaMask 是否安装：**
```js
if (window.ethereum == null) {
```

 `window.ethereum` 是 MetaMask 注入到浏览器中的对象。如果它不存在，表示用户没有安装 MetaMask。
 
**MetaMask 未安装的情况：**
```js
console.log("MetaMask not installed; using read-only defaults")
provider = ethers.getDefaultProvider()
```
如果 MetaMask 未安装，代码会输出一条信息到控制台，并使用 `ethers.getDefaultProvider()` 创建一个默认的提供者。这种提供者是只读的，只能进行读取操作，不能进行写入操作（如发送交易）。

**MetaMask 已安装的情况：**
```js
} else {
    provider = new ethers.BrowserProvider(window.ethereum)
    signer = await provider.getSigner();
}```

如果 MetaMask 已安装：

- `provider = new ethers.BrowserProvider(window.ethereum)`：创建一个 `BrowserProvider` 对象，它使用 MetaMask 提供的 EIP-1193 标准接口来与以太坊区块链进行交互。
- `signer = await provider.getSigner()`：请求一个签名者（signer）。签名者是一个可以执行写入操作（如发送交易）的对象，它使用用户 MetaMask 中的私钥进行签名。  

### Custom RPC Backend
这段代码的前提是你已经有一个运行中的以太坊节点，并且可以通过 JSON-RPC 接口进行访问。这个节点可以是本地的（例如使用 `geth` 或 `besu` 等以太坊客户端在本地运行），也可以是远程的（例如通过 Infura 或 Alchemy 提供的节点服务）。  





