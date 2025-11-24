# /ZN Income Strategy – Delta Moves Capital

This directory contains the complete income strategy framework for trading
10-Year Treasury Note futures (/ZN). The methodology centers around a
structured put-to-call rotation, designed to generate consistent weekly and
monthly premium while maintaining a neutral to slightly long bias on the
Treasury curve.

---

## Purpose
- Document the full /ZN income engine.
- Provide a standardized structure for future /ZN systems.
- Align with the broader Trading Master Notebook architecture.
- Serve as the central reference point for all /ZN premium-harvesting playbooks.

---

## File Index

### **Primary Playbooks**
- **zn-income-playbook.md**  
  Full ruleset for the 4-cycle /ZN income engine  
  (Short Put Cycle, Covered Call Cycle, Monthly Reset Cycle, Volatility Override)

### **Coming Additions**
- zn-roll-strategy.md (optional)
- zn-event-model.md (CPI/FOMC/NFP integration)
- zn-term-structure-model.md
- zn-yield-curve-risk.md

---

## Strategy Components

### 1. **Short Put Entry Engine (Cycle A)**
Weekly 7–10 DTE short puts (18–28 delta) used to generate income and accumulate
long futures contracts at improved entry prices.

### 2. **Covered Call Engine (Cycle B)**
Weekly 7–10 DTE short calls (10–15 delta) sold against held /ZN positions.

### 3. **Monthly Cost-Basis Reset (Cycle C)**
Every 20–30 days, evaluate cost basis, contract count, and trend context.

### 4. **High-Volatility Override (Cycle D)**
When MOVE >130, halt put entries and reduce overall aggressiveness.

---

## Folder Structure

```
zn/
└── income-strategy/
    ├── README.md
    └── zn-income-playbook.md
```

This structure will expand as additional playbooks and systems are developed.

---

## How to Add New /ZN Modules

1. Create a new file inside `income-strategy/`:
   ```
   zn/income-strategy/<new-file>.md
   ```
2. Add the file to the index above.
3. Reference it from the root `futures-trading/README.md`.
4. Commit and push.

---

## Notes
This strategy is part of the **Futures Trading Notebook** and maintained by  
**Delta Moves Capital**.