# راهنمای استایل‌دهی جوپیتر نوت‌بوک برای تدریس‌یارها

## مقدمه
این داکیومنت راهنمای کاملی برای تدریس‌یارهای درس برنامه‌سازی پیشرفته است که نحوه استفاده از کلاس‌های CSS موجود در فایل `style.css` برای ایجاد اسلایدهای یکپارچه و زیبا در جوپیتر نوت‌بوک را شرح می‌دهد.

---

## 🎯 اصول کلی

### 1. ساختار پایه هر سلول
```html
<link rel="stylesheet" href="style.css">
<div class="[نوع-کارت]" dir="rtl">
  <!-- محتوای شما -->
</div>
```

**⚠️ نکات مهم:**
- همیشه `<link rel="stylesheet" href="style.css">` را در ابتدای هر سلول قرار دهید
- `dir="rtl"` برای متن‌های فارسی الزامی است
- هر محتوا باید داخل یک `div` با کلاس مناسب قرار گیرد

---

## 🎨 انواع کارت‌ها و کاربردهای آن‌ها

### 1. کارت جلد (Cover Card)
**کاربرد:** صفحه اول هر جلسه
```html
<link rel="stylesheet" href="style.css">
<div class="card cover-card" dir="rtl">
    <p class="pretitle">به نام خدا</p>
    <div class="brand-center">
      <img src="img/Sbu-logo.png" alt="SBU Logo" class="logo" />
    </div>
    <h1 class="title">عنوان درس</h1>
    <p class="inst">دانشگاه شهید بهشتی · دانشکده مهندسی کامپیوتر</p>
    <p class="inst">دکتر مجتبی وحیدی اصل</p>
    <hr class="divider" />
    <h3>موضوع جلسه</h3>
    <div class="authors">نام تدریس‌یار</div>
</div>
```

**اجزای کلیدی:**
- `pretitle`: برای "به نام خدا"
- `brand-center` + `logo`: برای لوگوی دانشگاه
- `title`: عنوان اصلی درس
- `inst`: اطلاعات دانشگاه و استاد
- `authors`: نام تدریس‌یار

### 2. کارت معمولی (Standard Card)
**کاربرد:** محتوای اصلی درس
```html
<link rel="stylesheet" href="style.css">
<div class="card" dir="rtl">
  <h2>عنوان بخش</h2>
  <p>متن توضیحی...</p>
  <ul>
    <li>نکته اول</li>
    <li>نکته دوم</li>
  </ul>
</div>
```

### 3. کارت پررنگ (Bold Card)
**کاربرد:** فهرست مطالب یا نکات مهم
```html
<link rel="stylesheet" href="style.css">
<div class="card bold" dir="rtl">
  <h2>فهرست مطالب</h2>
  <ol>
    <li>بخش اول</li>
    <li>بخش دوم</li>
  </ol>
</div>
```

---

## 📝 سلسله‌مراتب عناوین

### استفاده از عناوین
```html
<h1>عنوان اصلی (فقط در کارت جلد)</h1>
<h2>عنوان بخش اصلی</h2>
<h3>زیرعنوان</h3>
<h4>عنوان فرعی (در صورت نیاز)</h4>
```

**رنگ‌بندی خودکار:**
- `h1`: گرادیان آبی-سبز
- `h2` و `h3`: قرمز (#dc2626)
- همه عناوین وسط‌چین هستند

---

## 🖼️ نمایش تصاویر

### تصاویر معمولی
```html
<div class="images">
  <img src="img/java.svg" alt="Java Logo" />
  <img src="img/flutter.jpg" alt="Flutter Logo" />
</div>
```
- ارتفاع: 170px
- نمایش در کنار هم با فاصله مناسب

### تصاویر بزرگ
```html
<div class="images-big">
  <img src="img/TIOBE.png" alt="TIOBE Index" />
</div>
```
- ارتفاع: 300px
- برای نمودارها و تصاویر مهم

---

## 💡 اجزای تکمیلی

### نکته‌های ویژه (Slide Notes)
```html
<div class="slide-note">
  <strong>نکته مهم:</strong> این یک نکته ویژه است که باید به آن توجه کرد.
</div>
```
- پس‌زمینه خاکستری روشن
- حاشیه نقطه‌چین
- برای تأکید بر نکات مهم

### جداکننده
```html
<hr class="divider" />
```
- خط گرادیان آبی-سبز
- برای جدا کردن بخش‌های مختلف

---

## 🎨 استایل‌دهی متن

### تأکید و رنگ‌ها
```html
<p>متن معمولی با <strong>تأکید آبی</strong> و <em>متن خاکستری</em></p>
<p>کد: <code>System.out.println()</code></p>
<a href="mailto:example@sbu.ac.ir">لینک آبی</a>
```

**رنگ‌بندی خودکار:**
- `strong`: آبی (#1d4ed8)
- `em`: خاکستری (#374151)
- `code`: LTR با پس‌زمینه
- `a`: آبی با hover effect

---

## 📋 فهرست‌ها

### فهرست نقطه‌ای
```html
<ul>
  <li>مورد اول</li>
  <li>مورد دوم</li>
</ul>
```

### فهرست شماره‌دار
```html
<ol>
  <li>گام اول</li>
  <li>گام دوم</li>
</ol>
```

**نکات:**
- فاصله‌گذاری خودکار
- تراز راست برای متن فارسی
- رنگ یکپارچه با بقیه متن

---

## 🎯 الگوهای رایج

### 1. اسلاید معرفی مفهوم
```html
<link rel="stylesheet" href="style.css">
<div class="card" dir="rtl">
  <h2>نام مفهوم</h2>
  <p>توضیح کلی مفهوم...</p>
  <ul>
    <li>ویژگی اول</li>
    <li>ویژگی دوم</li>
  </ul>
  <div class="images">
    <img src="img/concept.png" alt="مفهوم" />
  </div>
</div>
```

### 2. اسلاید مقایسه
```html
<link rel="stylesheet" href="style.css">
<div class="card" dir="rtl">
  <h2>مقایسه A و B</h2>
  <div class="images">
    <img src="img/option-a.png" alt="گزینه A" />
    <img src="img/option-b.png" alt="گزینه B" />
  </div>
  <div class="slide-note">
    <strong>نتیجه:</strong> گزینه A برای... مناسب‌تر است.
  </div>
</div>
```

### 3. اسلاید نمودار
```html
<link rel="stylesheet" href="style.css">
<div class="card" dir="rtl">
  <h3>آمار و ارقام</h3>
  <p>توضیح مختصر نمودار...</p>
  <hr class="divider" />
  <div class="images-big">
    <img src="img/chart.png" alt="نمودار" />
  </div>
</div>
```

---

## ⚠️ نکات مهم و بهترین شیوه‌ها

### ✅ کارهای درست
1. **همیشه CSS را لینک کنید**
2. **از `dir="rtl"` استفاده کنید**
3. **عناوین را سلسله‌مراتبی بنویسید**
4. **تصاویر را با alt مناسب قرار دهید**
5. **از کلاس‌های موجود استفاده کنید**

### ❌ کارهای نادرست
1. **استایل inline اضافه نکنید** (مگر موارد خاص)
2. **فونت‌های جدید تعریف نکنید**
3. **رنگ‌های سفارشی استفاده نکنید**
4. **ساختار HTML را تغییر ندهید**
5. **از کلاس‌های غیراستاندارد استفاده نکنید**

---

## 🚀 نمونه اسلاید کامل

```html
<link rel="stylesheet" href="style.css">
<div class="card" dir="rtl">
  <h2>آرایه‌ها در جاوا</h2>
  
  <p>
    <strong>آرایه</strong> مجموعه‌ای از عناصر هم‌نوع است که در حافظه به صورت 
    پیوسته ذخیره می‌شوند. در جاوا، آرایه‌ها <em>Reference Type</em> هستند.
  </p>
  
  <h3>انواع آرایه</h3>
  <ul>
    <li><strong>آرایه یک‌بعدی:</strong> <code>int[] numbers = new int[5];</code></li>
    <li><strong>آرایه چندبعدی:</strong> <code>int[][] matrix = new int[3][3];</code></li>
  </ul>
  
  <div class="images">
    <img src="img/array-1d.png" alt="آرایه یک‌بعدی" />
    <img src="img/array-2d.png" alt="آرایه دوبعدی" />
  </div>
  
  <div class="slide-note">
    <strong>نکته:</strong> اندیس آرایه‌ها در جاوا از صفر شروع می‌شود.
  </div>
  
  <hr class="divider" />
</div>
```

---

## 🎨 تنظیمات پیشرفته

### کارت‌های سفارشی (در موارد خاص)
```html
<div class="card" dir="rtl" style="background: #f9fafb; border: 2px solid #059669;">
  <h3 style="color: #047857;">عنوان ویژه</h3>
  <!-- محتوا -->
</div>
```

**⚠️ فقط در موارد خاص استفاده کنید!**

---

## 📞 راهنمایی و پشتیبانی

اگر سوالی دارید یا نیاز به کمک دارید:
1. ابتدا این داکیومنت را کامل مطالعه کنید
2. نمونه‌های موجود در فایل اصلی را بررسی کنید
3. در صورت نیاز با استاد درس تماس بگیرید

---

## 🏁 چک‌لیست نهایی

قبل از ارسال فایل جوپیتر:
- [ ] همه سلول‌ها CSS لینک دارند
- [ ] تمام محتوا داخل کارت‌های مناسب است
- [ ] عناوین سلسله‌مراتبی هستند
- [ ] تصاویر alt text دارند
- [ ] متن‌های فارسی RTL هستند
- [ ] استایل‌های inline غیرضروری حذف شده‌اند
- [ ] فایل در مرورگر تست شده است

---

**موفق باشید! 🎓**
