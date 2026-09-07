---
id: "E-product"
type: "entity"
title: "منتج (صنف)"
domain: "catalog"
tags: ["entity"]
related: ["[[E-crop]]", "[[E-price-limit]]", "[[S-admin-catalog]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# منتج (صنف)
<!-- generated from model.json — لا تعدّل يدوياً -->

كتالوج المنتجات والأصناف ووحدات القياس ودرجات الجودة.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| name | string | نعم |  |
| category | enum | نعم |  |
| units | json | نعم |  |
| quality_grades | json | نعم |  |

## الروابط
- relation: [[E-product|منتج (صنف)]] → [[E-crop|محصول]]
- relation: [[E-product|منتج (صنف)]] → [[E-price-limit|حد سعر]]

## الشاشات
- [[S-admin-catalog|الكتالوج والأصناف]]

## المراجع
-
