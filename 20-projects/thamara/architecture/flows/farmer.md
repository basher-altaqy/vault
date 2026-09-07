---
type: index
title: "تدفق شاشات farmer"
project: thamara
status: generated
date: 2026-09-07
---
# تدفق شاشات farmer
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  farmer_register["بيانات المزارع"]
  farmer_home["الرئيسية (مزارع)"]
  farmer_farms["مزارعي"]
  farmer_farm_add["إضافة مزرعة"]
  farmer_crops["محاصيلي"]
  farmer_crop_add["إضافة محصول"]
  farmer_sell_choose["اختيار نموذج البيع"]
  farmer_auction_create["إنشاء مزاد"]
  farmer_fixed_create["عرض بسعر ثابت"]
  farmer_listings["عروضي"]
  farmer_tender_browse["المناقصات المفتوحة"]
  farmer_offer_submit["تقديم عرض على مناقصة"]
  farmer_orders["صفقاتي (مزارع)"]
  farmer_register -->|حفظ| farmer_home
  farmer_home -->|مزارعي| farmer_farms
  farmer_home -->|محاصيلي| farmer_crops
  farmer_home -->|المناقصات| farmer_tender_browse
  farmer_home -->|صفقاتي| farmer_orders
  farmer_farms -->|إضافة مزرعة| farmer_farm_add
  farmer_farm_add -->|حفظ| farmer_farms
  farmer_crops -->|إضافة محصول| farmer_crop_add
  farmer_crop_add -->|حفظ ثم اختيار نموذج البيع| farmer_sell_choose
  farmer_sell_choose -->|مزاد مفتوح| farmer_auction_create
  farmer_sell_choose -->|بيع مباشر| farmer_fixed_create
  farmer_auction_create -->|نشر| farmer_listings
  farmer_fixed_create -->|نشر| farmer_listings
  farmer_tender_browse -->|تقديم عرض| farmer_offer_submit
  farmer_offer_submit -->|إرسال| farmer_tender_browse
```

- [[S-farmer-register|بيانات المزارع]]
- [[S-farmer-home|الرئيسية (مزارع)]]
- [[S-farmer-farms|مزارعي]]
- [[S-farmer-farm-add|إضافة مزرعة]]
- [[S-farmer-crops|محاصيلي]]
- [[S-farmer-crop-add|إضافة محصول]]
- [[S-farmer-sell-choose|اختيار نموذج البيع]]
- [[S-farmer-auction-create|إنشاء مزاد]]
- [[S-farmer-fixed-create|عرض بسعر ثابت]]
- [[S-farmer-listings|عروضي]]
- [[S-farmer-tender-browse|المناقصات المفتوحة]]
- [[S-farmer-offer-submit|تقديم عرض على مناقصة]]
- [[S-farmer-orders|صفقاتي (مزارع)]]
