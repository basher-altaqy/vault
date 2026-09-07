---
id: "E-farm"
type: "entity"
title: "مزرعة"
domain: "production"
tags: ["entity"]
related: ["[[E-farmer]]", "[[E-crop]]", "[[S-farmer-farms]]", "[[S-farmer-farm-add]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# مزرعة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| farmer_id | ref | نعم |  |
| name | string | نعم |  |
| location | geo | نعم | خريطة تفاعلية |
| tenure | enum | نعم |  |
| packaging_methods | json | نعم | صناديق، وزن صافي |

## الروابط
- relation: [[E-farmer|مزارع]] → [[E-farm|مزرعة]] (حيازات)
- relation: [[E-farm|مزرعة]] → [[E-crop|محصول]] (تُنتج)

## الشاشات
- [[S-farmer-farms|مزارعي]]
- [[S-farmer-farm-add|إضافة مزرعة]]

## المراجع
-
