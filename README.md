# BD-Interactive_map

ইন্টারেক্টিভ বাংলাদেশ মানচিত্র ও বিসিএস প্রস্তুতি পোর্টাল (বাংলা + English)।
Interactive Bangladesh map and study portal for BCS exam preparation (Bangla + English).

**File:** `interactive_bangladesh_map_for_bcs_exam_prep.html` — a single self-contained page (no build step). Open it in any modern browser.

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

## Map layer notes

- Layers are thematic overlays drawn on the existing district SVG; the base district geometry is unchanged.
- Marker coordinates use approximate real-world locations projected onto the page's map projection.
- Data compiled from Banglapedia, the Bangladesh Forest Department, Bangladesh Tea Board, the Liberation War Museum, the 2011 census and standard BCS geography textbooks.
