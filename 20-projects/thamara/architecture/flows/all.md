---
type: index
title: "تدفق شاشات all"
project: thamara
status: generated
date: 2026-09-07
---
# تدفق شاشات all
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  register["التسجيل واختيار الدور"]
  otp_verify["التحقق برمز OTP"]
  policy_sign["التوقيع على السياسات"]
  profile["الملف الشخصي"]
  notifications["الإشعارات"]
  report_create["تقديم بلاغ"]
  ticket_create["بطاقة دعم"]
  register -->|إرسال رمز التحقق| otp_verify
  otp_verify -->|تأكيد| policy_sign
  policy_sign -->|أوافق وأوقّع| farmer_register
```

- [[S-register|التسجيل واختيار الدور]]
- [[S-otp-verify|التحقق برمز OTP]]
- [[S-policy-sign|التوقيع على السياسات]]
- [[S-profile|الملف الشخصي]]
- [[S-notifications|الإشعارات]]
- [[S-report-create|تقديم بلاغ]]
- [[S-ticket-create|بطاقة دعم]]
