---
id: "E-tender"
type: "entity"
title: "مناقصة مغلقة"
domain: "trade"
tags: ["entity"]
related: ["[[E-trader]]", "[[E-offer]]", "[[S-farmer-tender-browse]]", "[[S-trader-tender-create]]", "[[S-trader-tenders]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# مناقصة مغلقة
<!-- generated from model.json — لا تعدّل يدوياً -->

طلب شراء من التاجر: كمية، جودة، سقف سعر، زمان ومكان الاستلام.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| trader_id | ref | نعم |  |
| product_id | ref | نعم |  |
| quantity | decimal | نعم |  |
| quality_grade | enum | نعم |  |
| price_cap | money | نعم |  |
| pickup_at | datetime | نعم |  |
| pickup_location | geo | نعم |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-trader|تاجر]] → [[E-tender|مناقصة مغلقة]]
- relation: [[E-tender|مناقصة مغلقة]] → [[E-offer|عرض على مناقصة]]
- shows: [[S-farmer-tender-browse|المناقصات المفتوحة]] → [[E-tender|مناقصة مغلقة]]

## الشاشات
- [[S-trader-tender-create|إنشاء مناقصة]]
- [[S-trader-tenders|مناقصاتي]]
- [[S-farmer-tender-browse|المناقصات المفتوحة]]

## المراجع
-
