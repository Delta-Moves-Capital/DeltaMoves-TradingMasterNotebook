# /ZN Futures Income Playbook – Delta Moves Capital

A complete rule-based system for generating consistent, neutral income using 10-Year T-Note futures (/ZN) through short puts, covered calls, and structured multi-cycle rotation.

---

## 1. Strategy Overview
This playbook defines a systematic income engine using /ZN futures:
- Sell **7–10 DTE short puts** to enter long contracts at improved prices.
- If assigned, hold 1–6 /ZN contracts.
- Sell **7–10 DTE covered calls** (10–15 delta) to generate weekly yield.
- Roll calls up/out as necessary.
- Rotate back to short puts once calls expire or are bought back.

This creates a dual-sided premium engine:
- **Short puts → paid entries**
- **Covered calls → paid exits**

---

## 2. Cycles & Rotation Model
A rotation system similar to your ES income framework, adapted for bond-market behavior.

### **Cycle A — Short Put Entry Engine (7–10 DTE)**
**Purpose:** Generate weekly yield and accumulate long contracts at favorable prices.
- Delta: **18–28** on short puts.
- Assignment is acceptable and expected 25–40% of cycles.
- Avoid new entries near CPI, FOMC, NFP, and Treasury auctions.
- Skip during abnormal rate volatility.

### **Cycle B — Covered Call Engine (7–10 DTE)**
**Purpose:** Harvest income from held long /ZN futures.
- Delta: **10–15** on short calls (15–20 in high vol).
- Roll up/out as soon as delta >25–30.
- Weekly harvest with controlled directional exposure.

### **Cycle C — Monthly Position Reset (20–30 Days)**
**Purpose:** Prevent cost-basis drift and maintain structural neutrality.
Every 20–30 days:
- Review futures cost basis.
- Reset long /ZN if trends have materially shifted.
- Adjust contract count.
- Rebalance put/call aggressiveness.

### **Cycle D — High-Volatility Override (MOVE >130)**
**Purpose:** Protect from rate-shock events.
- Halt new short puts.
- Maintain but do not add covered calls.
- Reduce delta aggressiveness.
- Resume normal operation when MOVE <110.

---

## 3. Market Characteristics Unique to /ZN
- Driven by **interest-rate repricing**, not equity-style trend flows.
- Strong trends around macro events; mean-reversion outside of them.
- European-style options (no early assignment risk).
- High liquidity and predictable weekly premium structure.

---

## 4. Short Put Entry Engine

### 4.1 Purpose
Generate income while accumulating long futures contracts at improved prices.

### 4.2 Strike Selection
- Short put delta: **18–28**.
- Avoid <10 delta (too weak) and >30 delta (too aggressive).

### 4.3 DTE
- **7–10 DTE**.
- Roll or close at **50–70% profit** or with **3–4 DTE remaining**.

### 4.4 Event Filters
Avoid new short puts within 24 hours of:
- CPI
- FOMC
- NFP
- 10-year Treasury auction/refunding days

### 4.5 Trend Filter
If /ZN moves >1.5× EM in a week, pause sells until mean reversion.

### 4.6 Assignment Rules
If assigned:
- Accept assignment.
- Immediately begin the covered-call cycle.

---

## 5. Covered Call Engine

### 5.1 Purpose
Harvest consistent yield from held /ZN futures.

### 5.2 Delta Selection
- Short call delta: **10–15** normally.
- High vol → **15–20 delta**.

### 5.3 DTE
- **7–10 DTE**.

### 5.4 Roll Triggers
- Profit ≥50–70%.
- Delta >25 → early roll.
- Delta >30 → mandatory roll up/out.

### 5.5 Roll Mechanics
- Roll **up** to keep upside open.
- Roll **out** during strong bullish /ZN trends.
- Never roll down.

---

## 6. Combined Income Cycle
**Step 1:** Sell 7–10 DTE short put.  
**Step 2:** If not assigned, repeat.  
**Step 3:** If assigned, hold long /ZN and begin covered calls.  
**Step 4:** Sell 7–10 DTE covered calls and roll as needed.  
**Step 5:** When calls are clear, return to Step 1.

This extracts premium from both entry and exit legs.

---

## 7. Volatility & Macro Filters

### MOVE Index Filter
- MOVE < 80 → reduce aggressiveness.
- MOVE 80–110 → normal trading.
- MOVE >130 → high-vol override (Cycle D).

### Macro Blackout
Avoid new positions 24 hours before:
- CPI
- FOMC
- NFP
- Treasury auctions

### Yield Shock Filter
If 2yr–10yr spread moves +10bp/day:
- Pause all new put or call sells for 48 hours.

---

## 8. Position Sizing & Risk
- Hold **1–6 /ZN** depending on capital.
- Maintain margin headroom for roll adjustments.

### Expected Income
- Weekly: **0.40–0.75%** of notional.
- Monthly: **1.6–3.0%**.
- Annual: **20–30%**.

---

## 9. Expected Move Integration
Use 1-week EM from CME, Tastytrade, or TOS.

**Put Entry Rule:** Strike ≈ 0.8× EM below spot.  
**Call Exit Rule:** Strike ≈ 0.8× EM above spot.

---

## 10. Recommended Repo Location
Place this file under:
```
futures-trading/zn-income-playbook.md
```
Link it in `/docs/README.md`.

---
