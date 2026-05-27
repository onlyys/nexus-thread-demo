# SSV Nexus · 讨论模块升级 Demo

> Nexus 评论区 → 讨论区 升级原型仓库。
> 📦 **当前开发中：v1.2.0**（2026-05-07 定稿 · 等待开发评审）
> 📌 **最新冻结版本：v1.1.0**（2026-05-06）—— Thread 化 + 我也来参加讨论独立卡片
> 📄 当前需求文档：[v1.2（定稿）](docs/requirement-v1.2.md)

---

## 🚀 在线预览

### 主线（v1.2 · 当前开发）

| Demo | 链接 |
|---|---|
| 🎯 **v1.2 Event 讨论区**（定稿） | [v1.2-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/v1.2-demo.html) |
| 🔍 v1.2 视觉方向对比（归档） | [v1.2-compare.html](https://onlyys.github.io/nexus-thread-demo/demos/v1.2-compare.html) |
| 🧵 v1.2 前的 Thread Demo（历史） | [thread-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/thread-demo.html) |
| 🔔 通知中心 | [notification-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/notification-demo.html) |
| 📡 通知触达配置 | [reach-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/reach-demo.html) |

### 目标地图 · GOALS（Notion 风 · 2026-05）

| Demo | 链接 |
|---|---|
| 🎯 **部门目标页**（公益平台部） | [ssv-nexus-goals.html](https://onlyys.github.io/nexus-thread-demo/demos/ssv-nexus-goals.html) |
| 📋 **关键策略 · 全部 Topic** | [ssv-nexus-strategy-topics.html](https://onlyys.github.io/nexus-thread-demo/demos/ssv-nexus-strategy-topics.html) |
| ✏️ **创建 Topic**（关联部门策略 · 弹窗选策略） | [create-topic.html](https://onlyys.github.io/nexus-thread-demo/demos/create-topic.html) |

### AI 洞察（Chat Insight）

| Demo | 链接 |
|---|---|
| ✦ **AI 洞察方案对比**（卡片 vs 全文字） | [chat-insight-compare.html](https://onlyys.github.io/nexus-thread-demo/demos/chat-insight-compare.html) |
| 📄 Chat Insight 设计方案文档 | [chat-insight-design.md](https://onlyys.github.io/nexus-thread-demo/docs/chat-insight-design.md) |

### 历史版本（已冻结 · 可回看对比）

| 版本 | 时间 | 核心改动 | 入口 |
|---|---|---|---|
| **v1.1.0** | 2026-05-06 | Thread 化 + 混合态 C + 标记已解决 + My 待办 + AI 总结右栏 | [v1.1 demo →](https://onlyys.github.io/nexus-thread-demo/demos/v1.1/thread-demo.html) |
| **v1.0.0** | 2026-04 月 | 评论改名"讨论" 9 处文案 | [v1.0 说明页 →](https://onlyys.github.io/nexus-thread-demo/demos/v1.0/index.html) |

---

## 🎯 v1.2 核心变化

> **定位修正**：Nexus 是信息透明 / 信息呈现 / AI 辅助决策平台，**不是研发辅助工具**。

| 改动 | 方向 |
|---|---|
| **撤销 Thread 概念** | 全站只有 Topic + Event，不再有"话题束"白底卡片 |
| **视觉降噪** | 讨论区靠字体字号+树形竖线表达结构，不靠边框/卡片 |
| **Meta 全隐藏** | 状态 chip (`✅ 已转为待办` 等) 全部移除；时间戳 hover 才显 |
| **树形竖线** | GitHub PR 风 —— 首条下来 T 字分叉到每条回复，末端收束 |
| **输入框置顶** | X 风格 —— 讨论区第一眼就是输入框（白底虚线 + ✨ 加入讨论） |
| **点赞 + 转待办浮层** | hover 才显、白底浮层、不占 layout，不抢内容 |
| **「来看」列表** | 替代 v1.1 My 待办 —— @ 驱动的信息请求，回了就闭环 |
| **署名简化** | `Brant 【钟嘉辉】` 取代 `钟嘉辉 · 技术架构` |
| **富内容降权** | 图片浅灰占位 / 文件 inline 链接 / @ 去底色 |

详细见 [requirement-v1.2.md](docs/requirement-v1.2.md)。

---

## 📁 目录结构

```
nexus-thread-demo/
├── README.md
├── demos/
│   ├── v1.2-demo.html                ← ⭐ v1.2 主 demo（定稿）
│   ├── v1.2-compare.html             ← v1.2 视觉方向对比（归档）
│   ├── thread-demo.html              ← v1.1 遗留（保留）
│   ├── chat-insight-compare.html     ← ✦ AI 洞察方案对比
│   ├── notification-demo.html
│   ├── reach-demo.html
│   ├── v1.1/                         ← v1.1.0 冻结副本
│   │   ├── thread-demo.html
│   │   ├── notification-demo.html
│   │   └── reach-demo.html
│   └── v1.0/
│       └── index.html                ← v1.0 文字说明页
└── docs/
    ├── requirement-v1.2.md           ← ⭐ 当前定稿
    ├── requirement-v1.1.md           ← v1.1 历史
    ├── requirement-v1.0.md           ← v1.0 历史
    ├── chat-insight-design.md        ← ✦ AI 洞察设计方案
    ├── v1.1/requirement.md           ← 冻结副本
    └── v1.0/requirement.md           ← 冻结副本
```

---

## 🎨 设计系统（v1.2 强化 · 向字号要层次）

核心 token：

| Token | 值 | 用途 |
|---|---|---|
| `#1f2328` | 墨黑 | 主文字 |
| `#f5f6f8` | 冷米白 | 页面底色 |
| `#e6e8eb` | 分隔线 / 树形竖线 | 2px |
| `#2563eb` | 品牌蓝 | 链接 / @ |
| `#c7d2fe` | 浅蓝虚线 | 发起框邀请感 |
| `#dbeafe` | 极淡蓝 | 链接下划线（降权）|
| `#9ca3af` | 中灰 | 辅助文字（【中文名】）|

字号梯度（v1.2 新定）：

```
Event 标题 26 → Event 正文 15.5
  ↓
首条 text 15 · 首条 author 14.5
  ↓
回复 text 14 · 回复 author 13.5
  ↓
子回复 text 13.5 · 子回复 author 12.5
```

**原则**：text 永远 ≥ author，让"讲了什么"大于"谁说的"。

---

## 🔁 版本管理约定

- **冻结**：每个正式版本 `vX.Y.Z` 完成时打 Git tag，并把 demo 复制到 `demos/vX.Y/` 子目录形成线上副本
- **主线**：`demos/v1.2-demo.html` 是当前最新状态
- **回看**：任何历史版本都可通过 `demos/vX.Y/` URL 永久访问

### 已发布版本一览

| 版本 | Tag | 发布日期 | 主题 |
|---|---|---|---|
| v1.0.0 | — | 2026-04 月 | 评论 → 讨论 文案改名（9 处） |
| v1.1.0 | `v1.1.0` | 2026-05-06 | Thread 化讨论区（已被 v1.2 撤销） |
| v1.2.0 | 🔵 定稿 | 2026-05-07 | 撤 Thread + 视觉降噪 + 树形竖线 + 「来看」列表 |

---

## 🔗 相关资料

- 🎨 [Nexus 参考原型](https://github.com/mx9702098-glitch/ssv-nexus-prototype)
- 👤 需求提出：brantli(李哲) · 2026-04-29
- ✏️ 设计：西比柚（onlyys）
- 📅 v1.0 发布：2026-04-30 · v1.1 冻结：2026-05-06 · v1.2 定稿：2026-05-07
