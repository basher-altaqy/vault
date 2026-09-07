---
id: "E-report"
type: "entity"
title: "بلاغ"
domain: "support"
tags: ["entity"]
related: ["[[E-user]]", "[[S-report-create]]", "[[S-admin-reports]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# بلاغ
<!-- generated from model.json — لا تعدّل يدوياً -->



## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| reporter_id | ref | نعم |  |
| kind | enum | نعم | رسائل مزعجة/احتيال/نصب/محتوى غير لائق/تخلف عن الدفع أو الاستلام |
| title | string | نعم |  |
| description | text | نعم |  |
| attachments | json | لا |  |
| conversation_ref | string | لا |  |
| ref_number | string | نعم |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-user|حساب]] → [[E-report|بلاغ]] (يبلّغ)

## الشاشات
- [[S-report-create|تقديم بلاغ]]
- [[S-admin-reports|البلاغات]]

## المراجع
-
