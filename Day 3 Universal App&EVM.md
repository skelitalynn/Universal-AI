# Day 3 Universal App&EVM

### 一、今日学习目标

- 什么是 Universal Blockchain（通用区块链）
- 什么是 Universal EVM / Universal App
- 什么是 Omnichain Smart Contract
- ZetaChain 在整个多链世界中的位置
- Gateway 在其中的作用

## 二、核心概念理解

### 1. 什么是 Universal Blockchain（通用区块链）

传统的区块链中每一条链的生态是封闭的

比如：ETH 上的资产不能直接被 Solana 使用；BTC 资产无法直接参与以太坊的 DeFi；每条链都需要单独写合约、部署、维护

而 Universal Blockchain 的目标就是打破链与链之间的隔离，让资产、数据、操作可以跨链流动。

ZetaChain 就扮演这个“连接者”的角色，使得开发者可以：

- 不用关心用户在什么链上
- 不用为每条链写一套代码
- 用一套逻辑，操控多条链

### 2. 什么是 Universal App（通用应用）

传统 DApp 的问题是它们只跑在某一条链上，比如：

- Uniswap → 只能在以太坊 / L2
- Magic Eden → 只服务于 Solana 生态

而 Universal App 是：一种可以同时与多条链交互的应用，不被单一链限制。

在 ZetaChain 上，一个 Universal App 可以：

- 接收 BTC
- 操作 ETH 合约
- 与 Solana 交互
- 在同一个程序逻辑里完成跨链行为

更重要的一点是**开发者只需要编写一次，而不是为每条链重复开发。**

因此我理解：Universal App = 一种跨链原生应用

### 3. 什么是 Universal EVM

EVM（Ethereum Virtual Machine）本来只为以太坊服务。

而 Universal EVM 是：由 ZetaChain 提供的、能“理解并控制多条链”的虚拟执行环境。

开发者写的合约，其实是在 Universal EVM 中运行，而这个 EVM 会负责与：

- Ethereum
- Bitcoin
- Solana
- Sui
- Ton 等

进行交互。

### 4. 什么是 Omnichain Smart Contract

Omnichain Smart Contract 指的是一个可跨多条链生效的智能合约。一般的智能合约只在一条链上有效，而 Omnichain 合约可以在 ZetaChain 上部署一次，然后它可以通过 Gateway 与多条链发生交互。

### 5. Gateway 是干嘛的？

Gateway 是一个非常关键的组件，它负责：

- 连接 ZetaChain 与外部链
- 接收和发送跨链信息
- 保证跨链操作的安全与一致性

## 三、为什么在 ZetaChain 上开发是有价值的？

我总结出三个主要原因：

1. **技术维度：**
    它解决的是一个真实、长期存在的问题：链与链之间不互通
2. **成本维度：**
    开发者只需要维护一套代码，避免多链开发的地狱
3. **未来趋势：**
    世界不会只剩一条链，多链共存是必然趋势
    ZetaChain 天生符合未来结构

### 四、 架构图

![image-20251126110604999](C:\Users\86183\AppData\Roaming\Typora\typora-user-images\image-20251126110604999.png)