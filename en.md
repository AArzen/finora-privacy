---
title: Finora – Privacy Policy
lang: en
permalink: /en
---

[Slovenščina](sl)

# Privacy Policy – Finora

Effective date: 18 November 2026

This privacy policy explains how the **Finora** app (Android and Windows) handles your data. The app is developed and published by Anže Arzenšek, an individual developer based in Slovenia ("the developer", "we").

## Summary

- Finora works without a server, without a user account and without ads.
- All your financial data is stored only on your device, in an encrypted database.
- The developer has no access to, and does not receive, your transactions, statements, accounts or settings.
- On Android the app does not have the internet permission, so it cannot send data anywhere by itself.
- Data leaves your device only when you choose so: when you save a backup or an export to a location you pick, or when you email us.

## 1. Data processed by the app on your device

Finora processes the data you enter or import yourself:

- imported bank statements (PDF, CSV, XLSX, camt.053) and the transactions read from them: date, amount, payee or payer, description, IBAN, balance;
- accounts, categories, categorisation rules, budgets, learned statement layouts and app settings;
- the lock PIN (stored only as a hash computed with Argon2id; the PIN itself is never stored).

This data is kept in the app's private storage, in a database encrypted with SQLCipher (AES-256). The database key is held by the operating system's secure storage (Android Keystore or Windows data protection). Automatic categorisation and detection of recurring payments run entirely on the device.

The app reads statement files when you import them; it keeps only the transactions and the data needed to recognise the same statement in the future.

**Biometrics.** If you enable fingerprint or face unlock, the check is performed by the operating system (Android BiometricPrompt or Windows Hello). Finora never sees or stores biometric data; it only receives a "success" or "failure" result from the system.

**Android backups.** Android's automatic backup (to Google Drive) is disabled for Finora, so app data is not copied to the cloud without your knowledge.

**Screenshots.** By default the app blocks screenshots and hides its content in the recent-apps overview. You can turn this off in Settings.

For this data the developer is not a controller within the meaning of the General Data Protection Regulation (GDPR), because we do not collect, receive or have access to it. You remain in control of it.

## 2. When data leaves the device by your choice

- **Backup.** When you create a backup, the app encrypts it (AES-256-GCM, key derived with Argon2id from your password or recovery key) and saves it to the location you choose in the system file picker (for example a folder on the device, a USB drive or a cloud service such as Google Drive). A file stored with a third party is subject to that service's terms. Without the password or recovery key nobody can read the backup – the developer cannot either.
- **CSV and PDF export.** Exported transactions and reports are not encrypted. You save the file where you choose and are responsible for it.
- **Sharing into Finora.** When you send a statement to Finora from another app ("Share", "Open with…"), Finora reads it only to import it.

## 3. Data the developer receives

### 3.1 Email (feedback and support)

The "Send feedback" button opens your email app with a draft message addressed to anze.ar@gmail.com. You send the message yourself and see its full content before sending. If the app adds technical details to the draft (such as the app and system version), you can remove them before sending.

When you write to us we receive your email address, your name (if your email client shows it) and the content of the message. We use them only to reply and to improve the app. The legal basis is our legitimate interest in answering your request (Art. 6(1)(f) GDPR). We keep messages as long as needed to handle them and delete them no later than 2 years after the last correspondence, or earlier on your request. Please do not include amounts, account numbers or other financial details in your message.

### 3.2 Crash and performance statistics (Android vitals)

If you have allowed your Android device to share usage and diagnostics data with Google, Google collects data about app crashes and freezes on your device (for example device model, Android version and the stack trace of a crash). In Google Play Console the developer sees this data **in aggregated form, without information that directly identifies you**, and uses it only to fix bugs. You manage this setting in your Android or Google settings, not in Finora. Google is the controller for this data (see section 4).


## 4. Google services

The Google Play version of the app uses the following Google services. Google processes the related data as an independent controller under its own privacy policy (<https://policies.google.com/privacy>); the developer does not receive this data except as described below.

- **Google Play (installation, updates, Android vitals).** Google processes the data needed to install and update apps and, depending on your settings, diagnostics data (section 3.2).
- **Play In-App Review.** The app may occasionally invite you to rate it. The dialog is shown by Google Play; your rating and comment go to Google, which publishes them in the store under its own rules. The developer sees public reviews like everyone else (during closed testing, reviews are visible only to the developer). You can delete your review in Google Play.
- **Play In-App Updates.** The app may ask Google Play whether a new version is available and offer you the update. Google Play uses device information, the app version and installed modules for this; the developer does not receive this data.

These services run through the Google Play Store app on your device; Finora itself does not open an internet connection.

## 5. What we do not do

- We do not show ads or use advertising identifiers.
- We do not use analytics or usage tracking.
- We do not sell or share data with third parties.
- We do not connect to your bank; transactions enter the app only from files you import yourself.
- We do not collect location, contacts, photos or other data from the device.

## 6. Retention and deletion

Data in the app stays on your device until you delete it:

- you can delete individual transactions, imports, accounts, categories and rules in the app (deleted transactions stay in the trash for 30 days and are then removed automatically);
- you can delete all data by uninstalling the app or in Android settings (Apps → Finora → Storage → Clear data);
- if you forget your PIN and do not have the recovery key, the app offers to erase all data.

Backups and exports you saved yourself must be deleted by you where you stored them. Because the developer does not hold your data, we cannot delete or restore it on your behalf.

## 7. Security

Data on the device is protected by the encrypted database, a PIN or biometric lock, automatic locking after inactivity and a limit on PIN attempts. Backups are encrypted. No system is perfectly secure; keeping your device secure (screen lock, system updates) is your responsibility.

## 8. Children

Finora is not intended for children under 15, and we do not knowingly collect data from them.

## 9. Your rights

For the data we receive (section 3) you have the right of access, rectification, erasure, restriction of processing, objection and data portability, and the right to withdraw consent at any time. Send requests to anze.ar@gmail.com; we reply within one month.

You can lodge a complaint with the supervisory authority: **Information Commissioner of the Republic of Slovenia** (Informacijski pooblaščenec), Dunajska cesta 22, 1000 Ljubljana, Slovenia, <https://www.ip-rs.si>.

## 10. Changes to this policy

We may update this policy, for example when new features are added. The new version will be published at this address with an updated date; for significant changes we will also mention it in the release notes.

## 11. Contact

Anže Arzenšek
Email: anze.ar@gmail.com
