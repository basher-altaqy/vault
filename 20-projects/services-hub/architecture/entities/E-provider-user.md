---
id: "E-provider-user"
type: "entity"
title: "مستخدم لدى الشركة"
domain: "partners"
tags: ["entity"]
related: ["[[E-provider]]", "[[S-partner-users]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# مستخدم لدى الشركة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| provider_id | ref | نعم |  |
| name | string | نعم |  |
| role | enum | نعم | admin | agronomist | data-entry | sales |

## الروابط
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-provider-user|مستخدم لدى الشركة]] (مستخدمون)

## الشاشات
- [[S-partner-users|مستخدمو الشركة]]

## المراجع
-
