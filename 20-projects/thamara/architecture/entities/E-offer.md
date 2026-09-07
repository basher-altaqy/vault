---
id: "E-offer"
type: "entity"
title: "عرض على مناقصة"
domain: "trade"
tags: ["entity"]
related: ["[[E-tender]]", "[[E-farmer]]", "[[S-farmer-offer-submit]]", "[[S-trader-offers-review]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# عرض على مناقصة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| tender_id | ref | نعم |  |
| farmer_id | ref | نعم |  |
| price | money | نعم |  |
| quantity | decimal | نعم |  |
| quality_grade | enum | نعم |  |
| ready_at | datetime | نعم |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-tender|مناقصة مغلقة]] → [[E-offer|عرض على مناقصة]]
- relation: [[E-farmer|مزارع]] → [[E-offer|عرض على مناقصة]]

## الشاشات
- [[S-farmer-offer-submit|تقديم عرض على مناقصة]]
- [[S-trader-offers-review|مراجعة عروض المناقصة]]

## المراجع
-
