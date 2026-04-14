# 飞猪酒店套餐产品知识库 - Activity Log

> **快速上手**: 倒序查看最近操作，了解最新进展

## [2026-04-14 19:35] init | Knowledge Base Created
- Name: fliggy-hotel-package-kb
- Path: ~/knowledge-bases/fliggy-hotel-package-kb
- Domain: 飞猪酒店套餐产品知识管理
- Product Scope: 频道页 → 酒店日历页 → 套餐详情页 → 套餐SKU浮层 → 下单页
- Core Goal: 提升D2O转化率
- Associated repos: https://github.com/mai-hub-ai/knowledge-bases.git
- Pages created: index.md, overview.md, onboarding.md, log.md
- Schema files: CLAUDE.md, conventions.md, source-types.md, code-repos.md

## [2026-04-14 19:45] ingest | 套餐各叶子类目id
- Source type: dingtalk_doc
- Source URL: https://alidocs.dingtalk.com/i/nodes/93NwLYZXWyZPdyb1CdZ6Xo47VkyEqBQm
- Raw file: raw/dingtalk-93NwLYZXWyZPdyb1CdZ6Xo47VkyEqBQm.md
- Pages created:
  - source-category-ids（源摘要页）
  - category-classification（概念页：类目分类体系）
  - booking-method（概念页：预约方式）
  - domestic-hotel-package（实体页：境内酒店套餐）
  - overseas-hotel-package（实体页：境外酒店套餐）
  - online-booking-package（实体页：在线预约套餐）
  - overseas-online-apply-package（实体页：境外在线申请套餐）
  - hotel-dining（实体页：酒店餐饮美食）
  - hotel-service（实体页：酒店服务（新））
- Pages updated: index.md, onboarding.md, overview.md
- Entities extracted: 6（含房类目4个，含餐/服务类目2个）
- Concepts extracted: 2（类目分类体系、预约方式）
- Key insight: 类目 ≠ 预约方式，电子凭证/日历套餐是预约方式而非类目

## [2026-04-14 20:00] ingest | 套餐详情页模块结构
- Source type: user_input
- Figma链接: https://www.figma.com/design/Ie64fxMQEYOqMfhyiRhyKU/Untitled?node-id=2-651
- Raw file: raw/detail-page-modules-structure.md
- Pages created:
  - source-detail-page-modules（源摘要页）
  - package-detail-page（页面实体页）
  - media-container（模块1：媒体容器区域）
  - price-area（模块2：价格区域）
  - brand-mind-area（模块3：品牌心智区）
  - header-info-area（模块4：头部信息区）
  - service-tag-area（模块5：服务标签区）
  - ranking-tag（模块6：榜单标签）
  - stock-up-tag-area（模块7：囤好货标签区）
  - date-selector-area（模块8：日期选择区）
  - calendar-component（模块9：日历组件）
  - package-selector-area（模块10：套餐选择区）
  - package-benefit-area（模块11：套餐权益描述区）
  - product-review-area（模块12：商品评价区）
  - shop-info-area（模块13：店铺信息区）
  - bottom-action-bar（模块14：底部操作栏）
- Pages updated: index.md, onboarding.md
- Entities extracted: 15（1页面 + 14模块）
- Key insight: 详情页14模块框架已建立，待补充详细信息
- Note: Figma链接当前无法直接访问

## [2026-04-14 20:15] ingest | 业务语义字典 + 服务标签区补充
- Source type: dingtalk_doc + user_input
- Source URLs:
  - 钉钉: https://alidocs.dingtalk.com/i/nodes/kDnRL6jAJMpxeYDohKK2m1YyVyMoPYe1
  - 用户输入: 语义字典+标签补充
- Raw files:
  - raw/dingtalk-kDnRL6jAJMpxeYDohKK2m1YyVyMoPYe1.md
  - raw/user-input-semantics-and-tags.md
- Pages created:
  - product-semantics（概念页：业务语义字典）
  - source-service-tag-config（源摘要页）
  - source-semantics-and-tags（源摘要页）
- Pages updated:
  - service-tag-area（模块5：服务标签区）← 详细补充
  - index.md, onboarding.md
- Concepts extracted: 1（业务语义字典：单店/通兑）
- Key insights:
  - 单店：item关联1个shid
  - 通兑：item关联>=2个shid
  - 服务标签区标签排序规则已明确
  - 节假日可住标签迭代：优先长假期

## [2026-04-14 20:30] ingest | 套餐商品详情页改版1.0（仅更新囤好货+媒体容器）
- Source type: dingtalk_doc
- Source URL: https://alidocs.dingtalk.com/i/nodes/oP0MALyR8kKL2Xb0H29q6rAL83bzYmDO
- Raw file: raw/dingtalk-oP0MALyR8kKL2Xb0H29q6rAL83bzYmDO.md
- Pages updated:
  - media-container（模块1：媒体容器区域）← 详细补充
  - stock-up-tag-area（模块7：囤好货标签区）← 详细补充
  - source-detail-page-prd（源摘要页）
  - index.md
- Key insights:
  - 媒体容器：导航栏位置变更、模块顺序调整（大促/非大促不同）、酒店图片上限<=5张
  - 囤好货规则：slogan变更（先囤后约、不约可退、过期可退）、新增可住日历
  - 可住日历：仅单店&单sku才透出，外露30天
- Note: 按用户要求仅更新囤好货规则和头部媒体容器，其他模块未新增

## [2026-04-14 21:00] ingest | 即买即约PRD + 迭代需求
- Source type: dingtalk_doc
- Source URLs:
  - https://alidocs.dingtalk.com/i/nodes/G1DKw2zgV2xZ1dypI1onoM558B5r9YAn
  - https://alidocs.dingtalk.com/i/nodes/ZgpG2NdyVXYDdEa4tQ0a4BDzJMwvDqPk
- Pages created:
  - source-即买即约PRD（源摘要页）
  - source-即买即约迭代（源摘要页）
  - order-page-overview（页面实体：下单页概览）
  - stock-up-order-page（页面实体：先囤后约下单页）
  - buy-and-book-order-page（页面实体：即买即约双Tab下单页）
  - calendar-order-page（页面实体：日历预订下单页）
  - overseas-order-page（页面实体：境内外酒店套餐下单页）
  - buy-and-book-calendar-page（页面实体：即买即约日历页）
- Pages updated:
  - booking-method（概念页：预约方式）← 补充即买即约详解
  - package-detail-page（页面实体：套餐详情页）← 补充即买即约入口判断
  - index.md
- Entities extracted: 6（下单页概览 + 4种下单页 + 即买即约日历页）
- Concepts extracted: 0（更新现有概念页）
- Key insights:
  - 即买即约：用户购买时直接创建套餐单+日历单
  - 先囤后约：传统模式，购买凭证后预约
  - 两种模式可出现在同一商品中
  - 即买即约入口在商品详情页开始
  - 下单页分为四种类型：先囤后约、即买即约双Tab、日历预订、境外

## [2026-04-14 21:30] update | 即买即约准入规则变更（白名单→黑名单）
- Source type: dingtalk_doc
- Source URL: https://alidocs.dingtalk.com/i/nodes/NZQYprEoWoDjdZb1IP1ZO0KRV1waOeDk
- Pages created:
  - source-即买即约全量配置（源摘要页）
- Pages updated:
  - booking-method（概念页：预约方式）← 准入规则变更
  - index.md
- Key changes:
  - 准入机制：白名单 → 黑名单
  - 默认支持：在线预约在售的国内套餐商品均支持即买即约
  - 新增不支持类型：定金预售、未到预约有效期商品、日历预订的品
  - 权益配置：可选（非必需）
  - 下单页Tab文案：支持自定义，兜底"火爆抢约 早订安心"
- Warning: 全量后不校验商品实际价库，可能存在日历约满场景
