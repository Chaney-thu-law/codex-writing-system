---
name: draft-in-my-voice
description: Draft, revise, continue, or polish Chinese legal-academic writing in the user's own voice, using the author style profile and corpus examples. Use this skill for abstracts, introductions, doctrinal analysis, literature reviews, conclusions, policy-comparative writing, and paragraph-level polishing.
---

# Goal

根据 `references/style_profile.md` 与作者语料，用作者本人的思维方式和表达习惯完成写作任务。重点是模仿作者的论证逻辑、问题意识和结构习惯，而不是机械复制表面措辞。

# Before writing

每次动笔前，先隐式判断本次任务属于哪一种：
- 教义学论文
- 政策/比较法论文
- 中文摘要
- 英文投稿段落
- 审稿回复
- 逐段润色
- 结论/摘要提炼
- 研究计划或申请材料

然后自动调用对应的风格子规则。

# Core writing rules

1. 先界定问题，再回答问题。
2. 先限定讨论对象，再讨论结论。
3. 先拆分争点，再分层推进，不要一段塞进多个未区分的问题。
4. 结论必须写出成立条件、适用边界或限制，不要用无限上纲的句子收尾。
5. 对法律问题，优先使用以下框架之一：
   - 概念界定 -> 争点拆分 -> 规范基础 -> 具体适用 -> 限制与边界
   - 请求权基础 -> 构成要件 -> 是否成立 -> 限制
   - 现实困境 -> 现有方案不足 -> 重构标准/解释路径 -> 结论
6. 对政策/比较法问题，优先使用以下框架之一：
   - 问题提出 -> 样本/材料说明 -> 分类与发现 -> 评价 -> 可借鉴之处
   - 现实压力 -> 制度缺位 -> 域外经验 -> 本土适用边界 -> 制度建议
7. 默认保持克制，不夸大创新点，不夸大结论力度。
8. 可以使用显式路标词，但不得堆砌。
9. 除非任务明确要求，不输出聊天式口吻、口号式结论或万能总结句。

# When revising existing text

1. 优先保留原有论证路径。
2. 先修：
   - 概念不准
   - 结构不清
   - 逻辑断裂
   - 结论过满
   - 套话太重
3. 后修：
   - 语气
   - 节奏
   - 字句顺滑
4. 若原文已经是作者本人写的，不要为了“更像学术”而过度改写。

# When the user asks for paragraph polishing

默认输出四部分：
1. 真正有问题的句子或短语
2. 问题类型（硬错误 / 不够贴作者习惯 / 论证力度失衡 / 结构问题）
3. 最小改动版
4. 优化表达版
5. 最后给出整段版本

# Forbidden patterns

1. 空泛AI腔：
   - “具有重要意义”
   - “随着……不断发展”
   - “值得深入思考”
   - “在实践中面临诸多挑战”
   除非上下文确有必要，否则不用或少用。
2. 只给结论，不写取舍理由。
3. 只写价值判断，不写概念边界。
4. 机械模仿作者常见连接词，导致文本发硬。
5. 编造文献、案例、规范依据。

# Quality check before finalizing

提交前自检：
- 这段话有没有先把讨论对象限定清楚？
- 有没有把两个不同问题混在一起？
- 结论是不是写得太满？
- 有没有出现模板化AI表达？
- 这一稿更像作者“会怎么想”，还是只是“像作者会怎么说”？

若两者冲突，优先选择前者。
