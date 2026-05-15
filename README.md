# Nexus — 组织级信息连接平台

> **异步 · 半结晶 · AI 增厚**  
> 解决项目间 / 团队间的信息断裂问题，让组织知道彼此在做什么。

---

## 项目概述

Nexus 是面向 20-200 人规模组织的信息共享、沉淀与发现平台。它不替代 Odin / WeThink / 企微等一线生产工具，而是作为**下游聚合层**——把散落在不同团队、不同工具里的信息碎片，通过 AI 自动建立关联、翻译语境、预警风险。

### 核心定位

| | 现有工具 | Nexus |
|---|---|---|
| 解决什么 | 把事做好（项目内执行） | 让组织知道你在做什么（跨项目/跨团队透明） |
| 信息形态 | 实时协作 | 异步结晶 |
| 关系 | 加法，不是替代 | 聚合层，不是新入口 |

---

## AI 三大角色

Nexus 的 AI 从**信息断裂**这一核心问题倒推，只做三件事：

### 1. 连接 — 跨源连接器

把分散在不同团队、不同工具里的信息碎片，自动建立关联。

> 张明团队做受助人画像，林敏团队做标签架构，王芳团队做捐赠者聚类——三个团队不知道彼此在做本质相同的底层工作。AI 看得到。

### 2. 翻译 — 跨语境翻译器

技术团队说「标签体系重构」，业务团队说「用户画像升级」，管理层想知道「这两件事是不是一个项目」。AI 把不同团队的表述映射到统一的组织语义空间。

### 3. 信号预警 — 组织级信号检测器

项目停更 14 天没人注意，上游评审已通过但下游还在等——这些信号淹没在日常信息流里。AI 持续监测信息流中的异常模式，主动预警。

---

## AI 产品密度：5 层能力矩阵

AI 在信息生命周期的**每个节点**都有介入，不是最后加一个「AI 总结」按钮，而是全链路增厚：

| 层次 | 能力 | 做什么 | AI 角色 |
|:---:|------|--------|:-------:|
| L1 | **增厚每条信息** | 发布时自动补充上下文（OKR、历史、关联团队） | 连接 + 翻译 |
| L2 | **维护知识图谱** | 持续维护项目-人-目标关系图，新信息自动更新 | 连接 |
| L3 | **主动生成洞察** | 扫描跨团队信息流，发现协同机会和信息断裂 | 连接 + 预警 |
| L4 | **时间线追踪** | 监测进展节奏，检测卡点和异常停滞 | 预警 |
| L5 | **角色化重建** | 同一信息按消费者角色重建叙事结构 | 翻译 |

5 层是**密度递增**关系：L1 → L2 → L3 → L4 → L5，每一层让前一层更有价值。

---

## 交互原型 Demo

所有 Demo 均为纯 HTML 文件，浏览器直接打开即可预览。

| Demo | 文件 | 说明 |
|------|------|------|
| Chat Insight（方案 A） | [`demos/nexus-slide-a-visual.html`](demos/nexus-slide-a-visual.html) | 结构化卡片式洞察呈现 |
| Chat Insight（对话式） | [`demos/nexus-chat-insight.html`](demos/nexus-chat-insight.html) | 对话式 AI 洞察交互 |
| 方案 A/B 对比 | [`demos/nexus-chat-insight-compare.html`](demos/nexus-chat-insight-compare.html) | 结构化卡片 vs 全文字的对比 |
| VP 驾驶舱 | [`demos/nexus-vp-dashboard.html`](demos/nexus-vp-dashboard.html) | 管理者视图：组织脉搏总览 |
| TL 工作台 | [`demos/nexus-tl-workbench.html`](demos/nexus-tl-workbench.html) | 团队负责人视图：团队脉搏 |
| IC 视图 | [`demos/nexus-ic-view.html`](demos/nexus-ic-view.html) | 普通员工视图：与我相关 |
| 汇报展示集 | [`demos/nexus-slides-showcase.html`](demos/nexus-slides-showcase.html) | 全部方案的汇报展示合集 |

### 快速预览

```bash
# macOS
open demos/nexus-vp-dashboard.html

# 或用任意浏览器打开 demos/ 下的 HTML 文件
```

---

## 设计文档

| 文档 | 说明 |
|------|------|
| [**方案说明 v2**](docs/design-spec-v2.md) | 最新版设计方案：AI 三角色 + 5 层密度 + Demo 解读 |
| [方案说明 v1](docs/design-spec-v1.md) | 初版设计方案 |
| [善擎参考资料](docs/shanqing-reference.md) | 善擎（ShanQing）产品架构参考，用于对照 Nexus 设计 |

---

## 设计原则

1. **发布必须抵消已有工作** — 发了就不用另写周报
2. **管理者先行** — 老板先发，降低社交压力
3. **场景框定** — 不做空白画布，预设场景消除「不知道发什么」焦虑
4. **极低摩擦输入** — MCP 一键导入会议记录 / OKR

---

## 目录结构

```
nexus-design/
├── README.md                 # 本文件
├── docs/
│   ├── design-spec-v2.md     # 方案说明（最新）
│   ├── design-spec-v1.md     # 方案说明（初版）
│   └── shanqing-reference.md # 善擎参考资料
└── demos/
    ├── nexus-chat-insight.html
    ├── nexus-chat-insight-compare.html
    ├── nexus-slide-a-visual.html
    ├── nexus-slides-showcase.html
    ├── nexus-vp-dashboard.html
    ├── nexus-tl-workbench.html
    └── nexus-ic-view.html
```

---

## License

Internal use only. © 2026
