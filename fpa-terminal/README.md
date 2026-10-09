# FP&A Terminal

**FP&A Financial Modeling, Valuation & Capital Allocation Engine**

An interactive, single-file FP&A terminal that runs entirely in the browser: an
integrated three-statement model, a DCF and reverse-DCF valuation stack,
budget-vs-actual variance bridges, and a capital allocation / ROIC engine — no
backend, no install, no spreadsheet.

👉 **Live demo:** https://theooomd.github.io/Finance-Projects/fpa-terminal/

---

## What it does

### Load real financial statements
- Reads PitchBook / Capital IQ-style Excel exports, SEC 10-K PDFs, CSV and TXT. Statement pages are found automatically in long filings (a 122-page 10-K is handled).
- Detects company name, ticker, exchange, currency, units (thousands / millions) and a business-model lens (SaaS, retail, industrial, banks, energy, real estate, general corporate).
- Handles source quirks: sign conventions, lease-inclusive debt, amortization embedded in cost of revenue (content-heavy companies), share counts reported in thousands.

### Validated against source data
The parsers are reconciled line by line against the source files. Example: the same company loaded from a raw 10-K PDF and from a PitchBook export matches to the dollar on every shared line (revenue to net income, balance sheet, debt, cash flow, EBITDA, free cash flow), and the DCF values agree within 2% once the same WACC is applied. Remaining differences are source presentation (a 10-K reports three years where PitchBook reports five).

### Market view
Enter a share price (never stored) to see market cap, EV/EBITDA, P/E, FCF yield and the growth rate the market price implies (reverse DCF). The DCF value is an intrinsic value today, not a 12-month price target.

### Integrated three-statement model
- Linked income statement, balance sheet and cash flow statement driven off a
  single assumption set (revenue drivers, opex, working capital, capex).
- Debt schedule with interest, amortisation and revolver mechanics.
- Built-in integrity checks (balance sheet ties, cash roll-forward) so a broken
  link surfaces immediately instead of silently distorting the output.
- Scenario engine with side-by-side comparison and scenario deltas.

### Valuation
- DCF with explicit WACC build-up, terminal value and discounting detail.
- **Reverse DCF** — solve for the growth and margin the current price implies.
- Sensitivity tables (fair value per share, NPV across discount rate × revenue).
- Tornado analysis ranking the drivers that actually move EBITDA and value.
- Monte Carlo simulation over uncertain drivers (triangular distributions), with
  EBITDA and ending-cash distributions and a cash fan chart.
- Football field summarising fair value per share across methods and scenarios.

### Operational FP&A & variance analysis
- Budget vs actual vs forecast, with revenue and EBITDA bridges.
- Price / volume / mix (PVM) decomposition by product and by region.
- Rolling forecast, forecast-version walk and forecast-accuracy backtesting.
- Workforce plan, non-headcount opex drivers, customer unit economics, cohort
  retention and SaaS metrics.

### Capital allocation
- Multi-year capital allocation statement across capex, M&A, dividends and
  buybacks.
- ROIC vs. hurdle rate, economic profit / EVA and DuPont ROIC decomposition,
  including incremental returns (ROIIC).
- Liquidity stack, drawdown view and covenant headroom stress-testing with a
  stressed covenant trajectory.
- Investment returns: NPV, IRR and payback on individual business cases.

### Output layer
- Executive deck and whiteboard view, ratio monitor, red flags & strengths, and
  a Sr. FP&A memo to the CFO.
- A command line for driving the model's functions directly.

---

## How to use it

1. Open the [live demo](https://theooomd.github.io/Finance-Projects/fpa-terminal/).
2. Run the **self-test on the sample company** to see the full model populated
   end to end.
3. Work through *Trace a question through the model* to follow a single question
   from assumption to statement to valuation.
4. Change the assumptions and watch the statements, covenants and fair value
   re-derive.

Everything is client-side: nothing is uploaded, and no data leaves the browser.

## Running locally

```bash
git clone https://github.com/TheoooMD/Finance-Projects.git
cd Finance-Projects/fpa-terminal
# open index.html directly, or serve it:
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Technical notes

- **Single file.** `index.html` contains the markup, styling and the full
  calculation engine — no build step, no dependencies to install.
- **No backend.** All modelling, simulation and charting runs in the browser.
- **External requests.** Runs entirely in the browser. Google Fonts are optional. Excel and PDF import/export load SheetJS and pdf.js from cdnjs on demand, so those features need a connection; the built-in sample works offline. Nothing you load is uploaded anywhere.
- Charts and tables are rendered from the model's own output, so every figure on
  screen is traceable back to an assumption.

## Disclaimer

Built as a demonstration of FP&A, valuation and capital-allocation methodology.
The sample company and all figures are illustrative. Nothing here is investment
advice.

## License

Copyright (c) 2026 Minh-Duc Theo HO. All rights reserved. Viewing and evaluation only, see [LICENSE](../LICENSE).

## Author

**Minh-Duc Theo HO**
