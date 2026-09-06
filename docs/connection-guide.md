# ModelGate / Sub2API 接入 Codex

本教程说明如何在 ModelGate / Sub2API 控制台创建 API 密钥，并通过 CC Switch 导入到 Codex。截图中的账号、余额、兑换码和密钥均已替换为无效示例。

## 1. 使用前确认

在接入任何第三方服务前，请确认相关服务的使用符合所在团队的安全要求、公司制度以及对应平台的服务条款。涉及账号、密钥和数据的操作，请由授权人员在授权设备上完成。

- API 控制台：<https://api.modelgate.website>
- 兑换码购买：<https://shop.modelgate.website>
- 客服 QQ 群：`176498720`

## 2. 准备环境

### 安装 Codex

- 官方下载：<https://chatgpt.com/download/>
- 项目原教程提供的第三方镜像：<https://codexapp.agentsmirror.com/>

优先使用官方下载渠道。第三方镜像不由本仓库维护，请自行判断来源可信度。

### 安装 CC Switch

从 [CC Switch Releases](https://github.com/farion1231/cc-switch/releases) 下载与你的操作系统匹配的当前版本。原教程使用的是 v3.16.5，但 GitHub Releases 页面更适合获取后续修复版本。

## 3. 兑换额度

注册并登录控制台，点击左侧“兑换”，输入已购买的兑换码并提交。

![在兑换页面输入示例兑换码](../site/assets/redeem-public.png)

> 不要在截图、Issue 或聊天记录中公开真实兑换码。

## 4. 创建 API 密钥

打开“API 密钥”，点击“创建密钥”，并按你的订阅或使用范围选择对应号池。

![创建 API 密钥](../site/assets/create-key-public.png)

密钥生成后请立即妥善保存，不要提交到本仓库。

## 5. 导入 CC Switch

在密钥列表中找到目标密钥，点击“导入到 CCS”。

![将示例密钥导入 CC Switch](../site/assets/use-key-public.png)

如果浏览器询问是否打开 CC Switch，请确认目标地址和应用名称后再继续。

## 6. 启用并重启 Codex

在 CC Switch 的 Codex 页面选择 ModelGate 配置并启用。

![在 CC Switch 中启用 ModelGate](../site/assets/enable-public.png)

随后彻底退出 Codex：

- Windows：在任务管理器中确认 Codex 进程已经结束；
- macOS：从菜单栏或 Dock 完全退出应用。

重新打开 Codex 后，新的配置才会生效。

## 排查清单

- 确认启用的是 Codex 页签下的 ModelGate 配置；
- 确认 Base URL 为 `https://api.modelgate.website`；
- 确认密钥没有多余空格且仍处于启用状态；
- 确认 Codex 已彻底退出并重新启动；
- 不要把真实密钥、兑换码或完整请求日志贴到公开 Issue。

[返回 README](../README.md)
