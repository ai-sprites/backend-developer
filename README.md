# backend-developer

独立后端开发角色：实现服务、接口与数据访问，按需选装实践。

## 复制到 AI 聊天

把下面这段粘贴到当前项目的 AI 聊天，让 AI 读取手册、自行识别客户端并放置资源。

```text
请阅读 https://github.com/ai-sprites/backend-developer 的 README、详细接入手册和资源清单，将 sprite-backend-developer 接入当前项目。
请自行识别当前客户端与项目已有约定，读取同一明确版本的资源，选择实际支持的位置和格式，保留已有规则与我的修改。默认只接入角色，实践按我的明确请求添加。
请完成文件放置和引用检查，再说明实际保存位置、采用版本及如何使用。只有聊天权限时先在本会话使用说明，如实说明没有写入项目；不能读取链接时再请我提供正文。
```

**[详细接入手册](docs/installation.md)** 说明 AI 如何选择资源、识别客户端、放置文件、处理已有内容和验证结果。用户无需执行安装命令，也无需先填写初始化选项。

## 资源清单

本版资源为 **v0.2.0**。角色主源独立可用；选中某项实践时，保留它的整个目录和相对引用。

| 资源 | 用途 | 接入范围 |
| --- | --- | --- |
| [templates/agent.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/templates/agent.md) | 角色主源 | 默认接入 |
| [skills/sprite-backend-developer-data/SKILL.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/skills/sprite-backend-developer-data/SKILL.md) | 数据变更入口 | 选中 `sprite-backend-developer-data` 时一同保存 |
| [skills/sprite-backend-developer-data/references/changes.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/skills/sprite-backend-developer-data/references/changes.md) | 数据变更配套参考 | 选中 `sprite-backend-developer-data` 时一同保存 |
| [skills/sprite-backend-developer-data/references/consistency-query.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/skills/sprite-backend-developer-data/references/consistency-query.md) | 数据变更配套参考 | 选中 `sprite-backend-developer-data` 时一同保存 |
| [skills/sprite-backend-developer-services/SKILL.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/skills/sprite-backend-developer-services/SKILL.md) | 服务开发入口 | 选中 `sprite-backend-developer-services` 时一同保存 |
| [skills/sprite-backend-developer-services/references/boundaries-auth.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/skills/sprite-backend-developer-services/references/boundaries-auth.md) | 服务开发配套参考 | 选中 `sprite-backend-developer-services` 时一同保存 |
| [skills/sprite-backend-developer-services/references/integrations.md](https://github.com/ai-sprites/backend-developer/blob/v0.2.0/skills/sprite-backend-developer-services/references/integrations.md) | 服务开发配套参考 | 选中 `sprite-backend-developer-services` 时一同保存 |

可以直接说：“再帮我添加 `sprite-backend-developer-data`，保留整个实践目录，其他内容不动。”也可只接入实践。

接入手册和 [工具适配说明](docs/tool-support.md) 用于指导操作，不必复制成业务文档。

## 开始使用

完成接入后，直接向 AI 描述任务，例如：

> 请用 sprite-backend-developer，按现有服务和接口约定实现这次改动，覆盖关键失败路径，报告实际验证结果。

客户端没有自动加载时，让 AI 先读取保存的角色文件或 Skill 入口。读取说明、写入项目和启动原生子代理是不同结果，按实际完成情况判断。

角色以当前请求和项目已有约定为依据；待确定项只影响依赖它的工作，不要求其他角色、完整 PRD 或固定流程。

## 后续维护

需要追加、更新或移除资源时，直接说明目标。AI 对照明确版本与现有文件比较，保留自定义，只处理指定范围；具体规则见 [手册](docs/installation.md#已有内容与后续维护)。

需要读取共享 Git 资料时，可单独使用 [artifact-bridge](https://github.com/ai-sprites/artifact-bridge)。
