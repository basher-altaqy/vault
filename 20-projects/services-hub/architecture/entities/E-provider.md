---
id: "E-provider"
type: "entity"
title: "شركة/جهة مقدّمة"
domain: "partners"
tags: ["entity"]
related: ["[[E-provider-user]]", "[[E-service]]", "[[E-region-dataset]]", "[[E-aggregate]]", "[[E-data-agreement]]", "[[S-partner-onboarding]]", "[[S-partner-home]]"]
source: "model"
project: "services-hub"
status: "generated"
date: 2026-09-07
generated: true
---
# شركة/جهة مقدّمة
<!-- generated from model.json — لا تعدّل يدوياً -->

الشريك الذي يقدم خدمة مساندة: شركة بذور، أسمدة، مختبر، مركز إرشاد، ممول.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| name | string | نعم |  |
| kind | enum | نعم | inputs | lab | advisory | finance | insurance | logistics | other |
| license | file | لا |  |
| contract_ref | string | لا | عقد مشاركة البيانات |
| regions | json | نعم |  |
| status | enum | نعم |  |

## الروابط
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-provider-user|مستخدم لدى الشركة]] (مستخدمون)
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-service|خدمة]] (يقدّم)
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-region-dataset|بيانات المنطقة (من الشركة)]] (تُدخل بيانات)
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-aggregate|إحصاء مجمّع للشركة]] (يرى مجمّعاً)
- relation: [[E-provider|شركة/جهة مقدّمة]] → [[E-data-agreement|اتفاقية بيانات]] (اتفاقية)

## الشاشات
- [[S-partner-onboarding|تسجيل الشركة الشريكة]]
- [[S-partner-home|لوحة الشركة (الرئيسية)]]

## المراجع
-
