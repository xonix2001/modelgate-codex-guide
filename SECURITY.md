# Security

## Reporting sensitive data exposure

如果你发现仓库中意外包含 API 密钥、兑换码、令牌、个人信息或其他敏感数据，请不要在公开 Issue 中复述该内容。请通过仓库所有者的 GitHub 个人资料联系渠道进行私下报告，并说明受影响的文件与提交。

## Credential hygiene

- 不要提交 `.env`、真实 API 密钥、兑换码或服务端配置；
- 文档和 Issue 中统一使用明显无效的占位值；
- 如果凭证曾进入 Git 历史，应立即在服务端吊销并轮换，而不是只删除当前文件。

本仓库仅为客户端接入文档，不接收或处理 API 请求。
