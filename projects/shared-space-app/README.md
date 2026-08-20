# Shared Space App

## الهدف
بناء تطبيق **iPhone فقط** باستخدام Flutter، خاص بين شخصين فقط، يعمل بالدعوة، ويكون هدية جاهزة قبل 1 يناير 2027.

## الفكرة الأساسية
مساحة مشتركة خاصة بين شخصين لحفظ الخطط، مشاركة أجزاء من اليوم، والرجوع للأشياء التي نريد عملها أو فعلناها معًا. التطبيق ليس Chat ولا Social Network، بل مساحة منظمة تحفظ الأشياء التي عادة تضيع بين المحادثات والتطبيقات.

## أهم المميزات
- Invite-only لشخصين.
- Home بسيط يبدأ بالملفات الأساسية التي تقود لكل محتوى داخل التطبيق.
- Morning / Daily Message لا تكون Card ثابتة داخل الـHome؛ تظهر كتجربة منفصلة عند أول فتح مناسب ثم تختفي من الصفحة الرئيسية.
- Home يحتوي Shared Tasks / Reminders للأشياء التي نحتاج نذكر بعض فيها، مع إمكانية وضع ✓ عند الإنجاز.
- كل Task أو Reminder يمكن أن يكون له عنوان، ملاحظة، تاريخ اختياري، Added by، وحالة Open / Done.
- الطرفان يستطيعان إضافة Tasks وتحديثها، وأي تغيير يظهر للطرف الآخر.
- Our Photos تكون مكتبة ألبومات مشتركة، وليس مجرد Feed صور.
- التطبيق ينشئ ألبوم صور جديد تلقائيًا لكل شهر، مثل: August 2026، September 2026، October 2026.
- كل الصور التي يضيفها الطرفان خلال الشهر تحفظ تلقائيًا داخل ألبوم ذلك الشهر.
- يقدر الطرفان أيضًا إنشاء Albums إضافية يدويًا للمناسبات أو الرحلات.
- كل Album يظهر ككتاب/دفتر بصري يمكن التنقل بين صفحاته بأسلوب scrapbook، مع Templates مختلفة لكل صفحة بدل Grid صور تقليدي.
- Our Letters مكان لحفظ الكلام والمشاعر المهمة بين الطرفين، وليس Chat. الرسائل تظهر كأوراق/Letters متراكبة ويمكن إضافة Paper Styles وStamps وDecorations لاحقًا.
- Open Later لرسائل تُفتح في تاريخ محدد.
- Restaurants & Cafes: Want to visit → Visited → Rating + Would go again.
- Movies & Series: Want to watch → Watched → Rating.
- Music links وقوائم مشتركة.
- Shared Plans للأشياء والأنشطة التي نريد عملها معًا.
- Notifications عند إضافة محتوى جديد أو Task/Reminder.
- Share to App من Safari / TikTok / Instagram / X / YouTube / Spotify / Google Maps عبر iOS Share Extension.

## اتجاه الـHome
الـHome ليس Dashboard مزدحمًا ولا يحتوي على Daily Message ثابتة. الفكرة الحالية:
1. Header بسيط للمساحة المشتركة.
2. Files / Collections واضحة للوصول إلى: Photos، Our Letters، Places، Watch، Music، Plans.
3. Shared Tasks / Reminders section ظاهر في الصفحة الرئيسية للأشياء الجديدة أو القريبة.
4. كل Task فيه checkbox؛ عند الإنجاز يتحول إلى Done بدل أن يختفي مباشرة حتى يقدر الطرفان يشوفون أنه تم.
5. Daily / Morning Message تظهر كتجربة منفصلة عند أول فتح مناسب ثم يدخل المستخدم إلى Home العادي.

## اتجاه الصور والألبومات
قسم الصور يكون مثل Bookshelf / Album Library. كل شهر له ألبومه الخاص تلقائيًا. كل ألبوم له Cover واسم الشهر والسنة، وعند فتحه يتحول إلى صفحات تشبه كتاب صور أو scrapbook. الصفحات يمكن أن تحتوي صور، نصوص، تاريخ، اقتباس، sticker، screenshot، أو blocks أخرى حسب الـTemplate.

## اتجاه Our Letters
Our Letters مصممة لحفظ الكلام والمشاعر التي لا نريد أن تضيع في Chat أو Shared Notes. كل Letter تحفظ النص والتاريخ والمرسل بشكل مستقل، وتظهر كرسائل ورقية متراكبة. التصميم منفصل عن المحتوى حتى نقدر مستقبلًا نضيف Paper Templates، Stamps، Envelopes، Fonts وDecorations بدون التأثير على الرسائل القديمة. الحذف لا يكون مباشرًا؛ الاتجاه لاحقًا Archive / Trash / Restore.

## اتجاه التصميم
خلفيات دافئة وCream، Rounded Cards، Gradients شفافة، تنظيم يشبه Library / Collections، Letters بشكل ورقي، وذكريات بأسلوب Polaroid / Scrapbook. Flutter هو مكان التصميم الأساسي، وFigma يستخدم عند الحاجة لعناصر رسومية خاصة مثل stamps أو stickers أو illustrations.

## التقنية المقترحة
- Flutter — iOS target only
- Xcode
- Firebase Authentication
- Cloud Firestore
- Firebase Storage
- Firebase Cloud Messaging / APNs
- iOS Share Extension
- Face ID App Lock لاحقًا إذا الوقت يسمح

## الإصدار الأول
التركيز على: Home Files، Shared Tasks / Reminders، Monthly Scrapbook Albums، Our Letters، Restaurants & Cafes، Movies & Series، Music، Shared Plans، Notifications، Share Links.
