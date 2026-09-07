---
id: "E-trader"
type: "entity"
title: "تاجر"
domain: "identity"
tags: ["entity"]
related: ["[[E-user]]", "[[E-bid]]", "[[E-tender]]", "[[E-order]]", "[[S-trader-register]]", "[[S-trader-home]]", "[[accounts]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# تاجر
<!-- generated from model.json — لا تعدّل يدوياً -->

المنشأة التجارية وممثلها القانوني.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| user_id | ref | نعم |  |
| company_name | string | نعم |  |
| company_email | string | نعم |  |
| company_phone | string | نعم |  |
| activity | enum | نعم | خضار/فواكه/حبوب |
| tax_number | string | نعم |  |
| license_number | string | نعم |  |
| hq_location | geo | نعم |  |
| commercial_register | file | نعم | PDF |
| balance | money | نعم | رصيد المزايدة |

## الروابط
- relation: [[E-user|حساب]] → [[E-trader|تاجر]] (ملف تاجر)
- relation: [[E-trader|تاجر]] → [[E-bid|مزايدة]] (يزايد)
- relation: [[E-trader|تاجر]] → [[E-tender|مناقصة مغلقة]] (يطرح مناقصة)
- relation: [[E-trader|تاجر]] → [[E-order|صفقة]] (يشتري)

## الشاشات
- [[S-trader-register|بيانات المنشأة]]
- [[S-trader-home|الرئيسية (تاجر)]]

## المراجع
[[accounts]]
