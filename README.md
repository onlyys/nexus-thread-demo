# SSV Nexus · 讨论模块升级 Demo

> Nexus 评论区 → 讨论区 升级原型仓库。
> 📦 **当前开发中：v1.2.0**（基于 v1.1.0 起）
> 📌 **最新冻结版本：v1.1.0**（2026-05-06）—— Thread 化 + 我也来参加讨论独立卡片
> 📄 当前需求文档：[v1.2（开发中）](docs/requirement-v1.2.md)

---

## 🚀 在线预览

### 主线（开发中 · 持续更新）

| Demo | 链接 |
|---|---|
| 🧵 **Thread 讨论模块** | [thread-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/thread-demo.html) |
| 🔔 通知中心 | [notification-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/notification-demo.html) |
| 📡 通知触达配置 | [reach-demo.html](https://onlyys.github.io/nexus-thread-demo/demos/reach-demo.html) |

### 历史版本（已冻结 · 可回看对比）

| 版本 | 时间 | 核心改动 | 入口 |
|---|---|---|---|
| **v1.1.0** | 2026-05-06 | Thread 化 + 混合态 C + 标记已解决 + My 待办 + AI 总结右栏 | [v1.1 demo →](https://onlyys.github.io/nexus-thread-demo/demos/v1.1/thread-demo.html) |
| **v1.0.0** | 2026-04 月 | 评论改名"讨论" 9 处文案 | [v1.0 说明页 →](https://onlyys.github.io/nexus-thread-demo/demos/v1.0/index.html) |

> 💡 v1.0 是纯文案改造、复用 Nexus 原生 UI，因此没有可点击 demo——见说明页或在 v1.1 demo 切到「新旧对比」场景。

---

## 📁 目录结构

```
nexus-thread-demo/
├── README.md
├── demos/
│   ├── thread-demo.html              ← 主线（开发中）
│   ├── notification-demo.html
│   ├── reach-demo.html
│   ├── v1.1/                         ← v1.1.0 冻结副本
│   │   ├── thread-demo.html
│   │   ├── notification-demo.html
│   │   └── reach-demo.html
│   └── v1.0/
│       └── index.html                ← v1.0 文字说明页
└── docs/
    ├── requirement-v1.2.md           ← 当前开发版本
    ├── requirement-v1.1.md           ← v1.1 历史
    ├── requirement-v1.0.md           ← v1.0 历史
    ├── v1.1/requirement.md           ← 冻结副本
    └── v1.0/requirement.md           ← 冻结副本
```

---

## 🎨 设计系统（沿用）

完全对齐 [mx9702098-glitch/ssv-nexus-prototype](https://github.com/mx9702098-glitch/ssv-nexus-prototype)：

| Token | 值 | 用途 |
|---|---|---|
| `#1f2328` | 墨黑 | 品牌 / 主文字 / 激活态 |
| `#f5f6f8` | 冷米白 | 页面底色 |
| `#e6e8eb` | 分隔线 | 边框 |
| `#2563eb` | 品牌蓝 | 链接 / @提及 / 转待办 |
| `#059669` | 成功绿 | 已完成 / 已解决 |
| `#c2410c` | 警示橙 | 等待回复 / 即将到期 |
| `#dc2626` | 告警红 | 未读 / 逾期 |

**字体**：`-apple-system, BlinkMacSystemFont, "PingFang SC", "Helvetica Neue"` 原生栈（不加载外部字体）

---

## 🔁 版本管理约定

- **冻结**：每个正式版本 `vX.Y.Z` 完成时打 Git tag，并把 demo 复制到 `demos/vX.Y/` 子目录形成线上副本
- **主线**：`demos/thread-demo.html` 始终代表"当前开发中的最新状态"，可能会随时变化
- **回看**：任何历史版本都可通过 `demos/vX.Y/` URL 永久访问
- **变更记录**：每个 `requirement-vX.Y.md` 的附录 B

### 已发布版本一览

| 版本 | Tag | 发布日期 | 主题 |
|---|---|---|---|
| v1.0.0 | — | 2026-04 月 | 评论 → 讨论 文案改名（9 处） |
| v1.1.0 | `v1.1.0` | 2026-05-06 | Thread 化讨论区 + 我也来参加讨论 |
| v1.2.0 | 🚧 开发中 | — | （待产品评审定题） |

---

## 🔗 相关资料

- 🎨 [Nexus 参考原型](https://github.com/mx9702098-glitch/ssv-nexus-prototype)
- 👤 需求提出：brantli(李哲) · 2026-04-29
- ✏️ 设计：西比柚（onlyys）
- 📅 v1.0 发布：2026-04-30 · v1.1 冻结：2026-05-06
