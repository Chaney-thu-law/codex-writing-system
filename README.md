# Codex Writing System

这个目录用于长期沉淀一位法学研究者的个人写作系统，供 Codex 或类似代理在后续写作、续写、润色、仿写与“从修改中学习”时反复调用。它的核心目标不是一次性生成文本，而是逐步积累作者本人的稳定风格、结构偏好、负面规则与修订痕迹。

## 1. `AGENTS.md` 的作用

`AGENTS.md` 是整个系统的最高层写作宪章。它规定代理在处理学术写作任务时应优先继承作者的思考方式、问题意识、论证路径与结论边界，而不是机械追求“学术腔”或堆砌空泛表达。

## 2. 三个 skills 的作用

- `.agents/skills/build-style-profile/SKILL.md`
  - 当新增论文、DOCX、PDF、终稿或代表作时使用。
  - 任务是整理语料台账，并把稳定、可执行的风格规则更新到 `references/style_profile.md`。

- `.agents/skills/draft-in-my-voice/SKILL.md`
  - 当需要起草、续写、改写、润色法学论文内容时使用。
  - 任务是根据 `references/style_profile.md` 与作者语料，用作者本人的问题意识和论证节奏完成写作。

- `.agents/skills/learn-from-edits/SKILL.md`
  - 当出现“旧稿 -> 作者改后稿”的成对样本时使用。
  - 任务是从修改差异中提炼长期偏好，并同步更新 `references/style_profile.md` 与 `references/edit_deltas.md`。

## 3. `references/` 目录的作用

- `references/corpus/`
  - 存放作者指定可代表其风格的原始语料，建议按需要继续细分子目录。

- `references/corpus/core/`
  - 当前核心语料区，适合放代表作、终稿、亲自大改稿等高价值样本。

- `references/revision_pairs/`
  - 存放“旧稿-改后稿”的对照样本，供代理学习作者真实修订偏好。

- `references/style_profile.md`
  - 长期维护的作者风格画像，是后续写作与润色任务的主要依据。

- `references/negative_rules.md`
  - 记录作者明确不喜欢的 AI 腔、论证毛病、标题风格和结论方式。

- `references/task_preferences.md`
  - 记录不同任务下的偏好，例如摘要、引言、审稿回复、段落润色等。

- `references/corpus_index.md`
  - 当前语料台账，记录文件名、类型、用途和备注，后续可继续补充权重与代表性说明。

- `references/edit_deltas.md`
  - 汇总作者实际改稿中体现出来的稳定偏好与待验证变化。

## 4. 如何继续往 `references/corpus` 里加入新 `docx`

1. 保留原始文件，不要覆盖来源文件。
2. 把新 `docx` 复制到 `references/corpus/core/`，或按需要新建更细的子目录。
3. 如果该文件是代表作、终稿或本人亲自大改稿，建议在 `references/corpus_index.md` 里补一行备注，注明“高权重”或“风格锚点”。
4. 之后运行 `build-style-profile`，让系统根据新增语料更新 `references/style_profile.md`。

## 5. 如何放置“旧稿-改后稿”到 `references/revision_pairs`

1. 为同一轮修改建立一个单独子目录，例如：`references/revision_pairs/2026-04-08-paper-01/`。
2. 在该目录中至少放入两份文件：
   - `draft_before.docx`
   - `draft_after.docx`
3. 如果有必要，可以额外放入 `notes.md`，说明这次修改的背景，例如“为投稿而压缩篇幅”或“作者亲自重写了导论部分”。
4. 之后运行 `learn-from-edits`，把本轮修改沉淀为长期规则或待验证冲突。

## 6. 两个最基础的使用示例

### 示例一：先建立 `style_profile`

可直接向代理下达类似任务：

```text
请使用 build-style-profile，读取 references/corpus/core 与 references/corpus_index.md，
先建立初版 style_profile，并明确哪些规则只是低置信观察，哪些规则已经比较稳定。
```

### 示例二：再根据 `style_profile` 起草一段法学论文内容

```text
请使用 draft-in-my-voice，基于 references/style_profile.md，
起草一段关于“人工智能生成内容著作权侵权请求权基础”的正文，要求先界定讨论对象，
再拆分争点，最后给出有边界的结论，不要出现空泛 AI 腔。
```

## 7. 使用边界

当前系统只完成了目录、技能说明与基础台账的搭建，尚未自动产出真正的作者风格分析结果。后续需要在补充语料、revision pairs 或作者明确反馈后，逐步完善 `style_profile.md`、`negative_rules.md` 和 `task_preferences.md`。
