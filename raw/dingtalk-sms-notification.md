# 套餐订单系统发放短信梳理

> 源文档: https://alidocs.dingtalk.com/i/nodes/Y1OQX0akWmv912lYhEeLBQ0NVGlDd3mE
> 抓取时间: 2026-04-16

| 短信场景 | 短信模板 | 短信内容 | 发送量级/天 | 套餐域短信任务编号 | 触发点 |
|------------|------------|------------|-----------------|---------------------------|---------|
| 截止预约自动退款 | 240942356 | 你购买的套餐"${item_name}"已过期，退款已原路返回支付账户，预计1-5天到账。添加专属人工福利官微信 | | | OnlineBookingExpireSmsTaskExecutor (hotel-fc) |
| 不可约变可约提醒 | 120456887 | 非常抱歉！您的套餐目前无法预约。获取第一时间可约状态通知，可添加专属微信1v1顾问 | | 1 | SmsSendProcessor (triptuan) |
| 预约提醒 | 220300935 | 您购买的套餐已恢复可约，库存有限，尽快预约吧！ | | 2 | CanBookSmsSendProcessor (triptuan) |
| 购买提醒 | 900125932 | 您购买的套餐已下单成功，点击链接添加专属行程管家领取888元优惠券 | | 3 | EnableNotifyListener (triptuan) + OnlineBookingPaidSuccSmsTaskExecutor (hotel-fc) |
| 退款成功提醒 | 310213555 | 您购买的套餐已经成功预约，入住时间为checkin-checkout，共n晚 | | 4 | RefundNotifyListener (triptuan) |
| 套餐引流-频道页 | 724605350 | 飞猪大促邀请添加官方福利官抽大额旅行基金及五星酒店房券 | | 11 | AttractUserSmsSendProcessor (tuan-task) |
| 套餐引流-商详页 | | | | 12 | |
| 套餐引流-支付成功页 | 724605350 | 套餐管家帮你快速预约、1对1咨询答疑、爆款提前预告 | | 13 | |
| 套餐引流-订详页 | | | | 14 | |
| 套餐引流-预约下单页 | 724605350 | 套餐专属管家1v1人工服务，千元优惠券礼包 | | 15 | |
| 套餐引流-预约成功页 | | | | 16 | |
| 套餐引流-申请退款页 | | | | 17 | |
| 澳门通支付订单 | 448232462 | | | | TccpPayOrderListener (tuan-trade) |
| 商家操作电子凭证预约单确认时发短信通知用户 | 310213555 | | | | EticketVoucherController (tuan-gateway) |
| 可约提醒短信 | 121944984 | | | | OnlineBookingSmsNoticeTaskExecutor (tuan-gateway + hotel-fc) |
| 0元囤代扣成功 | 733279299 | 您购买的套餐已下单成功，0元囤订单将在预约时自动扣款 | | | WithholdingResultHtsTask (tuan-trade) |
