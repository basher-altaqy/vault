---
id: "E-escrow"
type: "entity"
title: "حساب ضمان"
domain: "payment"
tags: ["entity"]
related: ["[[E-order]]", "[[S-admin-escrow]]", "[[S-trader-checkout]]", "[[S-trader-confirm-receipt]]", "[[S-transporter-confirm-delivery]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# حساب ضمان
<!-- generated from model.json — لا تعدّل يدوياً -->

يُعلَّق المبلغ الكامل ولا يُحرَّر إلا بتأكيد التاجر (استلام) والناقل (تسليم).

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| order_id | ref | نعم |  |
| total | money | نعم |  |
| bank_ref | string | لا | مرجع بوابة الدفع |
| receipt_confirmed_at | datetime | لا |  |
| delivery_confirmed_at | datetime | لا |  |
| released_at | datetime | لا |  |

## الروابط
- relation: [[E-order|صفقة]] → [[E-escrow|حساب ضمان]]
- shows: [[S-admin-escrow|حسابات الضمان]] → [[E-escrow|حساب ضمان]]

## الشاشات
- [[S-trader-checkout|الدفع (البوابة البنكية)]]
- [[S-trader-confirm-receipt|تأكيد الاستلام]]
- [[S-transporter-confirm-delivery|تأكيد التسليم]]
- [[S-admin-escrow|حسابات الضمان]]

## المراجع
-
