# FP&A Terminal

**FP&A Financial Modeling, Valuation & Capital Allocation Engine**

An interactive, single-file FP&A terminal that runs entirely in the browser: an
integrated three-statement model, a DCF and reverse-DCF valuation stack,
budget-vs-actual variance bridges, and a capital allocation / ROIC engine — no
backend, no install, no spreadsheet.

👉 **Live demo:** https://theooomd.github.io/Finance-Projects/fpa-terminal/

---

## What it does

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
- **Only external requests** are the Google Fonts stylesheets (IBM Plex Mono,
  IBM Plex Sans Condensed, Montserrat); the app works offline without them.
- Charts and tables are rendered from the model's own output, so every figure on
  screen is traceable back to an assumption.

## Disclaimer

Built as a demonstration of FP&A, valuation and capital-allocation methodology.
The sample company and all figures are illustrative. Nothing here is investment
advice.

## Author

**Minh-Duc Theo HO**
