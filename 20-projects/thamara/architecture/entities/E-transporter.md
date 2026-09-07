---
id: "E-transporter"
type: "entity"
title: "ناقل"
domain: "identity"
tags: ["entity"]
related: ["[[E-user]]", "[[E-shipment]]", "[[E-vehicle]]", "[[S-transporter-register]]", "[[S-transporter-home]]", "[[accounts]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# ناقل
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| kind | enum | نعم | فردي/شركة |
| license_document | file | نعم |  |
| coverage_areas | json | نعم |  |

## الروابط
- relation: [[E-user|حساب]] → [[E-transporter|ناقل]] (ملف ناقل)
- relation: [[E-transporter|ناقل]] → [[E-shipment|شحنة]] (ينقل)
- relation: [[E-transporter|ناقل]] → [[E-vehicle|مركبة]] (مركبات)

## الشاشات
- [[S-transporter-register|بيانات الناقل]]
- [[S-transporter-home|الرئيسية (ناقل)]]

## المراجع
[[accounts]]
