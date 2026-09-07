---
id: "E-core-farm"
type: "entity"
title: "مزرعة (من النواة)"
domain: "core"
tags: ["entity"]
related: ["[[E-farm-report]]", "[[E-region]]", "[[E-core-crop]]", "[[E-core-farmer]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# مزرعة (من النواة)
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| core_id | ref | نعم |  |
| governorate | string | نعم |  |
| location | geo | نعم |  |

## الروابط
- relation: [[E-core-farm|مزرعة (من النواة)]] → [[E-farm-report|تقرير/تحليل مرفوع]] (تحاليلها)
- relation: [[E-region|منطقة (محافظة/ناحية)]] → [[E-core-farm|مزرعة (من النواة)]] (مزارعها)
- relation: [[E-core-farm|مزرعة (من النواة)]] → [[E-core-crop|محصول (من النواة)]] (تُنتج)
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-core-farm|مزرعة (من النواة)]] (يملك)

## الشاشات
-

## المراجع
-
