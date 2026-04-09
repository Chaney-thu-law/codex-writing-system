---
name: build-style-profile
description: Analyze the user's own writing samples and update a reusable author style profile. Use this skill when new papers, DOCX/PDF files, drafts, or revised texts are added, or when asked to learn the author's writing style, argument pattern, structure, and preferences.
---

# Goal

你的任务是从作者本人的语料中，提炼出可复用、可更新、可执行的“风格画像”，并写入 `references/style_profile.md`。你要学习的不只是措辞，而是作者如何提出问题、如何界定概念、如何搭建结构、如何得出结论。

# Required inputs

优先读取并分类以下材料：
- `references/corpus/`：作者指定可代表其风格的论文、稿件、终稿、DOCX/PDF
- `references/revision_pairs/`：旧稿与作者修改稿的对照样本
- `references/negative_rules.md`
- `references/task_preferences.md`
- `references/corpus_index.md`（如果存在）

# Workflow

1. 先建立语料台账，写入 `references/corpus_index.md`
   - 文件名
   - 文体（论文/摘要/引言/文献综述/政策文/审稿回复/翻译等）
   - 作者指定权重（高/中/低）
   - 是否适合作为“个人风格锚点”
   - 备注

2. 提炼作者的稳定偏好，只记录“多次出现”或“作者明确确认”的规则。
   不要把单次偶然表达误判为硬规则。

3. 风格画像必须至少包含以下栏目：
   - 一、作者的核心问题意识
   - 二、常见文章结构
   - 三、段落推进方式
   - 四、概念界定与类型化习惯
   - 五、论证方法偏好
   - 六、证据与材料使用方式
   - 七、常用但可控的连接方式
   - 八、结论的语气与边界控制
   - 九、明确应避免的表达
   - 十、不同文体下的差异化规则
   - 十一、当前信心不足、需要补充语料验证的地方

4. 对语料做权重区分时，以作者的明确指示为准：
   - 作者明确标为“核心代表作”的材料，最高优先
   - 作者亲自大改的终稿，高优先
   - revision pairs，极高价值
   - 作者未特别说明但放入 corpus 的材料，默认中高权重
   - 作者明确说“不代表我”或“只供参考”的材料，降权

5. 若发现作者在不同场景下文风不同，要区分为：
   - 教义学论文风格
   - 政策/比较法论文风格
   - 中文摘要风格
   - 英文投稿风格
   - 审稿回复/段落润色风格

6. 更新 `references/style_profile.md` 时：
   - 保留旧规则
   - 仅在有更强新证据时修正旧规则
   - 对新增规则标明来源文件和信心等级（高/中/低）

# Output standard

最终写出的 `style_profile.md` 必须是一个以后能被别的 skill 直接调用的“操作性文件”，而不是空泛的文学评论。每条规则都应尽量可执行。

# Prohibitions

1. 不得因为“合著”形式自动否定其个人风格价值。
2. 不得只统计口头禅，不分析论证结构。
3. 不得为了凑规则而写不稳定的印象性判断。
4. 不得覆盖或删除旧规则，除非有明显相反证据。
