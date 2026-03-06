# 📱 VariantIQ — Variant Imbalance Agent

> **AI-Powered Electronics Inventory Intelligence Dashboard**  
> Detects hidden stockouts, variant-level imbalances, and recommends inventory reallocations for Apple & Samsung retail stores.

🔗 **[Live Demo →](https://sumedhsavla.github.io/variantiq/)**

---

## 🎯 The Problem

Electronics retailers face a hidden crisis: **variant-level inventory blindness**.

A store reports *"15 iPhones in stock"* — but when you look deeper:

| Variant | Stock | Demand |
|---------|-------|--------|
| 512GB   | 12    | Low    |
| 256GB   | 2     | Medium |
| 128GB   | 1     | **High** |

The system says **"in stock"**, but the variant 55% of customers want has almost no inventory.

**The result:**
- ❌ Lost sales from customers who leave empty-handed
- ❌ Excess premium inventory sitting on shelves
- ❌ Poor conversion rates with no system alert
- ❌ Revenue loss invisible to traditional inventory tracking

---

## 💡 The Solution

VariantIQ analyzes inventory at the **variant level** — not just product level — to surface mismatches between what customers want and what's actually on shelves.

It provides 5 core intelligence features, each solving a specific retail problem.

---

## ✨ Features

### 1. Variant Demand Tracking
Breaks down demand by storage tier (128GB / 256GB / 512GB / 1TB) for every product, showing the true demand distribution that aggregate "units sold" numbers hide.

**Why it matters:** Purchasing decisions based on total product demand miss the SKU-level reality.

### 2. Imbalance Detection
Directly compares demand share (%) against inventory share (%) for each variant. Flags shortages (demand > inventory), excess (inventory > demand), and balanced states.

**Why it matters:** A +35pp gap between demand and inventory for 128GB means you're systematically understocking your most popular variant.

### 3. Hidden Stockout Detection
Scans every store × product combination and identifies cases where total stock > 0 but a high-demand variant has 0 units. These products appear "available" in every system — but customers can't buy what they want.

**Why it matters:** Traditional stockout alerts only fire when total inventory hits zero. Hidden stockouts are invisible revenue loss.

### 4. Reallocation Recommendations
Identifies stores with surplus inventory (stock-to-demand ratio > 2.5x) and stores starving for the same variant (ratio < 0.5x), then recommends specific unit transfers.

**Why it matters:** You don't always need to order more — sometimes the right inventory exists, just in the wrong location.

### 5. Lifecycle Shift Detection
Models how variant demand migrates over a product's lifecycle: premium storage dominates at launch, mid-tier grows in months 3–5, and budget variants take over by month 6+.

**Why it matters:** Inventory mix should follow the demand curve — stocking 1TB units 6 months post-launch is a capital trap.

---

## 📊 Dashboard

### Overview
![Overview](screenshots/overview.png)
*Top-level KPIs, health score, brand distribution, and critical stockout alerts.*

### Imbalance Detection
![Imbalance](screenshots/imbalance.png)
*Side-by-side demand vs. inventory comparison with gap analysis.*

### Hidden Stockouts
![Stockouts](screenshots/stockouts.png)
*Products appearing "in stock" but with unavailable high-demand variants.*

> 📸 **Note:** Replace the screenshot paths above with actual screenshots after deploying.

---

## 🛠 Tech Stack

| Technology | Purpose |
|-----------|---------|
| **HTML / CSS / JavaScript** | Single-file application, zero build step |
| **Chart.js** | Interactive data visualizations |
| **PapaParse** | CSV parsing with auto-detection |
| **GitHub Pages** | Free static hosting |

---

## 📁 Data

### Demo Mode
Pre-loaded with realistic mock data covering:
- **8 retail stores** across US regions (Manhattan, SF, LA, Chicago, Miami, Dallas, Seattle, Brooklyn)
- **8 products** — iPhone 14/15/16 Pro/Pro Max, Galaxy S23/S24/S25+/S25 Ultra
- **Variant dimensions** — Storage (128GB → 1TB), Color, Lifecycle Phase (launch/mid/late)
- **Seeded random generator** for reproducible, realistic distributions with deliberate imbalances

### CSV Upload Mode
Upload your own inventory data with smart column mapping:
- **Auto-detects** common column names (stock, inventory, qty, demand, sales, etc.)
- **5 required fields:** Store, Model, Variant, Stock, Weekly Demand
- **5 optional fields:** Brand, Color, Region, SKU, Lifecycle Phase
- **Downloadable template** included

---

## 🚀 Getting Started

### Option 1: View Live
Visit the **[Live Demo →](https://sumedhsavla.github.io/variantiq/)**

### Option 2: Run Locally
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/variantiq.git

# Open in browser
open index.html
```
No dependencies. No build step. No server. Just open the file.

---

## 🧠 Key Concepts Demonstrated

- **SKU-level demand analysis** — Moving beyond product-level to variant-level intelligence
- **Inventory balancing algorithms** — Surplus/deficit detection using stock-to-demand ratios
- **Hidden stockout identification** — Finding conversion loss invisible to traditional systems
- **Lifecycle-aware planning** — Adjusting inventory mix as products mature through their lifecycle
- **Interactive data visualization** — Charts, tables, KPI cards with real-time filtering
- **CSV ingestion pipeline** — Column mapping, auto-detection, data transformation

---

## 📈 Business Impact (Demo Scenario)

Based on the demo dataset analysis:
- **46+ hidden stockouts** detected across 8 stores
- **20 reallocation opportunities** identified to balance inventory
- **Budget variants (128GB)** consistently understocked vs. 55% demand share
- **Premium variants (512GB/1TB)** overstocked with only 15% demand share
- Estimated **15–25% conversion improvement** from resolving variant imbalances

---

## 📄 License

MIT — free to use, modify, and distribute.

---


*Built as a portfolio project demonstrating inventory analytics, data visualization, and retail intelligence concepts.*
