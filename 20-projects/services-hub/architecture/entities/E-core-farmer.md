---
id: "E-core-farmer"
type: "entity"
title: "فلاح (من نواة ثمرة)"
domain: "core"
tags: ["entity"]
related: ["[[E-service-request]]", "[[E-farm-report]]", "[[E-insight]]", "[[E-core-farm]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# فلاح (من نواة ثمرة)
<!-- generated from model.json — لا تعدّل يدوياً -->

مرجع إلى حساب الفلاح في النواة. لا يُخزَّن هنا إلا المعرّف وموافقاته على مشاركة البيانات.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| core_id | ref | نعم |  |
| consents | json | نعم | لكل خدمة: مشاركة فردية أم مجمّعة |

## الروابط
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-service-request|طلب خدمة]] (يطلب)
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-farm-report|تقرير/تحليل مرفوع]] (يرفع)
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-insight|معلومة مخصصة للفلاح]] (يتلقى)
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-core-farm|مزرعة (من النواة)]] (يملك)

## الشاشات
-

## المراجع
-
