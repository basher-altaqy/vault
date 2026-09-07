---
id: "E-notification"
type: "entity"
title: "إشعار"
domain: "platform"
tags: ["entity"]
related: ["[[E-user]]", "[[S-notifications]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# إشعار
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| kind | enum | نعم |  |
| payload | json | نعم |  |
| read_at | datetime | لا |  |

## الروابط
- relation: [[E-user|حساب]] → [[E-notification|إشعار]]

## الشاشات
- [[S-notifications|الإشعارات]]

## المراجع
-
