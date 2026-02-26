# HubSpot CLI Account Switching Guide

This project uses two HubSpot portals:

- Production (Standard)
  - Name: `sumitomo-pharma`
  - Account ID: `242103119`

- Sandbox (Standard Sandbox)
  - Name: `sumitomo-destination`
  - Account ID: `245253942`

---

## 🔍 Check Current Active Account

Always check before uploading:

```bash
hs accounts list
```

The account shown under **Default Account** is the active one.

---

## 🔄 Switch to Production (Main Account)

```bash
hs accounts use sumitomo-pharma
```

or

```bash
hs accounts use 242103119
```

Verify:

```bash
hs accounts list
```

You should see:

```
Default Account
Account: sumitomo-pharma [standard]
```

⚠️ Be careful — this is PRODUCTION.

---

## 🧪 Switch to Sandbox

```bash
hs accounts use sumitomo-destination
```

or

```bash
hs accounts use 245253942
```

Verify:

```bash
hs accounts list
```

You should see:

```
Default Account
Account: sumitomo-destination [standard sandbox]
```

Safe for testing.

---

## 📥 Fetch Files From Portal

Example:

```bash
hs fetch "themes/smp_all_files" "./smp_all_files"
```

---

## 📤 Upload Files To Portal

Example:

```bash
hs upload "./smp_all_files" "themes/smp_all_files"
```

---

## 👀 Watch Mode (Auto Sync)

```bash
hs watch "./smp_all_files" "themes/smp_all_files"
```

---

## ⚠️ IMPORTANT RULE

Before every upload or watch command, ALWAYS run:

```bash
hs accounts list
```

Never upload to production by accident.
