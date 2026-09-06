# ModelGate / Sub2API Codex 接入指南

一份面向中文用户的公开接入指南：通过 **CC Switch** 将 **ModelGate / Sub2API** 配置给 **Codex** 使用。

> 本仓库目前只包含使用教程和静态教程页，不包含 API 中转站后端源码，也不是 OpenAI、Codex 或 CC Switch 的官方项目。

## 适用场景

- 已获得 ModelGate / Sub2API 账号和额度，希望在 Codex 中使用；
- 希望借助 CC Switch 完成客户端配置，避免手工编辑本地配置文件；
- 需要一份带脱敏截图的中文操作说明。

## 已确认的服务与客户端

| 项目 | 地址或说明 |
| --- | --- |
| API 控制台 / Base URL | `https://api.modelgate.website` |
| 兑换码购买 | `https://shop.modelgate.website` |
| 已验证的接入流程 | CC Switch → Codex |
| 支持平台 | Windows、macOS（以 Codex 与 CC Switch 的实际支持范围为准） |

仓库现有材料只验证了 **Codex + CC Switch** 的接入流程。其他协议、SDK、模型名称或原始 HTTP 路径请以服务控制台中的最新文档为准，本仓库不做未经验证的兼容性承诺。

## 快速开始

1. 安装 [Codex](https://chatgpt.com/download/) 和 [CC Switch](https://github.com/farion1231/cc-switch/releases)。
2. 打开 [ModelGate API 控制台](https://api.modelgate.website)，注册并登录。
3. 如需充值，在控制台“兑换”页面输入已购买的兑换码。
4. 在“API 密钥”页面创建密钥并选择对应号池。
5. 点击“导入到 CCS”，在 CC Switch 中启用 ModelGate 配置。
6. 彻底退出并重新打开 Codex。

完整图文步骤见 [docs/connection-guide.md](docs/connection-guide.md)，也可直接打开静态教程页 [site/index.html](site/index.html)。

## 配置示例

[`.env.example`](.env.example) 仅用于说明公开 Base URL 与密钥占位方式：

```dotenv
MODEL_GATE_BASE_URL=https://api.modelgate.website
MODEL_GATE_API_KEY=replace-with-your-own-key
```

CC Switch 的推荐操作是从控制台点击“导入到 CCS”。由于本仓库没有足够材料确认服务当前的原始 REST 路径、请求体和可用模型，因此不提供可能误导用户或触发真实上游调用的 `curl` 示例。请在控制台文档中复制与你的账号和模型对应的请求示例。

## 教程导航

- [完整接入教程](docs/connection-guide.md)
- [可直接浏览的静态教程页](site/index.html)
- [安全说明](SECURITY.md)

## 常见问题

### 导入后 Codex 没有使用新配置

仅关闭窗口可能不会结束进程。请在 Windows 任务管理器或 macOS 菜单栏中彻底退出 Codex，再重新打开。

### 可以把密钥发到 Issue 里排查吗？

不可以。请勿在 Issue、截图、日志或提交中公开 API 密钥、兑换码、账号信息和完整请求记录。需要展示配置时，请使用 `sk-demo...demo` 等明显无效的占位值。

### 本仓库能部署一个中转站吗？

不能。仓库不包含服务端程序，只提供现有服务的客户端接入说明。

### 其他客户端或 OpenAI SDK 是否可用？

现有材料无法确认。请以 ModelGate 控制台当前文档为准，并注意第三方服务条款、数据处理方式和费用规则。

## 安全与使用须知

- 第三方服务会处理你发送的请求；使用前确认其隐私政策、服务条款及所在团队的合规要求。
- API 密钥等同于凭证，不要提交到 GitHub、粘贴到公开讨论区或共享截图。
- 本仓库中的截图均使用示例值；界面可能随服务更新而变化。
- 购买、兑换和实际 API 调用可能产生费用，请自行核对计费和退款规则。

## License

[MIT](LICENSE)。文档中出现的第三方名称、商标和界面归各自权利人所有。
