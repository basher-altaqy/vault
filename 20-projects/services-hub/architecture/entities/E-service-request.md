---
id: "E-service-request"
type: "entity"
title: "طلب خدمة"
domain: "operations"
tags: ["entity"]
related: ["[[E-service]]", "[[E-core-farmer]]", "[[E-feedback]]", "[[S-farmer-service-request]]", "[[S-farmer-service-track]]", "[[S-partner-requests]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# طلب خدمة
<!-- generated from model.json — لا تعدّل يدوياً -->

طلب فلاح لخدمة: شراء مستلزم، حجز تحليل، طلب استشارة.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| service_id | ref | نعم |  |
| farmer_id | ref | نعم |  |
| farm_id | ref | لا |  |
| crop_id | ref | لا |  |
| input | json | نعم |  |
| status | enum | نعم | new | accepted | in-progress | delivered | closed | cancelled |
| price | money | لا |  |

## الروابط
- relation: [[E-service|خدمة]] → [[E-service-request|طلب خدمة]] (طلبات)
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-service-request|طلب خدمة]] (يطلب)
- relation: [[E-service-request|طلب خدمة]] → [[E-feedback|تغذية راجعة على خدمة]] (تقييم)

## الشاشات
- [[S-farmer-service-request|طلب الخدمة]]
- [[S-farmer-service-track|متابعة طلباتي]]
- [[S-partner-requests|الطلبات الواردة]]

## المراجع
-
