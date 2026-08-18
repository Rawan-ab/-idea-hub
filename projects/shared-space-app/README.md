# Shared Space App

## الهدف
بناء تطبيق Flutter خاص بين شخصين فقط، يعمل بالدعوة، ويكون هدية جاهزة قبل 1 يناير 2027.

## الفكرة الأساسية
مساحة مشتركة خاصة تحتوي على صور، رسائل ونوت على شكل كروت، مطاعم، أفلام ومسلسلات، موسيقى، Wishlist، وذكريات. كل إضافة من أحد الطرفين تظهر للطرف الآخر، مع إشعارات وتقييمات وحالات مثل Visited وWatched.

## أهم المميزات
- Invite-only لشخصين.
- Home فيه For You للرسائل والكروت الجديدة.
- Our Photos تكون مكتبة ألبومات مشتركة، وليس مجرد Feed صور.
- إنشاء Albums حسب المناسبة أو الرحلة أو الفترة، مثل: Daily، Trips، Us، 2026، Weekend وغيرها.
- كل Album يظهر ككتاب/دفتر بصري يمكن التنقل بين صفحاته، مستوحى من مراجع الـscrapbook والـbookshelf.
- داخل الألبوم يمكن للطرفين إضافة صور، Caption، تاريخ، ونصوص/ملاحظات صغيرة، مع إمكانية ترتيب الصور على الصفحة بأسلوب scrapbook.
- الطرفان يستطيعان إضافة صور لنفس الألبوم، وأي إضافة جديدة تظهر للطرف الآخر.
- Notes / Messages ككروت شخصية، مع ردود و❤️.
- Open Later لرسائل تُفتح في تاريخ محدد.
- Restaurants: Want to visit → Visited → Rating + Would go again.
- Movies & Series: Want to watch → Watching → Watched → Rating.
- Music links وقوائم مشتركة.
- Clothes / Wishlist.
- Memories Timeline.
- Notifications عند إضافة محتوى جديد.
- Share to App: مشاركة رابط من TikTok / Instagram / X / YouTube / Spotify / Google Maps / Safari وحفظه تلقائيًا في القسم المناسب.

## اتجاه الصور والألبومات
قسم الصور يكون مثل Bookshelf / Album Library. كل ألبوم له Cover واسمه، وعند فتحه يتحول إلى صفحات تشبه كتاب صور أو scrapbook. الهدف أن الصور تكون تجربة مشتركة نرجع لها ونرتبها، وليس Gallery تقليدي فقط.

## اتجاه التصميم
خلفيات دافئة وCream، كروت Rounded، Gradients شفافة، تنظيم يشبه Library / Collections، رسائل ملونة، Notes مرنة تحتوي نصوص وصور وصوت، وذكريات بأسلوب Polaroid / Scrapbook. مراجع الألبومات الجديدة تعتمد أيضًا على عرض الألبومات ككتب وصفحات قابلة للتصفح.

## التقنية المقترحة
- Flutter
- Firebase Authentication
- Cloud Firestore
- Firebase Storage
- Firebase Cloud Messaging
- iOS Share Extension + Android Share Intent

## الإصدار الأول
التركيز على: Home، Photo Albums، Notes/Messages، Restaurants، Movies & Series، Memories، Notifications، Share Links.
