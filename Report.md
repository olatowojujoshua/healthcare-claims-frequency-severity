Pure Premium Estimation & Risk Insights
Objective

The objective of this phase was to estimate the expected healthcare loss associated with inpatient services by integrating claim frequency and claim severity into a single actuarial metric known as the pure premium.

Methodology

Claim frequency was modeled using a Negative Binomial regression to address extreme overdispersion observed in discharge counts. Claim severity was modeled using a Gamma Generalized Linear Model with a log link, appropriate for strictly positive and right-skewed medical costs.

The expected loss was computed as:

Expected Loss
=
𝐸
(
Discharges
)
×
𝐸
(
Covered Charges
)
Expected Loss=E(Discharges)×E(Covered Charges)
Key Findings

The distribution of pure premium is highly right-skewed, with expected losses ranging from approximately 0.4 million to over 34 million.

A relatively small number of DRGs account for a disproportionate share of total expected losses, confirming significant risk concentration.

Geographic variation is evident, with certain states consistently exhibiting higher expected losses.

Business Implications

High-Risk DRGs:
These services require higher pricing margins, stronger utilization management, and potentially reinsurance support.

Low-Risk DRGs:
These services exhibit predictable costs and may be candidates for streamlined approval and competitive pricing.

Portfolio Management:
Separating frequency and severity provides a more accurate view of risk than aggregate averages, supporting better premium setting and reserve planning.

Conclusion

This analysis demonstrates that healthcare claims risk is best understood through a frequency–severity framework. The resulting pure premium estimates provide a robust, data-driven basis for pricing, capital allocation, and risk management decisions.
