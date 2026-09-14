# MFK — موقع ذكاء اصطناعي

## خطوات الرفع على Vercel

### 1. جهّز مفتاح API
- روح إلى console.anthropic.com
- سجّل حساب واعمل مفتاح API جديد (API Key)
- خله عندك جاهز، بتحتاجه بالخطوة 4

### 2. ارفع المشروع على GitHub
- سوّي مستودع (repository) جديد على GitHub
- ارفع فيه كل ملفات هذا المجلد (index.html, api/chat.js, package.json)

### 3. اربط المشروع بـ Vercel
- روح إلى vercel.com وسجّل دخول (تقدر تسجل بحساب GitHub)
- اضغط "Add New Project"
- اختر المستودع اللي رفعته
- اضغط Deploy (الإعدادات الافتراضية تكفي، لأن Vercel يكتشف مجلد `api` تلقائيًا)

### 4. أضف المفتاح كمتغيّر بيئة (Environment Variable)
- من داخل صفحة المشروع في Vercel، روح لـ Settings → Environment Variables
- أضف متغيّر باسم: `ANTHROPIC_API_KEY`
- والقيمة: المفتاح اللي جهزته بالخطوة 1
- احفظ، وبعدين اعمل Redeploy للمشروع من تبويب Deployments

### 5. خلاص
بعد الـ Redeploy بيعطيك Vercel رابط زي:
`https://mfk-ai-chat.vercel.app`

افتحه من أي جهاز أو متصفح، ويشتغل مباشرة — ما يظهر فيه أي ذكر لـ Claude أو Anthropic.

---

## ملاحظات
- كل سؤال يرسل يكلفك حسب استخدام API (حسب تسعير Anthropic)، فراقب الاستهلاك من console.anthropic.com
- لو تبي تغيّر الاسم أو الألوان، عدّل ملف `index.html`
- الموقع ما يخزن المحادثات، كل مرة تفتح الصفحة تبدأ محادثة جديدة
