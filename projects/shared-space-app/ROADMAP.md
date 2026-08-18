# Shared Space App — Execution Roadmap

**Goal:** تطبيق Flutter خاص بين شخصين فقط، يكون هدية جاهزة قبل 1 يناير 2027، مع نسخة مستقرة بحلول 20 ديسمبر 2026.

## مبدأ المشروع
التطبيق ليس Chat ولا Social Network. هو مساحة خاصة ومنظمة بين شخصين لحفظ الخطط، مشاركة اليوم، والرجوع للأشياء التي نريد عملها أو فعلناها معًا.

أي Feature جديدة لازم تخدم واحد من هذه الأهداف:
1. نشارك يومنا.
2. نحفظ شيء نريد عمله معًا.
3. نحفظ شيء فعلناه ونرجع له لاحقًا.

إذا ما تخدم واحد منها، تتأجل.

---

# المرحلة 0 — تجهيز المشروع | 18–24 أغسطس

## المطلوب
- تثبيت Flutter وVS Code وAndroid Studio / Xcode حسب الجهاز.
- إنشاء Flutter project منفصل للتطبيق.
- إنشاء Firebase project منفصل.
- جعل Repository الكود Private قبل إضافة أي أسرار أو إعدادات حساسة.
- تجهيز `.gitignore` بشكل صحيح.
- منع رفع أي صور أو رسائل أو بيانات شخصية إلى GitHub.
- إنشاء مجلدات المشروع الأساسية.

## قرار الخصوصية
- المستخدمون: شخصان فقط.
- الدخول عن طريق حساب + Invite خاص.
- لا يوجد Search Users.
- لا يوجد Profile عام.
- كل البيانات مربوطة بـ `spaceId` خاص.
- الصور والرسائل الحقيقية لا تدخل أثناء التطوير؛ نستخدم Test Data فقط.

**Deliverable:** Flutter app يفتح محليًا + Firebase جاهز + GitHub منظم.

---

# المرحلة 1 — Product Definition | 25 أغسطس–7 سبتمبر

## 1. تحديد الـMVP النهائي

### P0 — لازم تكون موجودة
- Login / Sign up.
- Create Space / Join with Invite.
- Home بسيط.
- Monthly Photo Albums.
- Notes / Message Cards.
- Restaurants & Cafes.
- Movies & Series.
- Music.
- Shared Plans.
- Notifications.
- Morning Card مرة واحدة صباحًا عند أول فتح يومي.

### P1 — بعد ما يشتغل الأساس
- Share to App من TikTok / Instagram / Spotify / Google Maps / Safari وغيرها.
- Open Later للرسائل.
- Reactions.
- Album خاص لمناسبة أو رحلة بجانب الألبومات الشهرية.

### P2 — بعد الهدية
- End-to-End Encryption كامل للصور والرسائل.
- Voice notes.
- Advanced scrapbook editor.
- AI classification المتقدم للروابط.

## 2. Navigation المقترح
Bottom Navigation:
- Home
- Library
- Add
- Photos
- Us / Settings

داخل Library:
- Restaurants & Cafes
- Movies & Series
- Music
- Shared Plans
- Notes / Cards

## 3. Home
لا يكون Dashboard مزدحم.
يعرض فقط:
- Morning Card إذا كانت أول مرة صباحًا.
- آخر Card من الطرف الثاني.
- آخر إضافة جديدة.
- Preview من ألبوم الشهر الحالي.
- شيء واحد من Shared Plans قريب أو جديد.

**Deliverable:** Product brief + User Flow + Screen Map + قائمة Features نهائية.

---

# المرحلة 2 — UX/UI Design | 8–28 سبتمبر

## Week 1 — Structure
- Splash.
- Login.
- Create Space.
- Join with Invite.
- Home wireframe.
- Library wireframe.

## Week 2 — Core Content
- Monthly Albums Library.
- Album Cover.
- Album Pages / scrapbook-style viewer.
- Notes Cards stack.
- Card composer.
- Restaurants list + details.
- Movies list + details.
- Music list.
- Shared Plans list.

## Week 3 — Interactions
- Rating flow.
- Visited / Watched states.
- Morning Card.
- Open Later locked state.
- Notifications states.
- Share-to-App save sheet.
- Empty / Loading / Error states.

## Design system
- Cream / warm background.
- Soft rounded cards.
- Translucent gradients.
- Colorful stacked message cards.
- Albums as books / shelf.
- Scrapbook / Polaroid photo direction.

**Deliverable:** Clickable Figma prototype يغطي النسخة الأولى كاملة.

---

# المرحلة 3 — Flutter Foundation | 29 سبتمبر–12 أكتوبر

## Week 1
- إنشاء Flutter project structure.
- Theme colors / spacing / typography.
- Reusable buttons/cards/inputs.
- Bottom navigation.
- Routing.

## Week 2
- Firebase Auth.
- Login / logout.
- Error handling.
- App lock placeholder.
- Secure local preferences.

**Deliverable:** التطبيق يفتح، يسجل دخول، والتنقل الأساسي يعمل.

---

# المرحلة 4 — Private Space + Security | 13–26 أكتوبر

## Database basics
Collections مقترحة:
- users
- spaces
- memberships
- albums
- photos
- cards
- restaurants
- movies
- music
- plans
- activities
- notifications

## Access rules
- أي User لا يقرأ إلا Space الخاص به.
- Membership لازم تكون موجودة للوصول.
- Invite يستخدم مرة واحدة أو له Expiry.
- كل media path مرتبط بـ spaceId.
- Firebase Storage Rules تمنع قراءة الملفات من خارج Space.

## Features
- Create Space.
- Generate Invite.
- Join Space.
- ربط حسابين فقط.
- Real-time sync.

**Deliverable:** حسابان حقيقيان يشاركان Space واحد ولا يستطيع حساب ثالث رؤية المحتوى.

---

# المرحلة 5 — Monthly Photos | 27 أكتوبر–9 نوفمبر

## النظام
- أول يوم من كل شهر ينشأ Album تلقائيًا عند أول استخدام.
- الاسم مثل `August 2026`.
- كل صورة جديدة تذهب افتراضيًا لألبوم الشهر الحالي.
- يمكن إنشاء ألبوم يدوي لرحلة أو مناسبة.

## داخل الألبوم
- Upload photo.
- Caption.
- Date.
- Added by.
- ترتيب الصور.
- Cover image.
- Book / scrapbook visual viewer.

## الأداء
- ضغط الصور قبل الرفع.
- Thumbnail منفصل.
- Lazy loading.

**Deliverable:** الطرفان يضيفان صورًا ويشاهدان ألبوم الشهر نفسه بشكل متزامن.

---

# المرحلة 6 — Cards + Morning Experience | 10–19 نوفمبر

## Notes / Messages
- Cards بدل Chat.
- Stack visual.
- ألوان متعددة.
- Text / title / date / emoji / optional image.
- Reactions.
- Reply بسيط على Card.

## Open Later
- Card مغلق حتى وقت محدد.
- لا يظهر محتواه قبل الموعد.

## Morning Card
- تظهر مرة واحدة فقط يوميًا عند أول فتح صباحي.
- المحتوى ممكن يكون: رسالة، اقتباس، صورة، أغنية، ذكرى.
- بعد فتحها لا تتكرر في نفس اليوم.

**Deliverable:** تجربة الرسائل الشخصية الأساسية تعمل بالكامل.

---

# المرحلة 7 — Shared Files | 20 نوفمبر–1 ديسمبر

## Restaurants & Cafes
- Want to visit.
- Visited.
- Rating لكل شخص.
- Would go again: Yes / No.
- Link / Map URL.

## Movies & Series
- Want to watch.
- Watched.
- Rating لكل شخص.

## Music
- Song title.
- Artist.
- Link.
- Added by.
- Date.

## Shared Plans
- Plan title.
- Optional date.
- Status: Planned / Done.
- Notes.

**Deliverable:** الملفات الأساسية تعمل وتدعم الإضافة من الطرفين.

---

# المرحلة 8 — Notifications + Share Links | 2–8 ديسمبر

## Notifications
- New Card.
- New Photo.
- New Restaurant / Movie / Song / Plan.
- Open Later ready.

## Share to App
ابدئي بالأسهل:
1. Safari / generic URLs.
2. Spotify.
3. Google Maps.
4. YouTube.
5. TikTok / Instagram / X حسب metadata المتاحة.

Flow:
Share → App → Preview → Suggested File → Save.

إذا ما عرف التطبيق النوع، المستخدم يختار الملف يدويًا.

**Deliverable:** مشاركة رابط من خارج التطبيق وحفظه داخله بنجاح.

---

# المرحلة 9 — Import سنتين من الذكريات | 9–14 ديسمبر

ممنوع تبدأ هذه المرحلة قبل استقرار الخصوصية والنسخ الاحتياطي.

## تجهيز المحتوى خارج التطبيق
قسّمي البيانات أولًا:
- صور حسب الأشهر.
- أغاني مهمة.
- أفلام شاهدتموها.
- مطاعم وأماكن.
- رسائل أو اقتباسات مهمة.
- أحداث أو خطط قديمة.

## الإدخال
- استيراد الصور بحسب تاريخها إلى Albums الشهرية القديمة.
- إنشاء Albums من بداية السنتين إلى الشهر الحالي.
- إضافة عدد مختار من Cards القديمة بدل نسخ كل المحادثات.
- إضافة الأغاني والأماكن والأفلام المهمة فقط.

## قاعدة مهمة
لا نحمّل كل شيء لمجرد وجوده. نختار الأشياء التي تعطي معنى للهدية.

**Deliverable:** عندما يفتح الشخص التطبيق لأول مرة يجد السنتين موجودتين بالفعل.

---

# المرحلة 10 — Privacy Hardening | 15–17 ديسمبر

- مراجعة Firebase Security Rules.
- اختبار حساب ثالث غير مصرح له.
- اختبار روابط الصور المباشرة.
- عدم تسجيل البيانات الحساسة في Logs.
- إزالة أي API keys غير مناسبة من الكود.
- Face ID / Touch ID App Lock إذا الوقت يسمح.
- Backup/restore test.
- مراجعة permissions للصور والإشعارات.

**Deliverable:** Privacy checklist كاملة ومختبرة.

---

# المرحلة 11 — Gift Polish | 18–20 ديسمبر

- الاسم النهائي.
- App Icon.
- Splash screen.
- Welcome message خاص بالسنتين.
- أول Morning Card مخصص.
- اختيار Cover لأهم Albums.
- Final animations/haptics.
- اختبار التطبيق على الجهازين الحقيقيين.

**Deliverable:** Gift-ready build بحلول 20 ديسمبر.

---

# Buffer | 21–31 ديسمبر

مسموح فقط:
- Bug fixes.
- تحسين أداء.
- تصحيح محتوى.
- تثبيت النسخة على الجهاز.
- Backup.

ممنوع:
- Feature كبيرة جديدة.
- تغيير قاعدة البيانات جذريًا.
- إعادة تصميم كاملة.

---

# Definition of Done

التطبيق يعتبر جاهزًا للهدية فقط إذا:
- شخصان فقط يستطيعان الدخول للمساحة.
- الصور والرسائل لا تظهر لأي حساب ثالث.
- Monthly Albums تعمل.
- Cards تعمل.
- Restaurants / Movies / Music / Plans تعمل.
- Notifications الأساسية تعمل.
- التطبيق لا ينهار أثناء الاستخدام العادي.
- محتوى السنتين تم إدخاله واختباره.
- توجد نسخة Backup قبل يوم الهدية.
