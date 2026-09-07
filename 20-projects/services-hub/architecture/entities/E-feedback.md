---
id: "E-feedback"
type: "entity"
title: "تغذية راجعة على خدمة"
domain: "data-up"
tags: ["entity"]
related: ["[[E-service-request]]", "[[S-farmer-feedback]]", "[[S-partner-analytics]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# تغذية راجعة على خدمة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| request_id | ref | نعم |  |
| farmer_id | ref | نعم |  |
| rating | int | نعم |  |
| outcome | json | لا | أثر الخدمة: إنتاجية، جودة، تكلفة |
| comment | text | لا |  |
| date | date | نعم |  |

## الروابط
- relation: [[E-service-request|طلب خدمة]] → [[E-feedback|تغذية راجعة على خدمة]] (تقييم)

## الشاشات
- [[S-farmer-feedback|تقييم الخدمة بعد التجربة]]
- [[S-partner-analytics|التحليلات المجمّعة]]

## المراجع
-
