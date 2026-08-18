# Shared Space App

## الهدف
بناء تطبيق **iPhone فقط** باستخدام Flutter، خاص بين شخصين فقط، يعمل بالدعوة، ويكون هدية جاهزة قبل 1 يناير 2027.

## الفكرة الأساسية
مساحة مشتركة خاصة تحتوي على صور، رسائل ونوت على شكل كروت، مطاعم ومقاهي، أفلام ومسلسلات، موسيقى، خطط مشتركة، وذكريات. كل إضافة من أحد الطرفين تظهر للطرف الآخر، مع إشعارات وتقييمات وحالات مثل Visited وWatched.

## أهم المميزات
- Invite-only لشخصين.
- Home فيه For You للرسائل والكروت الجديدة.
- Our Photos تكون مكتبة ألبومات مشتركة، وليس مجرد Feed صور.
- التطبيق ينشئ ألبوم صور جديد تلقائيًا لكل شهر، مثل: August 2026، September 2026، October 2026.
- كل الصور التي يضيفها الطرفان خلال الشهر تحفظ تلقائيًا داخل ألبوم ذلك الشهر.
- يقدر الطرفان أيضًا إنشاء Albums إضافية يدويًا للمناسبات أو الرحلات.
- كل Album يظهر ككتاب/دفتر بصري يمكن التنقل بين صفحاته بأسلوب scrapbook.
- Notes / Messages تكون كروت مكدسة بصريًا، مع ردود و❤️.
- Open Later لرسائل تُفتح في تاريخ محدد.
- Morning Card تظهر مرة واحدة فقط صباحًا عند أول فتح يومي.
- Restaurants & Cafes: Want to visit → Visited → Rating + Would go again.
- Movies & Series: Want to watch → Watched → Rating.
- Music links وقوائم مشتركة.
- Shared Plans للأشياء والأنشطة التي نريد عملها معًا.
- Notifications عند إضافة محتوى جديد.
- Share to App من Safari / TikTok / Instagram / X / YouTube / Spotify / Google Maps عبر iOS Share Extension.

## اتجاه الصور والألبومات
قسم الصور يكون مثل Bookshelf / Album Library. كل شهر له ألبومه الخاص تلقائيًا. كل ألبوم له Cover واسم الشهر والسنة، وعند فتحه يتحول إلى صفحات تشبه كتاب صور أو scrapbook.

## اتجاه الرسائل والكروت
قسم الرسائل لا يكون Chat تقليدي. كل رسالة تظهر كـ Card مستقلة، بألوان مختلفة ومظهر يشبه القصاصات الورقية أو الكروت المطبوعة، ويمكن سحبها أو قلبها واحدة واحدة.

## اتجاه التصميم
خلفيات دافئة وCream، كروت Rounded، Gradients شفافة، تنظيم يشبه Library / Collections، رسائل ملونة على شكل stacked cards، وذكريات بأسلوب Polaroid / Scrapbook.

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
التركيز على: Home، Monthly Photo Albums، Notes/Messages Cards، Restaurants & Cafes، Movies & Series، Music، Shared Plans، Notifications، Share Links.
