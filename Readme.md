# Infosys Limited (NSE: INFY) — Institutional Equity Research & Valuation Model

[![Ticker](https://img.shields.io/badge/NSE-INFY%20%7C%20BSE%3A%20500209-0A66C2?style=flat-square)](https://www.nseindia.com)
[![Sector](https://img.shields.io/badge/Sector-Enterprise%20IT%20Services-2E4053?style=flat-square)]()
[![Valuation](https://img.shields.io/badge/Methodology-FCFF%20DCF%20%26%20Trading%20Comps-1E8449?style=flat-square)]()
[![Accounting](https://img.shields.io/badge/Analysis-10--Yr%20Historical%20%26%20DuPont-B7950B?style=flat-square)]()

> **Executive Thesis:** At a reference market price of **₹1,151**, Infosys Limited presents a classic **intrinsic-versus-relative valuation divergence**. While a conservative, fundamentals-driven Discounted Cash Flow (DCF) model yields an intrinsic value of **₹918.48/share** ($1.25\text{x}$ P/IV) due to near-term constant-currency growth moderation ($1\%–2\%$ FY27 guidance), the stock trades at a substantial discount (`9.2x` EV/EBITDA; `15.0x` P/E) relative to Indian IT sector medians (`16.1x` EV/EBITDA; `23.4x` P/E), implying **₹1,326–₹1,974/share** on a relative basis.

This repository houses a full-stack financial model, regression-based forecasting engine, multi-scenario valuation framework, and institutional-grade research report evaluating Infosys Limited across **FY15–FY32E**.

---

Executive Thesis

At a reference price of ₹1,151, Infosys shows a clear gap between intrinsic and relative value. The base-case DCF gives ₹918.48 per share (price is 1.25x the DCF value) because the model capitalises cash flows at a 12.87% WACC and near-term growth is moderating (FY27 guidance is 1% to 2% in constant currency). At the same time the stock trades at a discount to Indian IT peers (9.2x EV/EBITDA and 15.0x P/E against peer medians of 16.1x and 23.4x), which implies ₹1,326 to ₹1,974 per share on a relative basis.

Executive Valuation Summary
Metric	Figure	Context
Reference market price	₹1,151.00	52-week range ₹980.40 to ₹1,728.00
Intrinsic value (base DCF)	₹918.48	20.2% below the market price (WACC 12.87%, terminal growth 4.00%)
DCF scenario range	₹665.54 to ₹1,673.38	WACC 11% to 18%, terminal growth 3% to 7%
Relative valuation (peer medians)	₹1,326 to ₹1,974	+15.2% to +71.5% versus price, across EV/Revenue, P/E and EV/EBITDA
FY26 revenue	₹178,650 cr	+9.61% year on year; 11.2% CAGR over nine years (FY17 to FY26)
FY26 free cash flow	₹31,259 cr	106.2% of net profit; ₹18,656 cr paid as dividends
FY26 return on equity	31.21%	Up 576 bps since FY20 despite lower gross and net margins
Net cash (Mar-26)	₹13,025 cr	₹22,201 cr cash and bank less ₹9,176 cr lease liabilities; no bank debt. The comps sheet uses ₹13,676 cr.
Repository Contents
Infosys_FM_and_V.xlsx                                  Excel workbook: statements, forecasts, WACC, DCF, comps, DuPont
Infosys_FM_and_V.pdf                                   Printable copy of all workbook schedules
Report_Infosys_Financial_Modelling_DCF_Valuation.pdf   21-page financial modelling and valuation report
Infosys_Equity_Research_Report.pdf                     18-page equity research report (rating, target price, thesis)
KEY_INSIGHTS.md                                        Investment memo: DCF versus comps, DuPont, model critique
README.md                                              This file
Methodology
1. Historical analysis and common-size diagnostics (FY17 to FY26)
Ten-year income statement, balance sheet and cash flow schedules built from NSE and Screener data.
Common-size and trend analysis to isolate structural margin shifts, notably a 665 bps fall in gross margin (34.86% to 28.21%) as other manufacturing (subcontracting) costs rose from 9.8% to 18.4% of sales.
2. Forecasting
Ordinary least squares regression of sales (FY15 to FY26, n = 12) on a year index: R² = 96.39%, F-statistic = 267.09, p = 1.53 x 10^-8.
Linear-trend projections of operating EBITDA and EPS (see Known Limitations).
3. Cost of capital (WACC = 12.87%)
Beta: two years of daily NSE closing returns against the Nifty 50 (n = 496) give a raw beta of 0.90 and a Blume-adjusted beta of 0.92 (R² = 17.67%). Because single-stock betas are noisy, the model uses the peer-median unlevered beta of 0.74 (TCS, HCLTech, Wipro, Tech Mahindra), relevered at a target D/E of 3.68% to 0.76.
Cost of equity (CAPM): 13.22% (risk-free rate 7.21%, equity risk premium 7.94%, beta 0.76).
Cost of debt: 4.88% pre-tax, 3.42% after tax, at a 3.55% target debt weight.
4. Intrinsic growth and FCFF DCF
Sustainable growth estimated as reinvestment rate x ROIC, using four-year medians (26.20% reinvestment rate; 9.50% explicit EBIT growth).
Five explicit years of free cash flow to the firm (FY27E to FY31E), mid-year discounting, Gordon Growth terminal value (4.00%) and a 20-cell sensitivity grid. About 70% of operating value comes from the terminal value.
5. Relative valuation, football field and DuPont
Trading comparables against nine listed Indian IT services companies on EV/Revenue, EV/EBITDA and P/E.
Football field combining DCF scenarios, peer-multiple values and the 52-week range.
Three-step DuPont decomposition of ROE (31.21%) and ROA (19.49%) over FY20 to FY26.
Key Takeaways
Why DCF and comps disagree: the DCF uses a high 12.87% discount rate and moderating growth, while the full peer median is lifted by high-growth mid-caps (Persistent Systems 39.4x EV/EBITDA, Coforge 30.6x). Against large-cap peers (TCS 11.7x, HCLTech 14.0x, Wipro 10.7x), Infosys at 9.2x still screens inexpensive.
The ROE paradox: net profit margin fell about 180 bps since FY20 (18.28% to 16.48%), yet ROE rose 576 bps, driven by asset turnover (1.03x to 1.18x) and a higher equity multiplier (1.35x to 1.60x) from non-interest-bearing operating liabilities and leases.

See KEY_INSIGHTS.md for the full memo.

Known Limitations
The explicit-period EBIT growth of 9.5% is above near-term guidance of 1% to 2% constant currency; it is supported in rupee terms by currency depreciation, so the DCF should not be read as conservative.
The terminal-year cash flow is grown at the explicit-period rate rather than the 4% terminal rate; correcting this lowers the DCF value by about ₹30 per share.
Base EBIT appears to include other income while cash is also added in the equity bridge.
The reinvestment rate and intrinsic growth inputs come from a volatile four-year series (-9% to +18%) and depend on EBIT figures that are being refreshed.
Operating EBITDA and EPS projections depend on an income-statement series that is being corrected for FY17 to FY25.
Tax is 30% in the WACC and 25% in the DCF; peer statistics include Infosys itself; reference prices differ across sheets (₹1,142 to ₹1,181) because of capture dates.
Data Sources

Screener (financial statements, sales history, peer market data), NSE (daily prices, Nifty 50 returns), company filings and press releases, and the author's Excel model.

Disclaimer

This model and the accompanying research were developed strictly for educational and portfolio demonstration purposes. They do not constitute investment advice, a solicitation, or a recommendation to buy or sell any security. Consult a SEBI-registered investment adviser before making financial decisions.
