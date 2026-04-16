---
title: "Source: 套餐订单系统发放短信梳理"
type: source
tags:
  - "#domain/notification"
  - "#type/capability"
created: 2026-04-16
updated: 2026-04-16
sources:
  - "raw/dingtalk-sms-notification.md"
direct_link: "raw/dingtalk-sms-notification.md"
aliases:
  - "短信梳理"
---
# 套餐订单系统发放短信梳理

## Direct Link
`raw/dingtalk-sms-notification.md`
钉钉原文: https://alidocs.dingtalk.com/i/nodes/Y1OQX0akWmv912lYhEeLBQ0NVGlDd3mE

## Summary
本文档完整梳理了飞猪酒店套餐订单系统的短信发送体系，涵盖 17 个短信场景（含部分未配置场景）。短信分为两大类：**订单生命周期通知**（覆盖购买、预约、退款、过期等关键节点）和**营销引流**（在频道页、商详页、支付成功页等触点引导用户添加微信福利官/管家）。文档列出了每个场景的短信模板ID、内容模板、触发点（代码入口类名+所属系统）。

## Narrative Thread
套餐短信体系围绕两条主线构建：一是保障用户订单信息透明（购买确认、预约成功、退款到账、过期提醒），二是通过各页面触点将用户引流至微信私域（福利官/管家）。通知类短信由订单状态变更事件驱动，分布在 triptuan 和 hotel-fc 两个系统中；引流类短信按用户所在页面分配不同任务编号（11-17），由 tuan-task 统一调度。

## Key Takeaways
- 短信体系覆盖 **17 个场景**，实际有内容配置的约 10 个
- 订单通知类短信几乎都附带**微信引流链接**（a.feizhu.com 短链）
- 购买提醒有**双触发点**：triptuan 的 EnableNotifyListener + hotel-fc 的 OnlineBookingPaidSuccSmsTaskExecutor
- 引流类短信统一使用模板 **724605350**（旧模板已废弃）
- 0元囤模式有独立的代扣成功短信（模板 733279299）
- 部分场景（商详页、订详页、预约成功页、申请退款页）**尚未配置**短信内容

## Entities Mentioned
- [[短信通知]] — 套餐底层能力，覆盖订单全生命周期和营销引流

## Concepts Introduced
- [[短信通知]] — 套餐系统短信发送的分类、触发机制和内容模板体系

## Constraints & Risks Documented
| Constraint / Risk | Type | Details |
|---|---|---|
| 部分引流场景未配置 | operational | 商详页(12)、订详页(14)、预约成功页(16)、申请退款页(17) 无短信内容 |
| 双系统触发 | technical | 购买提醒和可约提醒在 triptuan + hotel-fc 两个系统均有触发点，需注意去重 |
| 旧模板废弃 | operational | 引流场景中部分旧模板ID已删除线标注（如380763747、235103410） |

## Cross-references to Updated Pages
- [[短信通知]] — 新建概念页，完整记录发送逻辑和内容
