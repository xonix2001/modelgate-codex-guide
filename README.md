# 小黄AI中转站

> 从账号、额度、API 密钥到 CC Switch，一条清晰路径完成 Codex 接入。

[![服务入口](https://img.shields.io/badge/ModelGate-进入控制台-2563EB?style=for-the-badge)](https://api.modelgate.website)
[![购买兑换码](https://img.shields.io/badge/兑换码-前往购买-111827?style=for-the-badge)](https://shop.modelgate.website)
[![接入方式](https://img.shields.io/badge/Codex-CC%20Switch-22C55E?style=for-the-badge)](docs/connection-guide.md)

注册、兑换额度、创建密钥，再通过 CC Switch 导入配置。

![ModelGate 控制台与 CC Switch 接入展示](site/assets/create-key-public.png)

## 你可以用它做什么

| 清晰的接入路径 | CC Switch 快速导入 | 中文图文教程 |
| --- | --- | --- |
| 账号、额度、密钥集中管理 | 从控制台导入并启用配置 | 每一步都有脱敏截图可核对 |
| [进入 API 控制台](https://api.modelgate.website) | [下载 CC Switch](https://github.com/farion1231/cc-switch/releases) | [查看完整教程](docs/connection-guide.md) |



## 三步开始

1. 打开 [ModelGate API 控制台](https://api.modelgate.website)，注册并登录；需要额度时前往 [兑换码商店](https://shop.modelgate.website)。
2. 创建 API 密钥、选择对应号池，然后点击“导入到 CCS”。
3. 在 CC Switch 中启用配置，彻底退出并重新打开 Codex。

完整操作、安装地址和故障排查见 **[图文接入教程](docs/connection-guide.md)**，也可打开 **[宣传与教程页面](site/index.html)**。

<details>
<summary><strong>展开查看接入截图</strong></summary>

### 1. 兑换额度

![兑换额度](site/assets/redeem-public.png)

### 2. 创建并导入密钥

![创建 API 密钥](site/assets/create-key-public.png)

### 3. 使用密钥

![使用 API 密钥](site/assets/use-key-public.png)

### 4. 在 CC Switch 中启用

![启用配置](site/assets/enable-public.png)

</details>

## 已验证范围

| 项目 | 当前说明 |
| --- | --- |
| API 控制台 / Base URL | `https://api.modelgate.website` |
| 兑换码购买 | `https://shop.modelgate.website` |
| 已验证客户端流程 | CC Switch → Codex |
| 平台 | Windows、macOS（以客户端实际支持范围为准） |

本仓库展示并记录 ModelGate / Sub2API 的接入方式，不包含 API 中转后端源码，也不是 OpenAI、Codex 或 CC Switch 的官方项目。其他客户端、模型与原始 HTTP 路径请以控制台当前文档为准。


更多说明见 [SECURITY.md](SECURITY.md)。文档采用 [MIT License](LICENSE)，第三方名称、商标和界面归各自权利人所有。
