---
id: "E-aggregate"
type: "entity"
title: "إحصاء مجمّع للشركة"
domain: "analytics"
tags: ["entity"]
related: ["[[E-provider]]", "[[S-partner-analytics]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# إحصاء مجمّع للشركة
<!-- generated from model.json — لا تعدّل يدوياً -->

لا هوية فردية: أصناف ومساحات وتفاعل وتقييم بحسب المحافظة والموسم.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| provider_id | ref | نعم |  |
| region_id | ref | نعم |  |
| period | string | نعم |  |
| metrics | json | نعم |  |
| min_group_size | int | نعم | لا يُعرض تجميع دون حد أدنى من الفلاحين |

## الروابط
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-aggregate|إحصاء مجمّع للشركة]] (يرى مجمّعاً)

## الشاشات
- [[S-partner-analytics|التحليلات المجمّعة]]

## المراجع
-
