# X-Y Scatter Plot

An X-Y Scatter Plot, also known as a scatter diagram or scatter graph, is a type of plot or mathematical diagram that uses Cartesian coordinates to display values typically for two variables which are usually denoted as "X" and "Y". The purpose of using a scatter plot is to observe and show relationships between two numerical variables. When the data points are represented on the graph, patterns might emerge that suggest the nature of the relationship (if any) between the variables.

## Key Components

- **X-Axis (Horizontal Axis):** This is the [horizontal line](../h/horizontal_line.md) on the graph which typically represents the independent variable.
- **Y-Axis (Vertical Axis):** This is the vertical line on the graph which typically represents the dependent variable.
- **Data Points:** Each data point represents a pair of values corresponding to the X and Y variables and is plotted on the graph.
- **Title and Labels:** The graph typically includes a title that explains what is being represented, along with labels for both the X and Y axes to provide context for the values shown.

## Purpose and Uses

X-Y scatter plots are widely used for various purposes including:

- **Identifying Correlations:** Scatter plots can help determine if there is a relationship or [correlation](../c/correlation.md) between two variables. For example, does an increase in one variable lead to an increase or decrease in the other?
- **Detecting Outliers:** Points that deviate significantly from the overall pattern of the data can often be identified as outliers through scatter plots.
- **Data Trends:** Scatter plots can help in identifying [underlying](../u/underlying.md) trends, clusters, and patterns that might not be obvious in raw data.

## Interpretation

### Positive Correlation

A [positive correlation](../p/positive_correlation.md) is when the values of both variables increase together. This is indicated on the scatter plot by data points that [trend](../t/trend.md) upwards from the lower-left to the upper-right.

### Negative Correlation

A [negative correlation](../n/negative_correlation.md) is when one variable increases as the other decreases. This is shown on the scatter plot by data points that [trend](../t/trend.md) downwards from the upper-left to the lower-right.

### No Correlation

When there is no apparent relationship between the variables, the data points [will](../w/will.md) be scattered randomly with no discernible pattern.

## Technical Applications in Algo-Trading

In the context of algo-trading ([algorithmic trading](../a/algorithmic_trading.md)), X-Y scatter plots are particularly useful for:

1. **Pair [Trading Strategies](../t/trading_strategies.md):** Scatter plots can help identify the [linear relationship](../l/linear_relationship.md) between two securities. Traders can model the spread of two correlated securities and plot their prices to identify mispricings.
2. **Assessing Accuracy of [Trading Models](../t/trading_models.md):** Traders verify predicted versus actual trading results by plotting them on scatter graphs to see how closely their models follow [market](../m/market.md) patterns.
3. **Parameter [Optimization](../o/optimization.md):** When tuning algorithm parameters, scatter plots illustrate the impact of different variables on [trading performance](../t/trading_performance.md) or [risk](../r/risk.md), aiding in visual convergence toward optimal settings.

## Example in Algorithmic Trading

### Moving Averages

In an example involving moving averages, an X-Y scatter plot could be used to examine the relation between the length of a moving average (X-axis) and the resultant profitability or [volatility](../v/volatility.md) (Y-axis). By doing so, traders can visually perceive which moving average lengths consistently [yield](../y/yield.md) better results.

### Financial Institutions and Tools

Several financial institutions and [algorithmic trading](../a/algorithmic_trading.md) platforms provide [robust](../r/robust.md) tools to generate X-Y scatter plots, some of which include:

1. **[Bloomberg](../b/bloomberg.md) Terminal:** A computerized system providing financial data widely used globally [Bloomberg Terminal](https://www.bloomberg.com/professional/solution/bloomberg-terminal/).
2. **Thomson [Reuters](../r/reuters.md) Eikon:** A professional-grade software suite for [financial analysis](../f/financial_analysis.md) [Thomson Reuters Eikon](https://www.refinitiv.com/en/products/eikon-trading-software).
3. **Python Libraries:** Tools such as `matplotlib` and `seaborn` in Python are powerful for creating scatter plots programmatically. For instance, matplotlib can be found at [Matplotlib](https://matplotlib.org/).

## Python Example

Using Python, scatter plots can be easily generated using the `matplotlib` library:

``` python
[import](../i/import.md) matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 35]

plt.scatter(x, y)
plt.title('Sample X-Y Scatter Plot')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.show()
```

## Conclusion

X-Y scatter plots are invaluable for visualizing the relationships between two variables, identifying correlations, trends, and outliers. In the domain of [algorithmic trading](../a/algorithmic_trading.md), they facilitate the assessment of [trading strategies](../t/trading_strategies.md), model validations, and parameter optimizations. Tools like [Bloomberg](../b/bloomberg.md) Terminal and Python's `matplotlib` [offer](../o/offer.md) sophisticated means to construct these plots, proving indispensable in data analysis workflows.
