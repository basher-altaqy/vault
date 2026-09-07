---
id: "E-farmer"
type: "entity"
title: "مزارع"
domain: "identity"
tags: ["entity"]
related: ["[[E-user]]", "[[E-farm]]", "[[E-offer]]", "[[E-order]]", "[[S-farmer-register]]", "[[S-farmer-home]]", "[[accounts]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# مزارع
<!-- generated from model.json — لا تعدّل يدوياً -->

ملف المزارع: هيكلية الحيازة والتوثيق.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| tenure_types | json | نعم | ملك/إيجار/ضمان (قابلة للجمع) |
| id_document | file | لا | لشارة حساب موثق |

## الروابط
- relation: [[E-user|حساب]] → [[E-farmer|مزارع]]
- relation: [[E-farmer|مزارع]] → [[E-farm|مزرعة]] (حيازات)
- relation: [[E-farmer|مزارع]] → [[E-offer|عرض على مناقصة]]
- relation: [[E-farmer|مزارع]] → [[E-order|صفقة]]

## الشاشات
- [[S-farmer-register|بيانات المزارع]]
- [[S-farmer-home|الرئيسية (مزارع)]]

## المراجع
[[accounts]]
