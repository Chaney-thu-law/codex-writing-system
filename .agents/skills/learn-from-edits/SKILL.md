---
name: learn-from-edits
description: Compare a previous draft with the user's revised version, infer reusable writing preferences, and update the style profile. Use this skill whenever the user edits generated text or provides before-and-after versions.
---

# Goal

你的任务不是简单描述“改了什么”，而是从“旧稿 -> 作者改稿”的差异中，提炼作者稳定、可复用、可执行的偏好规则，并更新 `references/style_profile.md` 与 `references/edit_deltas.md`。

# Inputs

读取：
- 旧稿
- 作者修改稿
- `references/style_profile.md`
- `references/edit_deltas.md`（如果存在）
- `references/negative_rules.md`

# Workflow

1. 先逐段对齐旧稿与新稿。
2. 将修改分为以下类型：
   - 结构调整
   - 问题收束
   - 概念修正
   - 论证顺序调整
   - 语气克制化
   - 去AI腔
   - 术语统一
   - 结论限缩
   - 引注/规范表达调整
3. 对每一类修改，判断它是：
   - 一次性编辑
   - 明确偏好
   - 高置信硬规则
4. 只有在以下情况下，才将其写入长期画像：
   - 同类修改重复出现
   - 或者作者本次修改非常明显、方向非常一致
5. 将结果写入 `references/edit_deltas.md`，格式如下：
   - 原句问题
   - 作者如何改
   - 推断出的偏好
   - 是否纳入长期规则
   - 证据等级（高/中/低）

6. 然后同步更新 `references/style_profile.md`：
   - 新增规则
   - 修正规则
   - 新增“应避免表达”
   - 新增“不同任务的偏好差异”

# Very important weighting rules

1. 作者亲自改动的版本，高于任何既有语料。
2. 大幅结构改写，比单纯词语润色更能体现作者真实偏好。
3. 删除某种表达，通常比新增某种表达更值得重视，因为它更能反映作者厌恶点。
4. 若新修改与旧画像冲突，不要立即推翻旧画像；先记录为“待验证冲突”。

# Output standard

每次运行后，至少输出：
- 本次最值得记录的 3-10 条偏好变化
- 是否更新长期画像
- 更新了哪些规则
- 哪些变化仍需更多样本验证

# Prohibitions

1. 不得把一次偶然改动直接上升为永久规则。
2. 不得只盯词汇替换，忽略结构性修改。
3. 不得把作者为应付特定期刊做的特殊改法，误判成所有场景通用规则。
