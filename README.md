# MALLIKA GROCERY STORE — Android billing app

This is an original, offline-first Progressive Web App (PWA) for a small grocery shop. It is inspired by common POS workflows, not a copy of BillingFast.

## Included
- Fast product search and bill/cart
- Product inventory with purchase cost, sale price, stock and optional barcode
- Stock auto-deduction after completed sale
- Daily sales, item-cost and estimated profit reports
- Simple non-GST receipts with Android print dialog / Save as PDF
- Camera barcode scan where the browser supports `BarcodeDetector`; manual barcode entry and Bluetooth scanners are fallbacks
- JSON backup/restore and sales CSV export
- English/Bengali labels in the workflow
- Offline cache after first load on a supported browser

## Important limitations
- Records are stored in the browser's local storage on this device, not in a cloud account. Clearing browser/app data can erase them. Export backups regularly and keep them somewhere safe.
- This folder is a web app package, not a signed APK. You can install it on Android from a secure HTTPS URL using Chrome's **Add to Home screen / Install app**. To make a standalone APK, package it with Android Studio/Capacitor and sign it; that extra build step is not included here.
- Camera barcode scanning needs HTTPS and browser support. If unavailable, type the barcode or use a Bluetooth scanner that behaves like a keyboard.
- Printing depends on Android print services and printer compatibility.
- Profit is an estimate based on the product cost saved at the time of sale, minus bill discount. It excludes expenses, spoilage, supplier credits and other accounting adjustments.
- This is not GST invoicing software. Check local tax/accounting requirements before relying on it for statutory records.

## Install on Android (no subscription required for this app)
1. Download and extract `mallika_grocery_store.zip` on a computer, or keep the extracted folder.
2. Upload `index.html`, `manifest.webmanifest`, and `sw.js` together to a static HTTPS host you control. A static host is sufficient; no database server or paid subscription is built into the app. Hosting provider terms may change.
3. Open the HTTPS URL in Chrome on your Android phone.
4. Open Chrome's menu (⋮), choose **Install app** or **Add to Home screen**, then confirm.
5. Open **Shop Settings** and set shop name, phone and address.
6. Open **Stock / পণ্য**, add each product with purchase cost, selling price, opening stock, unit and barcode if available.
7. Create a test sale, check the stock deduction and print/save a test receipt.
8. Open **Backup / ব্যাকআপ** and download a JSON backup. Repeat regularly; keep copies outside the phone.

## Quick local preview
Open `index.html` in a browser to test the interface. PWA installation, service-worker offline caching and camera access work best when served from HTTPS (or localhost for development).

## Backup safety
A restore operation replaces the current product and sales data. Export a backup before restoring. Do not rely on this app as the only copy of important shop records.
