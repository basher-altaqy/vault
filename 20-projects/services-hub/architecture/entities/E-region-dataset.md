---
id: "E-region-dataset"
type: "entity"
title: "بيانات المنطقة (من الشركة)"
domain: "data-down"
tags: ["entity"]
related: ["[[E-provider]]", "[[E-region]]", "[[E-insight]]", "[[S-partner-region-data]]", "[[S-farmer-insights]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# بيانات المنطقة (من الشركة)
<!-- generated from model.json — لا تعدّل يدوياً -->

ما تُدخله الشركة لكل محافظة: توصيات، مواعيد، أسعار، تحذيرات آفات، حالة تربة عامة.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| provider_id | ref | نعم |  |
| region_id | ref | نعم |  |
| product | string | لا | المحصول المعني إن وُجد |
| kind | enum | نعم | recommendation | schedule | alert | price | soil-profile |
| payload | json | نعم |  |
| valid_from | date | نعم |  |
| valid_to | date | لا |  |

## الروابط
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-region-dataset|بيانات المنطقة (من الشركة)]] (تُدخل بيانات)
- relation: [[E-region|منطقة (محافظة/ناحية)]] → [[E-region-dataset|بيانات المنطقة (من الشركة)]] (بيانات المنطقة)
- relation: [[E-region-dataset|بيانات المنطقة (من الشركة)]] → [[E-insight|معلومة مخصصة للفلاح]] (تولّد)

## الشاشات
- [[S-partner-region-data|إدخال بيانات المحافظات]]
- [[S-farmer-insights|معلوماتي المخصصة (محصولي ومنطقتي)]]

## المراجع
-
