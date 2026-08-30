# BUILD SPECIFICATION — Arabic POS & Inventory App

## IMPORTANT — READ BEFORE BUILDING

Build a complete, functional Flutter Android application based on this specification.

This is a real POS and Inventory Management application for a retail shop.

Do NOT create a simple demo, mockup, static UI, or fake prototype.

All buttons, screens, navigation, database operations, calculations, inventory updates, sales, invoices, and reports must actually work.

---

# 1. APP INFORMATION

**Application Name:** متجري

**Application Type:** POS + Inventory Management

**Platform:** Android

**Framework:** Flutter + Dart

**Flutter Version:** ^3.38.4

**Language:** Arabic

**Layout:** RTL

**Design:** Modern Material 3

**Storage:** Local persistent database

**Internet:** The core application must work completely offline.

---

# 2. MAIN PURPOSE

Create an application that allows a shop owner to manage the entire shop from an Android phone.

The application must manage:

* Products
* Categories
* Inventory
* Purchases
* Sales
* Wholesale prices
* Retail prices
* Invoices
* Profits
* Reports
* Store settings

Example products:

* أدوات منزلية
* أدوات مطبخ
* أكواب بلاستيك
* مواد تنظيف
* أكياس نفايات
* سلال
* أغطية هواتف
* سماعات
* Earphones
* Speakers
* Chargers
* Cables
* Any other products

---

# 3. DASHBOARD

Create a professional Arabic dashboard.

Display:

* مبيعات اليوم
* أرباح اليوم
* عدد الفواتير
* عدد المنتجات
* المنتجات منخفضة المخزون
* المنتجات النافدة
* قيمة المخزون

Quick action buttons:

* بيع جديد
* إضافة منتج
* إضافة مخزون
* التقارير

All dashboard numbers must come from the real database.

Do NOT use fake numbers.

---

# 4. PRODUCTS

Create a complete product management system.

Each product must contain:

* ID
* اسم المنتج
* صورة اختيارية
* التصنيف
* الكمية الحالية
* سعر الشراء
* سعر الجملة
* سعر المفرق
* الحد الأدنى للمخزون
* باركود اختياري
* ملاحظات
* تاريخ الإضافة
* تاريخ آخر تعديل

Functions:

* إضافة منتج
* تعديل منتج
* حذف منتج
* البحث عن منتج
* عرض تفاصيل المنتج
* إضافة كمية
* تعديل المخزون
* فلترة حسب التصنيف

Before deleting a product, show a confirmation dialog.

---

# 5. CATEGORIES

Create category management.

Functions:

* إضافة تصنيف
* تعديل تصنيف
* حذف تصنيف

Default categories:

* أدوات منزلية
* أدوات مطبخ
* بلاستيك
* مواد تنظيف
* إكسسوارات موبايل
* سماعات
* شواحن
* كابلات
* أخرى

---

# 6. INVENTORY

Create a complete inventory screen.

Display:

* اسم المنتج
* الكمية
* سعر الشراء
* قيمة المخزون
* حالة المخزون

Calculate inventory value:

Quantity × Purchase Price

Stock status:

* إذا كانت الكمية = 0 → نفد المخزون
* إذا كانت الكمية أقل أو تساوي الحد الأدنى → مخزون منخفض
* إذا كانت الكمية أعلى من الحد الأدنى → متوفر

Do not allow negative stock by default.

---

# 7. ADD STOCK

Allow the owner to add stock to existing products.

Form:

* المنتج
* الكمية
* سعر الشراء
* التاريخ
* ملاحظات

When stock is added:

New Quantity = Old Quantity + Added Quantity

Save the stock movement in the database.

---

# 8. POS — NEW SALE

Create a fast professional POS screen.

The user must be able to:

1. Search for a product.
2. Select a product.
3. Add it to the cart.
4. Select quantity.
5. Select sale type.
6. Change quantity.
7. Remove products.
8. Complete the sale.

Sale types:

* جملة
* مفرق

If the user chooses جملة:

Use the wholesale price.

If the user chooses مفرق:

Use the retail price.

---

# 9. CART

The cart must display:

* اسم المنتج
* الكمية
* سعر الوحدة
* نوع السعر
* مجموع المنتج

Calculate:

Item Total = Unit Price × Quantity

Invoice Total = Sum of all Item Totals

Allow:

* زيادة الكمية
* تخفيض الكمية
* حذف المنتج

---

# 10. STOCK VALIDATION

Before completing a sale:

Check the available quantity.

If requested quantity is greater than available quantity, show:

"الكمية المطلوبة غير متوفرة في المخزون"

Do not complete the sale.

Never allow negative stock unless the owner explicitly enables it in Settings.

---

# 11. COMPLETE SALE

When the owner confirms a sale:

1. Validate the cart.
2. Validate stock.
3. Generate a unique invoice number.
4. Save the invoice.
5. Save invoice items.
6. Calculate profit.
7. Decrease stock automatically.
8. Save date and time.
9. Clear the cart.
10. Show a success message.
11. Open the invoice.

Success message:

"تمت عملية البيع بنجاح"

---

# 12. PROFIT CALCULATION

For every product:

Profit = Selling Price - Purchase Price

For multiple quantities:

Total Profit = (Selling Price - Purchase Price) × Quantity

Invoice Profit = Sum of all item profits

The application must use the purchase price that existed at the time of the sale.

Display:

* ربح المنتج
* ربح الفاتورة
* أرباح اليوم
* أرباح الأسبوع
* أرباح الشهر

---

# 13. INVOICES

Every completed sale must generate an invoice.

Invoice contains:

* اسم المتجر
* رقم الفاتورة
* التاريخ
* الوقت
* المنتجات
* الكميات
* سعر الوحدة
* نوع البيع
* الإجمالي
* الربح

Example:

فاتورة رقم: INV-000001

المنتج | الكمية | السعر | المجموع

Then:

الإجمالي

الربح

Provide:

* عرض الفاتورة
* مشاركة الفاتورة
* طباعة الفاتورة إذا كانت مدعومة

---

# 14. SALES HISTORY

Create a complete sales history.

Display:

* رقم الفاتورة
* التاريخ
* الوقت
* الإجمالي
* الربح

Functions:

* البحث
* فلترة حسب التاريخ
* فتح الفاتورة
* عرض تفاصيل الفاتورة

---

# 15. REPORTS

Create a professional reports section.

Daily report:

* مبيعات اليوم
* أرباح اليوم
* عدد الفواتير

Weekly report:

* إجمالي المبيعات
* إجمالي الأرباح

Monthly report:

* إجمالي المبيعات
* إجمالي الأرباح

Product reports:

* أكثر المنتجات مبيعًا
* المنتجات منخفضة المخزون
* المنتجات النافدة

Inventory report:

* إجمالي قيمة المخزون

Charts must use real database data.

---

# 16. SEARCH

Implement fast product search.

Search by:

* اسم المنتج
* الباركود إذا كان موجودًا

Search results should update immediately.

---

# 17. SETTINGS

Create an Arabic Settings screen.

Options:

* اسم المتجر
* رقم الهاتف
* عنوان المتجر
* العملة
* الوضع الليلي
* الوضع النهاري
* السماح بالمخزون السالب
* النسخ الاحتياطي
* استعادة البيانات

Settings must be saved permanently.

---

# 18. CURRENCY

The currency must be configurable.

Default:

USD

Allow examples:

* USD
* LBP
* $

Do not hard-code the currency throughout the application.

---

# 19. BACKUP & RESTORE

Implement local backup and restore.

Backup must include:

* Products
* Categories
* Inventory
* Stock movements
* Sales
* Invoices
* Settings

The user must be able to restore the data later.

---

# 20. OFFLINE MODE

The application must work without internet.

These features must work offline:

* Products
* Categories
* Inventory
* Stock
* Sales
* POS
* Invoices
* Reports
* Settings

Internet must NOT be required for normal POS operation.

---

# 21. DATABASE

Use a real persistent local database.

Recommended:

* SQLite
  OR
* Hive

Choose the most reliable option for the project.

Do NOT use:

* Temporary variables
* Fake JSON data
* Hard-coded sales
* Hard-coded reports

All important information must be stored persistently.

---

# 22. NAVIGATION

Use a bottom navigation bar.

Tabs:

1. الرئيسية
2. البيع
3. المنتجات
4. المخزون
5. التقارير

Settings should be accessible from the main dashboard.

---

# 23. UI / UX

Create a professional commercial POS interface.

Requirements:

* Arabic RTL
* Material 3
* Modern design
* Clean cards
* Rounded components
* Clear icons
* Large touch buttons
* Search bars
* Professional forms
* Confirmation dialogs
* Success messages
* Error messages
* Empty states
* Loading states
* Responsive layouts

The app must be easy to use with one hand on an Android phone.

---

# 24. THEMES

Support:

* Light Mode
* Dark Mode

Use Flutter ThemeData and ColorScheme.

Do not hard-code colors unnecessarily.

---

# 25. RESPONSIVE DESIGN

The application must work correctly on different Android screen sizes.

Avoid fixed dimensions that cause overflow.

Use responsive Flutter layouts.

---

# 26. PROJECT STRUCTURE

Use a clean structure:

lib/
├── core/
├── data/
│   ├── database/
│   └── repositories/
├── models/
├── services/
├── presentation/
│   ├── dashboard/
│   ├── pos/
│   ├── products/
│   ├── inventory/
│   ├── sales/
│   ├── reports/
│   └── settings/
├── widgets/
├── routes/
├── theme/
└── main.dart

Use reusable widgets.

Keep business logic separated from UI.

---

# 27. ERROR HANDLING

Handle:

* Empty product names
* Invalid prices
* Invalid quantities
* Missing categories
* Insufficient stock
* Database errors
* Backup errors
* Restore errors

All error messages should be clear and Arabic.

---

# 28. IMPORTANT — NO FAKE FUNCTIONALITY

Do NOT create:

* Fake buttons
* Fake reports
* Fake sales
* Fake inventory
* Fake database
* Placeholder screens
* TODO functionality

Every button must actually work.

Every displayed number must come from real stored data.

Every screen must be connected to the application logic and database.

---

# 29. TESTING

After building the application, test the following:

### Product Test

Add a product.

Close the app.

Open the app again.

The product must still exist.

### Stock Test

Add 10 units.

Confirm inventory becomes 10.

### Sales Test

Sell 3 units.

Inventory must become 7.

### Profit Test

Purchase price = 5

Selling price = 8

Quantity = 3

Expected profit:

(8 - 5) × 3 = 9

### Invoice Test

Complete a sale.

Confirm that a unique invoice is created and saved.

### History Test

Open sales history.

Confirm the invoice appears.

### Reports Test

Open reports.

Confirm the report uses the actual stored sale.

---

# 30. BUILD REQUIREMENTS

The project must support:

flutter pub get

flutter analyze

flutter run

flutter build apk --release

Fix all Flutter and Dart compilation errors before considering the application complete.

---

# 31. FINAL REQUIREMENT

Build the complete application from this specification.

The final application must include:

**Dashboard + Products + Categories + Inventory + Stock Management + POS + Sales + Invoices + Profit Calculation + Sales History + Reports + Settings + Backup + Restore + Offline Database + Arabic RTL**

The result must be a real, functional Android Flutter application suitable for daily use in a small retail shop.

Do not stop at the UI.

Implement the complete functionality.
