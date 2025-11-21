# SPX Iron Condor Rotation Manual
Delta Moves Capital – Index Options Income System

---

## 1. Purpose
A systematic, neutral-income rotation framework for SPX Iron Condors across three time horizons:

1. High Theta Engine (7–10 DTE)  
2. Moderate Theta Engine (10–15 DTE)  
3. Stable Theta Layer (20–30 DTE)

This diversified time structure delivers consistent theta income with controlled gamma and minimal directional exposure.

---

## 2. Strategy Overview
The system uses **three overlapping IC cycles**:

| Cycle   | DTE Range | Purpose        | Characteristics      |
| ------- | --------- | -------------- | -------------------- |
| Cycle A | 10–12 DTE | Moderate theta | Low–moderate gamma   |
| Cycle B | 7–10 DTE  | High theta     | Elevated gamma       |
| Cycle C | 20–30 DTE | Smooth theta   | Low gamma, long hold |

Time-diversified IC layers ensure continuous theta and reduced sensitivity to single news events.

---

## 3. IC Structure Rules

### 3.1 Delta Selection
- Short call delta: **6–12**  
- Short put delta: **6–12**  
- Delta difference per side: **≤ 6**

These maintain neutral directional exposure.

### 3.2 Wing Width Calculation
- **7–10 DTE:** Wing Width = **1.25× to 1.75× Expected Move (EM)**  
- **20–30 DTE:** Wing Width = **2× to 3× EM**

### 3.3 Minimum Credit Requirement
Credit ≥ **0.8%–1.2% of wing width**.

---

## 4. Entry Rules for Each Cycle

### Cycle A — 10–12 DTE (Moderate Theta)
- Wings: **1.5× EM**  
- Delta: **8–10**  
- Hold: **5–7 days**  
- Target: **30–40% max profit**

### Cycle B — 7–10 DTE (High Theta)
- Wings: **1.25×–1.5× EM**  
- Delta: **8–12**  
- Hold: **3–5 days**  
- Exit triggers: 40–50% profit, DTE ≤ 4, or delta skew > 10

### Cycle C — 20–30 DTE (Stable Layer)
- Wings: **2×–3× EM**  
- Delta: **5–10**  
- Hold: **10–15 days**  
- Exit triggers: 25–35% profit, remaining premium < 20%

---

## 5. Adjustment Logic

### Delta Skew Adjustments
| Condition             | Action                            |
| --------------------- | --------------------------------- |
| Delta spread > 10     | Roll one side closer or re-center |
| Delta spread > 15     | Mandatory adjust or close         |
| Break of short strike | Exit or widen                     |
| VIX spike             | Delay new entries                 |

### Gamma Controls
- Never hold ICs inside **≤ 2 DTE**.

---

## 6. Risk Filters
Do **not** open new ICs:
- Day before CPI
- Day before FOMC
- NFP morning
- VIX > 25
- SPX outside EM bands

---

## 7. Weekly Rotation Schedule

### Monday
- Open **Cycle A** (10–12 DTE)

### Wednesday
- Open **Cycle B** (7–8 DTE)

### Thursday
- Open **Cycle C** (20–30 DTE)

### Friday
- Close:
  - DTE ≤ 4
  - Profit ≥ target
  - Delta skew > 10

---

## 8. Position Sizing
- Cycle A: 20–30% allocation
- Cycle B: 30–40% allocation
- Cycle C: 20–30% allocation
- Cash buffer: 15–25%

Never exceed:
- 1× notional exposure per layer
- 3 ICs per cycle unless wings are very wide

---

## 9. Exit Rules (Non-Negotiable)
- **DTE ≤ 3 → Exit**  
- **Profit ≥ 40–50% → Exit**  
- **Short strike breached → Exit immediately**  
- **Delta skew > 15 → Exit or re-center**

---

## 10. Summary
Your income engine consists of:

- **Cycle A:** 10–12 DTE (moderate theta)  
- **Cycle B:** 7–10 DTE (high theta)  
- **Cycle C:** 20–30 DTE (smooth theta)  

Together, they produce:
- High theta  
- Low gamma  
- Time diversification  
- Stable, predictable income  
- Minimal directional exposure  
