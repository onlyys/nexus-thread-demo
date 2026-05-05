# SSV Nexus · 讨论模块升级 Demo

> Nexus 评论区 → 讨论区 升级原型，包含 **Thread 机制**、**讨论转待办**、**通知中心** 与 **触达配置** 三件套。
> 📦 版本：**v1.1**（2026-05-05 · 外壳与 Nexus 产品线对齐）
> 📄 需求文档：[docs/requirement-v1.0.md](docs/requirement-v1.0.md)

---

## 🚀 在线预览

| Demo | 链接 | 说明 |
|---|---|---|
| 🧵 **Thread 讨论模块**（主） | [thread-demo.html](https://onlyys.github.io/nexus-thread-demo/thread-demo.html) | 5 个场景页：话题列表 / Event 讨论区 / 新旧模式对比 / 空态文案替换 / 全链路流程 |
| 🔔 通知中心 | [notification-demo.html](https://onlyys.github.io/nexus-thread-demo/notification-demo.html) | 通知列表、未读筛选、@提及高优、企微 Bot 汇总 |
| 📡 通知触达配置 | [reach-demo.html](https://onlyys.github.io/nexus-thread-demo/reach-demo.html) | 渠道开关、免打扰时段、P1/P2/P3 优先级矩阵、聚合策略 |

**建议路径**：先 Thread Demo → 依次切 4 个场景 tab → 再看通知中心 + 触达配置。

---

## 🎯 v1.1 相比 v1.0 的主要变化

| 维度 | v1.0（已弃用） | v1.1（本版） |
|---|---|---|
| **外壳** | 自造：30px 圆角 Logo + 衬体字 + 顶部 tab | 与 [Nexus 参考原型](https://github.com/mx9702098-glitch/ssv-nexus-prototype) 完全一致：墨黑方块 Logo + 无衬线 "SSV Nexus" + 竖线 + slogan |
| **侧栏** | 业务化：筛选 / 分类 | 全局产品导航：TOPICS(ALL/MY) + TOOLS(Skills/插件) + ADMIN(定位/宪章/设置/通知中心/触达配置) |
| **字体** | DM Sans + Noto Serif SC（混用 serif） | `-apple-system, "PingFang SC"` 原生字体栈（与 Nexus 一致） |
| **场景页** | 4 个 | 5 个（新增"空态文案替换"，基于业务方截图对照） |

---

## 🧵 Thread Demo · 场景 tab 说明

### 1. 话题列表
- 带 `🔥 1 讨论激增` 红色热度标，对应需求文档 §4.6「讨论激增作为首屏热词」

### 2. Event 讨论区（主展示面）
- **3 条静态 Thread**：
  - `t1` 已有 4 条回复 + ✅ 已转为待办（展开看结论链）
  - `t2` 等待回复中
  - `t3` 暂无回复（首个回复场景）
- **发起新讨论**：虚线卡片 → 填写内容 → Enter 发送 → 讨论区自动新增 Thread + 右上角推送通知
- **📌 讨论转待办**：点任意 reply 的 `···` 菜单 → 弹窗填写（自动抓取 @的对象作为指派人） → Event 待办列表新增 + Thread 卡片出现 `✅ 已转为待办` chip + 底部系统消息
- **闭环**：勾选 Event 待办 → Thread 底部自动插「✓ xx 已完成关联待办」

### 3. 新旧模式对比
- 左：扁平评论 8 条（3 议题混排）
- 右：同样内容拆成 3 条 Thread（每议题独立成线）
- 问题 / 收益标注

### 4. 空态文案替换（基于业务方截图）
- 左：现网旧评论空态 "写下你的评论 / 暂无评论，来发表第一条吧"
- 右：新讨论空态 "发起讨论... / 还没有人发起讨论，来开启第一条"
- 附：9 处文案改动速览（§3.2 全量）

### 5. 全链路流程
- 6 步闭环：发起 → 通知 → 多人回复 → @指派 → 转待办 → 完成同步

---

## 🎨 设计系统

完全对齐 [mx9702098-glitch/ssv-nexus-prototype](https://github.com/mx9702098-glitch/ssv-nexus-prototype)：

| Token | 值 | 用途 |
|---|---|---|
| `#1f2328` | 墨黑 | 品牌 / 主文字 / 激活态 |
| `#f5f6f8` | 冷米白 | 页面底色 |
| `#e6e8eb` | 分隔线 | 边框 |
| `#2563eb` | 品牌蓝 | 链接 / @提及 / reply chip |
| `#059669` | 成功绿 | 已完成 / 已转待办 |
| `#c2410c` | 警示橙 | 等待回复 / 范围外 |
| `#ef4444` | 红点 | 未读 / 告警 |

- **字体**：`-apple-system, BlinkMacSystemFont, "PingFang SC", "Helvetica Neue"` 原生栈（不加载外部字体）
- **间距**：`r-sm=4 / r=8 / r-lg=12 / r-xl=16`
- **圆角语言**：按钮 8 / 卡片 12 / Logo 8

---

## 📁 目录结构

```
nexus-thread-demo/
├── README.md                   ← 本文件
├── thread-demo.html            ← 主 Demo（67 KB）
├── notification-demo.html      ← 通知中心（31 KB）
├── reach-demo.html             ← 触达配置（24 KB）
└── docs/
    └── requirement-v1.0.md     ← 需求文档 v1.0（11 KB）
```

---

## 📋 评审待确认决策点（出自需求文档 §10）

1. Thread 内回复是否支持附件（建议 A：支持）
2. 转待办时是否必须指派人（建议 A：必须）
3. Thread 是否支持"标记为已解决"（建议 A：支持）
4. 空 Thread（0 回复）是否折叠（建议 B：>10 条时折叠旧 Thread）
5. 历史评论数据迁移时机（建议 A：上线时一次性迁移）

---

## 🔗 相关资料

- 📄 [需求文档 v1.0](docs/requirement-v1.0.md)
- 🎨 [Nexus 参考原型](https://github.com/mx9702098-glitch/ssv-nexus-prototype)
- 👤 需求提出：brantli(李哲) · 2026-04-29
- ✏️ 设计：西比柚（onlyys）
