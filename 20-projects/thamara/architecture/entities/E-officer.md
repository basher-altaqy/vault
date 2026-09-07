---
id: "E-officer"
type: "entity"
title: "موظف حكومي"
domain: "governance"
tags: ["entity"]
related: ["[[E-user]]", "[[S-admin-users]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# موظف حكومي
<!-- generated from model.json — لا تعدّل يدوياً -->

يُنشأ داخلياً عبر الأدمن فقط.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| job_title | string | نعم |  |
| ministry | enum | نعم | التجارة الداخلية/الزراعة/النقل |
| permissions | json | نعم |  |

## الروابط
- relation: [[E-user|حساب]] → [[E-officer|موظف حكومي]] (ملف موظف)

## الشاشات
- [[S-admin-users|المستخدمون والتوثيق]]

## المراجع
-
