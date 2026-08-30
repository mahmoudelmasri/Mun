🛍️ Arabic POS & Inventory Management App

A modern Flutter-based Point of Sale (POS) and Inventory Management Application designed for small retail shops.

The application provides an easy Arabic RTL interface for managing products, stock, sales, invoices, prices, and profits.

📱 About The Application

This application helps shop owners manage their daily business from an Android phone.

It allows the owner to:

📦 Manage products and inventory
🛒 Create sales
💰 Manage wholesale and retail prices
🧾 Create invoices
📊 Track sales and profits
📈 View reports
⚠️ Monitor low-stock products
💾 Save data locally
📶 Work without an internet connection
✨ Features
🏠 Dashboard

The main dashboard displays:

Today's sales
Today's profit
Number of invoices
Number of products
Low-stock products
Total inventory value

Quick actions:

New Sale
Add Product
Inventory
Reports
📦 Product Management

Each product can contain:

Product name
Product image
Category
Current quantity
Purchase price
Wholesale price
Retail price
Minimum stock level
Barcode
Notes

Available actions:

Add product
Edit product
Delete product
Search products
Filter by category
Monitor stock levels
🛒 POS / Sales

The POS system allows the user to:

Search for a product
Add it to the cart
Choose wholesale or retail price
Select quantity
Edit the cart
Remove products
Complete the sale

After completing a sale, the application automatically:

Creates an invoice number
Saves the invoice
Saves date and time
Decreases inventory
Calculates profit
💵 Pricing System

Each product supports three prices:

Price	Description
Purchase Price	Cost of purchasing the product
Wholesale Price	Price for wholesale customers
Retail Price	Normal selling price

The user can select the appropriate price when creating a sale.

📊 Profit Calculation

Profit is calculated automatically.

Profit = Selling Price - Purchase Price

For multiple quantities:

Total Profit = (Selling Price - Purchase Price) × Quantity

The application provides:

Product profit
Invoice profit
Daily profit
Weekly profit
Monthly profit
📋 Inventory Management

The inventory section displays:

Product name
Current quantity
Purchase price
Inventory value
Stock status

Stock statuses:

🟢 Available
🟠 Low Stock
🔴 Out of Stock

The application automatically updates stock after every sale.

🧾 Invoices

Every completed sale generates an invoice containing:

Store name
Invoice number
Date
Time
Products
Quantities
Prices
Sale type
Total
Profit

Supported actions:

View invoice
Share invoice
Print invoice when supported
📜 Sales History

The application stores previous sales.

Users can view:

Invoice number
Date
Time
Total
Profit

Features:

Search invoices
Filter by date
View invoice details
📈 Reports

The reports section provides:

Daily sales
Weekly sales
Monthly sales
Total profit
Best-selling products
Low-stock products
Out-of-stock products
Total inventory value
🗂️ Categories

Users can create and manage product categories.

Example categories:

أدوات منزلية
بلاستيك
إكسسوارات موبايل
سماعات
شواحن
أخرى
⚙️ Settings

The settings section includes:

Store name
Phone number
Store address
Currency
Light mode
Dark mode
Stock settings
Backup
Restore
🌐 Offline Support

The application is designed as an offline-first application.

Core features work without an internet connection:

Product management
Sales
Inventory
Invoices
Reports

Data is stored locally and remains available after closing and reopening the application.

🛠️ Technology

The application is built using:

Flutter
Dart
Material Design
Local Database
RTL Arabic Support
📁 Project Structure
flutter_app/
│
├── android/
├── ios/
├── assets/
│
├── lib/
│   ├── core/
│   ├── data/
│   ├── models/
│   ├── services/
│   ├── presentation/
│   ├── widgets/
│   ├── routes/
│   ├── theme/
│   └── main.dart
│
├── pubspec.yaml
└── README.md
🚀 Installation
Requirements
Flutter SDK ^3.38.4
Dart SDK
Android Studio or VS Code
Android SDK
Flutter and Dart extensions
Install Dependencies
flutter pub get
Run Application
flutter run
📱 Build Android APK

For a release APK:

flutter build apk --release

The generated APK will normally be located in:

build/app/outputs/flutter-apk/app-release.apk
🔧 Development

Check the Flutter environment:

flutter doctor

Analyze the project:

flutter analyze

Format Dart code:

dart format .
🎨 Design

The application uses:

Modern Material UI
Arabic RTL layout
Responsive components
Light theme
Dark theme
Reusable widgets
Simple navigation

The goal is to provide a fast and easy POS experience for small shops.

🔐 Data

The application is designed to keep important business data stored locally.

Stored information includes:

Products
Categories
Inventory
Sales
Invoices
Settings
🗺️ Roadmap

Future improvements may include:

Barcode scanner

Bluetooth receipt printer

Product import/export

Excel export

PDF reports

Cloud backup

Multi-device synchronization

Multiple user accounts

Customer management

Supplier management

Expense management

Advanced analytics

👨‍💻 Project Status

Status: Active Development

The project is continuously being improved with new features, performance improvements, and bug fixes.

📄 License

This project is intended for personal and commercial development.

License information can be added here when the project is published.
