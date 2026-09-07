---
id: "E-auction"
type: "entity"
title: "مزاد مفتوح"
domain: "trade"
tags: ["entity"]
related: ["[[E-listing]]", "[[E-bid]]", "[[S-trader-auction-view]]", "[[S-farmer-auction-create]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# مزاد مفتوح
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| listing_id | ref | نعم |  |
| start_price | money | نعم |  |
| min_increment | money | نعم | لا يقل عن حد النظام |
| duration_hours | int | نعم | مثل 24 |
| final_countdown_min | int | نعم | يبدأ عند أول مزايدة |
| auto_extend_min | int | نعم | تمديد عند مزايدة في آخر 5 دقائق |
| ends_at | datetime | نعم |  |
| winner_bid_id | ref | لا |  |

## الروابط
- relation: [[E-listing|عرض بيع]] → [[E-auction|مزاد مفتوح]] (مزاد)
- relation: [[E-auction|مزاد مفتوح]] → [[E-bid|مزايدة]] (مزايدات)
- shows: [[S-trader-auction-view|صفحة المزاد والمزايدة]] → [[E-auction|مزاد مفتوح]]

## الشاشات
- [[S-farmer-auction-create|إنشاء مزاد]]
- [[S-trader-auction-view|صفحة المزاد والمزايدة]]

## المراجع
-
