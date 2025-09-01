# Hotel Booking Demand – Data Preprocessing
# Project Overview

#الهدف من المشروع هو تجهيز ومعالجة بيانات حجوزات الفنادق لتكون صالحة لبناء نماذج تنبؤية مستقبلًا.
#المشروع يمر بثلاث مراحل أساسية: EDA, Data Cleaning, و Feature Engineering & Preprocessing.

⚙️ Dataset

الملف المستخدم: hotel_bookings.csv

يحتوي على بيانات حجوزات لفندقين (City Hotel & Resort Hotel).

الأعمدة تشمل: تواريخ الحجز، معلومات العملاء، مدة الإقامة، عدد الأشخاص، طرق الدفع… إلخ.

# Phase 1 – Exploratory Data Analysis (EDA)

فحص البنية العامة للبيانات (.info(), .describe()).

تحليل missing values باستخدام جداول و visualizations.

اكتشاف outliers باستخدام boxplots و IQR.

كتابة Data Quality Report لتحديد الأعمدة التي تحتاج تنظيف.

# Phase 2 – Data Cleaning

معالجة الـ Missing Values:

company و agent → "None".

country → Mode أو "Unknown".

children → Median/Mode.

إزالة Duplicates.

معالجة Outliers (مثال: تحديد سقف لقيمة adr).

تحويل أنواع البيانات (مثل تحويل التواريخ لـ datetime).

# Phase 3 – Feature Engineering & Preprocessing

إنشاء Features جديدة:

total_guests = adults + children + babies.

total_nights = stays_in_weekend_nights + stays_in_week_nights.

is_family (حجز عائلي).

Encoding للمتغيرات التصنيفية:

One-Hot Encoding (للمتغيرات ذات الكارديناليتي المنخفضة).

Grouping rare categories كـ "Other".

إزالة الأعمدة المسربة للمعلومات:

reservation_status و reservation_status_date.

تقسيم البيانات إلى Train/Test split (80/20).

 Not Included (Out of Scope)

بناء النماذج التنبؤية.

Hyperparameter tuning.

Model evaluation.

📂 Project Structure
├── hotel_bookings.csv
├── notebook.ipynb   # يحتوي الكود والتحليلات
└── README.md        # وصف المشروع
