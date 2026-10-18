# BD-Interactive_map

ইন্টারেক্টিভ বাংলাদেশ মানচিত্র ও বিসিএস প্রস্তুতি পোর্টাল (বাংলা + English)।
Interactive Bangladesh map and study portal for BCS exam preparation (Bangla + English).

🌐 **Live site / লাইভ সাইট:** <https://tr4842.github.io/BD-Interactive_map/>

**File:** `interactive_bangladesh_map_for_bcs_exam_prep.html` — a single self-contained page (no build step). Open it in any modern browser.
`index.html` is a tiny redirect page for GitHub Pages; `.nojekyll` keeps the folder served as-is.

## Features

- **৬৪ জেলা মানচিত্র** — clickable district polygons, ৮ বিভাগ filter, zoom/pan, district search.
- **থিম্যাটিক ম্যাপ লেয়ার (৫টি নতুন)** — each layer recolours the map, adds numbered markers, a clickable side panel and a BCS note:
  1. 🏺 **প্রাচীন জনপদ** — পুণ্ড্র, বঙ্গ, সমতট, গৌড়, হরিকেল, চন্দ্রদ্বীপ, বরেন্দ্র (৭টি)
  2. 🎖️ **মুক্তিযুদ্ধের সেক্টর** — ১১টি সেক্টর, সদর দপ্তর, কমান্ডার ও ফোর্স (কে/এস/জেড ফোর্স)
  3. 🌳 **বনজ সম্পদ** — সুন্দরবন, পার্বত্য বন, মধুপুর-ভাওয়াল শালবন, রাতারগুল, লাউয়াছড়া, চা বাগান প্রভৃতি (১০টি)
  4. ⛰️ **ভূপ্রকৃতিগত বিভাগ** — পাহাড়, গড়, বরেন্দ্র, প্লাবন সমভূমি, হাওর, উপকূল, পাদদেশ (৭টি; ৬৪ জেলা কভার)
  5. 👥 **ক্ষুদ্র নৃগোষ্ঠী** — চাকমা, মারমা, ত্রিপুরা, সাঁওতাল, গারো, ম্রো, রাখাইন প্রভৃতি — ভাষা, ধর্ম, উৎসব, সমাজব্যবস্থা (১৬টি)
- **বিশেষ অধ্যায় ট্যাব** — সবগুলো নতুন টপিকের পূর্ণাঙ্গ টেবিল/কার্ড, এক নজরে সূত্র ও "ম্যাপে দেখুন" বাটন।
- **৬৪ জেলার ডিরেক্টরি** — প্রাচীন নাম, নদী, জিআই পণ্য, দর্শনীয় স্থান, ব্যক্তিত্ব।
- **বিখ্যাত ব্যক্তিত্ব ও ৭ বীরশ্রেষ্ঠ**, **কুইজ (৩১ প্রশ্ন)** ও **ফ্ল্যাশকার্ড**, পঠিত-অগ্রগতি (`localStorage`)।

## Bengali typography / বাংলা টাইপোগ্রাফি

The page ships its fonts inside the HTML file, so Bengali renders correctly (conjuncts, matras, nukta, Bengali digits) even offline and without Google Fonts:

| Role | Font | Source |
| --- | --- | --- |
| Bengali headings (`h1`, `h2`) | Noto Serif Bengali Variable (100–900) | SIL OFL 1.1 |
| Bengali body, UI and map labels | Noto Sans Bengali Variable (100–900) | SIL OFL 1.1 |
| Latin text and numerals | Inter Variable (100–900) | SIL OFL 1.1 |

All three are embedded as base64 `woff2` with `unicode-range` subsets and `font-display: swap`. There are no external font requests. The map's SVG labels explicitly use the Bengali UI face, and letter-spacing is reset on Bengali text so the matra line is never broken.

## Visitor counter / ভিজিটর কাউন্টার

A footer widget shows **today** (`day-YYYY-MM-DD`), **this month** (`month-YYYY-MM`) and **all-time** visitor counts from the free, cookie-free [Abacus](https://abacus.jasoncameron.dev) counter API (namespace `bd-map-visitors-2026`):

- the first page load of a local day calls `/hit` for all three keys; later loads only `/get` (state kept in `localStorage` under `bd_visit_day`), so refreshing does not inflate the numbers;
- one browser is counted once per day; numbers are formatted with Bengali digits in বাংলা mode and Latin digits in English mode;
- if the service is unreachable (offline, `file://`, rate limit), the widget stays hidden and the page works normally.

## Map layer notes

- Layers are thematic overlays drawn on the existing district SVG; the base district geometry is unchanged.
- Marker coordinates use approximate real-world locations projected onto the page's map projection.
- Data compiled from Banglapedia, the Bangladesh Forest Department, Bangladesh Tea Board, the Liberation War Museum, the 2011 census and standard BCS geography textbooks.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000/  (redirects to the map)
```
