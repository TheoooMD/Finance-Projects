# FP&A Terminal

**FP&A Financial Modeling, Valuation & Capital Allocation Engine** by **Minh-Duc Theo HO**

An interactive, single-file FP&A terminal that runs entirely in the browser: month-end
close, an integrated three-statement model, a DCF and reverse-DCF valuation stack,
budget-vs-actual variance bridges, and a capital allocation / ROIC engine. No
backend, no install, no spreadsheet.

👉 **Live demo:** https://theooomd.github.io/Finance-Projects/fpa-terminal/

---

## What it does

### Load real financial statements
- Reads PitchBook / Capital IQ-style Excel exports, SEC 10-K PDFs, CSV and TXT. Statement pages are found automatically in long filings (a 122-page 10-K is handled).
- Detects company name, ticker, exchange, currency, units (thousands / millions) and a business-model lens (SaaS, retail, industrial, banks, energy, real estate, general corporate).
- Handles source quirks: sign conventions, lease-inclusive debt, amortization embedded in cost of revenue (content-heavy companies), share counts reported in thousands.

### Month-end close
- Close calendar from WD-2 to WD+5 on real business days (US federal holidays skipped), with a task checklist, owners, dependencies and status.
- Flux analysis against prior month and budget, with editable thresholds and drafted driver commentary for every flagged line.
- Balance-sheet reconciliations (cash, AR roll-forward, deferred revenue, prepaids, accruals, ledger to statements) with reconciling items.
- Balanced adjusting journal entries with the P&L before and after adjustments.
- Close pack with open items, sign-off, print and copy.

### Integrated three-statement model
- Linked income statement, balance sheet and cash flow statement driven off a
  single assumption set (revenue drivers, opex, working capital, capex).
- Debt schedule with interest, amortisation and revolver mechanics.
- Built-in integrity checks (balance sheet ties, cash roll-forward) so a broken
  link surfaces immediately instead of silently distorting the output.
- Scenario engine with side-by-side comparison and scenario deltas.

### Operational FP&A & variance analysis
- Budget vs actual vs forecast, with revenue and EBITDA bridges.
- Price / volume / mix (PVM) decomposition by product and by region.
- Rolling forecast, forecast-version walk and forecast-accuracy backtesting.
- Workforce plan, non-headcount opex drivers, customer unit economics, cohort
  retention and SaaS metrics.

### Valuation
- DCF with explicit WACC build-up, terminal value and discounting detail.
- **Reverse DCF**: solve for the growth and margin the current price implies.
- Sensitivity tables (fair value per share, NPV across discount rate × revenue).
- Tornado analysis ranking the drivers that actually move EBITDA and value.
- Monte Carlo simulation over uncertain drivers (triangular distributions), with
  EBITDA and ending-cash distributions and a cash fan chart.
- Football field summarising fair value per share across methods and scenarios.

### Capital allocation
- Multi-year capital allocation statement across capex, M&A, dividends and
  buybacks.
- ROIC vs. hurdle rate, economic profit / EVA and DuPont ROIC decomposition,
  including incremental returns (ROIIC).
- Liquidity stack, drawdown view and covenant headroom stress-testing with a
  stressed covenant trajectory.
- Investment returns: NPV, IRR and payback on individual business cases.

### Output layer
- Board pack, whiteboard view, ratio monitor, red flags & strengths, and a
  Sr. FP&A memo to the CFO.
- A command line for driving the model's functions directly.

### Validated against source data
The parsers are reconciled line by line against the source files. Example: the same company loaded from a raw 10-K PDF and from a PitchBook export matches to the dollar on every shared line (revenue to net income, balance sheet, debt, cash flow, EBITDA, free cash flow), and the DCF values agree within 2% once the same WACC is applied. Remaining differences are source presentation (a 10-K reports three years where PitchBook reports five).

### Market view
Enter a share price (never stored) to see market cap, EV/EBITDA, P/E, FCF yield and the growth rate the market price implies (reverse DCF). The DCF value is an intrinsic value today, not a 12-month price target.

---

## How to use it

1. Open the [live demo](https://theooomd.github.io/Finance-Projects/fpa-terminal/).
2. Start the **guided walkthrough**, or **load the demo model** to see every view
   populated end to end.
3. Load your own statements, change the assumptions and watch the statements,
   covenants and fair value re-derive.

Everything is client-side: nothing is uploaded, and no data leaves the browser.

## Running locally

```bash
git clone https://github.com/TheoooMD/Finance-Projects.git
cd Finance-Projects/fpa-terminal
# open index.html directly, or serve it:
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Technical notes

- **Single file.** `fpa-terminal/index.html` contains the markup, styling and the
  full calculation engine: no build step, no dependencies to install.
- **External requests.** Runs entirely in the browser. Google Fonts are optional. Excel and PDF import/export load SheetJS and pdf.js from cdnjs on demand, so those features need a connection; the built-in sample works offline. Nothing you load is uploaded anywhere.
- Charts and tables are rendered from the model's own output, so every figure on
  screen is traceable back to an assumption.

## Disclaimer

Built as a demonstration of FP&A, valuation and capital-allocation methodology.
The sample company and all figures are illustrative. Nothing here is investment
advice.

## License

Copyright (c) 2026 Minh-Duc Theo HO. All rights reserved. Viewing and evaluation only, see [LICENSE](LICENSE).
