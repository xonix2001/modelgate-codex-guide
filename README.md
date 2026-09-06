# ModelGate：让 Codex 接入更简单

> 从账号、额度、API 密钥到 CC Switch，一条清晰路径完成 Codex 接入。

[![服务入口](https://img.shields.io/badge/ModelGate-进入控制台-2563EB?style=for-the-badge)](https://api.modelgate.website)
[![购买兑换码](https://img.shields.io/badge/兑换码-前往购买-111827?style=for-the-badge)](https://shop.modelgate.website)
[![接入方式](https://img.shields.io/badge/Codex-CC%20Switch-22C55E?style=for-the-badge)](docs/connection-guide.md)

ModelGate / Sub2API 面向希望在 Codex 中使用第三方 API 服务的中文用户。注册、兑换额度、创建密钥，再通过 CC Switch 导入配置，不需要手工翻找配置文件。

![ModelGate 控制台与 CC Switch 接入展示](site/assets/create-key-public.png)

## 你可以用它做什么

| 清晰的接入路径 | CC Switch 快速导入 | 中文图文教程 |
| --- | --- | --- |
| 账号、额度、密钥集中管理 | 从控制台导入并启用配置 | 每一步都有脱敏截图可核对 |
| [进入 API 控制台](https://api.modelgate.website) | [下载 CC Switch](https://github.com/farion1231/cc-switch/releases) | [查看完整教程](docs/connection-guide.md) |

## 调用是怎样发生的

```text
你在 Codex 中发起请求
          ↓
CC Switch 加载 ModelGate 配置
          ↓
请求发送到 api.modelgate.website
          ↓
结果返回 Codex
```

### 匿名调用动态（脱敏演示）

```text
刚刚      Codex 请求        ● 已完成
18 秒前   配置加载          ● 就绪
1 分钟前  API 请求          ● 已完成
```

上方记录用于展示服务运行时的体验，不代表实时统计，也不包含用户名、密钥、请求正文或消费金额。若后续接入可公开的匿名聚合接口，可替换为真实的调用量与成功率数据。

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

## 安全说明

- 不要在 Issue、截图、日志或提交中公开 API 密钥、兑换码、账号信息和完整请求记录。
- 第三方服务会处理发送的请求；使用前请确认隐私政策、服务条款和团队合规要求。
- 本仓库截图均已脱敏；界面可能随服务更新而变化。
- 购买、兑换和实际调用可能产生费用，请自行核对计费与退款规则。

更多说明见 [SECURITY.md](SECURITY.md)。文档采用 [MIT License](LICENSE)，第三方名称、商标和界面归各自权利人所有。
