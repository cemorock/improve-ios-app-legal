# Privacy Policy — Improve: Budget, Habits & More
Version: 1.1 Effective date: 2026-08-12 Last updated: 2026-08-12

##  1. The short version
Improve: Budget, Habits & More is a free app made by one person. It has no servers, no user accounts, and no analytics or advertising SDKs.
* Everything you enter stays on your device, in the app's private storage.
* If you are signed in to iCloud, your data also syncs to your own private iCloud account so it is available on your other devices. It goes to Apple, not to me. Sync is always on and follows your system iCloud settings; there is no separate switch inside the app.
* I cannot see your habits, expenses, notes, or locations. There is no mechanism by which I could — I do not operate a backend, and Apple's private CloudKit database is not accessible to app developers.
* The only outbound network request the app makes on its own is to a public currency-exchange-rate service, to convert between currencies. It sends only currency codes — no amounts, no personal data.
The rest of this document explains that in detail, because some laws require it.

## 2. Who is responsible
The person responsible for this app (the "data controller" under the EU General Data Protection Regulation and the Swiss Federal Act on Data Protection) is:
Cedric Bauer Switzerland Email: support@cedric-bauer.ch
Referred to below as "I", "me", or "the developer".
I have not appointed a Data Protection Officer, and am not required to.

## 3. What this policy covers
This policy covers the Improve: Budget, Habits & More iOS application distributed through the Apple App Store and TestFlight.
It does not cover:
* Apple's own services — iCloud, the App Store, TestFlight, Sign in with Apple ID, and iOS itself. Those are governed by Apple's Privacy Policy.

## 4. What data the app handles
All of the following is data you create. None of it is collected from you, purchased, or inferred from other sources.
### 4.1 Habits
* Habit names, icons, and colors
* Start/stop timestamps and session durations
* Weekly and historical time totals
* To-do items, their text, and completion state
### 4.2 Budget
* Expense amounts, currencies, dates, and free-text descriptions
* Categories, projects, and per-category monthly budget limits
* Recurring-expense rules and schedules
* Optional: the approximate location where an expense was recorded, if you grant location access and enable location tagging. This is stored as coordinates on your device. Where a country is shown, it is worked out on your device from map boundary data bundled inside the App — coordinates are never sent to a geocoding or address-lookup service
* Your chosen base currency and the exchange rate applied at the time an expense was saved
### 4.3 Inactive features
The App contains dormant code for a nutrition-tracking feature that is not reachable in this version. It has no interface, creates no records, requests no permissions, and neither reads from nor writes to Apple Health. It is mentioned here only for completeness.
### 4.4 App settings and state
* Accent color, selected background image (a copy is stored inside the app's own storage), base currency
* Onboarding completion state and the version number of the Terms you accepted
* Notification and widget preferences
* Whether app lock is enabled, and after how long the app re-locks. This is a single on/off setting. No biometric information is stored with it.
### 4.5 What the app does not handle
The app does not ask for, and has no ability to obtain:
* Your name, email address, phone number, or date of birth
* Any bank, card, or payment credentials
* Contacts, calendars, photos other than a background image you explicitly pick, microphone, or camera. The optional app lock uses Face ID or Touch ID, but this does not give the App access to the camera — see Section 8.2.
* Health or fitness data from HealthKit
* Advertising identifiers (IDFA), device fingerprints, or any cross-app or cross-site tracking

## 5. Where your data is stored
### 5.1 On your device
Data is stored in a local database inside the app's sandboxed container, protected by iOS file-level encryption and your device passcode/biometrics. If you have a passcode set, the data is encrypted at rest while the device is locked.
### 5.2 In your iCloud account
Sync is always on in this version of the App. If you are signed in to iCloud on your device and have iCloud Drive enabled, the App syncs your data to the private database of your personal iCloud account using Apple's CloudKit.
If you are not signed in to iCloud, or you have turned iCloud off for this App in iOS Settings, everything stays on the device and nothing is sent anywhere.
Key points, stated precisely:
* The data is stored in your iCloud account, under your Apple Account. It counts against your iCloud storage quota.
* I have no access to it. Apple's private CloudKit database is scoped to the individual user; the developer of an app cannot read, export, or delete the contents of any user's private database.
* Apple encrypts this data in transit and at rest. If you have Advanced Data Protection enabled on your Apple Account, CloudKit app data is end-to-end encrypted and Apple does not hold the keys. If you do not have Advanced Data Protection enabled, Apple holds the encryption keys and can in principle access the data, including in response to a lawful request. This is a property of iCloud, not of this app.
* Apple may store iCloud data on servers in multiple countries, including outside Switzerland and the EU/EEA. See Apple's privacy documentation for details.
### 5.3 Turning iCloud sync off
Sync follows your system-level iCloud settings. To stop it:
Settings → [your name] → iCloud → Saved to iCloud / See All → [APP NAME] → turn off.
If you turn sync off, the app keeps working with the data already on that device. Changes made afterwards will not sync to your other devices, and already-synced data will remain in iCloud until you delete it.
Note: this app does not offer an in-app switch for iCloud sync. Sync is handled entirely through the system iCloud settings above. This is intentional — an in-app toggle that silently detached the local database from the sync container would be a reliable way to lose data.

## 6. What I actually receive
To be explicit about the small amount of information that does reach me:

| Source | What I get | When |
|---|---|---|
| App Store Connect | Aggregate, anonymised metrics: downloads, sessions, crashes, device/OS mix, country | Always, from Apple. No individual users identifiable. |
| Crash & performance logs | Diagnostic reports via Apple, only if you have enabled Settings → Privacy & Security → Analytics & Improvements → Share With App Developers | Only with your opt-in |
| TestFlight feedback | Your email address, screenshot, comment, and device details — only if you submit feedback from within TestFlight | Only when you send it |
| Support email | Whatever you choose to put in the message | Only when you write to me |
| App Store reviews | Your public review and nickname | Only when you post one |

I do not receive your habits, expenses, notes, locations, or any of the content described in Section 4 — ever, through any of the above.

## 7. Network requests and third parties
### 7.1 Exchange rates
For currency conversion, the app requests published reference exchange rates from the Frankfurter API (api.frankfurter.dev), a free, open-source service that republishes European Central Bank reference rates.
* What is sent: currency codes (for example CHF, EUR) and a date. Your device's IP address is visible to that service, as it is with any HTTP request.
* What is not sent: amounts, descriptions, categories, locations, device identifiers, or anything else about you or your expenses.
* Rates are cached on device so the app does not need to contact the service repeatedly.
* Rates are indicative reference rates, not the rate your bank or card issuer used. See the Terms.
### 7.2 Apple
The app relies on Apple's platform services: iCloud/CloudKit (sync), the App Store and TestFlight (distribution), local notifications, WidgetKit, Siri and Shortcuts via App Intents. Your relationship with Apple for these is governed by Apple's terms and privacy policy.
### 7.3 No reverse geocoding
The App does not send location coordinates to any geocoding or address- lookup service. Country names are determined on your device from map boundary data bundled inside the App.
Map views draw using Apple's map imagery. That involves requesting map tiles for the area you are looking at, which is a normal request to Apple; your stored expense records are not part of it.
### 7.4 What is not present
The app contains no third-party analytics SDK, crash reporter, advertising network, attribution/SDK tracker, social login, or AI/large-language-model service. Nothing you type is sent to any model for processing.

## 8. Permissions the app may request
Every one of these is optional. Denying any of them leaves the rest of the app functional; the specific feature is simply unavailable.

| Permission | Why | If you deny |
|---|---|---|
| Location (Always) | To tag an expense with the place it happened — including when an expense is logged automatically in the background, for example from a Shortcut, while the App is not open — and to show tagged expenses on a map | Expenses are saved without a location; the map shows only entries tagged previously |
| Photo Library | To let you choose a background image. A copy is stored in the app's own storage; the app does not scan, index, or upload your library | You keep the bundled backgrounds |
| Notifications | Reminders and confirmations for habits and expense logging | No reminders |
| Siri & Shortcuts | To run app actions from Shortcuts or Siri | Shortcuts integration is unavailable |
| Face ID / Touch ID | To unlock the App, if you turn on app lock | App lock stays off, or you unlock with your device passcode |

You can change any of these at any time in Settings → [APP NAME].
### 8.1 What "Always" location access does and does not mean
Because expenses can be logged automatically while the App is closed, the App asks for Always location access. iOS will occasionally remind you that the App has used your location in the background. To be clear about what is happening:
* The App reads your location only at the moment an expense record is created. Nothing else triggers a location read.
* It does not track your movements, does not monitor when you enter or leave places, and does not run continuously in the background.
* It keeps no location history beyond the individual points attached to expenses you saved. There is no trail, no timeline, and no background log.
* As stated in Section 7.3, those coordinates never leave your device for geocoding, and as stated in Section 5, they are stored only on your device and in your own iCloud account.
If you would rather the App only had location access while it is open, choose While Using the App in Settings → [APP NAME] → Location. Everything keeps working; expenses you log by hand are still tagged, and expenses logged automatically in the background are simply saved without a location.

### 8.2 App lock and biometrics

You can optionally require Face ID, Touch ID, or your device passcode to open
the App.

This uses Apple's system authentication. The App asks iOS to verify that it is
you, and iOS answers with nothing more than **yes or no**.

- Your face or fingerprint data never leaves the Secure Enclave on your device.
  It is not available to the App, is not stored by the App, and is not synced,
  transmitted, or shared with anyone.
- The App does not receive images, scans, templates, or any other biometric
  information — only the success or failure result.
- Turning app lock on or off changes nothing about how your data is stored or
  synced. It is a lock on the door of the App, not a change to the data behind
  it.
- If biometric authentication is unavailable or fails, you can unlock the App
  with your device passcode.

**What app lock does not cover.** Home screen widgets and notifications from
this App are drawn by iOS outside the App, and are not hidden by app lock. If
you would rather they did not show figures, remove the widget or turn off
notification previews in iOS Settings.

## 9. Legal bases for processing (GDPR Article 6)
Because the app processes your data locally and in your own iCloud account rather than on my infrastructure, my role as controller is limited. Where the GDPR applies, the bases are:
* Article 6(1)(b) — performance of a contract: processing your entries on your device is what the app is for and what you asked it to do.
* Article 6(1)(a) — consent: optional permissions (location, photo library, notifications), and opt-in sharing of crash diagnostics. Withdrawable at any time in iOS Settings, with no effect on prior processing.
* Article 6(1)(f) — legitimate interests: aggregate, non-identifying App Store metrics used to fix bugs and decide what to build. You can object using the contact address above.
Under the Swiss Federal Act on Data Protection (FADP/nFADP), processing of personal data by a private person is permitted subject to the principles of lawfulness, good faith, proportionality, purpose limitation, accuracy and security, which this app is designed around.

Biometric authentication does not create special category data processing under
GDPR Article 9. Biometric information is processed solely by your device's
operating system for the purpose of unlocking it; the App receives only a
success or failure result and at no point processes biometric data itself.

## 10. How long data is kept
* On your device: until you delete it in the app, or delete the app. Deleting the app removes its local database.
* In iCloud: until you delete it. Important — deleting the app does not delete your iCloud data. To remove it, go to Settings → [your name] → iCloud → Manage Account Storage → [APP NAME] → Delete Data, or disable iCloud for the app and delete the data there.
* Support emails: kept as long as needed to deal with the request, then deleted, typically within 12 months.
* TestFlight feedback: retained by Apple according to Apple's policies; I delete my copies once the underlying issue is resolved.
I do not hold backups of your content, because I never have your content.

## 11. Your rights
Under the GDPR and the Swiss FADP you have the right to access, rectify, erase, restrict, port, and object to the processing of your personal data.
In practice, for this app, you exercise all of these directly, yourself:
* Access and portability: your data is on your device and visible to you in the App at all times, and is included in your encrypted iOS device backup.
* Rectification: edit any entry in the app.
* Erasure: delete entries in the app, delete the app, and delete the iCloud data as described in Section 10.
* Objection / withdrawal of consent: revoke permissions in iOS Settings.
For the limited data I do hold (Section 6 — support correspondence, TestFlight feedback), write to support@cedric-bauer.ch and I will respond within one month.
You also have the right to lodge a complaint with a supervisory authority:
* Switzerland: Federal Data Protection and Information Commissioner (FDPIC), Feldeggweg 1, 3003 Bern — edoeb.admin.ch
* EU/EEA: the data protection authority in your country of residence.

## 12. Children
This app is not directed at children and does not knowingly process data from anyone under 13 years of age. It contains no advertising, no social features, no user-to-user communication, and no external links to user-generated content.
If you believe a child has used the app in a way that concerns you, note that all data is on that child's device and in that Apple Account; you can remove it using the steps in Section 10.

## 13. International transfers
I do not transfer your data anywhere, because I do not receive it. Transfers that do occur are between you and third parties:
* Apple/iCloud: Apple operates a global infrastructure and may process data outside Switzerland and the EEA, under its own safeguards.
* Frankfurter API: the request described in Section 7.1 reaches a server which may be located outside Switzerland and the EEA. It carries no personal data other than the IP address inherent to any internet request.

## 14. Security
* No central database exists, so there is no server for an attacker to breach.
* Local data is protected by the iOS sandbox and device encryption.
* Sync data is protected by Apple's iCloud security, including end-to-end encryption if you enable Advanced Data Protection.
* Network requests use HTTPS.
Your part: use a device passcode, keep iOS updated, and do not install the app on a jailbroken device. No system is perfectly secure, and I cannot guarantee the security of data outside my control.

## 15. Changes to this policy
If this policy changes materially, the version number and effective date at the top will change, and the app will show you the update the next time you open it. Older versions are available on request.

## 16. Contact
Cedric Bauer — support@cedric-bauer.ch
I read every message, but this is a free app maintained by one person in their own time. Please be patient with response times.


