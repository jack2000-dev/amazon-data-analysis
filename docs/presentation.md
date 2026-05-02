# Amazon Sales Dataset — Stakeholder Presentation
**Presenter:** Jack
**Duration:** 15 minutes
**Audience:** Product & Marketing Stakeholders

---

## 🗓️ Agenda
| # | Section | Time |
|---|---|---|
| 1 | Business Context & Objective | 1 min |
| 2 | About the Data | 1 min |
| 3 | Key Findings (5 Questions) | 8 min |
| 4 | Recommendations | 3 min |
| 5 | Limitations & Next Steps | 1 min |
| 6 | Q&A | 1 min |

---

## 1. Business Context & Objective `[1 min]`

**Opening statement:**
> *"Today I want to share findings from an analysis of over 1,400 Amazon products —
> looking at how discount strategy, pricing, and category performance relate to
> customer satisfaction and engagement."*

**The core problem we set out to solve:**
Amazon is investing heavily in discounting, but we didn't have clear evidence that
it was actually improving customer satisfaction or driving more reviews.

**Our 5 guiding questions:**
1. Does a higher discount lead to a higher product rating?
2. Which categories have the highest average ratings?
3. Do heavily discounted products get reviewed more?
4. Does actual price affect customer rating?
5. Which categories receive the most reviews?

---

## 2. About the Data `[1 min]`

- **Source:** Amazon product listings (Kaggle — karkavelrajaj/amazon-sales-dataset)
- **Size:** 1,465 products across multiple categories
- **Key fields used:** Category, Discounted Price, Actual Price, Discount %, Rating, Review Count
- **Time period:** Static snapshot — January 2023
- **Cleaning applied:** Removed currency symbols, standardised types, extracted top-level
  categories, removed duplicates and invalid entries

> *"The data has been cleaned and validated before any analysis was run."*

---

## 3. Key Findings `[8 min — ~1.5 min per question]`

---

### Finding 1 — Discounts Do Not Improve Ratings
**Q: Does a higher discount lead to a higher product rating?**

- **Result:** Weak negative correlation — `r = -0.162`
- **What this means:** Products with larger discounts tend to have *slightly lower* ratings,
  not higher ones
- **Takeaway:** Discounting is not a lever for improving customer satisfaction

> *"If anything, heavily discounted products trend slightly toward lower ratings —
> which suggests discounting may be masking underlying quality issues rather than
> compensating for them."*

---

### Finding 2 — Category Quality Is Uneven
**Q: Which categories have the highest average ratings?**

- **Highest rated:** Office Products
- **Lowest rated:** Car & Motorbike and Musical Instruments *(both below 4.0 stars)*
- **Threshold:** A rating below 4.0 is considered a risk signal for customer trust on Amazon
- **Takeaway:** Two categories need urgent attention — the issue is likely post-purchase
  experience, not the product itself

> *"Customers don't usually rate a product poorly at checkout — they rate it poorly
> after it arrives damaged, underperforms, or comes with poor support."*

---

### Finding 3 — Discounts Do Not Drive Review Volume
**Q: Do heavily discounted products get reviewed more?**

- **Result:** Near-zero correlation — `r = 0.003`
- **What this means:** There is essentially no relationship between discount level
  and the number of reviews a product receives
- **Takeaway:** Discount campaigns are not an effective strategy to build review volume

> *"This tells us that customers don't review more just because they paid less.
> Review growth needs a dedicated strategy — not a discount."*

---

### Finding 4 — Price Is Not a Quality Signal
**Q: Does actual price affect customer rating?**

- **Result:** Weak positive correlation — `r = 0.128`
- **What this means:** Higher price barely influences rating — low-priced products
  regularly achieve top-tier ratings
- **Takeaway:** Budget products can compete on quality perception

> *"This is an opportunity. Our lower price-point products are already earning
> great ratings — we just need to market them as 'Best Value', not 'Cheap'."*

---

### Finding 5 — Electronics Dominates, But Office Products Is Hidden
**Q: Which categories receive the most reviews?**

- **Most reviewed:** Electronics — by a significant margin
- **Least reviewed:** Car & Motorbike
- **Hidden insight:** Office Products is the **highest-rated** category (Finding 2)
  but one of the **lowest in review volume** — a visibility gap, not a quality problem

> *"Office Products is our best-kept secret. Customers who buy it love it —
> but not enough people know about it yet."*

---

## 4. Recommendations `[3 min]`

### Rec 1 — Audit Discount Strategy
- **Action:** Stop using blanket discounts as a satisfaction tool
- **Next Step:** Audit the top 20% most-discounted products — if they're also the
  lowest-rated, discounting is masking a quality issue, not solving it
- **Owner:** Pricing Team

### Rec 2 — Improve Underperforming Categories
- **Action:** Prioritise after-purchase service for Car & Motorbike and Musical Instruments
- **Next Step:** Pull customer complaint data for these two categories to identify root cause
  (shipping damage? misleading listings? product quality?)
- **Owner:** Customer Experience Team

### Rec 3 — Build a Review Growth Program
- **Action:** Replace discount-driven review strategies with post-purchase engagement
  (follow-up emails, loyalty points for reviews)
- **Next Step:** A/B test a post-purchase email campaign vs. a discount campaign —
  measure review volume after 30 days
- **Owner:** Marketing Team

### Rec 4 — Reframe Budget Product Messaging
- **Action:** Market low-price, high-rated products as "Value for Money" picks
- **Next Step:** Identify the top 10 highest-rated products under ₹500 and
  feature them in a dedicated collection
- **Owner:** Marketing Team

### Rec 5 — Invest in Office Products Visibility
- **Action:** Increase sponsored placements and marketing for the Office Products category
- **Next Step:** Launch a targeted awareness campaign to grow review volume and
  build social proof for this category
- **Owner:** Marketing Team

---

## 5. Limitations & Next Steps `[1 min]`

### ⚠️ Limitations
- **Static snapshot** — no time-series data, so we cannot measure trends over time
- **Scraped data** — not sourced directly from Amazon; some values may have inaccuracies
- **No demographics** — we cannot segment findings by region, age group, or customer type
- **Correlation ≠ causation** — findings show relationships, not direct cause-and-effect

### 🔭 Suggested Next Steps
1. Obtain time-stamped transaction data to track rating trends over time
2. Run A/B test on discount vs. post-purchase email campaign (Rec 3)
3. Deep-dive analysis on Car & Motorbike and Musical Instruments complaint data
4. Repeat this analysis quarterly to track category improvement

---

## 6. Q&A `[1 min]`

> *"That's the summary of our findings. I'm happy to go deeper on any specific
> category, chart, or recommendation. What questions do you have?"*

---

## 📎 Appendix — Reference Data

| Metric | Value |
|---|---|
| Dataset size | 1,465 products |
| Categories analysed | 9 main categories |
| Q1 Correlation (Discount vs Rating) | r = -0.162 |
| Q3 Correlation (Discount vs Reviews) | r = 0.003 |
| Q4 Correlation (Price vs Rating) | r = 0.128 |
| Highest rated category | Office Products |
| Lowest rated category | Car & Motorbike |
| Most reviewed category | Electronics |
| Categories below 4.0 avg rating | Car & Motorbike, Musical Instruments |
