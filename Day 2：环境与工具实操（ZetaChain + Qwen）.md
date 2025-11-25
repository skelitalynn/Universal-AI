### Day 2：环境与工具实操（ZetaChain + Qwen）

#### 1. 今日目标

- 在本地配置 ZetaChain CLI 并成功运行
- 掌握基本区块链开发工具使用方式
- 完成一次 AI 接口（Qwen）的真实调用
- 搭建 Web3 + AI 的基本技术通路

------

#### 2. ZetaChain CLI 本地部署

在本地目录执行：

- `git clone https://github.com/zeta-chain/cli.git`
- `cd cli`
- `npm install --legacy-peer-deps`

虽然过程中出现 deprecated 和 bigint 警告信息，但均不影响使用。

通过执行：

```
npx tsx src/index.ts --help
```

成功看到 CLI 的完整命令列表，包括：

- new
- faucet
- query
- chains
- tokens
- balances
- contracts
- ask...

说明：**ZetaChain 官方 CLI 工具已经在本地成功运行。**

------

#### 3. 成功使用 ZetaChain 查询网络信息

通过命令：

```
npx tsx src/index.ts query
```

成功进入 query 模块，并能够访问：

- chains
- fees
- tokens
- contracts 等链上数据入口

这意味着：
 当前设备已具备与 ZetaChain 测试网交互的能力。

------

#### 4. Qwen API 连通性实测成功

通过 Postman 请求：

- Method: POST
- URL:
   `https://dashscope.aliyuncs.com/api/v1/services/aigc/text-generation/generation`
- Headers：
  - Content-Type: application/json
  - Authorization: Bearer <我的API Key>
- Body：

```
{
  "model": "qwen-turbo",
  "input": {
    "messages": [
      {
        "role": "user",
        "content": "Hello, this is my first Qwen API request."
      }
    ]
  }
}
```

返回结果：

- HTTP 200 OK
- 成功接收到 AI 生成文本响应

![image-20251125113439425](C:\Users\86183\AppData\Roaming\Typora\typora-user-images\image-20251125113439425.png)

| Faucet                                                       | Chain / Asset                                |
| :----------------------------------------------------------- | :------------------------------------------- |
| [Google Cloud Web3](https://cloud.google.com/application/web3/faucet/zetachain/testnet) | ZetaChain ZETA                               |
| [FaucetMe](https://zetachain.faucetme.pro/)                  | ZetaChain ZETA                               |
| [Optimism](https://console.optimism.io/faucet)               | Ethereum, Base                               |
| [Chainlink](https://faucets.chain.link/)                     | Ethereum, Base, Avalanche, Arbitrum, Polygon |
| [Circle](https://faucet.circle.com/)                         | USDC                                         |
| [Solana](https://faucet.solana.com/)                         | Solana                                       |
| [Polygon](https://faucet.polygon.technology/)                | Polygon                                      |
| [Binance Smart Chain](https://testnet.binance.org/faucet-smart) | BSC                                          |
| [mempool.space](https://mempool.space/testnet4/faucet)       | Bitcoin Testnet 4                            |
| [testnet4.dev](https://faucet.testnet4.dev/)                 | Bitcoin Testnet 4                            |
| [triangleplatform.com](https://faucet.triangleplatform.com/bitcoin/testnet) | Bitcoin Testnet 4                            |
| [Signet](https://signetfaucet.com/)                          | Bitcoin Signet                               |

# Explorers

| Name               | Mainnet                                                | Testnet                                                    | Description                                                  |
| :----------------- | :----------------------------------------------------- | :--------------------------------------------------------- | :----------------------------------------------------------- |
| Blockscout         | [Mainnet](https://zetachain.blockscout.com/)           | [Testnet](https://zetachain-testnet.blockscout.com/)       | EVM block explorer that lets you search transactions, addresses, and tokens, verify and interact with smart contracts, track cross-chain activity, and access data through HTTP and GraphQL APIs. |
| ExploreMe          | [Mainnet](https://zetachain.exploreme.pro/)            | [Testnet](https://testnet.zetachain.exploreme.pro/)        | EVM and Cosmos explorer with blocks, transactions, top accounts, contracts, tokens/NFTs, validators, proposals, params/uptime/API. |
| Mintscan           | [Mainnet](https://www.mintscan.io/zeta)                | —                                                          | Cosmos explorer with blocks, transactions, accounts, validators & staking, governance proposals, and params. |
| Nodejumper         | [Mainnet](https://app.nodejumper.io/zetachain)         | —                                                          | Node operator dashboard with chain indicators and APIs, and utilities. |
| Ping.pub           | [Mainnet](https://ping.pub/zetachain)                  | [Testnet](https://testnet.ping.pub/zetachain)              | Cosmos explorer with blocks, transactions, accounts, validators, and governance proposals. |
| Polkachu           | [Mainnet](https://www.polkachu.com/networks/zetachain) | [Testnet](https://polkachu.com/testnets/zetachain)         | Node operator dashboard with RPC/API endpoints, snapshots, state-sync, upgrade watcher, tools. |
| Explorers.guru     | [Mainnet](https://zetachain.explorers.guru/)           | [Testnet](https://testnet.zetachain.explorers.guru/)       | Cosmos explorer with blocks, transactions, accounts, validators, and governance proposals. |
| Staking Explorer   | —                                                      | [Testnet](https://staking-explorer.com/explorer/zetachain) | Cosmos explorer with validators, delegations, rewards/APR, uptime, and validator analytics. |
| Liveraven Explorer | —                                                      | [Testnet](https://testnet.explorer.liveraven.net/)         | Cosmos explorer with blocks, transactions, accounts, validators, and governance proposals. |
| NodeStake          | [Mainnet](https://explorer.nodestake.org/zetachain/)   | —                                                          | Cosmos explorer with blocks, transactions, accounts, validators, and governance proposals. |
| ITRocket           | —                                                      | [Testnet](https://testnet.itrocket.net/zetachain)          | Cosmos explorer with blocks, transactions, accounts, validators, and governance proposals. |

连接测试：状态码200

![image-20251125142058445](C:\Users\86183\AppData\Roaming\Typora\typora-user-images\image-20251125142058445.png)