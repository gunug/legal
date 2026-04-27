# legal
Legal documents (privacy policies, terms of service) for all applications.

* 개인정보처리방침 (Privacy Policy)
* 이용약관 (Terms of Service)
* 쿠키 정책 (Cookie Policy)
* 면책조항 (Disclaimer)

---

# 📁 Folder & File Naming Rules (HTML-based)

This repository stores legal documents for multiple applications.
Each application is organized by its package name, and documents are provided as HTML files.

---

## 🔹 1. Top-Level Folder (Application Identifier)

* Each application **must have its own top-level folder**
* Folder name **must match the application package name**
* Use only:

  * lowercase letters (`a-z`)
  * numbers (`0-9`)
  * dots (`.`)
* No spaces or special characters

### ✅ Examples

```
com.example.app
com.gunhee.runningmusic
com.company.product
```

---

## 🔹 2. File Format

* All legal documents must be **HTML files (`.html`)**
* Files should be **ready for direct web access**
* Each file must be independently viewable in a browser

---

## 🔹 3. File Naming Convention

* Use **kebab-case** (lowercase with hyphens)
* Use **standard, widely recognized legal document names**

### ✅ Standard File Names

```
privacy-policy.html
terms-of-service.html
cookie-policy.html
refund-policy.html
disclaimer.html
```

---

## 🔹 4. Recommended Structure

Each application folder should contain its legal documents directly:

```
/com.example.app/
  privacy-policy.html
  terms-of-service.html
```

---

## 🔹 5. Full Example Structure

```
/legal
  /com.gunhee.runningmusic
    privacy-policy.html
    terms-of-service.html
  /com.gunhee.timer
    privacy-policy.html
    terms-of-service.html
```

---

## 🔹 6. (Optional) Multi-language Support

### Option A: Filename suffix

```
privacy-policy.en.html
privacy-policy.ko.html
```

### Option B: Subfolders

```
/com.example.app/
  /en/
    privacy-policy.html
  /ko/
    privacy-policy.html
```

---

## 🔹 7. Key Principles

* Use **package name** for uniqueness and stability
* Keep structure **flat and simple**
* Use **standard file names** for better compliance and recognition
* Ensure all documents are **accessible via direct URL**

---

## ✅ Summary

* Folder = `package name`
* File = `kebab-case HTML`
* Structure = simple and consistent

---
