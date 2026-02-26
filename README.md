# HubSpot CLI Account Switching

## 1️⃣ Switch to Production (Main)

```bash
hs accounts use sumitomo-pharma
```

---

## 2️⃣ Switch to Sandbox

```bash
hs accounts use sumitomo-destination
```

---

## 3️⃣ Check Active Account

```bash
hs accounts list
```

---

## 4️⃣ Fetch File Manager Folder

Format:

```bash
hs filemanager fetch <hubspot_path> <local_path>
```

- First path → HubSpot File Manager path  
- Second path → Local project path  

Example:

```bash
hs filemanager fetch /information/lonasentape/img information/information/lonasentape
```
