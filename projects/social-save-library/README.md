# Social Save Library

## الهدف
تطبيق شخصي يجمع الروابط والمحفوظات من TikTok وInstagram وX وغيرها في مكان واحد منظم بدل تشتتها بين Saved وBookmarks.

## الفكرة الأساسية
المستخدم يضغط Share من أي تطبيق ثم يختار التطبيق. يتم حفظ الرابط مع المصدر والصورة المصغرة والعنوان/الوصف والتاريخ، ثم يُصنف إلى القسم المناسب تلقائيًا أو يدويًا.

## التصنيفات المقترحة
- Restaurants
- Travel
- Clothes
- Products
- Learning
- Ideas
- Videos
- Articles
- Recipes
- Other / Inbox

## أهم المميزات
- Share → Save to App.
- Inbox للعناصر غير المصنفة.
- Auto classification حسب الرابط والمحتوى.
- Search and filters.
- Favorites.
- Seen / Done.
- Archive / Delete.
- فتح المنشور الأصلي.
- Collections مخصصة لاحقًا.
- AI classification وبحث طبيعي لاحقًا.

## التقنية المقترحة
- Flutter
- Supabase + PostgreSQL
- Python + FastAPI لجلب Metadata والتصنيف
- iOS Share Extension + Android Share Intent
- AI classification في مرحلة لاحقة

## النسخة الأولى
التركيز على استقبال الرابط، حفظ Metadata، التصنيف، Inbox، البحث والفلاتر، وفتح الرابط الأصلي.
