<div align="center">

# 钱呢 · Qianne

![Version](https://img.shields.io/badge/Version-0.1.0-34C759?style=flat-square)
![Build](https://img.shields.io/badge/Build-1-6E7681?style=flat-square)
![Status](https://img.shields.io/badge/Status-In_Development-F2A93B?style=flat-square)
![Platform](https://img.shields.io/badge/Focus-iPhone-007AFF?style=flat-square)

### 钱呢？让每一笔钱，都有清楚的去向。

一款本地优先、原生体验的记账与资产管理 App。

从日常收支到账户资产，帮你看清钱去哪了、还剩多少、哪些钱还没收回来。

**原生体验 · 本地优先 · 规则一致**

</div>

---

## 版本信息

| 项目 | 当前信息 |
| --- | --- |
| App 版本 | **0.1.0** |
| 构建号 | **1**（App 内显示为 `0.1.0 (1)`） |
| 版本阶段 | 开发版本 · 本地记账 MVP |
| 当前重点 | iPhone 原生体验 |
| 工程最低系统 | iOS 26.0 · macOS 26.0 |
| 信息核对日期 | 2026-10-13 |

版本号与构建号来自 [Apple 工程配置](https://github.com/qianne-app/qianne-apple/blob/main/Qianne.xcodeproj/project.pbxproj)，随 App 版本变更同步维护。本页展示的是开发工程版本，正式发布信息以实际发布公告为准。

## 关于钱呢

钱呢希望让记账成为一件自然、轻松的事：快速记下一笔，随时查看流水，在需要时了解收支变化和资产状况。

我们从 iPhone 开始，以 SwiftUI 构建 Apple 原生客户端，逐步完善 iPad、Mac 体验；后续规划 Android、鸿蒙原生客户端，以及用于账号、同步与备份的 Go 后台。

## 核心功能

| 方向 | 内容 |
| --- | --- |
| 日常记账 | 支出、收入、转账，流水查看与编辑，多账本管理 |
| 资产管理 | 资金、信用、充值、投资等账户，资产分组，净资产与负债查看 |
| 账户详情 | 跨账本流水、余额走势、余额校准与账户管理 |
| 退款与报销 | 关联原支出查看退款，跟踪垫付与待报销款项 |
| 借入与借出 | 管理应付、应收，了解尚未归还或收回的金额 |
| 收支分析 | 月度、年度汇总，趋势、分类排行与明细下钻 |
| 分类与预算 | 分类管理、分类模板与预算进度 |

## 我们坚持的原则

- **本地优先**：当前 MVP 在本地 SQLite 中完成读写，核心记账不依赖后台连接。
- **原生体验**：各平台采用原生技术，尊重平台的交互习惯。
- **一套业务标准**：数据模型、计算规则和共享测试用例统一维护，各端实现保持一致。
- **金额准确**：金额使用最小货币单位的整数表示，余额、统计与预算按统一规则计算。
- **记录可追溯**：余额由初始金额和流水推导；退款、报销与余额调整各有明确的计算边界。

## 仓库导航

| 仓库 | 职责 | 技术 |
| --- | --- | --- |
| [qianne-apple](https://github.com/qianne-app/qianne-apple) | Apple 客户端、领域规则与本地存储 | Swift 6 · SwiftUI · GRDB · SQLite |
| [qianne-spec](https://github.com/qianne-app/qianne-spec) | 跨端数据模型、业务规则、SQLite 基准结构、同步协议草案与共享测试 | Markdown · SQL · JSON · Go 参考实现 |

以上两个仓库目前为私有仓库，访问需要相应权限。本页用于公开介绍项目。

## 开发进展

**当前：开发中的本地记账 MVP，以 iPhone 体验为重点。**

- 正在完善：记账、资产、统计、预算、退款、报销和借贷等核心流程。
- 逐步推进：iPad、Mac 的原生体验适配。
- 后续规划：Go 后台、账号体系、多设备同步、云端备份与共享账本，以及 Android、鸿蒙客户端。

多设备同步、云端服务和其他平台客户端仍属于规划内容。后续发布与可用范围以实际版本为准。

## 技术与协作

Apple 客户端采用 **SwiftUI → 数据存储层 → 领域规则层** 的分层结构，使用 GRDB / SQLite 保存本地数据。当前工程的最低系统配置为 iOS 26、macOS 26。

业务规则以 `qianne-spec` 为标准：先维护规则与共享测试，再由各端原生实现并验证同一批用例。Go 参考实现用于核验规则与测试数据，未来后台负责账号、同步和备份。

---

<div align="center">

**钱呢 · 把账记清，把钱看明白。**

</div>
