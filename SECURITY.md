# Security

## 不要公开提交的文件

请保持以下文件/目录不进入 Git：

- `secrets.json`
- `FIRST_RUN_PASSWORD.txt`
- `config.json`
- `data/`
- `cert/`
- `*.pem`, `*.key`, `*.p12`, `*.pfx`
- 日志、备份、缓存

仓库提供的 `.gitignore` 已覆盖这些常见路径，但提交前仍应人工检查 `git status`。

## 网络暴露

默认服务可绑定 `0.0.0.0`。如果设备位于不可信网络，不要仅依赖“知道端口”作为安全措施。请使用强密码、HTTPS、可信反向代理/防火墙，并限制可访问来源。

## API Key

API Key 不应硬编码进 `meetingai.py` 或提交到 Git。优先通过本地配置/秘密文件管理，并在分享诊断日志前检查是否含 Header、Token、Host、路径或会议内容。

## 漏洞报告

公开仓库建立后，建议在 GitHub Security 中启用 Private vulnerability reporting，并在此文件补充实际维护者联系渠道。
