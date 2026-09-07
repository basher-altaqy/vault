---
id: "E-insight"
type: "entity"
title: "معلومة مخصصة للفلاح"
domain: "data-down"
tags: ["entity"]
related: ["[[E-region-dataset]]", "[[E-farm-report]]", "[[E-core-farmer]]", "[[S-farmer-insights]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# معلومة مخصصة للفلاح
<!-- generated from model.json — لا تعدّل يدوياً -->

ناتج مطابقة بيانات المنطقة والخدمة مع محصول الفلاح وتقاريره: توصية شخصية.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| farmer_id | ref | نعم |  |
| crop_id | ref | لا |  |
| source_dataset_id | ref | لا |  |
| source_report_id | ref | لا |  |
| title | string | نعم |  |
| body | text | نعم |  |
| read_at | datetime | لا |  |

## الروابط
- relation: [[E-region-dataset|بيانات المنطقة (من الشركة)]] → [[E-insight|معلومة مخصصة للفلاح]] (تولّد)
- relation: [[E-farm-report|تقرير/تحليل مرفوع]] → [[E-insight|معلومة مخصصة للفلاح]] (تولّد)
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-insight|معلومة مخصصة للفلاح]] (يتلقى)

## الشاشات
- [[S-farmer-insights|معلوماتي المخصصة (محصولي ومنطقتي)]]

## المراجع
-
