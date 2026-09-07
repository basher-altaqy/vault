---
id: "E-ticket"
type: "entity"
title: "بطاقة دعم"
domain: "support"
tags: ["entity"]
related: ["[[E-user]]", "[[S-ticket-create]]", "[[S-admin-tickets]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# بطاقة دعم
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| title | string | نعم |  |
| category | enum | نعم |  |
| priority | enum | نعم |  |
| ref_number | string | نعم |  |
| status | enum | نعم | قيد المراجعة/قيد المعالجة/تم الحل |

## الروابط
- relation: [[E-user|حساب]] → [[E-ticket|بطاقة دعم]] (يطلب دعماً)

## الشاشات
- [[S-ticket-create|بطاقة دعم]]
- [[S-admin-tickets|بطاقات الدعم]]

## المراجع
-
