---
id: "E-farm-report"
type: "entity"
title: "تقرير/تحليل مرفوع"
domain: "data-up"
tags: ["entity"]
related: ["[[E-core-farmer]]", "[[E-core-farm]]", "[[E-core-crop]]", "[[E-insight]]", "[[S-farmer-upload-report]]", "[[S-partner-reports]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# تقرير/تحليل مرفوع
<!-- generated from model.json — لا تعدّل يدوياً -->

ما يرفعه الفلاح: تحليل تربة أو مياه أو منتج، صور، ملاحظات بعد تجربة خدمة.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| farmer_id | ref | نعم |  |
| farm_id | ref | لا |  |
| crop_id | ref | لا |  |
| kind | enum | نعم | soil | water | product | photo | note |
| file | file | لا |  |
| values | json | لا | قيم مستخرجة (pH، NPK…) |
| shared_with | json | نعم | الخدمات المسموح لها بالاطلاع |
| date | date | نعم |  |

## الروابط
- relation: [[E-core-farmer|فلاح (من نواة ثمرة)]] → [[E-farm-report|تقرير/تحليل مرفوع]] (يرفع)
- relation: [[E-core-farm|مزرعة (من النواة)]] → [[E-farm-report|تقرير/تحليل مرفوع]] (تحاليلها)
- relation: [[E-core-crop|محصول (من النواة)]] → [[E-farm-report|تقرير/تحليل مرفوع]] (تحاليله)
- relation: [[E-farm-report|تقرير/تحليل مرفوع]] → [[E-insight|معلومة مخصصة للفلاح]] (تولّد)

## الشاشات
- [[S-farmer-upload-report|رفع تحليل تربة/مياه/منتج]]
- [[S-partner-reports|التحاليل المشاركة معنا]]

## المراجع
-
