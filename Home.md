---
type: "index"
title: "الخزنة"
project: "global"
status: "generated"
date: 2026-09-07
---
# خزنة المشاريع

## المشاريع
<!-- vault:projects -->
- [[20-projects/thamara/index|ثمرة — سوق الهال الذكي]] · active
<!-- /vault:projects -->

## بانتظار المراجعة
<!-- vault:list status=pending limit=30 -->
- (لا شيء بعد)
<!-- /vault:list -->

## المساحات المشتركة
- [[10-principles/index|المبادئ والقيود والسياسات]]
- [[30-knowledge/index|المعرفة العامة]]
- [[40-ops/index|تشغيل الأتمتة]]
- [[50-log/index|السجل اليومي]]

## آخر القرارات
<!-- vault:list type=decision limit=10 -->
- 2026-09-07 · [[D-006-vault-obsidian|خزنة معرفة موحدة على نمط Obsidian]] · accepted
- 2026-09-05 · [[D-005-intake-haiku-low|جلسة الاستقبال على هايكو بجهد منخفض]] · accepted
- 2026-09-05 · [[D-004-github-pr-workflow|المستودع على GitHub وأسلوب Pull Request]] · accepted
- 2026-09-05 · [[D-003-jira-thm-project|جيرا: الموقع timeco والمشروع THM]] · accepted
- 2026-09-04 · [[D-002-telegram-first-channel|القناة الأولى تيليغرام]] · accepted
- 2026-09-04 · [[D-001-one-loop-first|البدء بحلقة واحدة فقط]] · accepted
<!-- /vault:list -->

## آخر أيام السجل
<!-- vault:list type=daily limit=7 -->
- 2026-09-07 · [[2026-09-07|2026-09-07]] · open
<!-- /vault:list -->

## كيف تعمل الخزنة
- كل ملاحظة لها frontmatter (النوع، المشروع، الحالة، التاريخ، المصدر) وروابط ويكي بين الملاحظات.
- الوارد من تيليغرام يظهر في «بانتظار المراجعة» ويُثبَّت من لوحة التحكم.
- القوائم أعلاه تولَّد آلياً بأمر `vault.mjs index`.
