# SSV Nexus · 讨论模块升级 Demo

> Nexus 评论区 → 讨论区 升级原型。v1.1 基于 2026-05-05 评审讨论迭代，聚焦 **Thread 默认态优化**、**标记已解决闭环**、**My 待办跟踪**。
> 📦 **当前版本：v1.1**（2026-05-05）· [查看变更日志](docs/requirement-v1.1.md#v10--v11-变更速览)
> 📄 **需求文档**：[v1.1（当前）](docs/requirement-v1.1.md) · [v1.0（历史）](docs/requirement-v1.0.md)

---

## 🚀 在线预览

| Demo | 链接 |
|---|---|
| 🧵 **Thread 讨论模块**（主菜 · 6 场景页） | [thread-demo.html](https://onlyys.github.io/nexus-thread-demo/thread-demo.html) |
| 🔔 通知中心 | [notification-demo.html](https://onlyys.github.io/nexus-thread-demo/notification-demo.html) |
| 📡 通知触达配置 | [reach-demo.html](https://onlyys.github.io/nexus-thread-demo/reach-demo.html) |

**建议路径**：Thread Demo 依次切 6 个 Tab → 通知中心 → 触达配置。

---

## 🆕 v1.1 相比 v1.0 的变化

### 交互改进

| 变化 | 说明 |
|---|---|
| **Thread 默认态**：全收起 → **混合态 C** | 首条消息 + 最新 1 条回复永远可见，中间历史折叠为"查看 N 条历史回复"；冷 Thread（>3 天无回复）整体收起打 🧊 标 |
| **系统消息克制化** | 原版居中绿字抢戏 → 11.5px 浅灰 + 细虚线 + 图标点色分层（蓝=转待办 / 绿=完成 / 蓝灰=已解决）|

### 新增功能

| 功能 | 入口 |
|---|---|
| ✓ **Thread 标记已解决** | Thread 头部 `···` 菜单 → `标记已解决`，hover 可撤销 |
| 📋 **My · 待办跟踪** | 新场景 Tab · 双视角（我的/我发出的）· 跨 Topic 聚合 · 状态筛选 |
| 💬 **空态文案替换** | 基于业务方截图，可视化所有 9 处文案改动 |

### 文档与定位

| 内容 | 说明 |
|---|---|
| **附录 A · Nexus vs Linear vs 飞书** | 在 AI 协同视角下的三者对比，明确 Nexus 差异化定位 |
| **附录 B · AI 在 Thread 中的角色（v1.2 规划）** | 5 个 AI 能力候选，按优先级排序 |

---

## 🧵 Thread Demo · 6 个场景 Tab

| # | 场景 | 看什么 |
|---|---|---|
| 1 | **话题列表** | 带 🔥 讨论激增 热度标，对应 §4.6 |
| 2 | **Event 讨论区** | 4 条 Thread（含 1 条冷态）· 混合态 C · 转待办 · 待办回写 · 标记已解决 |
| 3 | **新旧模式对比** | 左：扁平混排 8 条评论（3 议题乱飞）· 右：3 条 Thread（议题独立）|
| 4 | **空态文案替换** | 左：现网截图还原 · 右：v1.0 文案改后状态 + 9 处速览 |
| 5 | **My · 待办跟踪**🆕 | 双视角跨 Topic 聚合 · 状态筛选 · AI 参谋条 |
| 6 | **全链路流程** | 6 步闭环：发起→通知→回复→@→转待办→完成同步 |

---

## 🎨 设计系统

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

## 📁 目录结构

```
nexus-thread-demo/
├── README.md                   ← 本文件
├── thread-demo.html            ← 主 Demo（84 KB · 6 场景页）
├── notification-demo.html      ← 通知中心（31 KB · Nexus 外壳）
├── reach-demo.html             ← 触达配置（24 KB · Nexus 外壳）
└── docs/
    ├── requirement-v1.1.md     ← 需求文档 v1.1（当前）
    └── requirement-v1.0.md     ← 需求文档 v1.0（历史）
```

---

## 📋 当前待确认决策点（出自 v1.1 §10）

### ✅ v1.0 · 5 条已决（本次评审拍板）
1. Thread 内回复 **支持附件** ✅
2. 转待办 **必须指派人** ✅
3. Thread **支持标记已解决** ✅
4. 空 Thread **改为混合态 C**（不简单折叠）✅
5. 历史数据 **上线时一次性迁移** ✅

### 🆕 v1.1 · 3 条新待确认
6. Thread "已解决"权限范围
7. 指派人对待办的催办频率
8. AI 在 Thread 中的 5 个角色（Phase 2 选优先级）

---

## 🔗 相关资料

- 📄 [需求文档 v1.1](docs/requirement-v1.1.md) · [v1.0](docs/requirement-v1.0.md)
- 🎨 [Nexus 参考原型](https://github.com/mx9702098-glitch/ssv-nexus-prototype)
- 👤 需求提出：brantli(李哲) · 2026-04-29
- ✏️ 设计：西比柚（onlyys）
- 📅 v1.0 发布：2026-04-30 · v1.1 发布：2026-05-05

<!-- v1.1 rebuild trigger: 2026-05-06T10:26:54.517478 -->
