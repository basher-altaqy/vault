---
id: "E-vehicle"
type: "entity"
title: "مركبة"
domain: "logistics"
tags: ["entity"]
related: ["[[E-transporter]]", "[[S-transporter-vehicles]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# مركبة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| transporter_id | ref | نعم |  |
| capacity_kg | int | نعم |  |
| model | string | نعم |  |
| has_crane | bool | لا |  |
| has_scale | bool | لا |  |
| refrigerated | bool | لا |  |

## الروابط
- relation: [[E-transporter|ناقل]] → [[E-vehicle|مركبة]] (مركبات)

## الشاشات
- [[S-transporter-vehicles|مركباتي]]

## المراجع
-
