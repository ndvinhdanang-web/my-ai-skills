---
name: landing-pages-plus
description: Build high-converting, ultra-fast static HTML/Tailwind CSS landing pages modeled after the structured, transparent local-service and catalog layout of haikieu.com, featuring 3 B2B Theme Presets (IT/Home Services, Food/Beverage, Retail/Camera Packages), Local SEO JSON-LD Schema, Interactive Symptom/Combo Estimator, Google Sheets JSON (opensheet.elk.sh) with Stale-While-Revalidate localStorage caching, interactive booking/cart drawer, dynamic VietQR payment codes with 1-tap copy, social proof toast, n8n webhook or Zalo/Telegram order integration, SHA-256 Admin Gate, and an upgraded Visual Live Editor (auto-save draft, Undo/Redo, Mobile Preview toggle, password changer, and pre-built Section Templates with clean HTML export). Use whenever the user asks to create a landing page, service website, product catalog, or sales page using the Landing Pages Plus style or haikieu.com layout.
---

# Landing Pages Plus

Build single-file, ultra-fast static landing pages (HTML + Tailwind CSS + Vanilla JS) combining the structured, high-trust conversion architecture of `haikieu.com` with Local SEO structured data, interactive symptom/combo estimators, zero-backend Google Sheets CMS, instant `localStorage` caching, dynamic VietQR checkout with 1-tap copy, social proof notifications, n8n/Zalo/Telegram lead routing, and an upgraded **Visual Live Editor** (auto-save draft, Undo/Reset, Mobile Preview toggle, password changer, section library, and clean HTML export).

## Default Owner & Contact Profile

When building pages for the user's businesses unless explicitly overridden in the prompt, apply the exact business profile:

  - **TRUNG DUNG Computer / NPP Trung Dung:**
      - **Hotline / Zalo:** `0944 70 8765` (`tel:0944708765`, `https://zalo.me/0944708765`)
      - **Address:** `71 Man Quang 15, P. Son Tra, TP. Da Nang`
      - **Bank Account (VietQR):** `NGUYEN DUC VINH` (`0944708765`)
  - **NGOC ANH FOOD / Vinh Troc Food:**
      - **Hotline / Zalo:** `0944 70 8765` (`tel:0944708765`, `https://zalo.me/0944708765`)
      - **Address:** `71 Man Quang 15, P. Son Tra, TP. Da Nang`
      - **Bank Account (VietQR):** `NGUYEN DUC VINH` (`0944708765`)
      - **Theme Palette:** Warm cream background (`#FFFDF9` / `#FFF8EE`) paired with high-contrast reddish-brown typography and accents (`#9A3412` / `#451A03`) for outdoor readability.

## Quy Tac Bat Buoc Cho Landing Page (TRUNG DUNG Computer)

Khi tao hoac cap nhat landing page cho **TRUNG DUNG Computer**, bat buoc tuan thu day du 3 nhom quy tac sau:

1. **Header & Dieu Huong Tren Mobile:**
   - Khong de so dien thoai, nut hanh dong hay tieu de thuong hieu che mat hoac de len nhau tren man hinh nho (< 768px).
   - Dung bo cuc linh hoat (`flex-wrap`, `shrink-0`, `min-w-0`, `whitespace-nowrap`) va thanh link nhanh rieng cho mobile neu can de moi nut bam de cham, khong tran ngang (`overflow-x-hidden`).

2. **Cum Nut Noi (Zalo / Goi) & Social Toast Tren Mobile:**
   - Cum nut noi Zalo va Goi co dinh o goc duoi ben phai (`bottom-3 right-3 sm:bottom-4 sm:right-4`), kich thuoc gon (`text-xs sm:text-sm`), `whitespace-nowrap`, khong bi day lech hay tran mep man hinh.
   - Social Proof Toast (neu bat) dat o goc duoi ben trai (`bottom-20 sm:bottom-4 left-3 sm:left-4 right-28 sm:right-auto`) de khong de len cum nut Zalo/Goi tren dien thoai.

3. **Khung ADMIN LIVE EDITOR:**
   - Khoa mac dinh tren trang cong khai; chi bat khi mo khoa ma quan tri SHA-256 o chan trang.
   - Giu giao dien thanh `ADMIN LIVE EDITOR` 2 tang phia tren cung (`Undo`, `Redo`, `Lam moi gia Sheet`, `API / VietQR`, `Luu nhap`, `Xuat HTML sach`, nut `×` va thanh dinh dang chu/mau nen) va go sach cac chrome cua editor khi xuat `index.html`.

## 3 B2B Theme Presets (Multi-Preset Engine)

Automatically select or switch between these 3 domain-optimized visual & functional presets based on the business type:

1.  **Preset 1 - Ky thuat & Dich vu tai nha (Default `haikieu.com` Style):**
      - **Palette:** Crisp White (`#FFFFFF`) & Cool Slate (`#F8FAFC`) backgrounds, Deep Navy (`#0F172A`) headings, High-Trust Red (`#E11D48`) or Tech Blue (`#1D4ED8`) primary CTAs, Emerald (`#10B981`) badges.
      - **Focus:** Speed (15-30 min arrival), upfront transparent quotes, symptom-to-solution diagnostic selector, warranty slips, and district coverage matrix.
2.  **Preset 2 - Am thuc / Quan nhau / Ship do an:**
      - **Palette:** Warm Cream (`#FFFDF9` / `#FFF8EE`) background paired with high-contrast Reddish-Brown (`#9A3412` / `#451A03`) typography and Amber (`#D97706`) accents.
      - **Focus:** Large appetizing food photography, quick item/topping notes (e.g., *it mo, them banh hoi, tuong ot rieng*), combo bundles, and multi-platform badges (GrabFood, ShopeeFood, Zalo).
3.  **Preset 3 - Ban le / Thiet bi / Camera tron goi:**
      - **Palette:** Clean Modern Slate (`#F8FAFC`) & White (`#FFFFFF`), Deep Indigo/Blue (`#1E3A8A`) headers, Cyan/Blue (`#0284C7`) interactive highlights.
      - **Focus:** Package comparison cards (e.g., *Goi 2 mat, 4 mat, 8 mat*), hardware specifications, warranty duration tags, and instant package cost calculator.

## Layout Architecture (Inspired by haikieu.com)

Structure every generated page with these conversion-focused blocks in order:

1.  **Local SEO JSON-LD Schema (`<head>`):**
    
      - Automatically embed valid `<script type="application/ld+json">` blocks for `LocalBusiness` (name, telephone, address in Da Nang, openingHours, geo/areaServed) and `FAQPage` synced with the page's FAQ items, plus Open Graph (`og:title`, `og:description`, `og:image`) meta tags.

2.  **Top Utility Bar & Sticky Header:**
    
      - Compact top bar showing operating hours and availability badge (e.g., `Phuc vu T2-CN • 7:30-21:00` or `10:00-22:00`).
      - Sticky navigation bar with brand logo/title, 4 anchor links (`Bang gia`, `Quy trinh`, `Khu vuc`, `Lien he`), direct hotline button, and interactive Cart/Booking drawer trigger with item counter badge. On mobile (< 768px), use `flex-wrap`, `shrink-0`, `min-w-0`, `whitespace-nowrap`, `overflow-x-hidden`, and a dedicated mobile quick-link bar if needed so brand titles, phone numbers, and action buttons never overlap or overflow horizontally.

3.  **High-Trust Split Hero Section:**
    
      - **Left Column:** Location/speed eyebrow pill, bold value-driven H1 headline, concise subheadline emphasizing transparency and warranty/quality, and a multi-channel action bar (Primary Booking CTA, Direct Call button, Chat Zalo button, and optional Telegram link).
      - **Right Column:** A 2x2 grid of 4 core trust pillars paired with a compact 1-minute quick lead/callback card.

4.  **Interactive Symptom / Combo Estimator (`Ban dang gap van de gi?` / `Chon nhanh theo nhu cau`):**
    
      - Interactive clickable symptom or need pills (e.g., *"May chay cham, quat keu to"*, *"Camera mat tin hieu"*, *"Tiec nhau 4-6 nguoi"*). Clicking a pill reveals an instant recommended solution/package card with transparent estimated pricing and a 1-tap `+ Them vao phieu` button.

5.  **Transparent Pricing Principles & Dynamic Catalog Grid (Google Sheets Powered):**
    
      - Brief 3-column transparency callout explaining how pricing works (clear upfront quote, no hidden fees).
      - Category/featured filter pills (`Tat ca`, `Pho bien`, plus dynamic categories if present in data).
      - Responsive 3-column service/product cards showing `loading="lazy"` image, status badge, title, concise description, optional item note/option selector (e.g., topping/variant note), formatted VND price + unit, and `+ Chon` button (automatically disabled when `status` indicates unavailable).

6.  **4-Step Transparent Workflow (Quy trinh 4 buoc):**
    
      - 4 numbered cards with time/stage badges (`01` -> `02` -> `03` -> `04`).

7.  **Service Area & Arrival Time Matrix (Khu vuc phuc vu):**
    
      - Clean responsive grid or compact table listing districts/zones with estimated arrival or delivery times, operating hours, and a 1-tap **"Mo ban do chi duong"** link to Google Maps.

8.  **Commitments & Interactive FAQ Accordion:**
    
      - 4-to-6 card commitment block + native HTML `<details>/<summary>` FAQ accordion answering 4 to 5 common customer objections cleanly without external JS libraries.

9.  **Interactive Cart / Booking Drawer with Dynamic VietQR & 1-Tap Copy:**
    
      - Slide-over drawer displaying selected items, optional item notes, quantity controls (`-` / `+`), and live total calculation.
      - Toggleable **VietQR** section generating a live QR image via `https://img.vietqr.io/image/<BANK_ID>-<ACCOUNT_NO>-compact2.png?amount=<TOTAL>&addInfo=<INFO>&accountName=<NAME>` synced to the cart total, PLUS **1-tap Copy buttons** (`Sao chep STK` and `Sao chep Noi dung CK`) so mobile visitors can paste directly into their banking app without scanning.
      - Customer details form submitting JSON to a configurable **n8n Webhook URL**, with automatic clipboard copy + Zalo chat redirect fallback if no webhook is configured or if offline.

10. **Structured Footer, Social Proof Toast & Floating Multi-Channel Dock:**
    
      - 3-column footer with brand summary, address (`71 Man Quang 15, P. Son Tra, TP. Da Nang`), Google Maps direction link, hours/hotline, coverage areas, and the locked **Admin Gate** input (`input[type="password"]` + `"Mo"`) in the last column.
      - Lightweight, dismissible **Social Proof Toast** positioned in the bottom-left corner (`bottom-20 sm:bottom-4 left-3 sm:left-4 right-28 sm:right-auto` so it never overlaps the floating Zalo/Call dock on mobile) rotating subtle local order/booking activity (with toggle in Admin Panel).
      - Fixed bottom-right floating action dock (`bottom-3 right-3 sm:bottom-4 sm:right-4`, compact sizing `text-xs sm:text-sm`, `whitespace-nowrap`) for Hotline, Zalo, and Telegram without overflowing or shifting off-screen on mobile.

### Quy tac Bao mat Khu vuc Quan tri (Admin Gate - Bat buoc)

  - Moi tinh nang quan tri (Cai dat Google Sheets CMS, VietQR, Webhook, chinh sua SEO Meta/OG, bat/tat Social Proof Toast, doi mat khau Admin va nut Bat Che do Sua Trang Truc Tiep / Visual Live Editor) phai duoc an mac dinh khoi giao dien nguoi dung cong khai, chi bat khi mo khoa ma quan tri SHA-256 o chan trang.
  - Tai cot cuoi cung cua Footer, chi hien thi mot o nhap nho `input[type="password"]` (placeholder: `"Ma quan tri..."`) kem nut `"Mo"` (ho tro nhan phim `Enter`).
  - Xac thuc mat khau bang thuat toan bam **SHA-256** ngay tren trinh duyet (`crypto.subtle.digest`) thay vi luu chuoi mat khau dang ro trong ma nguon. Mat khau mac dinh la `123456` (hash: `8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92`).
  - Ho tro **Doi mat khau Admin truc tiep** trong bang Quan tri: nhap mat khau moi -> tinh SHA-256 moi -> cap nhat bien hash trong DOM/state de khi xuat file `index.html`, mat khau moi duoc luu vinh vien.
  - Khi nhap dung mat khau, luu trang thai mo khoa vao `sessionStorage` (dong tab tu khoa) va hien thi bang cong cu Quan tri (bao gom ca **Trinh chinh sua SEO nhanh**: `Meta Title`, `Meta Description`, `OG Image URL` va tu dong dong bo JSON-LD) kem nut `"Khoa lai"`.
  - Chan hoan toan phim tat `Ctrl + E`, tham so URL `?edit=1` va ham mo modal cau hinh neu chua mo khoa mat khau.
  - Khi xuat file `index.html` sach, tu dong dat lai giao dien ve trang thai khoa quan tri mac dinh.

## Built-In Visual Live Editor & Section Library (Mandatory)

Every generated landing page MUST include a self-contained, zero-dependency **Visual Live Editor** mode activated **only after unlocking the Admin Gate**, via:

  - Admin panel button (`Bat Che do Sua Trang Truc Tiep`), keyboard shortcut (`Ctrl + E`), or URL query parameter (`?edit=1`) when unlocked in `sessionStorage`.

Include these exact interactive capabilities inside the editor script:

1.  **Two-Tier Top Editor Bar, Auto-Save Draft, Undo/Redo & Mobile Preview Toggle:**
    
      - Keep the 2-tier top `ADMIN LIVE EDITOR` bar interface with `Undo`, `Redo`, `Lam moi gia Sheet`, `API / VietQR`, `Luu nhap`, `Xuat HTML sach`, close button `×`, and the text/background formatting toolbar.
      - **Auto-Save Draft (`localStorage`):** Automatically snapshot editable page state to `localStorage` on every edit so accidental `F5` refreshes never lose work; show a subtle `"Da luu nhap"` badge and offer `"Khoi phuc ban goc"` (Reset to Original).
      - **Undo / Redo Stack (`Hoan tac` / `Lam lai` / `Ctrl + Z` / `Ctrl + Y`):** Maintain an in-memory history stack of DOM snapshots (up to 20 steps) so the user can undo and redo text, image, style, or section changes cleanly.
      - **Mobile Preview Toggle (`Xem thu Mobile 390px`):** Toggle a centered 390px mobile viewport frame right inside the desktop browser to inspect responsive layout before exporting.

2.  **Direct Click-to-Edit (`contentEditable`):**
    
      - Clicking any heading (`h1`-`h4`), paragraph, badge, list item, table cell, FAQ summary/answer, or button label enables inline text editing with visual outline feedback.
      - Clicking any `<img>` opens an inline prompt/modal to replace `src` URL and `alt` text immediately.
      - Clicking any `<a>` button/link in edit mode prevents accidental navigation and lets the user edit label and `href` (`tel:`, `https://zalo.me/...`, anchor `#...`, or external URL).

3.  **Section-Level Controls & Insert Bars:**
    
      - Each `<section>` gets a floating top-right control bar in edit mode allowing the user to:
          * **Change Background Theme** (e.g., Light Cream `#FFFDF9`, Warm Cream `#FFF8EE`, Crisp White `#FFFFFF`, Slate `#F8FAFC`, or Brand Accent).
          * **Move Up / Move Down** (`insertBefore` / `after`) to reorder sections on the page.
          * **Duplicate Section** (`cloneNode(true)`).
          * **Delete Section** (with confirmation).
      - Render dashed `+ Chen Section tai day` insert bars between sections (plus a `+ Them Section` button on the bottom editor toolbar).

4.  **Pre-Built Domain-Specific Section Templates Modal:**
    
      - Clicking `+ Them Section` or `+ Chen Section tai day` opens a visual picker modal containing 8 to 10 ready-to-use, domain-matched HTML section templates (Symptom/Need Diagnostic Block, Combo/Package 3-Column Grid, Customer Testimonials, Brand Story / Photo + Text, Multi-Platform Ordering Apps, Wholesale / Bulk Pricing Table, Promo CTA Banner, 4-Step Workflow, Coverage Matrix, and FAQ Accordion) that insert cleanly at the chosen position.

5.  **Item/Card Controls & Clean HTML Export:**
    
      - Repeatable cards (trust pillars, symptom pills, workflow steps, commitments, FAQ items, table rows) can be duplicated, reordered, or deleted in edit mode.
      - Bottom floating editor dock / top 2-tier editor bar includes **`Xuat HTML sach` / `Xuat file index.html sach`**: clones `document.documentElement`, strips all editor toolbars, `contentEditable` attributes, temporary edit classes/modals, updates the active SHA-256 admin password hash and SEO meta/JSON-LD tags, and resets `?edit=1` as well as the Admin Gate UI back to its default locked state (`input[type="password"]` + `"Mo"`, hiding admin tools) so the downloaded `index.html` is 100% clean, secure, and ready to deploy directly to Cloudflare Pages.

## Technical Implementation Rules

  - **Single-File Delivery:** Output one self-contained HTML file using Tailwind CSS CDN (`https://cdn.tailwindcss.com`), Google Fonts (`Be Vietnam Pro`), and Vanilla JS.
  - **Stale-While-Revalidate Data Engine:**
      - Read `localStorage` cache synchronously on page load (falling back to realistic domain-specific demo items) for 0ms perceived load time.
      - Fetch fresh JSON asynchronously from `https://opensheet.elk.sh/<SHEET_ID>/<TAB_NAME>` using schema `id, name, description, price, unit, image, status, featured`.
      - Compare payload with cache; if changed, update `localStorage` and re-render smoothly. Wrap `fetch` in `try/catch` so network errors never break the UI.
  - **Visual & Copy Standards:**
      - Never use em-dashes or en-dashes in UI copy; use standard hyphens (`-`), colons, or bullet dots (`•`).
      - Warn against Google Drive share links in the `image` column; recommend direct image URLs.

## Gotchas

  - **Interactive Preview:** Always generate the complete, self-contained HTML file cleanly so it can be previewed immediately and deployed directly to Cloudflare Pages without manual code edits.
  - **Clean Export Hygiene:** Ensure the exported HTML file removes all injected editor DOM nodes (`#visual-editor-dock`, `.section-insert-bar`, `.section-controls`, `#section-library-modal`, and 2-tier editor bars/formatting toolbars), resets `contenteditable` attributes, preserves any updated SHA-256 password hash and SEO meta tags, and restores the default locked Admin Gate state before triggering the `Blob` download.
