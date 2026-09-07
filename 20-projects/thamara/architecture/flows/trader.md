---
type: index
title: "تدفق شاشات trader"
project: thamara
status: generated
date: 2026-09-07
---
# تدفق شاشات trader
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  trader_register["بيانات المنشأة"]
  trader_home["الرئيسية (تاجر)"]
  trader_market["السوق (العروض)"]
  trader_auction_view["صفحة المزاد والمزايدة"]
  trader_tender_create["إنشاء مناقصة"]
  trader_tenders["مناقصاتي"]
  trader_offers_review["مراجعة عروض المناقصة"]
  trader_transport_choose["اختيار الناقل"]
  trader_checkout["الدفع (البوابة البنكية)"]
  trader_orders["صفقاتي (تاجر)"]
  trader_confirm_receipt["تأكيد الاستلام"]
  trader_register -->|حفظ| trader_home
  trader_home -->|السوق| trader_market
  trader_home -->|مناقصاتي| trader_tenders
  trader_home -->|صفقاتي| trader_orders
  trader_market -->|فتح مزاد| trader_auction_view
  trader_market -->|شراء مباشر| trader_checkout
  trader_auction_view -->|عند الفوز: الدفع| trader_transport_choose
  trader_tender_create -->|نشر| trader_tenders
  trader_tenders -->|مراجعة العروض| trader_offers_review
  trader_tenders -->|مناقصة جديدة| trader_tender_create
  trader_offers_review -->|قبول عرض (يُخصم السعر فوراً)| trader_transport_choose
  trader_transport_choose -->|تأكيد والانتقال للدفع| trader_checkout
  trader_checkout -->|دفع| trader_orders
  trader_orders -->|تأكيد الاستلام| trader_confirm_receipt
  trader_confirm_receipt -->|تأكيد| trader_orders
```

- [[S-trader-register|بيانات المنشأة]]
- [[S-trader-home|الرئيسية (تاجر)]]
- [[S-trader-market|السوق (العروض)]]
- [[S-trader-auction-view|صفحة المزاد والمزايدة]]
- [[S-trader-tender-create|إنشاء مناقصة]]
- [[S-trader-tenders|مناقصاتي]]
- [[S-trader-offers-review|مراجعة عروض المناقصة]]
- [[S-trader-transport-choose|اختيار الناقل]]
- [[S-trader-checkout|الدفع (البوابة البنكية)]]
- [[S-trader-orders|صفقاتي (تاجر)]]
- [[S-trader-confirm-receipt|تأكيد الاستلام]]
