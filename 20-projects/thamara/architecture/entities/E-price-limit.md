---
id: "E-price-limit"
type: "entity"
title: "حد سعر"
domain: "governance"
tags: ["entity"]
related: ["[[E-product]]", "[[S-admin-price-limits]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# حد سعر
<!-- generated from model.json — لا تعدّل يدوياً -->

حدود الأسعار لكل صنف من وزارة التجارة الداخلية.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| product_id | ref | نعم |  |
| min_price | money | لا |  |
| max_price | money | لا |  |
| valid_from | date | نعم |  |
| source | string | نعم |  |

## الروابط
- relation: [[E-product|منتج (صنف)]] → [[E-price-limit|حد سعر]] (حد سعر)

## الشاشات
- [[S-admin-price-limits|حدود الأسعار (الوزارة)]]

## المراجع
-
