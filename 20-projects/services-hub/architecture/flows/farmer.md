---
type: index
title: "تدفق شاشات farmer"
project: services-hub
status: generated
date: 2026-09-07
---
# تدفق شاشات farmer
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  farmer_services["الخدمات المساندة (داخل تطبيق ثمرة)"]
  farmer_service_detail["تفاصيل خدمة وعروضها"]
  farmer_service_request["طلب الخدمة"]
  farmer_service_track["متابعة طلباتي"]
  farmer_feedback["تقييم الخدمة بعد التجربة"]
  farmer_upload_report["رفع تحليل تربة/مياه/منتج"]
  farmer_insights["معلوماتي المخصصة (محصولي ومنطقتي)"]
  farmer_services -->|فتح خدمة| farmer_service_detail
  farmer_services -->|معلوماتي المخصصة| farmer_insights
  farmer_services -->|رفع تحليل| farmer_upload_report
  farmer_service_detail -->|طلب| farmer_service_request
  farmer_service_request -->|إرسال| farmer_service_track
  farmer_service_track -->|تقييم| farmer_feedback
  farmer_upload_report -->|رفع| farmer_insights
  farmer_insights -->|فتح الخدمة المصدر| farmer_service_detail
```

- [[S-farmer-services|الخدمات المساندة (داخل تطبيق ثمرة)]]
- [[S-farmer-service-detail|تفاصيل خدمة وعروضها]]
- [[S-farmer-service-request|طلب الخدمة]]
- [[S-farmer-service-track|متابعة طلباتي]]
- [[S-farmer-feedback|تقييم الخدمة بعد التجربة]]
- [[S-farmer-upload-report|رفع تحليل تربة/مياه/منتج]]
- [[S-farmer-insights|معلوماتي المخصصة (محصولي ومنطقتي)]]
