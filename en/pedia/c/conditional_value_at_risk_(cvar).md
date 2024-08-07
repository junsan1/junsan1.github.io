# Conditional Value at Risk (CVaR)

Conditional [Value](../v/value.md) at [Risk](../r/risk.md) (CVaR), also known as Expected [Shortfall](../s/shortfall.md) (ES), is a [risk](../r/risk.md) assessment metric commonly used in [finance](../f/finance.md) and [economics](../e/economics.md) to measure the [risk](../r/risk.md) of loss in investments and portfolios. CVaR is particularly useful in scenarios where the [distribution](../d/distribution.md) of returns is not normal and is skewed. It provides a more comprehensive [risk](../r/risk.md) measure than the traditional [Value](../v/value.md) at [Risk](../r/risk.md) (VaR) by focusing not only on the threshold [value](../v/value.md) but also on the average losses that occur beyond this threshold.

### Introduction to CVaR

Conditional [Value](../v/value.md) at [Risk](../r/risk.md) can be described as the expected loss given that a loss is beyond the [Value](../v/value.md) at [Risk](../r/risk.md) (VaR) threshold. Unlike VaR, which only provides the maximum potential loss over a certain period for a given confidence level, CVaR gives an idea of the severity of losses in the tail end of the [distribution](../d/distribution.md). This makes CVaR a more sensitive and informative measure in the context of extreme [market](../m/market.md) events.

### Mathematical Definition

Mathematically, let \( L \) be a random variable representing the loss. The [Value](../v/value.md) at [Risk](../r/risk.md) at a confidence level \( \[alpha](../a/alpha.md) \) (typically 95% or 99%) is defined as:

\[ VaR_{\[alpha](../a/alpha.md)} = \inf \{ l \in \mathbb{R} : P(L > l) \leq 1 - \[alpha](../a/alpha.md) \} \]

The Conditional [Value](../v/value.md) at [Risk](../r/risk.md) at the same confidence level \( \[alpha](../a/alpha.md) \) is then defined as the [expected value](../e/expected_value.md) of the loss given that it exceeds \( VaR_{\[alpha](../a/alpha.md)} \):

\[ CVaR_{\[alpha](../a/alpha.md)} = E[L | L > VaR_{\[alpha](../a/alpha.md)}] \]

### Why Use CVaR?

1. **Better [Tail Risk](../t/tail_risk.md) Measurement**: CVaR provides a more accurate measure of potential extreme losses, particularly in non-normal distributions which are common in [financial markets](../f/financial_market.md).
2. **Regulatory Compliance**: Regulatory bodies like Basel Committee on Banking Supervision (BCBS) recommend using CVaR for [risk management](../r/risk_management.md) in banks and financial institutions.
3. **[Robust](../r/robust.md) [Risk Management](../r/risk_management.md)**: By considering the average loss beyond a certain point, CVaR helps in creating more resilient [risk management](../r/risk_management.md) strategies.

### Calculation of CVaR

Calculating CVaR typically involves the following steps:

1. **Determine VaR**: Calculate the [Value](../v/value.md) at [Risk](../r/risk.md) at the chosen confidence level.
2. **Tail Loss Calculation**: Identify the losses that exceed the VaR threshold.
3. **Average Calculation**: Compute the average of these tail losses to arrive at the CVaR.

#### Example Calculation

Assume you have the following hypothetical [loss distribution](../l/loss_distribution.md) for an investment portfolio over a specific period:

\[ \{-2\%, -1.5\%, -1\%, -0.5\%, 0\%, 0.5\%, 1\%, 1.5\%, 2\%, 2.5\%, 3\%, 3.5\%, 4\%, 4.5\%, 5\%, 5.5\%, 6\%, 6.5\%, 7\%, -10\% \} \]

If you want to calculate the CVaR at the 95% confidence level:

1. **Determine VaR**: Sort the losses in ascending [order](../o/order.md) and find the 95% percentile. In this case, VaR (95%) might be around the 19th loss when the sorted list is reviewed, \( VaR_{95\%} = 5.5\% \).
2. **Tail Loss Calculation**: Identify losses that exceed this VaR. Here, it would be the single largest loss, \(-10\% \).
3. **Average Calculation**: The CVaR (95%) would be the average of all losses beyond the VaR threshold:
\[ CVaR_{95\%} = (-10\%) = -10\% \]

### CVaR in Modern Financial Practices

CVaR is widely used in various financial applications, including [portfolio optimization](../p/portfolio_optimization.md), [risk management](../r/risk_management.md), and regulatory reporting.

#### Portfolio Optimization

In [portfolio optimization](../p/portfolio_optimization.md), CVaR is used to create portfolios that not only maximize returns but also minimize extreme losses. By incorporating CVaR into the [optimization](../o/optimization.md) process, investors can achieve a better balance between [risk](../r/risk.md) and [return](../r/return.md).

#### Risk Management

Banks and financial institutions use CVaR to assess and manage the [risk](../r/risk.md) of loss from their trading activities. By focusing on [tail risk](../t/tail_risk.md), they can prepare more effectively for potential financial downturns.

#### Regulatory Reporting

Regulations often require financial institutions to report [risk measures](../r/risk_measures.md). The [Basel III](../b/basel_iii.md) framework, for instance, recommends using CVaR for determining [capital](../c/capital.md) reserves.

### Tools and Software for CVaR Calculation

Several tools and [software platforms](../s/software_platforms_for_trading.md) facilitate CVaR calculation, including:

- **RiskMetrics**: RiskMetrics provides comprehensive [risk](../r/risk.md) analytics tools, including CVaR calculation (https://www.msci.com/riskmetrics-analytics).
- **MATLAB**: MATLAB offers various financial toolboxes that can calculate CVaR for different [asset](../a/asset.md) classes (https://www.mathworks.com/products/financial.html).
- **R Programming**: The `PerformanceAnalytics` package in R can be used for [financial risk](../f/financial_risk.md) assessment, including CVaR computation (https://cran.r-project.org/web/packages/PerformanceAnalytics/[index](../i/index_instrument.md).html).

### Conclusion

Conditional [Value](../v/value.md) at [Risk](../r/risk.md) (CVaR) provides a deeper understanding of potential extreme losses in a portfolio by considering the average losses beyond a certain confidence threshold. As [financial markets](../f/financial_market.md) become more complex and unpredictable, CVaR stands out as a crucial tool for investors and [risk](../r/risk.md) managers to mitigate and manage financial risks effectively. From [portfolio optimization](../p/portfolio_optimization.md) to regulatory compliance, the application of CVaR spans [multiple](../m/multiple.md) facets of modern financial practices, making it an indispensable measure in today's [risk management](../r/risk_management.md) toolbox.