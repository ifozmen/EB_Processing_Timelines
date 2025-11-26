# US EB Visa Priority Date Predictor

A simple, powerful tool to predict when your Employment-Based (EB) visa priority date will become current.

## ⚡ Quick Start (No Installation!)

### Google Colab (Recommended for Non-Programmers)

1. Click: [**Open in Google Colab**]
2. Click **Runtime → Run All** (or Ctrl+F9)
3. Scroll to the last cell and update your details:
   - Category: `2` (EB-2)
   - Country: `row` (Rest of World)
   - Priority Date: `2025-11-25`
4. Click the play button ▶️
5. Download results automatically

---

## 📊 What You Get

### 1️⃣ **Excel Report** with:
- Historical visa bulletin data (5 years)
- Movement statistics & trends
- **3 different projections** (optimistic, realistic, conservative)
- Month-by-month breakdown

### 2️⃣ **Beautiful 8-Panel Chart** showing:
- **Panels 1-6**: Historical trends & patterns
- **Panel 7**: Projection scenarios with confidence levels, When you'll be current (the big question!)
- **Panel 8**: Quick summary table with key dates

---

## 🎯 Example Results

```
Priority Date:          November 25, 2025
Current Status:         ❌ NOT YET CURRENT

Gap to Cover:           3.4 months
Current Movement Rate:  1.2 months per bulletin

PREDICTED CURRENT DATE:
├─ Optimistic (6-mo trend):    March 2026
├─ Realistic (12-mo trend):    April 2026
└─ Conservative (24-mo trend): May 2026

💡 Start preparing your I-485 for March 2026
```

---

## 🛠️ Configuration

Edit the **last cell** in the notebook:

```python
# Your details here:
category = '2'              # EB category: 1, 2, 3, or 4
country = 'row'             # india, china, mexico, philippines, or row
priority_date = '2025-11-25' # Your priority date
months_back = 60            # Months to analyze (default: 60 = 5 years)
```

| Option | Values | Example |
|--------|--------|---------|
| **Category** | `1` `2` `3` `4` | EB-2 visa → `'2'` |
| **Country** | `india` `china` `mexico` `philippines` `row` | Rest of World → `'row'` |
| **Priority Date** | `YYYY-MM-DD` format | November 25, 2025 → `'2025-11-25'` |

---

## 📈 How It Works

```
Step 1: Fetch → Scrapes State Dept visa bulletins (automated)
         ↓
Step 2: Extract → Finds your category & country data
         ↓
Step 3: Analyze → Calculates movement rates & trends
         ↓
Step 4: Project → Models 3 future scenarios
         ↓
Step 5: Report → Creates Excel + chart
         ↓
Step 6: Download → Files ready on your computer
```

---

## 🤔 Understanding the 8-Panel Chart

| Panel | Shows | What It Means |
|-------|-------|---------------|
| **1** | Blue line crossing red line | When you become current | Shows current trend
| **2** | Green/red bars + trend lines | How fast the queue is moving |
| **3** | Upward/downward line | Is the wait getting worse or better? |
| **4** | Bell curve | Are movements predictable or random? |
| **5** | Zig-zag line | Recent acceleration/deceleration |
| **6** | Yearly bars | Which years moved fastest? |
| **7** | ⭐ **Three dashed lines intersecting red line** | **YOUR ANSWER: Expected current date** |
| **8** | Text summary table | Quick reference for key dates |

---

## ❓ FAQ

### "What's a Priority Date?"
The date USCIS received your green card petition (I-140). Once this date becomes "current," you can file for adjustment of status (I-485).

### "What does ROW mean?"
**Rest of World** — all countries except India, China, Mexico, and Philippines (which have separate queues).

### "Why 3 different predictions?"
Because visa movement isn't perfectly predictable. The 3 scenarios give you a realistic range:
- **6-month trend** = Most recent (could be short-term spike)
- **12-month trend** = Balanced view
- **24-month trend** = Most conservative

### "Can I trust this?"
The tool uses **official State Dept data**. Projections are based on historical trends, which are ~70-80% accurate. Always check the official visa bulletin monthly for surprises!

### "My country/category isn't working"
Currently supports EB-1 through EB-4 for these countries:
- India, China, Mexico, Philippines, ROW
