---
type: index
title: "الخريطة المختصرة للكيانات"
project: services-hub
status: generated
date: 2026-09-07
---
# الخريطة المختصرة للكيانات
<!-- generated from model.json — لا تعدّل يدوياً -->

نظرة عامة بلغة العمل: الكيانات مجمّعة بحسب المجال والعلاقات بينها، بلا حقول أو تفاصيل تقنية. التفاصيل في [[erd|الكيانات والعلاقات]].

```mermaid
flowchart TB
  subgraph core["نواة ثمرة (مرجع)"]
    core_farmer(["فلاح (من نواة ثمرة)"])
    core_farm(["مزرعة (من النواة)"])
    core_crop(["محصول (من النواة)"])
    region(["منطقة (محافظة/ناحية)"])
  end
  subgraph partners["الشركات الشريكة"]
    provider(["شركة/جهة مقدّمة"])
    provider_user(["مستخدم لدى الشركة"])
  end
  subgraph catalog["الكتالوج"]
    service(["خدمة"])
    offering(["عرض/منتج للخدمة"])
  end
  subgraph operations["الطلبات والتشغيل"]
    service_request(["طلب خدمة"])
  end
  subgraph data_up["بيانات من الفلاح"]
    farm_report(["تقرير/تحليل مرفوع"])
    feedback(["تغذية راجعة على خدمة"])
  end
  subgraph data_down["بيانات إلى الفلاح"]
    region_dataset(["بيانات المنطقة (من الشركة)"])
    insight(["معلومة مخصصة للفلاح"])
  end
  subgraph analytics["التحليلات المجمّعة"]
    aggregate(["إحصاء مجمّع للشركة"])
  end
  subgraph governance["الرقابة الحكومية"]
    data_agreement(["اتفاقية بيانات"])
  end
  provider -->|"مستخدمون"| provider_user
  provider -->|"يقدّم"| service
  service -->|"عروض"| offering
  service -->|"طلبات"| service_request
  core_farmer -->|"يطلب"| service_request
  core_farmer -->|"يرفع"| farm_report
  core_farm -->|"تحاليلها"| farm_report
  core_crop -->|"تحاليله"| farm_report
  service_request -->|"تقييم"| feedback
  provider -->|"تُدخل بيانات"| region_dataset
  region -->|"بيانات المنطقة"| region_dataset
  region -->|"مزارعها"| core_farm
  region_dataset -->|"تولّد"| insight
  farm_report -->|"تولّد"| insight
  core_farmer -->|"يتلقى"| insight
  provider -->|"يرى مجمّعاً"| aggregate
  provider -->|"اتفاقية"| data_agreement
  core_farm -->|"تُنتج"| core_crop
  core_farmer -->|"يملك"| core_farm
```

## المجالات
- **نواة ثمرة (مرجع)**: [[E-core-farmer|فلاح (من نواة ثمرة)]]، [[E-core-farm|مزرعة (من النواة)]]، [[E-core-crop|محصول (من النواة)]]، [[E-region|منطقة (محافظة/ناحية)]]
- **الشركات الشريكة**: [[E-provider|شركة/جهة مقدّمة]]، [[E-provider-user|مستخدم لدى الشركة]]
- **الكتالوج**: [[E-service|خدمة]]، [[E-offering|عرض/منتج للخدمة]]
- **الطلبات والتشغيل**: [[E-service-request|طلب خدمة]]
- **بيانات من الفلاح**: [[E-farm-report|تقرير/تحليل مرفوع]]، [[E-feedback|تغذية راجعة على خدمة]]
- **بيانات إلى الفلاح**: [[E-region-dataset|بيانات المنطقة (من الشركة)]]، [[E-insight|معلومة مخصصة للفلاح]]
- **التحليلات المجمّعة**: [[E-aggregate|إحصاء مجمّع للشركة]]
- **الرقابة الحكومية**: [[E-data-agreement|اتفاقية بيانات]]
