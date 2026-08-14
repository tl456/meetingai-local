# Privacy

MeetingAI Local 以本地运行和本地数据保存为优先设计，但“local-first”并不等于所有配置都自动离线。

## 本地数据

运行后可能生成：

- `data/meetings/`：会议逐字稿、事件、笔记、分析结果、导入音频等；
- `data/knowledge/`：本地知识库原文与索引；
- `config.json`：运行配置，可能包含内部网络地址；
- `secrets.json`：认证与敏感配置；
- `FIRST_RUN_PASSWORD.txt`：首次登录密码；
- `cert/`、`*.pem`、`*.key`：HTTPS 证书和私钥；
- 日志、缓存和备份。

这些内容不应提交到公开 Git 仓库。

## 可能的外部网络请求

以下能力是否联网取决于配置：

- OpenAI-compatible / 其他云端 AI Provider；
- 联网搜索；
- Pip 依赖安装；
- ModelScope / HuggingFace 模型下载；
- 软件更新 manifest。

使用云端 Provider 前，请自行确认会议数据和知识库内容是否允许发送给相应服务。

## 公开截图

当前公开截图中的会议标题、Origin、代理 Host、GPU / 数据目录等可能识别个人环境的信息已在原截图中做遮挡；发布包重新编码图片并移除了 EXIF、ICC 和 comment 元数据。
