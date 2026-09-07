---
id: "E-shipment"
type: "entity"
title: "شحنة"
domain: "logistics"
tags: ["entity"]
related: ["[[E-order]]", "[[E-transporter]]", "[[S-trader-transport-choose]]", "[[S-transporter-requests]]", "[[S-transporter-deliveries]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# شحنة
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| order_id | ref | نعم |  |
| transporter_id | ref | لا |  |
| vehicle_id | ref | لا |  |
| agreed_fee | money | لا |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-order|صفقة]] → [[E-shipment|شحنة]]
- relation: [[E-transporter|ناقل]] → [[E-shipment|شحنة]]

## الشاشات
- [[S-trader-transport-choose|اختيار الناقل]]
- [[S-transporter-requests|طلبات النقل]]
- [[S-transporter-deliveries|توصيلاتي]]

## المراجع
-
