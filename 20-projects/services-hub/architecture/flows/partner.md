---
type: index
title: "تدفق شاشات partner"
project: services-hub
status: generated
date: 2026-09-07
---
# تدفق شاشات partner
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  partner_onboarding["تسجيل الشركة الشريكة"]
  partner_home["لوحة الشركة (الرئيسية)"]
  partner_services["إدارة الخدمات"]
  partner_offerings["العروض والمنتجات"]
  partner_region_data["إدخال بيانات المحافظات"]
  partner_requests["الطلبات الواردة"]
  partner_reports["التحاليل المشاركة معنا"]
  partner_analytics["التحليلات المجمّعة"]
  partner_users["مستخدمو الشركة"]
  partner_onboarding -->|إرسال للاعتماد| partner_home
  partner_home -->|خدماتي| partner_services
  partner_home -->|بيانات المحافظات| partner_region_data
  partner_home -->|الطلبات| partner_requests
  partner_home -->|التحليلات| partner_analytics
  partner_services -->|العروض| partner_offerings
```

- [[S-partner-onboarding|تسجيل الشركة الشريكة]]
- [[S-partner-home|لوحة الشركة (الرئيسية)]]
- [[S-partner-services|إدارة الخدمات]]
- [[S-partner-offerings|العروض والمنتجات]]
- [[S-partner-region-data|إدخال بيانات المحافظات]]
- [[S-partner-requests|الطلبات الواردة]]
- [[S-partner-reports|التحاليل المشاركة معنا]]
- [[S-partner-analytics|التحليلات المجمّعة]]
- [[S-partner-users|مستخدمو الشركة]]
