---
type: index
title: "الخريطة المختصرة للكيانات"
project: thamara
status: generated
date: 2026-09-07
---
# الخريطة المختصرة للكيانات
<!-- generated from model.json — لا تعدّل يدوياً -->

نظرة عامة بلغة العمل: الكيانات مجمّعة بحسب المجال والعلاقات بينها، بلا حقول أو تفاصيل تقنية. التفاصيل في [[erd|الكيانات والعلاقات]].

```mermaid
flowchart TB
  subgraph identity["الهوية والحسابات"]
    user(["حساب"])
    role(["دور"])
    farmer(["مزارع"])
    trader(["تاجر"])
    transporter(["ناقل"])
  end
  subgraph logistics["النقل"]
    vehicle(["مركبة"])
    shipment(["شحنة"])
  end
  subgraph governance["الرقابة الحكومية"]
    officer(["موظف حكومي"])
    price_limit(["حد سعر"])
    blacklist(["قائمة سوداء"])
  end
  subgraph production["الإنتاج"]
    farm(["مزرعة"])
    crop(["محصول"])
  end
  subgraph catalog["الكتالوج"]
    product(["منتج (صنف)"])
  end
  subgraph trade["التداول"]
    listing(["عرض بيع"])
    auction(["مزاد مفتوح"])
    bid(["مزايدة"])
    tender(["مناقصة مغلقة"])
    offer(["عرض على مناقصة"])
    order(["صفقة"])
  end
  subgraph payment["الدفع والضمان"]
    escrow(["حساب ضمان"])
  end
  subgraph support["البلاغات والدعم"]
    report(["بلاغ"])
    ticket(["بطاقة دعم"])
  end
  subgraph platform["المنصة"]
    notification(["إشعار"])
  end
  user -->|"أدوار"| role
  user -->|"ملف مزارع"| farmer
  user -->|"ملف تاجر"| trader
  user -->|"ملف ناقل"| transporter
  user -->|"ملف موظف"| officer
  farmer -->|"حيازات"| farm
  farm -->|"تُنتج"| crop
  product -->|"صنف المحصول"| crop
  crop -->|"يُعرض في"| listing
  listing -->|"مزاد"| auction
  auction -->|"مزايدات"| bid
  trader -->|"يزايد"| bid
  trader -->|"يطرح مناقصة"| tender
  tender -->|"تتلقى عروضاً"| offer
  farmer -->|"يقدّم عرضاً"| offer
  trader -->|"يشتري"| order
  farmer -->|"يبيع"| order
  order -->|"يُضمن بـ"| escrow
  order -->|"تُشحن"| shipment
  transporter -->|"ينقل"| shipment
  transporter -->|"مركبات"| vehicle
  product -->|"حد سعر"| price_limit
  user -->|"يبلّغ"| report
  user -->|"يطلب دعماً"| ticket
  user -->|"قد يُحظر"| blacklist
  user -->|"يتلقى إشعارات"| notification
```

## المجالات
- **الهوية والحسابات**: [[E-user|حساب]]، [[E-role|دور]]، [[E-farmer|مزارع]]، [[E-trader|تاجر]]، [[E-transporter|ناقل]]
- **النقل**: [[E-vehicle|مركبة]]، [[E-shipment|شحنة]]
- **الرقابة الحكومية**: [[E-officer|موظف حكومي]]، [[E-price-limit|حد سعر]]، [[E-blacklist|قائمة سوداء]]
- **الإنتاج**: [[E-farm|مزرعة]]، [[E-crop|محصول]]
- **الكتالوج**: [[E-product|منتج (صنف)]]
- **التداول**: [[E-listing|عرض بيع]]، [[E-auction|مزاد مفتوح]]، [[E-bid|مزايدة]]، [[E-tender|مناقصة مغلقة]]، [[E-offer|عرض على مناقصة]]، [[E-order|صفقة]]
- **الدفع والضمان**: [[E-escrow|حساب ضمان]]
- **البلاغات والدعم**: [[E-report|بلاغ]]، [[E-ticket|بطاقة دعم]]
- **المنصة**: [[E-notification|إشعار]]
