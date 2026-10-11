---
title: Onhaven Privacy Policy
---

# Onhaven Privacy Policy

**Privacy Policy** · [Support](/onhaven-legal/support/) · [User Guide](/onhaven-legal/guide/)

**English** · [繁體中文](/onhaven-legal/zh/)

**Last updated:** November 9, 2026

## 1. Introduction

Onhaven is a personal and family finance app for iPhone developed by **Chen Chao Yu** ("we", "us", "our"). It brings your investments, income, spending, and retirement goals together, and evaluates your financial health.

Onhaven is built on one principle: **your financial records stay on your device.** You can use the whole app without an account. The optional family sync feature is end-to-end encrypted, so our server only ever holds data it cannot read.

This policy explains what leaves your device, where it goes, and what we deliberately never collect.

## 2. Data Stored Only on Your Device

Everything you record in Onhaven is stored in a local database on your iPhone:

- Holdings, transactions, and investment accounts
- Income, expenses, bank and card transactions
- Family status (number of adults, children, elders; the primary earner's age), family members, and goals
- Imported statement data, exchange rates, and app settings

If you don't use family sync, **none of this is sent to our server.** Uninstalling the app deletes it.

Secrets such as your family key, device key, and any API keys you enter (for example a Solana RPC or Jupiter key) are stored in the iOS Keychain, on this device only.

## 3. Data We Store on Our Server (Only If You Sign In)

Signing in is optional and is only needed for family sync, which keeps the records of several family members' devices in sync.

### 3.1 Account

- **Apple user ID**: the identifier *Sign in with Apple* gives us, used to recognize your account.
- **Email address**: shared by Apple when you first sign in. This may be a private relay address you chose. We use it only to recognize you if you contact support. We never use it for marketing.

### 3.2 Devices and Family

- **Device type** (always "iPhone/iPad" or "Mac", not the name you gave your device in iOS Settings) and a **device public key**, generated on the device. The private key never leaves it.
- **Family name** (the name you enter when creating the family, stored in plain text), membership, and each member's role (owner or member). Your household profile, family member details, and goals are synced records and are encrypted as described in Section 3.3.
- **Pending invites.** These hold a hash of the invite token, and the family key encrypted to the joining device. The one-time secret that unlocks an invite exists only in the QR code or invite code shown on screen. It is never sent to our server.
- **Sync access.** The date each device's automatic sync is unlocked until, a record of each rewarded ad that unlocked sync, and your Onhaven Pro expiry date.

### 3.3 Synced Records — End-to-End Encrypted

- Every record you sync is encrypted on your device with your family's key, using AES-GCM. **Our server stores only the ciphertext.** It also keeps the record's type, a version number, and when it was last updated.
- The family key is created on a family device and passed directly between devices by QR code. **We never have it, and we cannot decrypt your records.** For the same reason, we cannot recover your data if every family device and your recovery key are lost.

## 4. Data Sent to Third Parties to Make Features Work

Some features need data from the internet. In each case we send the minimum needed, and never your amounts, balances, or holdings:

| Feature | Sent to | What is sent |
|---|---|---|
| Stock prices and price history | Yahoo Finance (`query1.finance.yahoo.com`), Taiwan Stock Exchange (`mis.twse.com.tw`) | Ticker symbols only |
| Exchange rates | ExchangeRate-API (`open.er-api.com`) | Nothing about you; rates are only downloaded |
| Crypto wallet tracking (optional) | Solana RPC (public, or one you choose such as Helius), Jupiter API | Your wallet's **public** address |
| Statement reading, category suggestions, and AI analysis (when the cloud model is used) | Apple Private Cloud Compute | The statement pages, transaction descriptions, or financial figures being processed |

**Apple Intelligence.** Onhaven uses Apple Intelligence in three places:

- **Reading brokerage and card statements.** This uses Apple's *Private Cloud Compute* when your device supports it, because statements are often too long for the on-device model. Otherwise it uses the on-device model.
- **Suggesting categories for bank transactions.** When Private Cloud Compute is used, only the descriptions of uncategorized rows are sent, with account and reference numbers removed.
- **AI analysis on the Evaluate tab.** This runs on your device unless you turn on **Use the Larger Cloud Model** yourself.

Data sent to Private Cloud Compute leaves your device. Apple processes it in a verifiable private environment and does not retain it. Each of these screens tells you whether the on-device or the cloud model will be used before anything is sent. Bank statements themselves are always read on-device, from the PDF's text layer.

These providers have their own privacy policies. We have no control over them.

### 4.1 Advertising (iPhone)

Without an Onhaven Pro subscription, and after the free trial, some features require watching a short rewarded ad from **Google AdMob**: one ad for each statement you import, and one ad to unlock automatic family sync on that device for one day. Ads play only when you choose to watch one. The Mac version shows no ads.

- **What Google collects.** The Google Mobile Ads SDK starts when the app opens, so Google can receive device and usage data even before you watch an ad. This includes your IP address and approximate location derived from it, device information, ad interactions, performance and crash data, and, if you allow tracking, your device's Advertising Identifier (IDFA). Google uses this data to deliver and measure ads and to prevent fraud. See <https://policies.google.com/technologies/partner-sites>.
- **What Onhaven never gives Google.** We do not pass amounts, balances, holdings, categories, institution names, or any other financial record to the ads SDK.
- **Confirming a sync ad.** For ads that unlock sync, the app gives Google your Onhaven account ID and device ID, which are random identifiers. Google sends them back to our server to confirm you finished the ad.
- **Your choices.** The first time you choose to watch an ad, iOS asks whether Onhaven may track you (*App Tracking Transparency*). If you decline, you can still watch ads, and they won't use your IDFA. You can change this at any time in iOS *Settings → Privacy & Security → Tracking*. Where the law requires it (for example in the EEA, the UK, and Switzerland), Google's consent form appears first, and **Ad Privacy Options** in Onhaven's Settings lets you change or withdraw your choice.
- **US state privacy laws.** Under some US state laws, this advertising data may count as "selling" or "sharing" personal information. You can opt out using the choices above.

Subscribing to Onhaven Pro means you no longer need to watch ads to import statements or to use automatic family sync.

### 4.2 Subscriptions

Onhaven Pro is an optional, auto-renewing subscription sold through the App Store. Apple processes the payment, and we never receive your card or billing details. When you are signed in, the app sends the signed App Store transaction to our server to confirm the subscription, and we store its expiry date with your account. To manage or cancel it, open iOS *Settings → Apple Account → Subscriptions*.

## 5. Device Permissions

- **Camera**: used only to scan a family invite or key-recovery QR code. Images are not stored or sent anywhere.
- **Face ID / passcode**: used to confirm it's you before showing your recovery key, leaving a family, or deleting your account. Verification is done by iOS. We never receive biometric data.
- **Files**: statements you choose are opened only when you pick them. They are read on-device, or by the optional cloud model described in Section 4, and are not uploaded to our server.
- **Tracking (*App Tracking Transparency*)**: requested only when you choose to watch an ad, as described in Section 4.1.

## 6. Data We Do Not Collect

- No advertising identifiers or tracking by Onhaven itself. The only exception is the Google ads SDK described in Section 4.1.
- No third-party analytics or crash-reporting SDKs. The Google ads SDK collects its own diagnostics, as described in Section 4.1.
- No bank or brokerage logins. Onhaven never connects to your financial institutions. You import statements yourself.
- Onhaven never asks for your location, contacts, photos library, health data, or microphone.
- No payment information. Purchases are handled entirely by Apple.

## 7. How We Protect Data

- End-to-end encryption of synced records (AES-GCM with keys derived via HKDF, and Curve25519 key agreement when passing the family key to a new device).
- Encryption in transit: all connections use HTTPS (TLS).
- Device keys and the family key live in the iOS Keychain, restricted to this device.
- We keep only what sync needs, and we never log record contents.

## 8. Service Providers

- **Apple Inc.**: Sign in with Apple, Apple Intelligence and Private Cloud Compute, App Store distribution. <https://www.apple.com/legal/privacy/>
- **Google Cloud (Cloud Run)**: hosts the sync server.
- **Neon (PostgreSQL)**: the sync server's database. It holds ciphertext for your records, plus the account and family metadata listed in Section 3.
- **Google AdMob**: rewarded ads on iPhone, as described in Section 4.1. <https://policies.google.com/privacy>

We never sell, rent, or share your financial records. Apart from the advertising data Google collects as described in Section 4.1, we do not share your data with advertisers or data brokers.

## 9. Retention and Deletion

| Data | Retention |
|---|---|
| Records on your device | Until you delete them or uninstall the app |
| Account, devices, and invites on the server | Deleted immediately when you tap **Delete Account** in the app |
| Encrypted family records on the server | Kept while the family exists. Deleted when the owner deletes the family, or when the last member leaves |
| Sync access dates, rewarded-ad records, and subscription expiry on the server | Deleted with your account |
| Server access logs | Automatically rotated, up to 30 days |
| Advertising data collected by Google | Under Google's own retention policies |

**To delete your account:** open the last tab (**Account** or **Family**) and scroll to the bottom, or open **Family Sync**, then tap **Delete Account**. You'll confirm with Apple once more, so we can also revoke Onhaven's *Sign in with Apple* access. If you are the owner of a family with other members, you'll first choose whether to transfer ownership or delete the family. Your records on this device are kept, and the app keeps working without an account.

You can also stop Onhaven from using your Apple ID at any time: in iOS, open *Settings → Apple Account → Sign-In & Security → Sign in with Apple*. Onhaven signs out automatically when you do this.

## 10. Your Rights

- **Your financial records**: The complete, readable records live on your devices. You can view, edit, or delete them in the app at any time; if Family Sync is on, your changes are encrypted and synced to the server and your family's devices. The synced records on our server are ciphertext we cannot decrypt, so we cannot read or correct them for you, or provide a readable copy.
- **Account and family group information**: For the plain-text data listed in Sections 3.1 and 3.2 (Apple user ID, email, device type, family name, and member roles), you can contact us to request a copy or a correction.
- **Deletion**: Deleting your account or your family in the app (see Section 9) deletes the corresponding data on our server. You can also contact us and we will do it for you.

If you are in the EU, UK, California, or another jurisdiction with similar laws, these are also your rights under the GDPR, UK GDPR, CCPA/CPRA, and similar laws. We will respond within the time those laws require.

## 11. Not Financial Advice

Onhaven's evaluations, recommendations, and AI analysis are informational only. They are not investment, tax, or legal advice. Please consult a qualified professional before making financial decisions.

## 12. Children

Onhaven is not directed to children under 13, and we do not knowingly collect personal data from them.

## 13. International Transfers

Our sync server runs in Google Cloud's Taiwan region (`asia-east1`). Our providers may process data in other regions. Synced records are end-to-end encrypted wherever they are stored.

## 14. Changes to This Policy

When we make material changes, we will update the "Last updated" date above and, where required, tell you in the app.

## 15. Contact

**Email:** [dayou99.dev@gmail.com](mailto:dayou99.dev@gmail.com)

---

*This policy is provided in English and Traditional Chinese. If the two versions conflict, the English version controls.*
