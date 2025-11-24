# Delta Moves Capital – Trading Master Notebook
Comprehensive navigation index for all trading documentation, strategy playbooks,
and structured research folders.

---

## Repository Structure Overview
```
DeltaMoves-TradingMasterNotebook/
├── docs/
├── options-trading/
│   └── income-strategies/
│       └── spx-iron-condor-rotation.md
├── futures-trading/
│   ├── bond-futures.md
│   ├── calendar-spreads.md
│   ├── equity-index-futures.md
│   ├── futures-volatility.md
│   ├── zn/
│   │   └── income-strategy/
│   │       ├── README.md
│   │       ├── _index.md
│   │       └── zn-income-playbook.md
│   ├── es/
│   │   └── income-strategy/
│   │       └── _index.md
│   ├── nq/
│   │   └── income-strategy/
│   │       └── _index.md
│   └── rty/
│       └── income-strategy/
│           └── _index.md
└── README.md (root)
```

---

## Documentation Index (docs/)
- **[Git Workflow Cheat Sheet](docs/git-workflow-cheatsheet.md)** – Git commands, workflow, commit structure

---

## Options Trading

### Income Strategies
Location: `options-trading/income-strategies/`

- **[SPX Iron Condor Rotation](options-trading/income-strategies/spx-iron-condor-rotation.md)**

---

## Futures Trading

### General Futures Topics
- **[Bond Futures](futures-trading/bond-futures.md)**
- **[Calendar Spreads](futures-trading/calendar-spreads.md)**
- **[Equity Index Futures](futures-trading/equity-index-futures.md)**
- **[Futures Volatility](futures-trading/futures-volatility.md)**

---

### ZN – 10-Year Treasury Notes
Location: `futures-trading/zn/`

#### Income Strategy
`futures-trading/zn/income-strategy/`

- **[ZN Income Playbook](futures-trading/zn/income-strategy/zn-income-playbook.md)**
- **[ZN Income Strategy Index](futures-trading/zn/income-strategy/_index.md)**
- **[ZN Income Strategy README](futures-trading/zn/income-strategy/README.md)**

---

### ES – S&P 500 Futures
Location: `futures-trading/es/`

- **[ES Section Index](futures-trading/es/_index.md)**

---

### NQ – Nasdaq 100 Futures
Location: `futures-trading/nq/`

- **[NQ Section Index](futures-trading/nq/_index.md)**

---

### RTY – Russell 2000 Futures
Location: `futures-trading/rty/`

- **[RTY Section Index](futures-trading/rty/_index.md)**

---

## Adding New Playbooks (Procedure)
1. Create a folder under the appropriate instrument:
   `futures-trading/<symbol>/<strategy-name>/`
2. Add the playbook file: `<strategy>.md`
3. Add an `_index.md` to expose the section on GitHub Pages.
4. Update:
   - `futures-trading/README.md`
   - This navigation index
   - Any `/docs/` index files

---

*Maintained by Delta Moves Capital.*