# backend-developer

后端开发角色与分阶段服务开发 Skill：沿真实调用链完成规划、实现和验证，数据工作保留独立专项。

## Skill 能力

| Skill | 负责什么 | 产出 |
| --- | --- | --- |
| [sprite-backend-developer-services](skills/sprite-backend-developer-services/SKILL.md) | 总流程、阶段选择和执行标准 | 明确当前阶段与完成条件 |
| [sprite-backend-developer-plan](skills/sprite-backend-developer-plan/SKILL.md) | 范围、调用链、契约影响与实施安排 | 可直接实施的依据，按需计划/任务表 |
| [sprite-backend-developer-implement](skills/sprite-backend-developer-implement/SKILL.md) | 服务、API、后台任务与集成实现 | 实际代码、适用契约与测试 |
| [sprite-backend-developer-verify](skills/sprite-backend-developer-verify/SKILL.md) | 运行检查、审查差异与交接 | 真实验证结果和实现说明 |
| [sprite-backend-developer-data](skills/sprite-backend-developer-data/SKILL.md)（可选） | 一致性、查询、事务与已授权数据变化 | 数据问题的代码/方案/执行记录 |

```text
skills/
├── sprite-backend-developer-services/
│   ├── SKILL.md
│   ├── references/      工作方法、边界授权、集成恢复与交付
│   └── assets/templates/  完整实施计划、任务和说明模板
├── sprite-backend-developer-plan/
│   └── SKILL.md
├── sprite-backend-developer-implement/
│   └── SKILL.md
├── sprite-backend-developer-verify/
│   └── SKILL.md
└── sprite-backend-developer-data/   可独立安装的数据专项
    ├── SKILL.md
    └── references/      数据方法、查询一致性与变更恢复
```

默认安装总流程和三个阶段，保持四个同级目录。阶段各有完整输入、步骤、输出和完成检查，共用 `sprite-backend-developer-services/references/` 与 `assets/`。数据专项按实际任务选择，可独立使用。

## 工作顺序

```text
请求 / 验收 / 真实契约
        │
PLAN    sprite-backend-developer-plan       → 最小完整改动与检查安排
        │
BUILD   sprite-backend-developer-implement  → 代码、契约、测试
        │
VERIFY  sprite-backend-developer-verify     → 真实结果与实现说明
        └─ 实现问题 → 修复 → 复验

需要深化的数据问题 → sprite-backend-developer-data
```

已有充分依据直接实现，已有改动直接验证；小改动不强建三份文档。框架、库与工具选择属于当前已授权开发的本职工作，普通选择简述理由，无须等架构师先出选型文件；只暂停依赖未决事项的部分。

## 直接使用

> 用 `$sprite-backend-developer-services` 按现有接口约定完成这次改动，覆盖关键失败路径并报告实际验证结果。

> 用 `$sprite-backend-developer-plan` 理清这次后端改动的范围、顺序和验证方法。

> 用 `$sprite-backend-developer-implement` 按已确认方案实现服务和测试。

> 用 `$sprite-backend-developer-verify` 检查这份改动并交付真实验证结果。

> 用 `$sprite-backend-developer-data` 定位这个事务、查询或数据变更问题。

客户端不支持 `$` 调用时，让 AI 读取保存的同名 `SKILL.md`；也可直接使用 [后端开发角色](templates/agent.md)。读取说明、保存资源、实际加载、启动原生子代理和执行任务分别按真实结果判断。

## 接入当前项目

```text
请读取 https://github.com/ai-sprites/backend-developer 的 README 和接入手册，将 sprite-backend-developer 角色及 sprite-backend-developer-services、sprite-backend-developer-plan、sprite-backend-developer-implement、sprite-backend-developer-verify 四个完整 Skill 接入当前项目。
固定同一明确版本，原样复制角色、全部 SKILL.md、参考与模板，保持四个同级目录、名称和内部相对引用；只适配当前客户端目录、元数据和入口。保留项目规则、自定义和未选资源，不合并阶段、不用摘要替代原文；数据专项按明确请求或实际任务需要完整接入。
资料来源和业务仓库已有选择就沿用，缺项合并用白话问一次，可稍后配置。业务文档和附件统一放业务仓库 docs/backend-developer/；跨 Git 确有需要时按手册补齐 bridge 并告知，不另外索取安装确认。
完成后核对实际文件、引用、采用版本和加载状态。旧版按手册保护自定义并补齐阶段；只有聊天权限时明确未写入项目，读取不到原文就说明缺项。
```

[接入手册](docs/installation.md) 说明完整安装、旧版升级与加载检查，用户无需执行安装命令。角色可自由组合，也可只安装所需能力及其依赖。

## 产物与交接

交付实际服务代码、相应测试和实现说明，写清契约/数据影响、精确检查、限制与下一步。计划按复杂度需要，任务表有排序或分工价值才建，小改动可直接在回复说明。

业务文档和必要附件统一放业务仓库 `docs/backend-developer/`，可按功能分组；源码、测试、迁移、配置和构建输出保持工程原目录。旧产物保留有效内容迁入、避免覆盖，同步引用与已有索引。详见 [模板与交付](skills/sprite-backend-developer-services/references/delivery.md) 和 [产物交接](docs/artifact-handoff.md)。

资料 host repo、版本和功能/文件由用户指定或沿用项目约定；普通本地资料与纯接入不安装 bridge，确需跨 Git 读取、固定版本、比较或留存时复用或补齐。更新、追加和移除只处理指定范围，保护自定义，见 [维护规则](docs/installation.md#已有内容与后续维护)。

## 完整资源

<details>
<summary>角色、阶段、共享参考与模板清单</summary>

清单对应当前页面或 checkout 版本。接入固定完整 Git 提交后读取同批资源；历史 **v0.2.0** 可明确选用，以该标签内容为准。安装资源不等于生成全部业务文档。

| 资源 | 用途 | 接入范围 |
| --- | --- | --- |
| [templates/agent.md](templates/agent.md) | 职责、任务路由与边界 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-data/SKILL.md](skills/sprite-backend-developer-data/SKILL.md) | 独立 Skill 入口 | 使用数据专项时完整接入 |
| [skills/sprite-backend-developer-data/references/changes.md](skills/sprite-backend-developer-data/references/changes.md) | 工作方法与专业参考 | 使用数据专项时完整接入 |
| [skills/sprite-backend-developer-data/references/consistency-query.md](skills/sprite-backend-developer-data/references/consistency-query.md) | 工作方法与专业参考 | 使用数据专项时完整接入 |
| [skills/sprite-backend-developer-data/references/workflow.md](skills/sprite-backend-developer-data/references/workflow.md) | 工作方法与专业参考 | 使用数据专项时完整接入 |
| [skills/sprite-backend-developer-implement/SKILL.md](skills/sprite-backend-developer-implement/SKILL.md) | 独立 Skill 入口 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-plan/SKILL.md](skills/sprite-backend-developer-plan/SKILL.md) | 独立 Skill 入口 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/SKILL.md](skills/sprite-backend-developer-services/SKILL.md) | 独立 Skill 入口 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/assets/templates/implementation-notes.md](skills/sprite-backend-developer-services/assets/templates/implementation-notes.md) | 完整产物模板 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/assets/templates/implementation-plan.md](skills/sprite-backend-developer-services/assets/templates/implementation-plan.md) | 完整产物模板 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/assets/templates/implementation-tasks.md](skills/sprite-backend-developer-services/assets/templates/implementation-tasks.md) | 完整产物模板 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/references/boundaries-auth.md](skills/sprite-backend-developer-services/references/boundaries-auth.md) | 工作方法与专业参考 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/references/delivery.md](skills/sprite-backend-developer-services/references/delivery.md) | 工作方法与专业参考 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/references/integrations.md](skills/sprite-backend-developer-services/references/integrations.md) | 工作方法与专业参考 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-services/references/workflow.md](skills/sprite-backend-developer-services/references/workflow.md) | 工作方法与专业参考 | 随角色默认完整接入 |
| [skills/sprite-backend-developer-verify/SKILL.md](skills/sprite-backend-developer-verify/SKILL.md) | 独立 Skill 入口 | 随角色默认完整接入 |

</details>
