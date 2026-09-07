---
type: runbook
title: "تشغيل مركز ثمرة على السيرفر"
project: global
status: active
date: 2026-09-05
domain: infra
tags: [server, runbook]
related: []
source: claude
---

## قبل البدء
1. تأكد أن السيرفر يرد: `ssh rizik@185.216.132.211 'echo ok'` (في 2026-09-05 كان لا يرد من أي مكان في العالم).
2. أوقف الجلسة على جهازك (أغلق نافذة Windows Terminal) لأن بوت تيليغرام يقبل مستمعاً واحداً فقط.
3. أنشئ رمز دخول كلاود طويل الأمد من جهازك (يفتح المتصفح مرة واحدة):
   ```powershell
   claude setup-token
   ```
   وانسخ الرمز الناتج (يبدأ بـ `sk-ant-oat01-`).

## النشر (من جهازك)
```powershell
cd C:\Users\NTC\Desktop\thamara-ops
powershell -ExecutionPolicy Bypass -File .\server\deploy.ps1 -Setup
```
- ينسخ المجلد إلى `/opt/thamara-ops` مع رمز تيليغرام وقائمة الوصول، ثم يشغّل `setup.sh` (Node 22، Claude Code، Bun، إضافة تيليغرام، استنساخ `thamara-core` إلى `/opt/thamara-core`، خدمة systemd).
- إن كان SSH بكلمة مرور فستُطلب عدة مرات؛ يُفضَّل إضافة مفتاح: `ssh-keygen -t ed25519` ثم نسخ المفتاح العام إلى `~/.ssh/authorized_keys` على السيرفر.

## تفعيل الخدمة (على السيرفر)
```bash
echo 'CLAUDE_CODE_OAUTH_TOKEN=sk-ant-oat01-...' > /opt/thamara-ops/server/intake.env
chmod 600 /opt/thamara-ops/server/intake.env
sudo systemctl restart thamara-intake
sudo systemctl status thamara-intake --no-pager
tmux attach -t thamara     # لمشاهدة الجلسة، اخرج بـ Ctrl+B ثم D
```
عند التشغيل الأول يصلك في تيليغرام «🟢 جلسة ثمرة تعمل الآن على السيرفر». أي سقوط يُعاد تشغيله خلال 15 ثانية مع تنبيه.

## التحديث لاحقاً
أعد `deploy.ps1` بلا `-Setup` ثم `sudo systemctl restart thamara-intake`.

## ملاحظات
- الجلسة على السيرفر تعمل بـ `--dangerously-skip-permissions` لأن لا أحد يجيب عن طلبات الإذن؛ القيود في `.claude/settings.json` (منع force push وreset --hard وقراءة الأسرار) ونطاق العمل مجلدا ثمرة فقط. يُفضَّل مستخدم لينكس مستقل (`thamara`) بدل `rizik` حتى لا يشارك رتل صلاحياته.
- المنفّذون (`run-task.mjs`) يعملون في `/opt/thamara-worktrees/THM-n` ويستخدمون الرمز نفسه.
