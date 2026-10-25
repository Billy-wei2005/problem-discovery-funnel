# Problem Discovery Funnel

一个“宽进严出”的 Codex Skill，用于收集现实问题线索、按明确研究方向进行二次复核，并将证据充分的候选晋级为可审计的正式问题节点。

它只研究问题，不生成解决方案、产品构想、商业计划或投资判断。

## 三层问题库

```text
problem-library/
├── 01-candidate-pool/       # 高召回、低过滤的原始候选线索
├── 02-directional-review/   # 围绕明确方向的翻找、核对与二次采纳
└── 03-verified-nodes/       # 经过严格证据审查的正式问题节点
```

第一层允许保存荒谬、疯狂、互相矛盾或证据不足的线索。第二层的“不采纳”不会删除第一层记录。第三层保留支持证据、反证、证据缺口、依赖关系和版本历史。

## 安装

将整个目录复制到 Codex skills 目录：

```bash
cp -R problem-discovery-funnel ~/.codex/skills/
```

然后在 Codex 中使用：

```text
$problem-discovery-funnel 收集这批访谈中的问题线索，先只做开放式初选。
```

```text
$problem-discovery-funnel 以“临床交接中的上下文丢失”为方向复核候选池，暂时不要生成正式节点。
```

```text
$problem-discovery-funnel 严格核验已采纳候选，并把符合条件的记录晋级为正式问题节点。
```

## 结构

- `SKILL.md`：入口、阶段路由和共同认识论约束。
- `references/01-open-collection.md`：开放式初选规则及候选卡 Schema。
- `references/02-directional-review.md`：方向性复核与二次采纳记录。
- `references/03-strict-verification.md`：严格验证及正式节点 Schema。
- `references/evidence-taxonomy.md`：证据层级、受控词表与同构判断门槛。
- `problem-library/`：三层实际记录库。

## 核心原则

> 初选追求不漏，复核追求相关，验证追求不假；所有阶段都保留审计轨迹。
