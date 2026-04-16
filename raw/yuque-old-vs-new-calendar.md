# 新旧日历页对比参考

> 来源：语雀 - 埋铭的知识/项目文档
> URL: https://aliyuque.antfin.com/fqicv9/kg7h1z/ig1p07zatt5243ys
> 摄入时间：2026-04-16
> 标题：HotelCalendar DateItem 样式与数据结构对照文档

## 切换逻辑
- useNewCalendar 字段（服务端下发）决定使用哪套日期组件
- useNewCalendar = false → DateComponent（旧版/预约日历），3行布局
- useNewCalendar = true → DateComponent2（新版/可约日历），4行布局

## 接口
- 酒店日历（calendarScene=1）：mtop.trip.hotel.onlinebooking.calendar
- 订单预约日历（calendarScene=3）：mtop.fliggy.traveldetail.onlinebooking.v2.calendar.query

## 旧版（DateComponent）3行布局
- 顶部行：selectedNote > 升房图标 > "休"标签(橙底#FF7300) > tExt文案 > 空占位
  - tExt颜色：紧张→红#FF401A，可升房/可协商→棕#805540，其他→#5C5F66
- 中间行：dateHoliday/dateToday(28rpx) > 日期数字(36rpx)
- 底部行：bExt(加价文案)

## 新版（DateComponent2）4行布局
- Row1：today/holiday标签(20rpx) + "休"标签(黄底#FFE033)
- Row2：日期数字
- Row3：dateDesc(状态文案：可约/约满/紧张) + 加价
- Row4：升房/候补/预约有礼标签

## 新旧关键差异
- 布局：3行→4行（状态文案独立行）
- "休"标签：橙底白字→黄底黑字
- 节假日/今天：旧版替代日期数字，新版独立Row1不替代
- 状态文案：旧版在顶部行tExt，新版在Row3 dateDesc
- 升房/候补：旧版在顶部行图标，新版在Row4独立标签
- 加价：旧版在底部行bExt，新版在Row3与状态文案同行
