---
type: index
title: "الكيانات والعلاقات"
project: thamara
status: generated
date: 2026-09-07
---
# الكيانات والعلاقات
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
erDiagram
  user {
    string name_ar
    string name_en
    string phone
    string email
    string nationality
    date birth_date
    string birth_place
    enum verification
    datetime policy_signed_at
    string wallet_ref
  }
  role {
    ref user_id
    enum kind
    enum status
  }
  farmer {
    ref user_id
    json tenure_types
    file id_document
  }
  trader {
    ref user_id
    string company_name
    string company_email
    string company_phone
    enum activity
    string tax_number
    string license_number
    geo hq_location
    file commercial_register
    money balance
  }
  transporter {
    ref user_id
    enum kind
    file license_document
    json coverage_areas
  }
  vehicle {
    ref transporter_id
    int capacity_kg
    string model
    bool has_crane
    bool has_scale
    bool refrigerated
  }
  officer {
    ref user_id
    string job_title
    enum ministry
    json permissions
  }
  farm {
    ref farmer_id
    string name
    geo location
    enum tenure
    json packaging_methods
  }
  product {
    string name
    enum category
    json units
    json quality_grades
  }
  crop {
    ref farm_id
    ref product_id
    string name
    string variety
    decimal quantity
    enum unit
    date harvest_date
    date expiry_date
    enum quality_grade
    string size
    string color
    json photos
    json packaging
    json supply_range
  }
  listing {
    ref crop_id
    enum kind
    string title
    text description
    enum status
    ref price_limit_id
  }
  auction {
    ref listing_id
    money start_price
    money min_increment
    int duration_hours
    int final_countdown_min
    int auto_extend_min
    datetime ends_at
    ref winner_bid_id
  }
  bid {
    ref auction_id
    ref trader_id
    string alias
    money amount
    money reserved_amount
    datetime placed_at
  }
  tender {
    ref trader_id
    ref product_id
    decimal quantity
    enum quality_grade
    money price_cap
    datetime pickup_at
    geo pickup_location
    enum status
  }
  offer {
    ref tender_id
    ref farmer_id
    money price
    decimal quantity
    enum quality_grade
    datetime ready_at
    enum status
  }
  order {
    ref listing_id
    ref tender_id
    ref trader_id
    ref farmer_id
    money crop_amount
    money platform_fee
    money transport_fee
    enum status
  }
  escrow {
    ref order_id
    money total
    string bank_ref
    datetime receipt_confirmed_at
    datetime delivery_confirmed_at
    datetime released_at
  }
  shipment {
    ref order_id
    ref transporter_id
    ref vehicle_id
    money agreed_fee
    enum status
  }
  price_limit {
    ref product_id
    money min_price
    money max_price
    date valid_from
    string source
  }
  blacklist {
    ref user_id
    text reason
    ref report_id
    date since
  }
  report {
    ref reporter_id
    enum kind
    string title
    text description
    json attachments
    string conversation_ref
    string ref_number
    enum status
  }
  ticket {
    ref user_id
    string title
    enum category
    enum priority
    string ref_number
    enum status
  }
  notification {
    ref user_id
    enum kind
    json payload
    datetime read_at
  }
  user ||--o{ role : "أدوار"
  user ||--|| farmer : "ملف مزارع"
  user ||--|| trader : "ملف تاجر"
  user ||--|| transporter : "ملف ناقل"
  user ||--|| officer : "ملف موظف"
  farmer ||--o{ farm : "حيازات"
  farm ||--o{ crop : "تُنتج"
  product ||--o{ crop : "صنف المحصول"
  crop ||--o{ listing : "يُعرض في"
  listing ||--|| auction : "مزاد"
  auction ||--o{ bid : "مزايدات"
  trader ||--o{ bid : "يزايد"
  trader ||--o{ tender : "يطرح مناقصة"
  tender ||--o{ offer : "تتلقى عروضاً"
  farmer ||--o{ offer : "يقدّم عرضاً"
  trader ||--o{ order : "يشتري"
  farmer ||--o{ order : "يبيع"
  order ||--|| escrow : "يُضمن بـ"
  order ||--|| shipment : "تُشحن"
  transporter ||--o{ shipment : "ينقل"
  transporter ||--o{ vehicle : "مركبات"
  product ||--o{ price_limit : "حد سعر"
  user ||--o{ report : "يبلّغ"
  user ||--o{ ticket : "يطلب دعماً"
  user ||--|| blacklist : "قد يُحظر"
  user ||--o{ notification : "يتلقى إشعارات"
```

## الكيانات
- [[E-user|حساب]] (10 حقل)
- [[E-role|دور]] (3 حقل)
- [[E-farmer|مزارع]] (3 حقل)
- [[E-trader|تاجر]] (10 حقل)
- [[E-transporter|ناقل]] (4 حقل)
- [[E-vehicle|مركبة]] (6 حقل)
- [[E-officer|موظف حكومي]] (4 حقل)
- [[E-farm|مزرعة]] (5 حقل)
- [[E-product|منتج (صنف)]] (4 حقل)
- [[E-crop|محصول]] (14 حقل)
- [[E-listing|عرض بيع]] (6 حقل)
- [[E-auction|مزاد مفتوح]] (8 حقل)
- [[E-bid|مزايدة]] (6 حقل)
- [[E-tender|مناقصة مغلقة]] (8 حقل)
- [[E-offer|عرض على مناقصة]] (7 حقل)
- [[E-order|صفقة]] (8 حقل)
- [[E-escrow|حساب ضمان]] (6 حقل)
- [[E-shipment|شحنة]] (5 حقل)
- [[E-price-limit|حد سعر]] (5 حقل)
- [[E-blacklist|قائمة سوداء]] (4 حقل)
- [[E-report|بلاغ]] (8 حقل)
- [[E-ticket|بطاقة دعم]] (6 حقل)
- [[E-notification|إشعار]] (4 حقل)
