# backend-developer

独立后端开发角色：实现服务、接口与数据访问，按需选装实践。

## 复制到 AI 聊天

把下面这段粘贴到当前项目的 AI 聊天，让 AI 读取手册、自行识别客户端并放置资源。

```text
请阅读 https://github.com/ai-sprites/backend-developer 的 README、详细接入手册和资源清单，将 sprite-backend-developer 接入当前项目。
请自行识别当前客户端与项目已有约定，读取同一明确版本的资源，选择实际支持的位置和格式，保留已有规则与我的修改。默认只接入角色，实践按我的明确请求添加；当前任务确需资料桥接时按手册自动补齐并告知我，无需再单独确认安装。
接入时请主动确认本次角色、上游资料 host repo 和产物保存 repo/目录；已明确的不重问，只把缺项合并为一次自然语言询问，允许我回答“暂无/稍后配置”。先完成角色接入，不因业务未定阻塞；真正读取时再补所需版本、功能或文件路径。
请完成文件放置和引用检查，再说明实际保存位置、采用版本及如何使用。只有聊天权限时先在本会话使用说明，如实说明没有写入项目；不能读取链接时再请我提供正文。
```

**[详细接入手册](docs/installation.md)** 说明 AI 如何选择资源、识别客户端、放置文件、处理已有内容和验证结果。用户无需执行安装命令；资料位置会主动引导确认，也可稍后配置。

## 资源清单

本清单对应当前阅读的仓库版本，资源链接随该页面或 checkout 的版本变化。接入时先固定为一个完整 Git 提交，再读取该提交的同批资源。历史 **v0.2.0** 仍可明确选用，但内容以该标签为准。角色主源独立可用；选中某项实践时，保留它的整个目录和相对引用。

| 资源 | 用途 | 接入范围 |
| --- | --- | --- |
| [templates/agent.md](templates/agent.md) | 角色主源 | 默认接入 |
| [skills/sprite-backend-developer-data/SKILL.md](skills/sprite-backend-developer-data/SKILL.md) | 数据变更入口 | 选中 `sprite-backend-developer-data` 时一同保存 |
| [skills/sprite-backend-developer-data/references/changes.md](skills/sprite-backend-developer-data/references/changes.md) | 数据变更配套参考 | 选中 `sprite-backend-developer-data` 时一同保存 |
| [skills/sprite-backend-developer-data/references/consistency-query.md](skills/sprite-backend-developer-data/references/consistency-query.md) | 数据变更配套参考 | 选中 `sprite-backend-developer-data` 时一同保存 |
| [skills/sprite-backend-developer-services/SKILL.md](skills/sprite-backend-developer-services/SKILL.md) | 服务开发入口 | 选中 `sprite-backend-developer-services` 时一同保存 |
| [skills/sprite-backend-developer-services/references/boundaries-auth.md](skills/sprite-backend-developer-services/references/boundaries-auth.md) | 服务开发配套参考 | 选中 `sprite-backend-developer-services` 时一同保存 |
| [skills/sprite-backend-developer-services/references/integrations.md](skills/sprite-backend-developer-services/references/integrations.md) | 服务开发配套参考 | 选中 `sprite-backend-developer-services` 时一同保存 |

可以直接说：“再帮我添加 `sprite-backend-developer-data`，保留整个实践目录，其他内容不动。”也可只接入实践。

接入、加载检查和用户需要完成的步骤统一见 [接入手册](docs/installation.md)，不复制成业务文档。

## 开始使用

完成接入后，直接向 AI 描述任务，例如：

> 请用 sprite-backend-developer，按现有服务和接口约定实现这次改动，覆盖关键失败路径，报告实际验证结果。

客户端没有自动加载时，让 AI 先读取保存的角色文件或 Skill 入口。读取说明、写入项目和启动原生子代理是不同结果，按实际完成情况判断。

角色以当前请求和项目已有约定为依据；待确定项只影响依赖它的工作，不要求其他角色、完整 PRD 或固定流程。

## 留存与交接

实现或修复任务交付实际服务代码、相应测试和实现说明，说明契约与数据影响、真实检查、限制与下一步。 内容详略随任务调整，沿用已有文档；小改动可直接在回复中说明；完整功能或需要交接时保存到你指定的业务仓库/目录，并给出真实链接。已有文件优先；没有位置约定时可用 `docs/artifacts/<feature-id>/backend.md`。角色安装目录与业务产物目录分开。

角色可以自由组合；资料 host repo、版本和功能或文件由你指定，已有项目约定就沿用。当前任务确需跨 Git 读取、固定版本、比较或留存时，AI 会复用或按需补齐 artifact-bridge；普通本地资料和纯角色接入不安装它。目录、Git 与认证条件见 [产物交接说明](docs/artifact-handoff.md)。

## 后续维护

需要追加、更新或移除资源时，直接说明目标。AI 对照明确版本与现有文件比较，保留自定义，只处理指定范围；具体规则见 [手册](docs/installation.md#已有内容与后续维护)。
