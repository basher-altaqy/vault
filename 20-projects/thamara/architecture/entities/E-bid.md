---
id: "E-bid"
type: "entity"
title: "مزايدة"
domain: "trade"
tags: ["entity"]
related: ["[[E-auction]]", "[[E-trader]]", "[[S-trader-auction-view]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# مزايدة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| auction_id | ref | نعم |  |
| trader_id | ref | نعم |  |
| alias | string | نعم | اسم مستعار حتى انتهاء المزاد |
| amount | money | نعم |  |
| reserved_amount | money | نعم | محجوز من الرصيد |
| placed_at | datetime | نعم |  |

## الروابط
- relation: [[E-auction|مزاد مفتوح]] → [[E-bid|مزايدة]] (مزايدات)
- relation: [[E-trader|تاجر]] → [[E-bid|مزايدة]] (يزايد)

## الشاشات
- [[S-trader-auction-view|صفحة المزاد والمزايدة]]

## المراجع
-
