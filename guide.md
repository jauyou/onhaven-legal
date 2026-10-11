---
title: Onhaven User Guide
permalink: /guide/
---

# Onhaven User Guide

[Privacy Policy](/onhaven-legal/) · [Support](/onhaven-legal/support/) · **User Guide**

**English** · [繁體中文](/onhaven-legal/guide/zh/)

**Last updated:** October 11, 2026

Onhaven puts your investments, cash flow, and long-term goals in one place and evaluates them every quarter. All of it runs on your iPhone. This guide walks through each part of the app.

- [1. Getting started](#1-getting-started)
- [2. How Onhaven organizes time: quarters](#2-how-onhaven-organizes-time-quarters)
- [3. Portfolio](#3-portfolio)
- [4. Cash Flow](#4-cash-flow)
- [5. Evaluate](#5-evaluate)
- [6. Account / Family tab](#6-account--family-tab)
- [7. Crypto wallets](#7-crypto-wallets)
- [8. Family sync](#8-family-sync)
- [9. Currencies and exchange rates](#9-currencies-and-exchange-rates)
- [10. Sample data](#10-sample-data)

## 1. Getting started

The first time you open Onhaven, a short setup appears:

1. **Family status.** Enter how many adults, children, and elders are in your household, and optionally the primary earner's age. The evaluation uses this to tailor its advice; for example, it recommends a larger emergency fund when you have dependents. You can skip this and fill it in later.
2. **Sign in (optional).** Sign in with Apple is only needed if you want to sync with family members' devices. Tap **Not now** to use Onhaven entirely on this device.
3. **Explore with Sample Data.** Fills the app with a sample household so you can see every screen before entering your own numbers (see [Sample data](#10-sample-data)).

There are four tabs along the bottom: **Portfolio**, **Cash Flow**, **Evaluate**, and **Account** (it's called **Family** once you join a family).

## 2. How Onhaven organizes time: quarters

Onhaven records your finances by **year and quarter** (for example 2026 Q3). Holdings are a snapshot of what you held in a quarter. Income and expenses are totals for the quarter they belong to. Imported statements are filed under the quarter of their dates.

When a new quarter starts and an account has no statement yet, its holdings carry forward from the last quarter that had one. Onhaven marks these as carried forward, so you know they still need updating.

## 3. Portfolio

The Portfolio tab shows your current position:

- **Total value, unrealized P/L, and invested cost**, with a trend chart. The gap between the two lines is your unrealized gain or loss.
- **Asset allocation**, broken down by market, account, or family member.
- **Largest positions**, which show how concentrated you are.
- **Directional exposure**, which nets options and stock together. It shows how many shares, or how much money, is at risk if an underlying moves up or down.

### Adding holdings

- **Add Holding** (pencil icon): enter a symbol or name, the quantity, cost, and market value, and pick an account.
- **Import from Statement**: choose a brokerage statement PDF or image. Onhaven reads the holdings and transactions and shows them for review. Nothing is saved until you tap **Import**. The review checks the holdings against the statement's own total. If they don't add up, import stays locked until you confirm you've checked the difference.
- **Imported Statements**: lists every statement you've imported. If one was read wrong, you can delete the whole statement.

Statement reading uses Apple Intelligence. When your device supports Apple's *Private Cloud Compute*, Onhaven uses it, because it reads long statements far more accurately. Otherwise it falls back to the on-device model. The import screen always tells you which one it's using. When the on-device model is used, every row starts unchecked so you can verify the numbers first.

### Refreshing prices

Pull down on the Portfolio tab, or tap **Refresh Values**, to fetch current quotes. This revalues the current quarter's listed securities and re-reads crypto wallets. Only ticker symbols are sent.

## 4. Cash Flow

Cash Flow has four sections, chosen with the picker at the top:

- **Income** and **Expenses**: add quarterly entries by hand, such as salary, bonuses, rent, or travel.
- **Cards**: import a credit card statement PDF to record spending transaction by transaction. Onhaven checks the transactions against the totals printed on the statement. Payments to the card issuer are listed but aren't counted as spending.
- **Bank**: import a monthly bank statement PDF. Every row is checked against the running balance printed after it, so amounts and directions match the statement exactly. Here you can:
  - Mark transfers between your own accounts so they aren't counted as income or spending. Onhaven pairs matching transfers automatically.
  - Choose whether a higher-than-usual salary payment counts as a bonus.
  - Tap **Suggest Categories** to have Apple Intelligence fill in categories for uncategorized rows. Suggestions are marked, so you can review them before importing.

Bank statements must be PDFs downloaded from your bank. Scans have no text layer and can't be read.

## 5. Evaluate

Pick a quarter to see:

- An **overall score** out of 100
- **Cash flow**: savings rate, and emergency fund in months compared with the recommended number
- **Investments**: net worth (with deposits and card debt factored in when imported), change from last quarter, and largest holding share
- **Findings & Recommendations** from Onhaven's rule-based evaluation
- **Goals**: see below
- **AI Deep Analysis**: on devices with Apple Intelligence, tap **Generate AI Analysis** for a written summary of your situation. It runs on-device unless you turn on the larger cloud model.

The gear icon opens **Settings**: base currency, exchange rates, crypto settings, and sample data.

> Evaluations and AI analysis are for information only and are not financial advice.

### Goals

Add a goal with a target amount and the quarter you want it by, for example a home down payment or retirement. Onhaven shows whether your current assets and monthly savings get you there, and how much more you'd need each month. All goals share one pool of assets: the nearest deadline is funded first, so the same money is never counted twice. The recommended emergency fund is set aside and isn't counted toward goals.

For the growth assumption, you can enter a rate yourself, or tap **Fetch Holdings' Price History** to derive one from your holdings' past five years or more. Only ticker symbols are sent.

## 6. Account / Family tab

- **Family members**: add the people in your household, then add accounts under each one (brokerage accounts, bank accounts, credit cards, or crypto wallets). This lets the Portfolio tab break things down by owner. Statement imports can also create the account for you.
- **Family status snapshots**: the household details from setup carry forward to every later quarter. When something changes, such as a new baby or a parent moving in, tap **Add Snapshot**. The new status applies from that quarter onward.
- **Family Sync** (cloud icon in the toolbar): see [Family sync](#8-family-sync).
- **Leave Family / Delete Account**: at the bottom of the tab when you're signed in. Both ask for Face ID first.

## 7. Crypto wallets

Onhaven can track Solana wallets read-only. It never asks for a seed phrase and cannot move funds.

1. In the Account tab, open a family member, tap **Add Account**, and choose **Wallet**.
2. Paste the wallet's **public** address.
3. Onhaven reads token balances, staking, and DeFi positions from the chain and values them in USD. Tap **Refresh Wallet** to update, or **Load Older Trades** to build up cost history.

Under **Settings → Crypto** you can set a private RPC (for example Helius) for faster, more reliable reads, add a Jupiter API key, choose where positions come from, and turn automatic refresh on or off. Keys are stored in this device's Keychain.

## 8. Family sync

Family sync keeps the records on several family members' iPhones in sync. Records are encrypted on your device with a family key the server never sees.

**Create a family** (one person):
1. In the Account tab, tap the **Family Sync** cloud icon and sign in with Apple.
2. Enter a family name and tap **Create & Generate Family Key**.
3. **Save your recovery key.** Write it down or store it somewhere safe. It's the only way to get your data back if every family device is lost.

**Invite a member:**
1. On a family device, open **Members → Invite Member**. A QR code appears.
2. On the new member's iPhone, sign in with their own Apple ID, choose **Join Family**, and tap **Scan QR Code**. They can also paste the invite code.
3. The family key passes directly from the QR code to the new device, and syncing starts.

**New phone or reinstalled the app?** Your family is still there, but the key isn't on this device yet. Either:
- On another family device, choose **Help Recover Key** and scan its QR code from the new device, or
- Enter your **recovery key** (it starts with `OHVKEY1-`).

**Members**: the owner can swipe to remove a member. That member's devices delete the family key and all family records the next time they connect.

**Leaving**: when you leave a family, its records are deleted from your device; everyone else keeps theirs. If you're the owner and others remain, you'll first choose to transfer ownership or delete the family for everyone.

Sync runs automatically when records change. You can also tap **Sync** in Family Sync to sync manually.

## 9. Currencies and exchange rates

Every record keeps its original currency. Subtotals and the evaluation are converted to your **base currency** (Settings → Currency). Exchange rates update automatically when the app opens. You can turn that off and enter rates yourself under **Settings → Exchange Rates**. Only rates are downloaded; nothing is uploaded.

Turn on **Native Currency in Breakdowns** to show allocation groups in their own currency when every item in the group shares one.

## 10. Sample data

Choose **Explore with Sample Data** during setup, or **Settings → Sample Data → Load Sample Data**. It fills Onhaven with ten quarters of a sample household. You can only load it while the app is empty and you're not in a family.

While sample data is loaded:
- Family sync is paused, so the sample records are never shared.
- Statement import is disabled, so your real records can't get mixed into the sample accounts.

Tap **Clear Sample Data** at any time. It removes only the sample records; anything you added yourself is kept.

---

Questions? See [Support](/onhaven-legal/support/) or email [dayou99.dev@gmail.com](mailto:dayou99.dev@gmail.com).
