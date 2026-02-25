# German Salary Calculator (Brutto → Netto)

A clean, modern **single-page** German salary calculator with **tooltips**, **dark mode**, and a live **deduction breakdown**.

## Exact mode (matches brutto-netto-rechner.info)

The page now supports an **Exact** engine that embeds the original calculator from `brutto-netto-rechner.info` in an iframe and auto-syncs your inputs via a standard form POST.

- This is the only way to guarantee **1:1 identical results** without re-implementing the full official payroll/tax logic.
- Requires an internet connection and that the upstream site remains available/embeddable.

## Run it

- Open `index.html` in your browser (double-click or drag into a browser), **or**
- Serve it locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## What it calculates (estimate)

Given a gross salary (annual or monthly), it estimates:

- **Employee social contributions**:
  - Health insurance (KV) (statutory) using base rate + half “Zusatzbeitrag”
  - Care insurance (PV), including a childless surcharge (and a Sachsen adjustment)
  - Pension insurance (RV)
  - Unemployment insurance (AV)
- **Income tax (ESt)** using a simplified progressive tax function (zones + top rates)
- **Solidarity surcharge (Soli)** (simplified threshold + 5.5% above)
- **Church tax (Kirchensteuer)** (8% in BY/BW, 9% elsewhere) as a % of income tax

## Important notes / assumptions

- **This is not official payroll software**: Germany payroll can vary due to many factors (allowances, bonuses, exact insurance details, pension plans, special deductions, etc.).
- **Steuerklasse**: Tax class affects *withholding*; annual reality may differ after filing. The page uses a pragmatic approximation so the UI “feels” like payroll.
- **Private health insurance (PKV)**: when enabled, KV is replaced by your entered monthly premium (PV can be optionally estimated).

## Shareable results

Use **“Copy link”** to generate a URL with your inputs encoded in the query string.
