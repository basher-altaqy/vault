---
id: "S-trader-auction-view"
type: "screen"
title: "صفحة المزاد والمزايدة"
domain: "trader"
tags: ["screen", "trader"]
related: ["[[E-auction]]", "[[S-trader-transport-choose]]"]
source: "model"
status: "planned"
design: ""
project: "thamara"
date: 2026-09-07
generated: true
---
# صفحة المزاد والمزايدة
<!-- generated from model.json — لا تعدّل يدوياً -->

**الدور:** trader · **الحالة:** planned



## الخانات
- amount

## الإجراءات
- مزايدة (يستدعي [[A-bids.create]])
- عند الفوز: الدفع → [[S-trader-transport-choose|اختيار الناقل]]

## الروابط
- shows: [[S-trader-auction-view|صفحة المزاد والمزايدة]] → [[E-auction|مزاد مفتوح]]

## المراجع
-
