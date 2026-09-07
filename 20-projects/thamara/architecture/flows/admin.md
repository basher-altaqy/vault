---
type: index
title: "تدفق شاشات admin"
project: thamara
status: generated
date: 2026-09-07
---
# تدفق شاشات admin
<!-- generated from model.json — لا تعدّل يدوياً -->

```mermaid
flowchart LR
  admin_dashboard["لوحة الإدارة"]
  admin_users["المستخدمون والتوثيق"]
  admin_catalog["الكتالوج والأصناف"]
  admin_price_limits["حدود الأسعار (الوزارة)"]
  admin_reports["البلاغات"]
  admin_blacklist["القائمة السوداء"]
  admin_tickets["بطاقات الدعم"]
  admin_escrow["حسابات الضمان"]
  admin_dashboard -->|المستخدمون| admin_users
  admin_dashboard -->|حدود الأسعار| admin_price_limits
  admin_dashboard -->|البلاغات| admin_reports
  admin_dashboard -->|الدعم| admin_tickets
  admin_dashboard -->|الضمان| admin_escrow
  admin_users -->|القائمة السوداء| admin_blacklist
  admin_reports -->|حظر وإدراج في القائمة السوداء| admin_blacklist
```

- [[S-admin-dashboard|لوحة الإدارة]]
- [[S-admin-users|المستخدمون والتوثيق]]
- [[S-admin-catalog|الكتالوج والأصناف]]
- [[S-admin-price-limits|حدود الأسعار (الوزارة)]]
- [[S-admin-reports|البلاغات]]
- [[S-admin-blacklist|القائمة السوداء]]
- [[S-admin-tickets|بطاقات الدعم]]
- [[S-admin-escrow|حسابات الضمان]]
