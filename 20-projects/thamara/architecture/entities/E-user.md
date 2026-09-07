---
id: "E-user"
type: "entity"
title: "حساب"
domain: "identity"
tags: ["entity"]
related: ["[[E-role]]", "[[E-farmer]]", "[[E-trader]]", "[[E-transporter]]", "[[E-officer]]", "[[E-report]]", "[[E-ticket]]", "[[E-blacklist]]", "[[E-notification]]", "[[S-register]]", "[[S-otp-verify]]", "[[S-profile]]", "[[accounts]]"]
source: "model"
project: "thamara"
status: "generated"
date: 2026-09-07
generated: true
---
# حساب
<!-- generated from model.json — لا تعدّل يدوياً -->

حساب واحد لكل شخص بأدوار متعددة (مزارع، تاجر، ناقل، موظف). التفعيل بمصادقة مزدوجة: OTP + اعتماد الأدمن.

## الحقول
| الحقل | النوع | إلزامي | ملاحظة |
|---|---|---|---|
| name_ar | string | نعم | كما في الهوية |
| name_en | string | لا |  |
| phone | string | نعم | مرتبط بالهوية، OTP |
| email | string | نعم |  |
| nationality | string | لا |  |
| birth_date | date | لا |  |
| birth_place | string | لا |  |
| verification | enum | نعم | unverified | verified | suspended |
| policy_signed_at | datetime | نعم | التوقيع الإلكتروني على السياسات |
| wallet_ref | string | لا | محفظة أو حساب بنكي |

## الروابط
- relation: [[E-user|حساب]] → [[E-role|دور]] (أدوار)
- relation: [[E-user|حساب]] → [[E-farmer|مزارع]]
- relation: [[E-user|حساب]] → [[E-trader|تاجر]]
- relation: [[E-user|حساب]] → [[E-transporter|ناقل]]
- relation: [[E-user|حساب]] → [[E-officer|موظف حكومي]]
- relation: [[E-user|حساب]] → [[E-report|بلاغ]]
- relation: [[E-user|حساب]] → [[E-ticket|بطاقة دعم]]
- relation: [[E-user|حساب]] → [[E-blacklist|قائمة سوداء]]
- relation: [[E-user|حساب]] → [[E-notification|إشعار]]

## الشاشات
- [[S-register|التسجيل واختيار الدور]]
- [[S-otp-verify|التحقق برمز OTP]]
- [[S-profile|الملف الشخصي]]

## المراجع
[[accounts]]
