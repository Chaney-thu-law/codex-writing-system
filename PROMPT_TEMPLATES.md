# PROMPT_TEMPLATES

这是本项目的可直接复制模板页。  
这里只保留尽量短、但足够明确的提示词。

---

# 一、初始化画像

## 模板 1：首次建立 style_profile
请读取 `references/corpus/core/` 中的语料，使用 `build-style-profile` 建立 `references/style_profile.md` 初版，并补全 `references/corpus_index.md`。重点提炼我的问题提出方式、概念界定方式、段落推进方式、结论边界控制方式。完成后向我总结 8—12 条最稳定特征。

## 模板 2：新增语料后更新画像
我刚在 `references/corpus/core/` 中加入了新语料。请使用 `build-style-profile` 更新 `references/corpus_index.md`，并增量更新 `references/style_profile.md`。说明新语料带来了哪些补充或修正，不要轻易推翻旧规则。

---

# 二、起草类模板

## 模板 3：起草引言
请根据 `references/style_profile.md` 和 `references/corpus/core/` 中的语料，使用 `draft-in-my-voice` 起草一段法学论文引言。主题是：  
【填主题】  
要求：先提出现实问题，再收束为规范争点；分层清楚；不要写空泛AI腔；结论保持克制。

## 模板 4：起草摘要
请根据 `references/style_profile.md`，使用 `draft-in-my-voice` 起草这篇文章的中文摘要。主题是：  
【填主题】  
要求：保持法学摘要风格，概括研究对象、核心问题、分析路径和主要结论；不要写万能套话；篇幅控制在【填字数】字左右。

## 模板 5：起草结论
请根据 `references/style_profile.md`，使用 `draft-in-my-voice` 起草本文结论。主题是：  
【填主题】  
要求：回收前文主要论证，保持结论边界，不夸大创新点，不写口号式收尾。

## 模板 6：起草正文分析段落
请根据 `references/style_profile.md` 和已有语料，使用 `draft-in-my-voice` 起草一段正文。主题是：  
【填主题】  
要求：先界定问题，再展开分析，再给出有限结论；尽量贴近我现有论文的论证节奏。

---

# 三、润色类模板

## 模板 7：逐段润色
请使用 `draft-in-my-voice` 润色我下面这段文字。要求：优先保留原有论证路径；区分结构问题、概念问题、表达问题；先给最小改动版，再给优化表达版，最后给整段版本。  

【粘贴段落】

## 模板 8：只做最小改动
请根据 `references/style_profile.md`，对我下面这段话只做最小改动。要求：不重写论证，只修正明显的结构、概念或表达问题，尽量保留原句。  

【粘贴段落】

## 模板 9：把一段话改得更像我
请根据 `references/style_profile.md` 和 `references/negative_rules.md`，把我下面这段话改得更像我本人会写的版本。要求：不要堆砌连接词，不要模板化，不要写得像通用公文。  

【粘贴段落】

---

# 四、从修改中学习

## 模板 10：分析一组前后对照
请读取 `references/revision_pairs/` 中我刚加入的前后对照样本，使用 `learn-from-edits`：分析我改了什么，判断哪些属于稳定偏好，并更新 `references/edit_deltas.md`；如有必要，再增量更新 `references/style_profile.md`。

## 模板 11：只做差异总结
请读取 `references/revision_pairs/` 中我刚加入的前后对照样本，简要总结这次修改最能体现我偏好的 5—8 条变化。先不要更新文件，先给我看结论。

---

# 五、更新负面清单

## 模板 12：补充 negative_rules
请根据我下面新增的内容，更新 `references/negative_rules.md`。要求：保持原有结构，只做归类、整理和压缩表达，不要擅自扩写成我没说过的偏好。  

【粘贴新增内容】

## 模板 13：根据最近改稿反推负面偏好
请结合我最近的改稿记录，判断哪些表达、论证方式或收尾方式是我持续在回避的，并提出建议是否需要更新 `references/negative_rules.md`。先给建议，不要直接改文件。

---

# 六、项目能力简表

## 模板 14：简短列菜单
请基于当前项目中的 `AGENTS.md`、`README.md` 和 `.agents/skills/`，简要列出你现在可执行的功能菜单，并为每个功能给出一句最短调用方式。控制在 300 字以内。

## 模板 15：帮我分流当前任务
我现在要做的是：  
【一句话描述任务】  
请不要直接开始写，而是先告诉我：这个任务更适合对应 `TASK_MENU.md` 的哪一类、我该复制哪条模板、以及是否需要先补材料。控制在 200 字以内。

---

# 七、推荐起手式

如果你现在不知道先用哪条，最常见的起手式是这三句：

## 起手式 A：第一次正式使用
请先读取 `references/corpus/core/` 中的语料，使用 `build-style-profile` 建立 `references/style_profile.md` 初版，同时补全 `references/corpus_index.md`。完成后向我总结 8—12 条最稳定的写作特征。

## 起手式 B：直接开始写
请根据 `references/style_profile.md` 和 `references/corpus/core/` 中的语料，使用 `draft-in-my-voice` 起草以下主题的正文段落：  
【填主题】  
要求：分层清楚、结论克制、不要空泛AI腔。

## 起手式 C：让我越用越像我
请读取 `references/revision_pairs/` 中我刚加入的样本，使用 `learn-from-edits` 分析我的修改，并更新 `references/edit_deltas.md`；必要时再增量更新 `references/style_profile.md`。