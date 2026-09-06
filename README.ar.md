<div align="center">

<img src="assets/aidoit-readme-cover.png" alt="AiDoIt يوحّد مزودي الذكاء الاصطناعي والنماذج وأدوات البرمجة" width="100%" />

<br />

[简体中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [العربية](README.ar.md) · [Español](README.es.md)

<br />

[![الإصدار](https://img.shields.io/badge/Release-v0.0.9-7c3aed?style=for-the-badge)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0ea5e9?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-x64%20%7C%20ARM64-e95420?style=for-the-badge&logo=ubuntu&logoColor=white)](HelpMd/Ubuntu/README.md)
[![الخصوصية](https://img.shields.io/badge/API_Keys-محلية-10b981?style=for-the-badge)](#-الأمان-والخصوصية)
[![الترخيص](https://img.shields.io/badge/License-GPLv3-f59e0b?style=for-the-badge)](LICENSE)

### تطبيق واحد لأدوات ونماذج البرمجة بالذكاء الاصطناعي

يدعم AiDoIt نظامي **Windows وUbuntu بمعماريتي x64 وARM64**. أدر **Codex وChatGPT وClaude Code وClaude Desktop وDeepSeek Harness** على Windows، وثبّت Codex وClaude Code على خوادم Ubuntu، وبدّل بين الحسابات الرسمية ونماذج مزودي الخدمات الخارجيين.

[التنزيل الآن](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) · [البدء السريع](#-البدء-السريع) · [الأدلة المصورة](#-الوثائق) · [الإبلاغ عن مشكلة](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)

</div>

<div dir="rtl">

---

## ✨ لماذا AiDoIt؟

| الإمكانية | ما الذي تحصل عليه |
|---|---|
| **Windows + Ubuntu** | دعم Windows 10/11 وبيئات Ubuntu CLI بمعماريتي x64 وARM64 |
| **لوحة تحكم موحدة** | إدارة Codex وClaude وDeepSeek Harness دون تعديل ملفات الإعداد باستمرار |
| **اكتشاف تلقائي** | اكتشاف تطبيقات سطح المكتب وأدوات CLI وحالة تسجيل الدخول وبيئة التشغيل |
| **عدة Providers ونماذج** | فصل المزودين وبيانات الاعتماد وقوائم النماذج والتبديل بينها في أي وقت |
| **اختبار قبل التفعيل** | قياس التوفر الحقيقي وزمن استجابة النموذج قبل تطبيقه |
| **إعدادات معزولة** | إدارة Codex وClaude وHarness بصورة مستقلة لمنع التداخل |
| **استعادة آمنة** | حفظ الحالة الأصلية واستعادة الإعداد الرسمي عند إيقاف التكامل |
| **تحديث داخل التطبيق** | بدءًا من `v0.0.7` يمكن اكتشاف الإصدارات المستقرة اللاحقة وتثبيتها من التطبيق |
| **مفاتيح محلية** | تبقى مفاتيح API على جهازك ولا تعرض الواجهة قيمتها كاملة |

<br />

<img src="assets/aidoit-workflow-intl.svg" alt="اتصال المزودين والنماذج عبر AiDoIt بأدوات Codex وClaude وDeepSeek Harness" width="100%" />

## 📦 التنزيل والتثبيت

### Windows 10/11 x64

الإصدار المستقر الحالي لـ Windows هو **AiDoIt v0.0.9**. نزّله فقط من [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest).

| الحزمة | الاستخدام المقترح | التنزيل |
|---|---|---|
| `AiDoIt_0.0.9_x64-setup.exe` | برنامج التثبيت القياسي الموصى به لمعظم المستخدمين | [تنزيل Setup EXE](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_x64-setup.exe) |

> [!TIP]
> للتحقق من المجموع الاختباري أو الترقية أو تثبيت MSI بصمت، راجع [دليل تثبيت Windows](HelpMd/Windows/Installation/README.md).

### macOS (Apple Silicon)

[تنزيل AiDoIt v0.0.9 DMG](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_aarch64.dmg)

اسحب AiDoIt إلى Applications.

يستخدم هذا الإصدار توقيع ad-hoc ولم يخضع لتوثيق Apple. عند التشغيل الأول قد تحتاج إلى النقر بزر الفأرة الأيمن واختيار فتح.

### Ubuntu x64 / ARM64

ثبّت Codex أو Claude Code أو كليهما على خادم Ubuntu باستخدام السكربت المباشر:

```bash
curl -fsSL https://service.aidoit.pro/install | bash
```

يمكن إلغاء التثبيت واستعادة إعداد المستخدم المحفوظ قبل التثبيت:

```bash
curl -fsSL https://service.aidoit.pro/uninstall | bash
```

> [!IMPORTANT]
> ينفّذ `curl | bash` سكربتًا بعيدًا مباشرة. تحقق من النطاق والمصدر أولًا، ثم اتبع [دليل Ubuntu المصور](HelpMd/Ubuntu/README.md).

## 🚀 البدء السريع

### Windows

1. ثبّت AiDoIt وشغّله وانتظر اكتشاف الأدوات المحلية وحالة تسجيل الدخول.
2. افتح **تكامل Codex** أو **تكامل Claude Code** أو **DeepSeek Harness**.
3. أضف Provider وأدخل Base URL ومفتاح API من مصدر موثوق.
4. اجلب النماذج أو أضفها، ثم نفّذ اختبار التوفر أولًا.
5. اختر الـ Provider والنموذج الافتراضيين وفعّل التكامل.
6. عطّل التكامل الخارجي متى شئت لاستعادة الإعداد الرسمي السابق.

### Ubuntu

1. سجّل الدخول كمستخدم Linux العادي الذي سيشغّل Codex أو Claude Code.
2. نفّذ أمر التثبيت واختر طريقة الدخول `sk` أو `account`.
3. اختر هدف النشر `both` أو `codex` أو `claude`.
4. شغّل `codex` أو `claude` واستخدم `/model` لاختيار نموذج واختباره.

| أريد أن… | ابدأ من هنا |
|---|---|
| أستخدم نماذج Provider في Codex أو ChatGPT | [دليل Codex على Windows](HelpMd/Windows/Codex/README.md) |
| أستخدم نماذج Provider في Claude Code أو Claude Desktop | [دليل Claude على Windows](HelpMd/Windows/Claude/README.md) |
| أهيئ Codex أو Claude Code على Ubuntu | [تثبيت Ubuntu واستخدامه](HelpMd/Ubuntu/README.md) |

## 🧩 الوظائف الأساسية

<details open>
<summary><strong>تكامل Codex وChatGPT</strong></summary>

- اكتشاف Codex وChatGPT وCodex CLI وحالة تسجيل الدخول تلقائيًا.
- استخدام النماذج الرسمية ونماذج Providers الخارجيين معًا.
- تثبيت Codex واختياره وتشغيله، مع اختبار النموذج قبل التفعيل.
- عند انشغال التطبيق يمكن اختيار الإغلاق العادي أو الإجباري قبل المتابعة.

</details>

<details>
<summary><strong>Claude Code وClaude Desktop</strong></summary>

- اكتشاف Claude Code وتثبيته وتشغيله تلقائيًا.
- اكتشاف Claude Desktop وفتحه أو اختيار حزمة تثبيت محلية.
- فصل Providers والنماذج وبيانات الاعتماد الخاصة بـ Claude عن Codex.
- استعادة الإعدادات والنماذج السابقة عند إيقاف التكامل.

</details>

<details>
<summary><strong>إدارة DeepSeek Harness</strong></summary>

- تثبيت DeepSeek Harness Web وتشغيله وإيقافه وفتحه.
- إدارة Providers وبيانات الاعتماد والنماذج والنموذج الافتراضي بصورة مستقلة.
- عرض قدرات السياق والاستدلال وتنفيذ اختبارات استجابة حقيقية.
- عدم تغيير Agents والأدوات والجلسات وسجل المهام الموجود في Harness.
- حماية الإعداد النشط أثناء التشغيل وإتاحته للتعديل بعد الإيقاف.

</details>

<details>
<summary><strong>إدارة Providers والنماذج</strong></summary>

- إضافة عدة Providers بعناوين ومفاتيح ونماذج وحالات مستقلة.
- جلب نماذج الخدمة تلقائيًا أو إدارة القائمة يدويًا.
- اختيار النماذج المفضلة والافتراضية دون إعادة إدخال بيانات الاعتماد.
- تبديل الواجهة بين الصينية والإنجليزية مع حفظ الاختيار.

</details>

## 📚 الوثائق

| المنصة | الأدلة |
|---|---|
| Windows | [التثبيت والترقية](HelpMd/Windows/Installation/README.md) · [Codex](HelpMd/Windows/Codex/README.md) · [Claude](HelpMd/Windows/Claude/README.md) |
| macOS | [Codex](HelpMd/macOS/Codex/README.md) · [Claude](HelpMd/macOS/Claude/README.md) |
| Ubuntu | [التثبيت والإعداد والاختبار](HelpMd/Ubuntu/README.md) |

يمكنك أيضًا تصفح [مركز مساعدة AiDoIt](HelpMd/README.md) حسب المنصة.

## 🔐 الأمان والخصوصية

- تبقى مفاتيح API والإعدادات على جهازك، ولا تعرض الواجهة المفتاح كاملًا.
- تبقى بيانات اعتماد Codex وClaude وHarness وإعداداتها منفصلة.
- يحفظ AiDoIt الحالة الأصلية قبل التفعيل ويمكنه استعادة الإعداد الرسمي لاحقًا.
- أخفِ المفاتيح وأسماء المستخدمين والمسارات المحلية وعناوين الخدمات قبل نشر Issues أو السجلات أو الصور.

> [!IMPORTANT]
> يدير AiDoIt الإعداد والتوجيه محليًا. تظل الطلبات المرسلة إلى Providers خارجيين خاضعة لسياساتهم وأسعارهم وشروطهم. استخدم فقط الخدمات التي تثق بها.

## ❓ الأسئلة الشائعة

<details>
<summary><strong>هل يستبدل AiDoIt إعدادي الرسمي؟</strong></summary>

يحفظ الحالة الأصلية عند التفعيل ويمكنه استعادتها عند الإيقاف. تُدار إعدادات Codex وClaude وHarness بصورة مستقلة.

</details>

<details>
<summary><strong>لماذا يفشل اكتشاف النموذج أو اختباره؟</strong></summary>

تحقق من Base URL ومفتاح API واتصال الشبكة ودعم الـ Provider للبروتوكول المطلوب. لا تنشر مفتاحًا كاملًا.

</details>

## 💬 التواصل والملاحظات

- المشروع: [AiDoIt-Platform/AiDoIt](https://github.com/AiDoIt-Platform/AiDoIt)
- المشكلات والاقتراحات: [إنشاء Issue](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)
- الإصدارات السابقة: [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases)
- الترخيص: [GNU GPL v3](LICENSE)

</div>

<div align="center">

**AiDoIt — أدخل أي نموذج إلى سير عمل تطوير الذكاء الاصطناعي بسهولة أكبر.**

</div>
