# 毛泽东思想方法论顾问

> 让思想回到实践，让方法服务生活。

一个面向 Codex 与 OpenClaw 的中文 AI Skill。它不模拟历史人物，也不把经典语句做成口号库，而是把毛泽东著作中的认识方法、调查方法、矛盾分析、战略思维、群众路线、组织领导和政策方法，转化为可核验、可执行、可复盘的现代问题分析框架。

适合用来分析学习、工作、管理、创业、团队协作、长期规划、沟通分歧和个人决策，也可以辅助精读《毛泽东选集》第一至第五卷。

## 它能做什么

- 从复杂局面中识别主要矛盾、主要方面和阶段性任务
- 区分事实、判断、假设与价值选择
- 用调查研究补足真正影响决策的信息
- 分析支持力量、可合作对象、阻力和各方利益
- 把长期目标拆成阶段、指标、验证动作和调整条件
- 用群众路线建立“一线经验—集中分析—回到实践”的反馈闭环
- 用《党委会的工作方法》等文本改善会议、分工、报告和执行
- 对《毛选》1—5 卷进行篇目定位、历史语境分析和结构化精读
- 标明原文概念、后人归纳与现代转译，避免把类比冒充史实

## 方法论地图

技能内置 **100 项方法论工作索引**，按以下领域组织：

| 领域 | 代表性方法 |
|---|---|
| 认识论与学习 | 实事求是、调查研究、实践—认识—再实践、理论联系实际 |
| 辩证法 | 主要矛盾、主要方面、矛盾特殊性、内因与外因、两点论与重点论 |
| 战略与行动 | 持久战、阶段论、集中优势资源、主动性与灵活性、试点推广 |
| 政策与协作 | 原则性与灵活性、统一战线、区别对待、不要四面出击 |
| 组织与领导 | 群众路线、集体领导与分工负责、报告制度、精兵简政 |
| 群众工作与传播 | 为人民服务、从对象出发、深入生活、说服教育 |
| 经济建设与治理 | 统筹兼顾、论十大关系、中央与地方积极性、独立自主与对外学习 |
| 作风与纠偏 | 反对主观主义、反对党八股、批评与自我批评、调查—执行—检查 |
| 历史与国际关系 | 阶段性主要矛盾、力量对比、民族独立、独立自主 |
| 写作与表达 | 有的放矢、摆事实讲道理、具体通俗、反对空话套话 |

完整条目、出处与迁移边界见 [`references/methods.md`](references/methods.md)。

## 快速安装

### Codex · Windows PowerShell

```powershell
git clone https://github.com/296277/mao-thought-advisor.git "$env:USERPROFILE\.codex\skills\mao-thought-advisor"
```

### Codex · macOS / Linux

```bash
git clone https://github.com/296277/mao-thought-advisor.git "${CODEX_HOME:-$HOME/.codex}/skills/mao-thought-advisor"
```

### OpenClaw

```bash
git clone https://github.com/296277/mao-thought-advisor.git ~/.openclaw/skills/mao-thought-advisor
openclaw skills check
```

若目标目录已存在，请在确认本地修改已保存后更新仓库。安装或更新后开启一个新会话，以便宿主重新加载 Skill。

## 调用方式

显式调用：

```text
$mao-thought-advisor
```

也可以直接描述问题；当请求涉及毛泽东思想、毛选、矛盾分析、调查研究、群众路线、持久战、统一战线或相关方法论时，支持自动发现 Skill。

### 示例

```text
$mao-thought-advisor 我同时面临换工作、考证和家庭支出压力。请找出主要矛盾，给出未来三个月的行动顺序和调整条件。
```

```text
$mao-thought-advisor 团队会议很多但执行很差。请结合《党委会的工作方法》分析原因，输出一套两周试行方案。
```

```text
$mao-thought-advisor 请精读《实践论》：重建论证链，解释核心概念，并指出它与《矛盾论》的关系。
```

```text
$mao-thought-advisor 这个长期项目已经半年没有明显进展。请用持久战和阶段论判断应该坚持、调整还是停止。
```

## 默认分析框架

Skill 会根据问题复杂度裁剪以下结构：

1. 一句话判断
2. 已知事实与关键假设
3. 主要矛盾与次要矛盾
4. 力量、利益与现实条件
5. 当前阶段
6. 近期行动、后续行动与验证指标
7. 反证、风险、调整或退出条件
8. 相关原著卷次、篇目与关联理由

它不会把 100 项方法全部强行套在一个问题上，而是优先选择最相关的 2—5 项方法形成组合。

## 《毛选》1—5 卷精读

项目包含五卷导读索引与精读协议，可用于：

- 定位篇目、卷次、写作阶段和核心议题
- 重建“前提—事实/例证—推理—结论”的论证链
- 识别核心概念、批评对象、隐含前提和失效条件
- 比较同一概念在革命、建设与治理语境中的变化
- 建立概念表、问题表、方法表和争议表
- 区分文本证据、跨篇解释、历史推断与现代类比

仓库不收录《毛泽东选集》整卷原文。需要逐字引用、页码核验或完整精读时，应使用有权访问的可靠版本，并按照 [`references/close-reading-protocol.md`](references/close-reading-protocol.md) 建立可回溯笔记。

## 项目结构

```text
mao-thought-advisor/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── methods.md
    ├── source-map.md
    ├── volumes-1-5.md
    ├── close-reading-protocol.md
    └── decision-checklist.md
```

- [`SKILL.md`](SKILL.md)：触发范围、工作方式、回答结构与边界
- [`references/methods.md`](references/methods.md)：100 项方法论工作索引
- [`references/source-map.md`](references/source-map.md)：方法与主要文本出处地图
- [`references/volumes-1-5.md`](references/volumes-1-5.md)：《毛选》第一至第五卷导读索引
- [`references/close-reading-protocol.md`](references/close-reading-protocol.md)：原文精读与证据分级协议
- [`references/decision-checklist.md`](references/decision-checklist.md)：12 项重大决策自查清单

## 史料原则

- 原文概念、后人概括和现代操作化必须分别标明
- 篇名、日期、卷次、页码和引文不确定时必须核验
- 搜索摘要与论坛转载只能用于发现线索，不能直接作为原文证据
- 第五卷及政治运动相关文本需要说明编纂背景、历史后果与研究争议
- 历史结论不得脱离时代条件机械套用于当代生活

## 使用边界

本项目用于历史思想研究与合法的现实问题分析。战争、斗争、敌我等历史概念在现代应用中只转译为非暴力的竞争、协商、组织、风险控制和问题解决方法，不用于暴力、迫害、非法监控、仇恨动员或政治操纵。

它不能替代法律、医疗、财务和心理健康等专业意见。

## 参与完善

欢迎通过 Issue 或 Pull Request 提交：

- 可核验的篇目、日期、版本和出处修正
- 方法条目的遗漏、重复或错误归类
- 更清晰的现代应用案例
- 《毛选》不同篇目之间的交叉引用
- Codex 与 OpenClaw 的兼容性改进

提交史料修正时，请尽量附上版本、出版社、年份、页码或可靠公开链接。

## License

项目原创说明、结构化索引和 Skill 配置采用 [MIT License](LICENSE)。书名、篇名、历史材料及引用内容的权利归其各自权利人所有。
