---
id: "E-service"
type: "entity"
title: "خدمة"
domain: "catalog"
tags: ["entity"]
related: ["[[E-provider]]", "[[E-offering]]", "[[E-service-request]]", "[[S-partner-services]]", "[[S-farmer-services]]", "[[S-farmer-service-detail]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# خدمة
<!-- generated from model.json — لا تعدّل يدوياً -->

تعريف الخدمة كما تظهر داخل تطبيق ثمرة.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| provider_id | ref | نعم |  |
| title | string | نعم |  |
| category | enum | نعم | seeds | fertilizer | pesticide | soil-test | water-test | product-test | advisory | finance | insurance |
| description | text | نعم |  |
| input_schema | json | نعم | ما يُطلب من الفلاح عند الطلب |
| output_schema | json | نعم | ما تعيده الخدمة للفلاح |
| pricing | json | لا |  |
| regions | json | نعم |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-service|خدمة]] (يقدّم)
- relation: [[E-service|خدمة]] → [[E-offering|عرض/منتج للخدمة]] (عروض)
- relation: [[E-service|خدمة]] → [[E-service-request|طلب خدمة]] (طلبات)

## الشاشات
- [[S-partner-services|إدارة الخدمات]]
- [[S-farmer-services|الخدمات المساندة (داخل تطبيق ثمرة)]]
- [[S-farmer-service-detail|تفاصيل خدمة وعروضها]]

## المراجع
-
