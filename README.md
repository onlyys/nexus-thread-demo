# SSV Nexus · 讨论模块升级 Demo

> Nexus 评论区 → 讨论区 升级原型演示，含 Thread 机制、通知中心、触达配置。

## 在线预览

| 页面 | 链接 | 说明 |
|---|---|---|
| 🧵 Thread Demo | [thread-demo.html](https://onlyys.github.io/nexus-thread-demo/thread-demo.html) | 讨论模块核心交互（话题列表 / Event 详情 / Thread 展开收起 / 转子任务 / 新旧对比） |
| 🔔 通知中心 | [notification-demo.html](https://onlyys.github.io/nexus-thread-demo/notification-demo.html) | 通知列表、未读状态、详情面板、筛选、Bot 推送 |
| 📡 触达配置 | [reach-demo.html](https://onlyys.github.io/nexus-thread-demo/reach-demo.html) | 渠道开关、免打扰时段、P1/P2/P3 优先级矩阵、聚合策略 |

## 设计系统

基于 [ssv-nexus-prototype](https://github.com/mx9702098-glitch/ssv-nexus-prototype) 的 Design Token：

- `--paper: #FAFAF8` 暖米白背景
- `--ink: #1A1918` 正文墨色
- `--blue: #2563EB` 品牌蓝 / @提及
- `--green: #059669` 成功 / 已完成
- 字体：DM Sans + Noto Sans SC + Noto Serif SC

## 目录结构

```
├── thread-demo.html         # 讨论模块核心 Demo
├── notification-demo.html   # 通知中心 Demo
├── reach-demo.html          # 触达配置 Demo
├── docs/
│   └── requirement-v1.0.md  # 需求文档 v1.0
└── README.md
```

## 需求概览

本次升级分为两个方面：

1. **文案改名**：评论 → 讨论（9 处文案改动）
2. **Thread 机制 + 讨论转子任务**（结构性功能升级）

详见 [需求文档](docs/requirement-v1.0.md)

## 如何预览

1. 开启 GitHub Pages（Settings → Pages → Source: main / root）
2. 访问 `https://onlyys.github.io/nexus-thread-demo/thread-demo.html`

或直接下载 HTML 文件本地打开即可。
