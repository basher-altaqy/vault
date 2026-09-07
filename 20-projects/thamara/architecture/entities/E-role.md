---
id: "E-role"
type: "entity"
title: "دور"
domain: "identity"
tags: ["entity"]
related: ["[[E-user]]", "[[S-register]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# دور
<!-- generated from model.json — لا تعدّل يدوياً -->

أدوار الحساب: farmer, trader, transporter, officer, admin.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| kind | enum | نعم |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-user|حساب]] → [[E-role|دور]] (أدوار)

## الشاشات
- [[S-register|التسجيل واختيار الدور]]

## المراجع
-
