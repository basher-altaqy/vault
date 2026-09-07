---
id: "E-blacklist"
type: "entity"
title: "قائمة سوداء"
domain: "governance"
tags: ["entity"]
related: ["[[E-user]]", "[[S-admin-blacklist]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# قائمة سوداء
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| reason | text | نعم |  |
| report_id | ref | لا |  |
| since | date | نعم |  |

## الروابط
- relation: [[E-user|حساب]] → [[E-blacklist|قائمة سوداء]] (قد يُحظر)

## الشاشات
- [[S-admin-blacklist|القائمة السوداء]]

## المراجع
-
