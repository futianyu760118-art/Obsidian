---
title: Skill封装与使用
date: 2026-10-13
type: note
dimension: self
status: active
updated: 2026-10-14
tags:
  - 元宝/对话
  - Agent/Skill
  - 前端/交互
  - 工作流
aliases:
  - Web 高级交互 Skill
source: '[[90_来源/元宝对话/AI制作应用的交互细节关键]]'
source_url: 'https://yb.tencent.com/s/UzMq1eJIsdJa'
---

# Skill 封装与使用

## 目标

把“网页高级交互细节”从一次性对话整理成 Agent 可以复用的 Skill：当开发者提出网页质感、微交互、动画或用户体验需求时，自动判断适用模式并输出可落地的代码和注意事项。

## 标准入口

Skill 的入口文件应为 `SKILL.md`，至少包含：

- 名称、版本、描述、标签。
- 触发条件和不适用场景。
- 输出格式要求。
- 交互技巧的决策树。
- 参考文档和代码片段的路径。

## 建议目录结构

```text
web-advanced-interaction/
├── SKILL.md
├── README.md
├── references/
│   ├── skill-01-feedback-button.md
│   ├── skill-02-check-linkage.md
│   ├── skill-03-stacked-card.md
│   ├── skill-04-snap-card.md
│   ├── skill-05-inertial-scroll.md
│   ├── skill-06-circular-reveal.md
│   └── form-enhancement.md
└── assets/snippets/
```

## 推荐调用流程

1. 识别页面类型、技术栈和目标交互。
2. 判断属于六类模式中的哪一类，标记优先级。
3. 先给最小可行改动，再给完整组件化方案。
4. 输出 HTML、CSS、JavaScript 或框架代码。
5. 说明浏览器兼容性、无障碍、性能和降级方案。
6. 根据用户反馈继续迭代，而不是一次堆叠所有动画。

## 输出模板

```text
场景判断
→ 适用技巧与优先级
→ 核心交互逻辑
→ 可直接使用的代码
→ 接入位置
→ 验证清单
→ 兼容性与注意事项
```

## 使用示例

```text
使用 web-advanced-interaction skill，给这个询盘表单增加提交中、成功和失败状态，保持现有 HTML 结构不变。
```

或：

```text
使用 web-advanced-interaction skill，先分析这个页面最值得加入的两个微交互，再给出最小改动代码。
```

## 当前材料状态

原始分享：[Skill项目封装为Agent调用文件](https://yb.tencent.com/s/UzMq1eJIsdJa)。该页面正文当前无法稳定读取，以下整理以本地导入的对话原文为准。

来源对话中提到过一个 `web-advanced-interaction-skill.zip`，但当前导入文件夹里只有两份 Markdown 原始记录，没有发现该压缩包。压缩包内的完整代码和文件结构应以实际文件为准，不应仅依据对话中的描述恢复。

## 相关

- [[03_公司/资料/Web高级交互设计]]
- [[00_收件箱/待确认事项]]
- [[90_来源/元宝对话/元宝对话索引]]
