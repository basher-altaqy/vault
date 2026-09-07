---
id: "E-crop"
type: "entity"
title: "محصول"
domain: "production"
tags: ["entity"]
related: ["[[E-farm]]", "[[E-product]]", "[[E-listing]]", "[[S-farmer-crops]]", "[[S-farmer-crop-add]]", "[[S-farmer-sell-choose]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# محصول
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| farm_id | ref | نعم |  |
| product_id | ref | نعم |  |
| name | string | نعم |  |
| variety | string | لا |  |
| quantity | decimal | نعم |  |
| unit | enum | نعم |  |
| harvest_date | date | نعم |  |
| expiry_date | date | لا |  |
| quality_grade | enum | نعم |  |
| size | string | لا |  |
| color | string | لا |  |
| photos | json | نعم | 1 إلى 10 صور |
| packaging | json | نعم |  |
| supply_range | json | نعم |  |

## الروابط
- relation: [[E-farm|مزرعة]] → [[E-crop|محصول]]
- relation: [[E-product|منتج (صنف)]] → [[E-crop|محصول]]
- relation: [[E-crop|محصول]] → [[E-listing|عرض بيع]]
- shows: [[S-farmer-crops|محاصيلي]] → [[E-crop|محصول]]

## الشاشات
- [[S-farmer-crops|محاصيلي]]
- [[S-farmer-crop-add|إضافة محصول]]
- [[S-farmer-sell-choose|اختيار نموذج البيع]]

## المراجع
-
