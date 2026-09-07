---
id: "E-data-agreement"
type: "entity"
title: "اتفاقية بيانات"
domain: "governance"
tags: ["entity"]
related: ["[[E-provider]]", "[[S-admin-agreements]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# اتفاقية بيانات
<!-- generated from model.json — لا تعدّل يدوياً -->

ما يحق للشركة رؤيته مقابل ما تقدمه، وحدود التجميع، ومدة الاتفاق.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| provider_id | ref | نعم |  |
| scope | json | نعم |  |
| min_group_size | int | نعم |  |
| starts | date | نعم |  |
| ends | date | لا |  |

## الروابط
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-data-agreement|اتفاقية بيانات]] (اتفاقية)

## الشاشات
- [[S-admin-agreements|اتفاقيات البيانات والاعتماد]]

## المراجع
-
