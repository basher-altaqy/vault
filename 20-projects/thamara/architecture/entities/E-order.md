---
id: "E-order"
type: "entity"
title: "صفقة"
domain: "trade"
tags: ["entity"]
related: ["[[E-trader]]", "[[E-farmer]]", "[[E-escrow]]", "[[E-shipment]]", "[[S-trader-orders]]", "[[S-trader-checkout]]", "[[S-farmer-orders]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# صفقة
<!-- generated from model.json — لا تعدّل يدوياً -->

تنتج عن فوز مزاد أو قبول عرض أو شراء مباشر. تشمل المحصول + العمولة + النقل.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| listing_id | ref | لا |  |
| tender_id | ref | لا |  |
| trader_id | ref | نعم |  |
| farmer_id | ref | نعم |  |
| crop_amount | money | نعم |  |
| platform_fee | money | نعم |  |
| transport_fee | money | لا |  |
| status | enum | نعم | created | paid | shipped | received | delivered | released | disputed |

## الروابط
- relation: [[E-trader|تاجر]] → [[E-order|صفقة]] (يشتري)
- relation: [[E-farmer|مزارع]] → [[E-order|صفقة]] (يبيع)
- relation: [[E-order|صفقة]] → [[E-escrow|حساب ضمان]] (يُضمن بـ)
- relation: [[E-order|صفقة]] → [[E-shipment|شحنة]] (تُشحن)
- shows: [[S-trader-orders|صفقاتي (تاجر)]] → [[E-order|صفقة]]

## الشاشات
- [[S-trader-checkout|الدفع (البوابة البنكية)]]
- [[S-trader-orders|صفقاتي (تاجر)]]
- [[S-farmer-orders|صفقاتي (مزارع)]]

## المراجع
-
