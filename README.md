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

# 🏠 Updating `index.html` (Root Landing Page)

The root [`index.html`](./index.html) is the landing page that lists all applications and their legal documents. It must be updated whenever an app is added/removed or a document is added/changed.

---

## 🔹 1. When to Update

Update `index.html` whenever any of the following happens:

* A new application folder is added
* A new legal document is added to an existing app (e.g., `terms-of-service.html`)
* A new language version is added (e.g., `privacy-policy.ja.html`)
* An existing file is renamed or removed
* An app is discontinued and its folder is removed

---

## 🔹 2. Adding a New Application

Copy an existing `<article class="app-card">` block and replace the values:

```html
<article class="app-card">
  <h2 class="app-name">App Display Name</h2>
  <p class="app-package">com.company.appname</p>

  <div class="doc-group">
    <p class="doc-label">Privacy Policy / 개인정보처리방침</p>
    <div class="btn-row">
      <a class="btn btn-primary" href="./com.company.appname/privacy-policy.ko.html">
        <span class="lang-tag">KO</span>
        <span>한국어</span>
      </a>
      <a class="btn btn-secondary" href="./com.company.appname/privacy-policy.en.html">
        <span class="lang-tag">EN</span>
        <span>English</span>
      </a>
    </div>
  </div>
</article>
```

* `app-name` — user-facing app title
* `app-package` — the package name (must match the folder name)
* `href` — relative path to the document

---

## 🔹 3. Adding Another Document Type to an Existing App

Add a new `<div class="doc-group">` block inside the same `<article>`:

```html
<div class="doc-group">
  <p class="doc-label">Terms of Service / 이용약관</p>
  <div class="btn-row">
    <a class="btn btn-primary" href="./com.company.appname/terms-of-service.ko.html">
      <span class="lang-tag">KO</span>
      <span>한국어</span>
    </a>
    <a class="btn btn-secondary" href="./com.company.appname/terms-of-service.en.html">
      <span class="lang-tag">EN</span>
      <span>English</span>
    </a>
  </div>
</div>
```

---

## 🔹 4. Adding Another Language

Add another `<a class="btn ...">` link inside the existing `<div class="btn-row">`:

```html
<a class="btn btn-secondary" href="./com.company.appname/privacy-policy.ja.html">
  <span class="lang-tag">JA</span>
  <span>日本語</span>
</a>
```

* The first/primary language uses `btn-primary` (filled style)
* Additional languages use `btn-secondary` (outlined style)

---

## 🔹 5. Verification Checklist

Before committing changes to `index.html`:

* [ ] Every `href` matches an actual file path (no broken links)
* [ ] Every `app-package` matches its folder name exactly
* [ ] Each app has at least one document group
* [ ] Buttons are ordered consistently (KO first, then EN, then others)
* [ ] Open `index.html` in a browser locally and click every button to confirm

---

## 🔹 6. Key Principles

* `index.html` is the **single source of truth** for navigation — keep it in sync with the file tree
* Match the existing card structure for visual consistency
* Do not break existing URLs after deployment (renaming a file requires updating its `href` and notifying anywhere the URL was published, e.g., Play Console)

---
