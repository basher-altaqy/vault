---
id: "E-listing"
type: "entity"
title: "عرض بيع"
domain: "trade"
tags: ["entity"]
related: ["[[E-crop]]", "[[E-auction]]", "[[S-trader-market]]", "[[S-farmer-listings]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# عرض بيع
<!-- generated from model.json — لا تعدّل يدوياً -->

عرض محصول بأحد النماذج: auction | tender | fixed.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| crop_id | ref | نعم |  |
| kind | enum | نعم |  |
| title | string | نعم |  |
| description | text | لا |  |
| status | enum | نعم |  |
| price_limit_id | ref | لا | حد الوزارة المطبّق |

## الروابط
- relation: [[E-crop|محصول]] → [[E-listing|عرض بيع]] (يُعرض في)
- relation: [[E-listing|عرض بيع]] → [[E-auction|مزاد مفتوح]] (مزاد)
- shows: [[S-trader-market|السوق (العروض)]] → [[E-listing|عرض بيع]]

## الشاشات
- [[S-farmer-listings|عروضي]]
- [[S-trader-market|السوق (العروض)]]

## المراجع
-
