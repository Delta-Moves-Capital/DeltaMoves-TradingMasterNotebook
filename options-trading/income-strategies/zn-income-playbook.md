# /ZN Futures Income Playbook – Delta Moves Capital

A complete rule-based system for generating consistent, neutral income using 10-Year T-Note futures (/ZN) through short puts and covered calls.

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

## 2. Market Characteristics Unique to /ZN
- Treasury futures are driven by **interest rates**, not equity-market momentum.
- Volatility is dominated by macro events: CPI, FOMC, NFP, Treasury auctions.
- /ZN trends strongly during rate repricing and mean reverts outside those periods.
- Options are European-style; early assignment risk is negligible.

---

## 3. Short Put Entry Engine

### 3.1 Purpose
Generate income while accumulating long futures contracts at better-than-market prices.

### 3.2 Strike Selection
- Short put delta: **0.18–0.28**.
- Avoid <10 delta (too weak) and >30 delta (too aggressive).

### 3.3 DTE
- **7–10 DTE**.
- Roll or close at **50–70% profit** or with **3–4 DTE** remaining.

### 3.4 Event Filters (No New Entries)
Avoid initiating short puts within 24 hours of:
- CPI
- FOMC
- NFP
- 10-year Treasury auction/refunding days

### 3.5 Trend Filter
If /ZN moves >1.5× expected move in a week:
- Pause put selling until mean reversion.

### 3.6 Assignment Rules
If assigned:
- Accept assignment and hold the long contract.
- Immediately begin the covered-call cycle.

---

## 4. Covered Call Engine

### 4.1 Purpose
Harvest steady weekly yield from long /ZN futures.

### 4.2 Delta Selection
- Short call delta: **10–15** under normal conditions.
- In high vol: **15–20 delta**.

### 4.3 DTE
- **7–10 DTE** for consistent rotation.

### 4.4 Roll Triggers
- Profit ≥ 50–70%.
- Short call delta >25 → roll early.
- Short call delta >30 → roll up/out immediately.

### 4.5 Roll Mechanics
- **Roll up** to higher strikes when possible.
- **Roll out** to next expiration during strong trends.
- Never roll **down**.

---

## 5. Combined Income Cycle

### Step 1: Sell weekly 7–10 DTE put
Collect premium and wait.

### Step 2: If not assigned
Resell a new contract next week.

### Step 3: If assigned → hold long /ZN contract
Begin covered-call selling immediately.

### Step 4: Sell weekly 7–10 DTE covered calls
Roll up/out as needed.

### Step 5: When calls expire or are bought back
Return to Step 1.

This structure harvests premium on **both sides** of the trade.

---

## 6. Volatility & Macro Filters

### 6.1 MOVE Index Filter
- MOVE < 80 → reduce short-put exposure.
- MOVE 80–110 → operate normally.
- MOVE >130 → **no new short puts**.

### 6.2 Macro Blackout Window (New Entries Only)
Do not initiate new positions within 24 hours of:
- CPI
- FOMC
- NFP
- Treasury auctions (10yr)

### 6.3 Yield Shock Filter
If 2yr–10yr spread moves >10bp/day:
- Pause new options selling for 48 hours.

---

## 7. Position Sizing & Risk

### Recommended Size
- Maintain **1–6 /ZN contracts** depending on account size.
- Keep enough margin for rolling calls.

### Income Expectations
- Weekly: **0.40–0.75%** of notional.
- Monthly: **1.6–3.0%**.
- Annualized: **20–30%**.

### Assignment Frequency
- Target: **25–40%**.
- Too frequent = strike too aggressive.
- Too rare = strike too conservative.

---

## 8. Emergency Procedures

### /ZN price surges (yields drop fast)
- Short call delta >30 → roll up/out.
- Avoid deep ITM calls.

### /ZN price collapses (yields rise fast)
- Short puts may assign → acceptable.
- Reduce aggressiveness next cycle.

### MOVE >150
- Close short puts.
- Maintain but avoid adding call risk.

---

## 9. Expected Move Integration
Use 1-week expected move models from:
- Tastytrade
- CME
- Thinkorswim IV-based EM

**Put EM Rule:** Strike ≈ 0.8× EM below spot.  
**Call EM Rule:** Strike ≈ 0.8× EM above spot.

---

## 10. Recommended Repo Location
Place this file in:
```
futures-trading/zn-income-playbook.md
```

Add a link to this file from `/docs/README.md`.

---
