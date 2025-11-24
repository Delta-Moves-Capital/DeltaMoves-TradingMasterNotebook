# Futures Trading – Delta Moves Capital

This directory contains all futures-related trading documentation, organized by
instrument and strategy type. The structure is designed for scalability as new
systems, playbooks, and studies are added over time.

---

## Purpose
- Centralize all futures trading knowledge.
- Keep general education separate from instrument-specific strategies.
- Provide clear navigation for income, scalping, rotation, and volatility systems.
- Support GitHub Pages rendering and long-term documentation growth.

---

## Directory Structure

### **General Futures Topics**
These files provide market-wide education and reference material:

- **bond-futures.md** – Overview of Treasury futures and rate-sensitive products.
- **calendar-spreads.md** – Structure and mechanics of futures calendar spreads.
- **equity-index-futures.md** – ES/NQ/RTY overview, contract specs, behavior.
- **futures-volatility.md** – Understanding volatility regimes, term structure, and EM.

---

## Instrument-Specific Playbooks

Each futures instrument receives its own folder and strategy modules.

### **/ZN (10-Year T-Notes)**
```
zn/
└── income-strategy/
    └── zn-income-playbook.md
```

### **/ES (S&P 500 Futures)**
```
es/
└── income-strategy/
```

### **/NQ (Nasdaq Futures)**
```
nq/
└── income-strategy/
```

### **/RTY (Russell Futures)**
```
rty/
└── income-strategy/
```

---

## How to Add New Futures Strategies

1. Create a new directory under the instrument name:
   ```
   futures-trading/<instrument>/<strategy-name>
   ```

2. Add the playbook or documentation file (e.g., `es-scalping-framework.md`).

3. Update this README with a link to the new file.

4. (Optional) Add to GitHub Pages navigation for publishing.

---

## Notes
This folder is maintained by **Delta Moves Capital** and is part of the  
Trading Master Notebook structure.
