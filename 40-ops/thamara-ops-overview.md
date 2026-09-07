---
type: runbook
title: "مركز thamara-ops: نظرة عامة وأوامر تيليغرام"
project: global
status: active
date: 2026-09-05
domain: process
tags: [ops, telegram]
related: ["[[server-runbook]]"]
source: claude
---

## ما هو جاهز (نفّذه كلاود في 2026-09-04)
- `CLAUDE.md`: خوارزمية الالتقاط والتفكيك والموافقة والتنفيذ.
- `docs/spec-souq-alhal-v4.md`: وثيقة المواصفات كمرجع فهم. `docs/decisions.md`: قراراتك.
- `state/proposals.json`: المقترحات المعلّقة. `proposals/P-example.json`: قالب مقترح.
- `scripts/jira.mjs`: إنشاء المهام في جيرا عبر REST إن لم يعمل MCP.
- `start.ps1`: تشغيل الجلسة مع قناة تيليغرام.
- مثبّت على الجهاز: Claude Code CLI 2.1.261، Bun 1.4.1، إضافة تيليغرام الرسمية، خادم MCP الرسمي لأتلاسيان.

## ما أُنجز في 2026-09-05
1. **بوت تيليغرام:** @thamara_ops_bot، الرمز محفوظ في `~/.claude/channels/telegram/.env`.
2. **الوصول:** `~/.claude/channels/telegram/access.json` بسياسة `allowlist` ومعرّفك الرقمي `768269169` فقط. لا اقتران مطلوب.
3. **جيرا:** الموقع `https://timeco.atlassian.net` مضبوط في `config.json`.

## ما بقي عليك
2. **شغّل الجلسة:** في PowerShell داخل هذا المجلد:
   ```powershell
   powershell -ExecutionPolicy Bypass -File .\start.ps1
   ```
   ثم أرسل أي مهمة للبوت من تيليغرام.
4. **جيرا:** الموقع مضبوط في `config.json`: `https://timeco.atlassian.net` والمشروع `THM`.
   أ. أنشئ رمز API من https://id.atlassian.com/manage-profile/security/api-tokens وضعه في ملف `.env` داخل هذا المجلد:
   ```
   JIRA_EMAIL=platformratl@gmail.com
   JIRA_API_TOKEN=...
   ```
   ب. أنشئ المشروع وتحقق من الاتصال:
   ```powershell
   node scripts/jira.mjs create-project
   node scripts/jira.mjs check
   ```
   ج. (اختياري، للأدوات المباشرة داخل الجلسة) نفّذ `/mcp` واختر `atlassian` وسجّل الدخول بحساب أتلاسيان.
5. **المستودع الهدف:** عدّل `targetRepo` في `config.json` إلى مجلد كود ثمرة (أو اتركه ليُنشأ `thamara-core` عند أول مهمة).

## البنية بعد تحسينات 2026-09-05
- **جلسة استقبال** (تيليغرام ↔ كلاود) لا تنفّذ كوداً؛ تفهم وتفكّك وتنسّق.
- **منفّذ منفصل لكل مهمة**: `node scripts/run-task.mjs THM-n` → worktree مستقل، جلسة كلاود غير تفاعلية، commit/push، PR، تعليق جيرا، تقرير تيليغرام. سجل كل تشغيل في `state/runs/`.
- **أذونات مسبقة** في `.claude/settings.json` (مسموح: git، node scripts، تعديل مجلدي ثمرة؛ ممنوع: force push، reset --hard، قراءة الأسرار).
- **إشعار استلام** 👀 على كل رسالة تصل، وفهرس المواصفات `docs/spec-index.md` لقراءة القسم المعني فقط، وسياسات الموافقة الدائمة في `docs/policies.md`.
- **أوامر تيليغرام**: «وافق P-n»، «عدّل P-n: …»، «ألغِ P-n»، «ادمج THM-n»، «أنجزت THM-n: القرار»، «أعد THM-n»، «سياسة: …».
- **السيرفر**: `server/deploy.ps1` ينشر المجلد وقناة تيليغرام إلى `/opt/thamara-ops`، و`server/setup.sh` يثبّت الأدوات ويسجّل خدمة systemd `thamara-intake` (tmux + حارس يعيد التشغيل ويُنبّه في تيليغرام). لا تشغّل الجلسة على الجهاز والسيرفر معاً (البوت يقبل مستمعاً واحداً).

## الاستخدام اليومي
- أرسل المهمة نصاً للبوت. يرد خلال دقيقة بمقترح `P-n` من 3 إلى 8 مهام.
- «وافق P-n» أو «وافق P-n عدا 2» أو «عدّل P-n: …» أو «ألغِ P-n».
- بعد الموافقة تُنشأ المهام في جيرا ويبدأ التنفيذ، وبعد كل مهمة يصلك تقرير من 3 أسطر وسؤال واحد.
- الجلسة يجب أن تبقى مفتوحة على الجهاز (أو لاحقاً على السيرفر داخل tmux).

## ملاحظات
- واتساب غير مدعوم رسمياً في قنوات كلاود كود؛ يُضاف لاحقاً عبر Meta Cloud API كقناة مخصصة.
- عند وجود طلب إذن أثناء غيابك تتوقف الجلسة حتى تعود؛ لتشغيل غير مراقَب استخدم `--dangerously-skip-permissions` فقط على جهاز موثوق.
