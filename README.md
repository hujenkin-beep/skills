# Skills 仓库

这个仓库用于集中存放可复用的 Codex skills。以后每个 skill 都应放在独立目录中，并至少包含一个 `SKILL.md`，用于描述触发场景、执行流程和领域规则。

## 当前 Skills

| Skill | 显示名称 | 用途 |
| --- | --- | --- |
| [`wechat-miniapp-name-generator`](./wechat-miniapp-name-generator/SKILL.md) | 微信小程序起名 | 根据小程序背景、核心功能、目标用户和要解决的问题，生成微信搜索友好的中文小程序名称。 |

## wechat-miniapp-name-generator

`wechat-miniapp-name-generator` 是一个微信小程序命名技能。它把小程序名称视为微信搜索优化决策，而不是单纯的品牌口号，优先推荐关键词清晰、功能明确、符合微信命名约束的名称。

适用场景：

- 为新的微信小程序生成候选名称。
- 优化已有小程序名称，让核心搜索词更靠前。
- 生成小程序简称建议。
- 编写能自然覆盖关键词的简介文案。
- 按微信小程序命名规则检查合规风险。
- 评估已有名称是否过于抽象、泛化、难搜索或可能侵权。

常见输入：

- 产品背景：小程序为什么存在，服务什么场景。
- 基础功能：用户可以在小程序里完成什么操作。
- 解决的问题：对应的痛点、任务或目标结果。
- 目标用户或使用场景：谁在什么情况下使用。
- 可选约束：品牌词、语气、行业、已有名称、不可用名称或期望关键词。

主要输出：

- 一句话用户任务总结。
- 关键词地图。
- 排序后的候选名称表。
- 最佳 3 个名称及定位说明。
- 简称建议。
- 小程序简介文案。
- 微信后台提交前的核验清单。

相关文件：

- [`wechat-miniapp-name-generator/SKILL.md`](./wechat-miniapp-name-generator/SKILL.md)：技能主体，包含命名原则、工作流程、规则快照、评分清单和输出格式。
- [`wechat-miniapp-name-generator/agents/openai.yaml`](./wechat-miniapp-name-generator/agents/openai.yaml)：OpenAI 代理界面配置，包含显示名称、简介和默认提示词。
- [`wechat-miniapp-name-generator/agents/openai-yaml-analysis.md`](./wechat-miniapp-name-generator/agents/openai-yaml-analysis.md)：`openai.yaml` 的字段分析文档。

## 新增 Skill 约定

新增 skill 时建议使用以下目录结构：

```text
skill-name/
  SKILL.md
  agents/
    openai.yaml
```

新增后请同步更新本 README 的“当前 Skills”表格，并用一小节说明该 skill 的用途、适用场景、输入输出和关键文件。
