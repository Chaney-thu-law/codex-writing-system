# TASK_MENU

这是本项目的任务菜单。  
每一类任务都给出：适用场景、推荐 skill、输入材料、输出产物、可直接复制的提示词。

---

# 任务 1：建立/更新风格画像

## 适用场景
- 第一次使用这个项目
- 新增了新的代表性 docx
- 感觉当前 `style_profile.md` 还太粗
- 想让系统重新梳理我的写作习惯

## 推荐调用的 skill
- `build-style-profile`

## 输入材料
- `references/corpus/core/` 中的 docx
- `references/negative_rules.md`
- `references/task_preferences.md`
- 现有的 `references/style_profile.md`（如果已存在）
- 现有的 `references/corpus_index.md`（如果已存在）

## 输出产物
- 更新后的 `references/style_profile.md`
- 更新后的 `references/corpus_index.md`

## 可直接复制的提示词
请读取 `references/corpus/core/` 中的语料，使用 `build-style-profile`：
1. 建立或更新 `references/style_profile.md`；
2. 补全 `references/corpus_index.md`；
3. 重点提炼我的问题提出方式、概念界定方式、段落推进方式、结论边界控制方式；
4. 不要编造不存在的期刊信息或作者分工；
5. 完成后向我简要总结你识别出的 8—12 条最稳定特征。

---

# 任务 2：按我的风格起草新内容

## 适用场景
- 我准备写一段新的法学论文正文
- 我想写引言、摘要、结论、文献综述、分析段落
- 我希望起草内容尽量贴近我已有论文的论证习惯

## 推荐调用的 skill
- `draft-in-my-voice`

## 输入材料
- `references/style_profile.md`
- `references/corpus/core/` 中已有语料
- 我本次给出的具体主题、任务和限制条件

## 输出产物
- 一段或多段可直接进入论文的中文文本
- 若我要求，也可以输出多个版本

## 可直接复制的提示词
请根据 `references/style_profile.md` 和 `references/corpus/core/` 中的语料，使用 `draft-in-my-voice` 起草以下内容：  
【在这里写题目/主题】  
要求：  
1. 先提出现实问题，再收束为规范争点；  
2. 保持法学论文风格，不要写空泛AI腔；  
3. 论证分层清楚，结论保持克制；  
4. 输出为可直接进入正文的中文段落。

---

# 任务 3：润色我现有的段落

## 适用场景
- 我已经写好一段，但想更像“我自己写得更稳”
- 我不想让 Codex 重写，只想让它优化
- 我希望尽量保留原有论证路径

## 推荐调用的 skill
- `draft-in-my-voice`

## 输入材料
- 我当前提供的段落
- `references/style_profile.md`
- 如有需要，也可以同时参考 `references/negative_rules.md`

## 输出产物
- 问题识别
- 最小改动版
- 优化表达版
- 整段润色版

## 可直接复制的提示词
请使用 `draft-in-my-voice` 润色我下面这段文字。  
要求：  
1. 优先保留原有论证路径，不要过度改写；  
2. 区分结构问题、概念问题、表达问题；  
3. 先给最小改动版，再给优化表达版，最后给整段版本；  
4. 尽量贴近 `references/style_profile.md` 中总结出的风格。  

【在这里粘贴段落】

---

# 任务 4：从“旧稿—改后稿”中学习

## 适用场景
- 我开始保存“旧稿—改后稿”样本
- 我希望系统从我的修改中持续贴近我
- 我想把我最近的改稿偏好沉淀下来

## 推荐调用的 skill
- `learn-from-edits`

## 输入材料
- `references/revision_pairs/` 中的前后对照样本
- `references/style_profile.md`
- `references/edit_deltas.md`
- `references/negative_rules.md`

## 输出产物
- 更新后的 `references/edit_deltas.md`
- 必要时增量更新后的 `references/style_profile.md`

## 可直接复制的提示词
请读取 `references/revision_pairs/` 中我刚加入的前后对照样本，使用 `learn-from-edits`：  
1. 分析我改了什么；  
2. 判断哪些属于稳定偏好；  
3. 更新 `references/edit_deltas.md`；  
4. 如有必要，增量更新 `references/style_profile.md`；  
5. 不要把一次性改动误判为永久规则。

---

# 任务 5：新增 docx 语料后更新系统

## 适用场景
- 我刚放进了新的论文、终稿、摘要或其他代表性文本
- 我希望系统把这些新材料纳入风格学习

## 推荐调用的 skill
- `build-style-profile`

## 输入材料
- 新增的 docx
- 旧的 `references/style_profile.md`
- 旧的 `references/corpus_index.md`

## 输出产物
- 更新后的 `references/corpus_index.md`
- 增量更新后的 `references/style_profile.md`

## 可直接复制的提示词
我刚在 `references/corpus/core/` 中加入了新语料。  
请使用 `build-style-profile`：  
1. 先更新 `references/corpus_index.md`；  
2. 再增量更新 `references/style_profile.md`；  
3. 说明新语料对既有风格画像带来了哪些补充或修正；  
4. 不要随意推翻旧规则，除非新证据明显更强。

---

# 任务 6：更新 negative_rules.md

## 适用场景
- 我想补充“我讨厌的AI腔”
- 我想补充“我不喜欢的论证毛病”
- 我想把“看起来不像我写的特征”写进去

## 推荐调用的 skill
- 不必须调用 skill
- 如涉及同步更新画像，可结合 `build-style-profile` 或 `learn-from-edits`

## 输入材料
- 我本次新增的不喜欢项
- `references/negative_rules.md`

## 输出产物
- 更新后的 `references/negative_rules.md`
- 如我要求，也可同步更新 `style_profile.md`

## 可直接复制的提示词
请根据我下面新增的内容，更新 `references/negative_rules.md`。  
要求：  
1. 保持原有结构；  
2. 只做整理、归类和表述压缩，不要擅自扩写成我没说过的偏好；  
3. 如这些内容足以影响风格画像，请再建议我是否需要同步更新 `references/style_profile.md`。  

【在这里写新增内容】

---

# 任务 7：查看当前项目可用能力的简短菜单

## 适用场景
- 我一时忘了当前项目有哪些模块
- 我刚新增或调整了 skill
- 我想快速让 Codex 自报当前可执行能力

## 推荐调用的 skill
- 不固定
- 让 Codex基于当前项目文件做简短总结即可

## 输入材料
- 当前项目内的 `AGENTS.md`
- `.agents/skills/`
- `README.md`
- 本菜单文件

## 输出产物
- 一份简短能力菜单
- 每项能力的一句最短调用方式

## 可直接复制的提示词
请基于当前项目中的 `AGENTS.md`、`README.md` 和 `.agents/skills/`，简要列出你现在可执行的功能菜单，并为每个功能给出一句最短调用方式。  
要求：  
1. 控制在 300 字以内；  
2. 只列当前项目里真实存在的功能；  
3. 不要长篇解释。

---

# 任务 8：我不知道该选哪个任务时

## 适用场景
- 我现在手上的工作有点模糊
- 我不确定该先建画像、先起草、还是先润色
- 我想让 Codex 帮我做最小限度的任务分流

## 推荐调用的 skill
- 不固定

## 输入材料
- 你对当前任务的一句话描述

## 输出产物
- 一个简短建议：先做什么、看哪个文件、用哪个模板

## 可直接复制的提示词
我现在要做的是：  
【在这里用一句话描述】  
请你不要直接开始写，而是先告诉我：  
1. 这个任务更适合对应 `TASK_MENU.md` 的哪一类；  
2. 我应该优先复制哪条模板；  
3. 如果有必要，再提醒我先补什么材料。  
控制在 200 字以内。