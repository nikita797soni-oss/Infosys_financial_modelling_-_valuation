# Investment Memo & Key Analytical Insights: Infosys Limited (NSE: INFY)
An investment memo built from the Excel financial model in this repository. It explains what the numbers say, why the valuation methods disagree, and where the model is weak.

**Valuation date:** 13 November 2026 | **Reference price:** ₹1,151 | **Currency:** INR, crore unless stated | **Financial year ends:** 31 March

> Educational project. Not investment advice. See the disclaimer at the end.

---


## 1. Bottom Line

| Method | Value per share | Versus ₹1,151 |
|---|---|---|
| Base-case DCF (WACC 12.87%, terminal growth 4%) | ₹918.48 | -20.2% |
| DCF base range (terminal growth 3% to 7%) | ₹855.85 to ₹1,235.08 | -25.6% to +7.3% |
| Peer-median EV/Revenue | ₹1,326 | +15.2% |
| Peer-median P/E | ₹1,777 | +54.4% |
| Peer-median EV/EBITDA | ₹1,974 | +71.5% |
| Large-cap peer P/E (16.8x x LTM EPS ₹75.8) | ₹1,273 | +10.6% |
| 52-week trading range | ₹980.40 to ₹1,728.00 | |

**Reading:** the market price sits between the DCF and the multiples. Infosys is a high-quality, cash-rich business that the model cannot call clearly cheap or clearly expensive. A blend of the DCF and the large-cap P/E value gives roughly ₹1,095, within about 5% of the price (see `Infosys_Equity_Research_Report.pdf`).

---

## 2. Why the DCF and the Comps Disagree

**The DCF is low because of two things: a high discount rate and a terminal-value-heavy structure.**

- WACC is 12.87% (cost of equity 13.22%). Debt is only 3.55% of capital, so WACC is essentially the cost of equity.
- About 69.9% of operating value (₹251,664 cr of ₹360,137 cr) comes from the terminal value, so small changes in WACC or terminal growth move the answer a lot.

**The comps are high because the peer set is skewed.**

| Company | EV/EBITDA | P/E |
|---|---|---|
| Infosys | 9.2x | 15.0x |
| TCS | 11.7x | 16.8x |
| HCL Technologies | 14.0x | 20.4x |
| Wipro | 10.7x | 14.6x |
| Tech Mahindra | 20.5x | 31.0x |
| LTIMindtree | 16.1x | 24.3x |
| Persistent Systems | 39.4x | 55.2x |
| Coforge | 30.6x | 42.8x |
| Oracle Financial Services | 16.5x | 24.2x |
| Mphasis | 16.2x | 23.4x |
| **Peer median (model)** | **16.1x** | **23.4x** |

- The median is pulled up by high-growth mid-caps (Persistent, Coforge). Against the three large-cap peers (TCS, HCL, Wipro), EV/EBITDA is 10.7x to 14.0x and Infosys at 9.2x still looks inexpensive, but the gap is much smaller than the headline suggests.
- The model's peer statistics include Infosys itself. Excluding it would be cleaner.

**Takeaway:** neither method is "right". The DCF says the price already assumes more than the base-case cash flows deliver at a 12.87% discount rate. The multiples say Infosys is cheap against peers that are growing faster. Both statements can be true.

---

## 3. What Drives the DCF

### Valuation bridge

| Item | ₹ crore |
|---|---|
| PV of FCFF, FY27E to FY31E | 108,473 |
| PV of terminal value | 251,664 |
| Operating asset value | 360,137 |
| Add: cash and bank | 22,201 |
| Less: lease liabilities | (9,176) |
| Equity value | 373,162 |
| Shares (crore) | 406.28 |
| **Value per share** | **₹918.48** |

### Sensitivity (value per share, ₹)

| Terminal growth \ WACC | 11.00% | 12.87% | 15.00% | 18.00% |
|---|---|---|---|---|
| 3.00% | 986 | 856 | 757 | 666 |
| 4.00% (base) | 1,084 | 919 | 799 | 692 |
| 5.38% | 1,277 | 1,033 | 871 | 735 |
| 6.00% | 1,399 | 1,099 | 910 | 757 |
| 7.00% | 1,673 | 1,235 | 986 | 799 |

**Insights**

- The ₹1,151 price is reached only at an 11% WACC with terminal growth of 5.38% or more, or at the base WACC with 7% terminal growth.
- At 4% terminal growth, moving WACC from 12.87% to 11% adds about ₹166 per share; moving to 15% removes about ₹120.
- Discount rate matters more than any single-year forecast.

---

## 4. The Margin Story

| Metric | FY17 | FY26 | Change |
|---|---|---|---|
| Gross margin | 34.86% | 28.21% | -665 bps |
| Operating EBITDA margin (before other income) | 27.2% | 23.7% | -3.5 points |
| Net profit margin | 21.0% | 16.5% | -4.5 points |

- **Cause:** other manufacturing expenses (subcontracting and pass-through costs) rose from 9.8% to 18.4% of sales. Employee cost stayed between 52.6% and 56.1% of sales.
- **Offsets:** selling and administrative cost fell from 6.7% to about 3.8% of sales, and tax as a share of sales fell from 8.2% to 5.9%, cushioning the net margin.
- **Implication:** growth has been bought with lower-margin work. The 20% to 22% operating margin guidance range leaves little room for margin-led upside.

---

## 5. The ROE Paradox (DuPont)

ROE rose from 25.45% to 31.21% between FY20 and FY26, even though the net margin fell.

| | FY20 | FY21 | FY22 | FY23 | FY24 | FY25 | FY26 |
|---|---|---|---|---|---|---|---|
| Net profit margin | 18.3% | 19.3% | 18.2% | 16.4% | 17.1% | 16.4% | 16.5% |
| Asset turnover | 1.03x | 1.01x | 1.09x | 1.22x | 1.18x | 1.15x | 1.18x |
| Equity multiplier | 1.35x | 1.41x | 1.48x | 1.60x | 1.59x | 1.54x | 1.60x |
| **ROE** | **25.45%** | **27.29%** | **29.15%** | **31.97%** | **32.08%** | **29.05%** | **31.21%** |
| ROA | 18.87% | 19.42% | 19.72% | 19.97% | 20.13% | 18.82% | 19.49% |

**Insights**

- Margin was a drag (about -180 bps). Asset turnover (+0.15x) and the equity multiplier (+0.25x) did the work.
- The leverage is not financial debt. The only borrowings are lease liabilities (₹9,176 cr). The multiplier rose because other liabilities grew from ₹21,717 cr (FY20) to ₹52,260 cr (FY26).
- ROA has been stable at roughly 19% to 20%, so asset profitability itself has not changed much.
- A high ROE built partly on operating liabilities is less durable than one built on margin.

---

## 6. Cash Quality and Balance Sheet

| FY26 | ₹ crore |
|---|---|
| Operating cash flow | 33,986 |
| Capital expenditure | 2,727 |
| Free cash flow | 31,259 |
| Dividends paid | 18,656 |
| Cash and bank | 22,201 |
| Investments | 21,880 |
| Lease liabilities | 9,176 |

- Operating cash flow was 115% of net profit and free cash flow 106%, so earnings are well backed by cash.
- Dividends absorbed about 60% of free cash flow, leaving room for acquisitions or buybacks.
- **Watch points:** receivables rose from 14.8% to 22.8% of total assets and debtor days from 66 to 72. Cash and bank fell from 27% to 14% of assets over FY17 to FY26 as more cash moved into investments and receivables.

---

## 7. Cost of Capital: Strengths and Weaknesses

| Input | Value | Comment |
|---|---|---|
| Risk-free rate | 7.21% | Model input |
| Equity risk premium | 7.94% | 26-year average market return (15.15%) less risk-free rate |
| Beta used | 0.76 | Peer-median unlevered 0.74 relevered at 3.68% D/E |
| Cost of equity | 13.22% | CAPM |
| Pre-tax / post-tax cost of debt | 4.88% / 3.42% | FY26 interest divided by debt; 30% tax |
| WACC | 12.87% | 96.45% equity, 3.55% debt |

**Beta evidence**

- Own regression beta: 0.90 (95% confidence interval 0.73 to 1.07), Blume-adjusted 0.92, R² 17.67%, n = 496.
- The model uses the peer-based 0.76 because single-stock betas are noisy. Using 0.92 instead would raise the cost of equity to about 14.5% and lower the DCF further.

**Critique**

- A 7.94% premium built from a long-run average return that includes swings of -52% (2008) and +76% (2009) is a blunt estimate.
- Tax is 30% in the WACC but 25% in the DCF.
- A WACC near 12.9% is high for a net-cash company; most of the DCF-versus-price gap is a discount-rate question.

---

## 8. Forecasting Critique

- **Sales regression (FY15 to FY26, n = 12):** R² 96.39%, F-statistic 267.09, p = 1.53 x 10^-8. It forecasts FY27E to FY30E sales of ₹184,695 cr, ₹196,540 cr, ₹208,385 cr and ₹220,230 cr.
- A linear trend adds a fixed rupee amount each year, so implied percentage growth fades (3.4% in FY27E to 5.7% in FY30E). That is a transparent baseline but not a view on the business.
- **Blind spots:** it cannot see guidance, currency moves or AI-driven price deflation. A weaker rupee lifts rupee revenue far more than dollar revenue, so rupee-based trends can overstate underlying demand.
- The DCF does not use the regression forecasts. It grows EBIT at 9.5% a year from reinvestment rate x ROIC, which makes it independent of the regression but dependent on a volatile input (see section 10).

---

## 9. Business Risks and Catalysts

**Risks**

- Growth: guidance for FY27 is 1% to 2% in constant currency, cut more than once during the year.
- AI-led price deflation in traditional services across the sector.
- Weakness in retail, hi-tech and manufacturing; North America (over half of revenue) is shrinking.
- Wage inflation and pricing pressure compressing the 20% to 22% margin band.
- US policy: tariffs, immigration rules and visa programmes.

**Catalysts**

- Large deals converting to revenue (Q2 FY27 large-deal value was US$5.2 billion, 62% net new).
- AI-led revenue scaling (10.5% of revenue in Q2 FY27).
- Capital return and a weaker rupee.

---

## 10. Model Critique and Known Limitations

An honest list of issues, in rough order of importance.

1. **Terminal cash flow is grown at the wrong rate.** The FY32 cash flow used for the terminal value (₹38,518 cr) is the FY31 figure grown at the 9.5% explicit rate, not the 4% terminal rate. Correcting it lowers the DCF to about ₹888 per share (about 3% lower).
2. **9.5% EBIT growth is above guidance.** It exceeds 1% to 2% constant-currency guidance and is supported near term by rupee depreciation, so the DCF should not be called conservative.
3. **Growth and reinvestment inputs are provisional.** The 9.5% growth and 26.2% reinvestment rate are four-year medians of a series that swings from -9% to +18%, and they depend on EBIT figures that are being refreshed.
4. **EBIT definition.** Base EBIT (₹40,377 cr) appears to include other income (about 1.7% of sales) while cash is also added in the equity bridge.
5. **Income statement rows need correction.** In the current workbook, lines below gross profit for FY17 to FY25 contain errors (for example negative EBITDA in early years). The reports in this repository rebuild those lines from the common-size statement. EBITDA and EPS trend projections should be re-run once the workbook is corrected.
6. **Working capital ratios.** Payable days are measured on total other liabilities, which flatters the cash conversion cycle. On trade payables alone (₹4,744 cr), FY26 payable days would be about 13, not 107.
7. **Comps.** Peer statistics include Infosys itself, and the peer set mixes large caps with high-growth mid-caps.
8. **Consistency.** Reference prices differ across sheets (₹1,142 to ₹1,181) because of capture dates, and net cash is ₹13,025 cr in the DCF bridge but ₹13,676 cr in the comps sheet.

---

## 11. What Would Change the View

| Evidence | Direction |
|---|---|
| Constant-currency growth sustained above about 3% with margin at or above 21% | More positive |
| Share price falling toward ₹950 to ₹1,000 | More positive (the blended value implies a double-digit return) |
| Further guidance cuts with margin below 20% | More negative |
| Large-deal pipeline failing to convert into revenue | More negative |
| A lower, defensible WACC (11% to 12%) | DCF moves toward the market price |
| Peer multiples de-rating | Comps value moves toward the market price |

---

## 12. How to Improve the Model

- Fix the terminal-value growth rate and re-run the DCF.
- Correct the FY17 to FY25 income statement rows and re-run EBITDA, EPS and ROIC.
- Separate other income from EBIT.
- Use one tax rate and one net cash figure throughout.
- Exclude Infosys from its own peer statistics and add a size-matched peer subset.
- Add scenario analysis with explicit growth and margin paths, Value-at-Risk (historical and Monte Carlo) and an Altman Z-score.
- Replace the single reference price with a dated price series.

---

## Data Sources

Screener (financial statements, sales history, peer market data), NSE (daily prices, Nifty 50 returns), company filings and press releases, and the author's Excel model.

## Disclaimer

This memo was developed strictly for educational and portfolio demonstration purposes. It does not constitute investment advice, a solicitation, or a recommendation to buy or sell any security. Consult a SEBI-registered investment adviser before making financial decisions.
