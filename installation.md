
# كيفية تثبيت Flutter على نظام ويندوز 2023

في هذا الدليل، نشرح خطوات تثبيت Flutter SDK على نظام Windows.

---

## الخطوة 1: تحميل Flutter SDK

1. انتقل إلى موقع Flutter الرسمي.
2. اختر النسخة المناسبة لنظام Windows.
3. قم بتحميل الملف المضغوط (*.zip*).
4. فك الضغط في مجلد مثل `C:\flutter`.

---

## الخطوة 2: إضافة Flutter إلى مسار النظام (PATH)

- افتح **Control Panel** → **System and Security** → **System** → **Advanced system settings** → **Environment Variables**.
- في **System variables**، اختر متغير `Path` واضغط على **Edit**.
- أضف المسار: `C:\flutter\bin`.
- اضغط OK لحفظ التغييرات.

---

## الخطوة 3: إعداد المشروع وتثبيت Android Studio

1. حمّل **Android Studio** من الموقع الرسمي.
2. أثناء التثبيت، فعل:
   - Android SDK
   - Android SDK Platform-Tools
   - Android SDK Build-Tools
   - Android Virtual Device

3. بعد التثبيت:
   - افتح Android Studio → SDK Manager → تأكد من تحديث SDK وPlatform‑Tools.
   - في AVD Manager، أنشئ محرّك Android وهمي (emulator) لتجربة التطبيقات.

---

## الخطوة 4: التحقق باستخدام `flutter doctor`

- افتح **PowerShell** أو **Command Prompt**.
- اكتب:
  ```bash
  flutter doctor
  ```
- ستظهر قائمة بالحزم المطلوبة والمفقودة. أكمل تثبيت كل الأنظمة أو الأدوات الموصى بها.
- عند وجود تحذير مثل:
  > Warning: `dart` on your path resolves to C:\dart\bin\dart.exe, which is not inside your current Flutter SDK checkout at C:\flutter...

  يُنصح بإعادة ترتيب مسار النظام ليضع `C:\flutter\bin` في المقدمة لتجنّب تضارب في المسارات ([arabflutter.com](https://arabflutter.com/install-flutter/?utm_source=chatgpt.com), [pub.dev](https://pub.dev/packages/arabic_roman_conv?utm_source=chatgpt.com), [stackoverflow.com](https://stackoverflow.com/questions/77404790/i-have-a-problem-in-setup-flutter-when-i-was-installed-flutter-in-my-computer-a?utm_source=chatgpt.com)).

---

## ملاحظة خاصة ببيئة اللغة العربية

إذا كانت لغة جهازك هي العربية، فقد تواجه بعض المشاكل أثناء التهيئة مثل تعذّر التعرف على `dart.exe`. أحد المستخدمين ذكر أن المشكلة اختفت بعد تغيير لغة النظام إلى الإنجليزية ([stackoverflow.com](https://stackoverflow.com/questions/77404790/i-have-a-problem-in-setup-flutter-when-i-was-installed-flutter-in-my-computer-a?utm_source=chatgpt.com)).

---

## نصائح نهائية

- وفّر دائمًا نسخة من Flutter SDK في مجلّد بدون مسافات أو رموز غير لاتينية.
- استخدم دائمًا كمرة التحديثات وتحقق بانتظام من `flutter upgrade`.
- جرّب تشغيل مشروع Flutter بسيط:
  ```bash
  flutter create my_app
  cd my_app
  flutter run
  ```

---

## خلاصة

| المرحلة            | الوصف |
|--------------------|-------|
| 🚀 التحميل         | تحميل Flutter SDK من الموقع الرسمي |
| 🔧 الإعداد         | إضافة Flutter إلى PATH |
| 💻 تثبيت البيئة    | Android Studio + SDK + AVD |
| ✅ التحقق          | تشغيل `flutter doctor` لحل المشكلات |

بعد الانتهاء من الخطوات السابقة، ستكون بيئة Flutter جاهزة للعمل على Windows 10 أو 11. بامكانك البدء بإنشاء تطبيقك الأول باستخدام Visual Studio Code أو Android Studio.

---

## روابط مفيدة

- [Flutter الرسمي](https://flutter.dev)
- [Android Studio](https://developer.android.com/studio)

---

> هذا الدليل مبني على:
> - **كيفية تثبيت Flutter على نظام ويندوز 2023** من arabflutter.com ([arabflutter.com](https://arabflutter.com/install-flutter/?utm_source=chatgpt.com))  
> - تجربة مستخدم حقيقي تم فيها تغيير لغة النظام من العربية إلى الإنجليزية لحل مشكلة بيئة Dart ([github.com](https://github.com/moesaeed/Flutter-Arabic-RTL-Internationalization?utm_source=chatgpt.com))
