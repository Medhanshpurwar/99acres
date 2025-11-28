
## 99acres Seller Rating & Review Fetcher – Part B (Prototype)

### 1. Project Overview

This is a **browser-based prototype** that helps home buyers evaluate **property sellers/channel partners** on 99acres by showing their **Google Business ratings, review counts, and recent customer reviews** in one place.

It is designed for buyers searching **new projects in Whitefield, Bangalore (₹3 Cr budget)** so they can easily answer:

> *“Can I trust this seller? What do real customers say?”*

### Key Goals

* Build trust through real Google reviews
* Save time by avoiding manual Google searches
* Show both positive and negative feedback
* Keep the experience simple and user-friendly

---

### 2. Tech Stack & Architecture

**Frontend:**

* HTML5, CSS3, Vanilla JavaScript

**Data:**

* Static client-side JSON dataset (10 real sellers)

**Deployment:**

* Single static HTML file (no backend, no server needed)

**Why Static?**

* Fast loading
* Easy to run anywhere
* Zero infrastructure cost
* Easy to maintain

---

### 3. Main Features

✅ **Search** – Find sellers by name or Google Business name
✅ **Star Ratings** – Visual stars + color-coded scores
✅ **Sorting**

* By Rating
* By Review Count
* By Newest Reviews

✅ **Filters** – Show sellers above selected rating thresholds
✅ **Review Preview** – Top 3 recent Google reviews per seller
✅ **CSV Export** – Download seller data for offline use
✅ **Demo Buttons** – Quick view for key sellers (PropTiger, NIVASHAN, etc.)
✅ **Google Redirect** – Direct links to full Google profiles
✅ **Stats Panel** – Shows total sellers, average rating, and best-rated seller

---

### 4. How It Works (Workflow)

1. User enters seller name or clicks demo buttons
2. JavaScript filters in-memory dataset
3. Applies rating filter and sorting
4. Renders seller cards dynamically
5. Shows statistics panel
6. Optional CSV download

---

### 5. Data Structure (Simplified)

Each seller is stored as:

```js
{
  id: 1,
  seller_name: "PropTiger",
  google_business_name: "Proptiger Marketing Services Pvt. Ltd",
  google_rating: "4.2/5",
  total_review_count: 341,
  matched_by: "Name",
  search_url: "...",
  reviews: [
    { text: "...", date: "2025-05-28", stars: 5 }
  ]
}
```

---

### 6. Assumptions & Limitations

* Uses **static, manually collected data** (not real-time)
* Limited to **10 sellers** (prototype scope)
* Reviews are assumed genuine (from Google)
* Matching between 99acres names and Google names is manual
* No backend, authentication, or live API integration

**Reliability Snapshot**

| Aspect        | Reliability |
| ------------- | ----------- |
| Ratings       | High        |
| Review Count  | High        |
| Review Text   | High        |
| Name Matching | Medium      |
| Freshness     | Medium      |

---

### 7. How to Use

#### For Buyers

1. Open the HTML file in any browser
2. Use demo buttons or search box
3. Apply rating and sort filters
4. Read recent reviews
5. Click **“View on Google”** to verify
6. Export CSV if needed

#### For Developers

* Open HTML directly (no setup required)
* Add sellers by extending the `sellersData` array
* Modify logic inside:

  * `searchSeller()`
  * `sortSellers()`
  * `renderSeller()`

---

### 8. Future Enhancements (Roadmap)

**Short-Term**

* Google Places API integration
* Fuzzy name matching
* Automatic daily refresh

**Mid-Term**

* Sentiment analysis
* Multi-platform reviews (Facebook, Trustpilot)
* User accounts and notifications

**Long-Term**

* AI-based seller recommendations
* Mobile apps (iOS/Android)
* Direct 99acres integration

---

### 9. Project Value

✅ Increases buyer trust
✅ Improves transparency
✅ Reduces research time
✅ Lays foundation for production-ready system
