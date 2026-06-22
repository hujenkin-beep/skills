# openai.yaml 文件分析

## 文件位置

`wechat-miniapp-name-generator/agents/openai.yaml`

## 文件用途

该文件定义了 `wechat-miniapp-name-generator` 技能在 OpenAI 代理环境中的界面展示信息和默认调用提示词。它不是技能的核心执行逻辑，而是一个轻量入口配置，用于告诉宿主环境：

- 用户界面中如何展示该技能。
- 如何用一句话解释该技能。
- 当用户需要调用该技能时，可以使用什么默认提示词。

核心起名方法、命名约束、输出格式和校验规则位于上一级的 `wechat-miniapp-name-generator/SKILL.md`。

## 当前内容概览

```yaml
interface:
  display_name: "微信小程序起名"
  short_description: "根据小程序背景、功能和用户搜索意图，生成微信搜索友好的名称"
  default_prompt: "使用 $wechat-miniapp-name-generator，根据我的小程序背景、核心功能、目标用户和要解决的问题，生成微信搜索友好的小程序名称。"
```

## 字段说明

| 字段 | 当前值 | 作用 |
| --- | --- | --- |
| `interface` | 顶层对象 | 聚合与界面展示相关的配置。 |
| `display_name` | `微信小程序起名` | 技能在界面中显示的名称，面向中文用户，简洁明确。 |
| `short_description` | `根据小程序背景、功能和用户搜索意图，生成微信搜索友好的名称` | 技能摘要，强调输入信息、搜索意图和输出目标。 |
| `default_prompt` | 中文调用提示词 | 默认提示用户使用 `$wechat-miniapp-name-generator`，并说明需要提供产品背景、核心功能、目标用户和要解决的问题。 |

## 与 SKILL.md 的关系

`openai.yaml` 负责“入口表达”，`SKILL.md` 负责“执行规则”。

- `openai.yaml` 面向宿主平台和用户入口，字段少、职责轻。
- `SKILL.md` 面向模型执行，包含完整的工作流、微信命名规则、评分清单、输出格式和示例。
- 两者通过技能名 `$wechat-miniapp-name-generator` 建立调用关系。

当前 `default_prompt` 中引用的技能名与 `SKILL.md` 前置元数据中的 `name: wechat-miniapp-name-generator` 一致，这是正确的。

## 当前配置优点

- 展示名称简短，用户能快速理解用途。
- 简介明确指向“小程序背景”“功能”“用户搜索意图”“微信搜索友好名称”等关键信息。
- 默认提示词包含技能调用名，便于宿主环境准确触发技能。
- `default_prompt` 提醒用户提供产品背景、核心功能、目标用户和要解决的问题，和 `SKILL.md` 的输入要求一致。

## 可能的问题

1. 文件只提供入口配置，没有附带示例输入。  
   这不一定是缺陷，但如果宿主环境支持更丰富的配置，增加示例会降低用户开始使用的成本。

## 优化建议

当前配置已经完成中文化，并补充了“用户搜索意图”和“目标用户”等输入引导。推荐继续使用以下版本：

```yaml
interface:
  display_name: "微信小程序起名"
  short_description: "根据小程序背景、功能和用户搜索意图，生成微信搜索友好的名称"
  default_prompt: "使用 $wechat-miniapp-name-generator，根据我的小程序背景、核心功能、目标用户和要解决的问题，生成微信搜索友好的小程序名称。"
```

## 结论

当前 `openai.yaml` 结构清晰、字段有效，能够作为 `wechat-miniapp-name-generator` 技能的 OpenAI 代理入口配置正常使用。配置已统一为中文，并在简介和默认提示词中补充了搜索意图、目标用户和要解决的问题，更贴合中文小程序命名场景。
