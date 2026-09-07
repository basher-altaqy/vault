---
id: "E-core-crop"
type: "entity"
title: "محصول (من النواة)"
domain: "core"
tags: ["entity"]
related: ["[[E-farm-report]]", "[[E-core-farm]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# محصول (من النواة)
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| core_id | ref | نعم |  |
| product | string | نعم |  |
| season | string | لا |  |

## الروابط
- relation: [[E-core-crop|محصول (من النواة)]] → [[E-farm-report|تقرير/تحليل مرفوع]] (تحاليله)
- relation: [[E-core-farm|مزرعة (من النواة)]] → [[E-core-crop|محصول (من النواة)]] (تُنتج)

## الشاشات
-

## المراجع
-
