---
type: index
title: "الكيانات والعلاقات"
project: services-hub
status: generated
date: 2026-09-07
---
# الكيانات والعلاقات
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
erDiagram
  core_farmer {
    ref core_id
    json consents
  }
  core_farm {
    ref core_id
    string governorate
    geo location
  }
  core_crop {
    ref core_id
    string product
    string season
  }
  region {
    string governorate
    string district
    string climate_zone
  }
  provider {
    string name
    enum kind
    file license
    string contract_ref
    json regions
    enum status
  }
  provider_user {
    ref provider_id
    string name
    enum role
  }
  service {
    ref provider_id
    string title
    enum category
    text description
    json input_schema
    json output_schema
    json pricing
    json regions
    enum status
  }
  offering {
    ref service_id
    string name
    json spec
    money price
    json availability
    json suitable_products
  }
  service_request {
    ref service_id
    ref farmer_id
    ref farm_id
    ref crop_id
    json input
    enum status
    money price
  }
  farm_report {
    ref farmer_id
    ref farm_id
    ref crop_id
    enum kind
    file file
    json values
    json shared_with
    date date
  }
  feedback {
    ref request_id
    ref farmer_id
    int rating
    json outcome
    text comment
    date date
  }
  region_dataset {
    ref provider_id
    ref region_id
    string product
    enum kind
    json payload
    date valid_from
    date valid_to
  }
  insight {
    ref farmer_id
    ref crop_id
    ref source_dataset_id
    ref source_report_id
    string title
    text body
    datetime read_at
  }
  aggregate {
    ref provider_id
    ref region_id
    string period
    json metrics
    int min_group_size
  }
  data_agreement {
    ref provider_id
    json scope
    int min_group_size
    date starts
    date ends
  }
  provider ||--o{ provider_user : "مستخدمون"
  provider ||--o{ service : "يقدّم"
  service ||--o{ offering : "عروض"
  service ||--o{ service_request : "طلبات"
  core_farmer ||--o{ service_request : "يطلب"
  core_farmer ||--o{ farm_report : "يرفع"
  core_farm ||--o{ farm_report : "تحاليلها"
  core_crop ||--o{ farm_report : "تحاليله"
  service_request ||--|| feedback : "تقييم"
  provider ||--o{ region_dataset : "تُدخل بيانات"
  region ||--o{ region_dataset : "بيانات المنطقة"
  region ||--o{ core_farm : "مزارعها"
  region_dataset ||--o{ insight : "تولّد"
  farm_report ||--o{ insight : "تولّد"
  core_farmer ||--o{ insight : "يتلقى"
  provider ||--o{ aggregate : "يرى مجمّعاً"
  provider ||--|| data_agreement : "اتفاقية"
  core_farm ||--o{ core_crop : "تُنتج"
  core_farmer ||--o{ core_farm : "يملك"
```

## الكيانات
- [[E-core-farmer|فلاح (من نواة ثمرة)]] (2 حقل)
- [[E-core-farm|مزرعة (من النواة)]] (3 حقل)
- [[E-core-crop|محصول (من النواة)]] (3 حقل)
- [[E-region|منطقة (محافظة/ناحية)]] (3 حقل)
- [[E-provider|شركة/جهة مقدّمة]] (6 حقل)
- [[E-provider-user|مستخدم لدى الشركة]] (3 حقل)
- [[E-service|خدمة]] (9 حقل)
- [[E-offering|عرض/منتج للخدمة]] (6 حقل)
- [[E-service-request|طلب خدمة]] (7 حقل)
- [[E-farm-report|تقرير/تحليل مرفوع]] (8 حقل)
- [[E-feedback|تغذية راجعة على خدمة]] (6 حقل)
- [[E-region-dataset|بيانات المنطقة (من الشركة)]] (7 حقل)
- [[E-insight|معلومة مخصصة للفلاح]] (7 حقل)
- [[E-aggregate|إحصاء مجمّع للشركة]] (5 حقل)
- [[E-data-agreement|اتفاقية بيانات]] (5 حقل)
