# Infosys Limited (NSE: INFY) — Institutional Equity Research & Valuation Model

[![Ticker](https://img.shields.io/badge/NSE-INFY%20%7C%20BSE%3A%20500209-0A66C2?style=flat-square)](https://www.nseindia.com)
[![Sector](https://img.shields.io/badge/Sector-Enterprise%20IT%20Services-2E4053?style=flat-square)]()
[![Valuation](https://img.shields.io/badge/Methodology-FCFF%20DCF%20%26%20Trading%20Comps-1E8449?style=flat-square)]()
[![Accounting](https://img.shields.io/badge/Analysis-10--Yr%20Historical%20%26%20DuPont-B7950B?style=flat-square)]()

> **Executive Thesis:** At a reference market price of **₹1,151**, Infosys Limited presents a classic **intrinsic-versus-relative valuation divergence**. While a conservative, fundamentals-driven Discounted Cash Flow (DCF) model yields an intrinsic value of **₹918.48/share** ($1.25\text{x}$ P/IV) due to near-term constant-currency growth moderation ($1\%–2\%$ FY27 guidance), the stock trades at a substantial discount (`9.2x` EV/EBITDA; `15.0x` P/E) relative to Indian IT sector medians (`16.1x` EV/EBITDA; `23.4x` P/E), implying **₹1,326–₹1,974/share** on a relative basis.

This repository houses a full-stack financial model, regression-based forecasting engine, multi-scenario valuation framework, and institutional-grade research report evaluating Infosys Limited across **FY15–FY32E**.

---

## 📌 Executive Valuation Summary

*Valuation Date: November 13, 2026 | Currency: INR (₹) in Crores, except per-share data*

| Valuation & Financial Metric | Figure | Analytical Context & Benchmark |
| :--- | :--- | :--- |
| **Reference Market Price (CMP)** | **₹1,151.00** | 52-Week Range: ₹980.40 – ₹1,728.00 |
| **Intrinsic Value (Base DCF)** | **₹918.48** | Implies **$-20.2\%$ downside** ($\text{WACC} = 12.87\%$, $g = 4.00\%$) |
| **DCF Scenario Range (Bear – Bull)** | **₹665.54 – ₹1,673.38** | WACC sensitivity ($11.00\%–18.00\%$) & terminal $g$ ($3.00\%–7.00\%$) |
| **Relative Valuation (Comps Median)** | **₹1,326.00 – ₹1,974.00** | Implies **$+15.2\%$ to $+71.5\%$ upside** across `EV/Rev`, `P/E`, `EV/EBITDA` |
| **FY26 Revenue & 10-Yr CAGR** | **₹178,650 Cr** | $+9.61\%$ YoY growth; $11.2\%$ CAGR (FY17–FY26) |
| **FY26 Free Cash Flow (FCF)** | **₹31,259 Cr** | $106.2\%$ FCF-to-Net-Profit conversion; ₹18,656 Cr dividends paid |
| **FY26 Return on Equity (ROE)** | **$31.21\%$** | Expanded $+576\text{ bps}$ since FY20 despite gross margin compression |
| **Net Cash Position (FY26)** | **₹13,676 Cr** | ₹22,201 Cr cash & bank vs. ₹9,176 Cr lease liabilities (zero bank debt) |

---

## 🗂️ Repository Architecture

```text
├── Infosys_FM&V.xlsx                                      # Dynamic, formula-driven 3-statement & valuation Excel workbook
├── Report_Infosys_Financial_Modelling_DCF_Valuation.pdf   # 21-page institutional equity research report with visual analytics
├── Infosys_FM&V.pdf                                       # Complete printable audit trail of all Excel model schedules
├── KEY_INSIGHTS.md                                        # Deep-dive investment memo: DCF vs. Comps, DuPont & Risk Critique
└── README.md                                              # Project documentation & methodological framework
```

---

## ⚙️ Financial Modelling & Valuation Methodology

The Excel workbook (`Infosys_FM&V.xlsx`) is engineered with dynamic cell referencing, clear separation of hardcoded inputs and calculated outputs, and institutional valuation conventions:

### 1. Historical Normalization & Common-Size Diagnostics (`FY17–FY26`)
* Reconstructed 10-year Income Statement, Balance Sheet, and Cash Flow schedules from NSE/Screener filings.
* Conducted vertical (common-size) and horizontal trend analyses to isolate structural margin shifts—specifically tracking the $670\text{ bps}$ gross margin compression ($34.86\% \rightarrow 28.21\%$) caused by rising pass-through/subcontracting costs.

### 2. Econometric Forecasting (`FY27E–FY32E`)
* Built Ordinary Least Squares (OLS) linear regression models regressing historical revenue (`FY15–FY26`, $n=12$) against time-series weights ($R^2 = 96.39\%$, $F\text{-stat} = 267.09$, $p = 1.53 \times 10^{-8}$) alongside operating EBITDA and EPS trend projections.

### 3. Cost of Capital (`WACC = 12.87%`)
* **Beta Estimation & De-leveraging:** Regressed 2 years of daily NSE closing returns ($n = 496$) against the Nifty 50 ($\beta_{\text{raw}} = 0.90$, Blume-adjusted $\beta = 0.92$). To eliminate single-stock estimation noise ($R^2 = 17.67\%$), unlevered 5-year monthly betas across Tier-1 Indian IT peers (TCS, HCLTech, Wipro, Tech Mahindra) to derive a peer-median unlevered beta of **$0.74$**, relevered at a target $D/E$ of $3.68\%$ to **$0.76$**.
* **CAPM Cost of Equity ($K_e$):** $7.21\%\text{ (10-Yr GoI Yield)} + 0.76 \times 7.94\%\text{ (26-Yr Nifty ERP)} = \mathbf{13.22\%}$.
* **After-Tax Cost of Debt ($K_d$):** $4.88\%\text{ pre-tax} \times (1 - 0.30) = \mathbf{3.42\%}$, weighted at $3.55\%$ target debt-to-capital.

### 4. Intrinsic Growth & FCFF Discounted Cash Flow (`DCF`)
* **Reinvestment-Driven Growth:** Computed sustainable operating growth via $g = \text{Reinvestment Rate} \times \text{ROIC}$, utilizing 4-year medians ($26.20\%$ reinvestment rate; $9.50\%$ explicit EBIT growth) to smooth working capital volatility.
* **Discounting & Terminal Value:** Projected 5-year explicit Unlevered Free Cash Flows (`FY27E–FY31E`) discounted via the **mid-year convention**, paired with a Gordon Growth terminal value ($g = 4.00\%$) and a 20-cell two-way sensitivity matrix.

### 5. Relative Valuation, Football Field & DuPont Decomposition
* **Trading Comps:** Benchmarked Infosys against 9 listed Indian IT services firms across `EV/Revenue`, `EV/EBITDA`, and `P/E` multiples.
* **Football Field Triangulation:** Synthesized Bear/Base/Bull DCF ranges, peer-multiple implied valuations, and the 52-week trading band.
* **3-Step DuPont Analysis:** Decomposed ROE ($31.21\%$) and ROA ($19.49\%$) across `FY20–FY26` to separate operational profitability from asset velocity and non-financial operating leverage.

---

## 🔍 Executive Takeaways (Preview)

* **Why DCF and Comps Disagree:** The DCF penalizes Infosys for near-term top-line deceleration ($1\%–2\%$ FY27 guidance) and capitalizes cash flows at a $12.87\%$ discount rate, whereas peer multiples are inflated by high-growth mid-caps (Persistent Systems at `39.4x` EV/EBITDA; Coforge at `30.6x`). Even against pure-play Tier-1 peers (TCS `11.7x`, HCLTech `14.0x`, Wipro `10.7x`), Infosys at `9.2x` screens attractively valued.
* **The ROE Paradox:** Despite a $180\text{ bps}$ contraction in net profit margin since FY20, ROE climbed $+576\text{ bps}$ to **$31.21\%$**, engineered through superior asset turnover ($1.03\text{x} \rightarrow 1.18\text{x}$) and non-interest-bearing operating leverage (equity multiplier $1.35\text{x} \rightarrow 1.60\text{x}$).

📄 **Read the full analytical memo and model critique in [`KEY_INSIGHTS.md`](./KEY_INSIGHTS.md).**

---

## ⚠️ Disclaimer

*This financial model and accompanying research documentation were developed strictly for educational and portfolio demonstration purposes. They do not constitute investment advice, a solicitation, or a recommendation to buy or sell any security. Consult a SEBI-registered investment advisor before making financial decisions.*