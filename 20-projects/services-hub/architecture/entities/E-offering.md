---
id: "E-offering"
type: "entity"
title: "عرض/منتج للخدمة"
domain: "catalog"
tags: ["entity"]
related: ["[[E-service]]", "[[S-partner-offerings]]", "[[S-farmer-service-detail]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# عرض/منتج للخدمة
<!-- generated from model.json — لا تعدّل يدوياً -->

صنف بذور أو سماد أو باقة تحليل بسعر وتوافر بحسب المنطقة.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| service_id | ref | نعم |  |
| name | string | نعم |  |
| spec | json | لا |  |
| price | money | لا |  |
| availability | json | نعم | بحسب المحافظة |
| suitable_products | json | لا | المحاصيل المناسبة |

## الروابط
- relation: [[E-service|خدمة]] → [[E-offering|عرض/منتج للخدمة]] (عروض)

## الشاشات
- [[S-partner-offerings|العروض والمنتجات]]
- [[S-farmer-service-detail|تفاصيل خدمة وعروضها]]

## المراجع
-
