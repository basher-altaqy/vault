---
type: index
title: "تدفق شاشات transporter"
project: thamara
status: generated
date: 2026-09-07
---
# تدفق شاشات transporter
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  transporter_register["بيانات الناقل"]
  transporter_home["الرئيسية (ناقل)"]
  transporter_vehicles["مركباتي"]
  transporter_requests["طلبات النقل"]
  transporter_deliveries["توصيلاتي"]
  transporter_confirm_delivery["تأكيد التسليم"]
  transporter_register -->|حفظ| transporter_vehicles
  transporter_home -->|طلبات النقل| transporter_requests
  transporter_home -->|مركباتي| transporter_vehicles
  transporter_home -->|توصيلاتي| transporter_deliveries
  transporter_deliveries -->|تأكيد التسليم| transporter_confirm_delivery
  transporter_confirm_delivery -->|تأكيد| transporter_deliveries
```

- [[S-transporter-register|بيانات الناقل]]
- [[S-transporter-home|الرئيسية (ناقل)]]
- [[S-transporter-vehicles|مركباتي]]
- [[S-transporter-requests|طلبات النقل]]
- [[S-transporter-deliveries|توصيلاتي]]
- [[S-transporter-confirm-delivery|تأكيد التسليم]]
