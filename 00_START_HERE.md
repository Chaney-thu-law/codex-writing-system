# 00_START_HERE

这是这个项目的快速入口页。  
你每次打开 `codex-writing-system`，先看这里，再决定去哪个文件找对应模板。

---

## 这个项目是做什么的

这是一个面向“按我自己的风格进行法学学术写作与修改”的 Codex 工作区。

它的核心分工是：

- `AGENTS.md`：长期稳定规则
- `.agents/skills/`：可复用工作流
- `references/corpus/`：我的代表性语料
- `references/style_profile.md`：对我文风和论证方式的当前总结
- `references/negative_rules.md`：我明确不喜欢的表达和论证方式
- `references/revision_pairs/`：旧稿—改后稿对照样本
- `references/edit_deltas.md`：从我修改中提炼出的偏好变化记录

---

## 我每次进入项目时，建议这样做

### 情况一：我是第一次正式使用这个项目
先做这一件事：

1. 让 Codex 基于 `references/corpus/core/` 中的语料建立 `references/style_profile.md` 初版。
2. 同时补全 `references/corpus_index.md`。

去看：
- `TASK_MENU.md` 的“任务 1：建立/更新风格画像”
- `PROMPT_TEMPLATES.md` 的“初始化画像”模板

---

### 情况二：我已经有了 style_profile，想直接写东西
直接让 Codex按我的风格起草或润色。

去看：
- `TASK_MENU.md` 的“任务 2：按我的风格起草新内容”
- `TASK_MENU.md` 的“任务 3：润色我现有的段落”
- `PROMPT_TEMPLATES.md` 的“起草类模板”“润色类模板”

---

### 情况三：我新增了新的 docx
把新文件放进：
- `references/corpus/core/`  
或按需要放进你后续自己扩展的子目录。

然后让 Codex：
1. 更新 `references/corpus_index.md`
2. 增量更新 `references/style_profile.md`

去看：
- `TASK_MENU.md` 的“任务 5：新增 docx 语料后更新系统”
- `PROMPT_TEMPLATES.md` 的“新增语料后更新”模板

---

### 情况四：我后来保存了“旧稿—改后稿”
把成对文件放进：
- `references/revision_pairs/`

建议命名清楚一些，例如：
- `2026-04-08_摘要_旧稿.md`
- `2026-04-08_摘要_改后.md`

然后让 Codex：
1. 比较前后差异
2. 更新 `references/edit_deltas.md`
3. 必要时增量更新 `references/style_profile.md`

去看：
- `TASK_MENU.md` 的“任务 4：从旧稿—改后稿中学习”
- `PROMPT_TEMPLATES.md` 的“从修改中学习”模板

---

## 最短启动流程

如果你现在只想尽快开始，请直接做下面三步：

### 第一步
确认当前工作目录就是：
`C:\Users\61622\Desktop\codex-writing-system`

### 第二步
打开 `PROMPT_TEMPLATES.md`

### 第三步
复制你当前任务对应的模板给 Codex

---

## 我最常用的四类任务

### 1. 初始化或更新风格画像
看：
- `TASK_MENU.md` 第 1 节
- `PROMPT_TEMPLATES.md` 的“初始化画像”“更新画像”模板

### 2. 按我的风格起草
看：
- `TASK_MENU.md` 第 2 节
- `PROMPT_TEMPLATES.md` 的“起草引言 / 摘要 / 结论 / 正文段落”模板

### 3. 润色我现有的文字
看：
- `TASK_MENU.md` 第 3 节
- `PROMPT_TEMPLATES.md` 的“逐段润色”模板

### 4. 让系统从我的修改中继续贴近我
看：
- `TASK_MENU.md` 第 4 节
- `PROMPT_TEMPLATES.md` 的“从修改中学习”模板

---

## 当我不确定现在该怎么做时

优先顺序：

1. 先看 `TASK_MENU.md`
2. 再去 `PROMPT_TEMPLATES.md` 复制模板
3. 若仍不确定，再让 Codex简短总结当前项目可用能力

建议只让它“简短总结”，不要每次都让它长篇重列菜单。

---

## 一句提醒

这个项目的目标不是让 Codex“临场发挥像我”，而是让它逐步形成一个稳定、可更新、可维护的个人写作系统。