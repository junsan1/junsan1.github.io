# Weighted Median

In the realm of [algorithmic trading](../a/algorithmic_trading.md), various statistical measures are employed to make data-driven decisions. One such measure is the "[weighted](../w/weighted.md) [median](../m/median.md)," which extends the concept of a [median](../m/median.md) to [weighted](../w/weighted.md) data points. This sophisticated concept is essential for certain financial models and algorithms that prioritize some data points over others based on their significance or reliability.

## Definition

The [weighted](../w/weighted.md) [median](../m/median.md) is a [value](../v/value.md) that separates the higher half from the lower half of a dataset, with each data point assigned a specific weight. Unlike the simple [median](../m/median.md)—where each data point has an equal importance—the [weighted](../w/weighted.md) [median](../m/median.md) gives more influence to certain data points based on their assigned weights.

Formally, given a set of values \(x_1, x_2, ..., x_n\) and corresponding non-negative weights \(w_1, w_2, ..., w_n\), the [weighted](../w/weighted.md) [median](../m/median.md) is a [value](../v/value.md) \(x_m\) such that the following conditions [hold](../h/hold.md):

1. The sum of weights for values less than \(x_m\) is less than or equal to half the total weight.
2. The sum of weights for values greater than \(x_m\) is less than or equal to half the total weight.

Mathematically, it can be expressed as:
\[ \sum_{x_i < x_m} w_i \leq \frac{W}{2} \quad \text{and} \quad \sum_{x_i > x_m} w_i \leq \frac{W}{2} \]
where \(W = \sum_{i=1}^{n} w_i\) is the total weight of all data points.

## Calculation

The algorithm to compute the [weighted](../w/weighted.md) [median](../m/median.md) involves the following steps:

1. **Sort the Data**: Arrange the data points in ascending [order](../o/order.md).
2. **Compute the Cumulative Weights**: Calculate cumulative weights for the sorted data points.
3. **Identify the [Median](../m/median.md)**: Find the point where the cumulative weight is closest to half of the total weight.

Let’s consider an example with data points and weights:
- Data points: \([2, 4, 5, 8, 10]\)
- Weights: \([1, 2, 1, 2, 3]\)

First, sort the data points and their corresponding weights:
- Sorted data points: \([2, 4, 5, 8, 10]\)
- Sorted weights: \([1, 2, 1, 2, 3]\)

Next, calculate the cumulative weights:
- Cumulative weights: \([1, 3, 4, 6, 9]\)

The total weight \(W\) is 9. The [weighted](../w/weighted.md) [median](../m/median.md) is the data point where the cumulative weight reaches or exceeds \(W/2 = 4.5\). In this case, it’s 8.

## Applications in Algorithmic Trading

The [weighted](../w/weighted.md) [median](../m/median.md) is particularly useful in the [finance](../f/finance.md) domain for various tasks, such as:

### 1. Robust Portfolio Optimization
Investment portfolios often contain assets with varying levels of [risk](../r/risk.md) and [return](../r/return.md). The [weighted](../w/weighted.md) [median](../m/median.md) can help in constructing a [robust](../r/robust.md) portfolio by placing more emphasis on reliable assets with higher weights. This assists in minimizing the impact of outlier data points or assets with lower reliability.

### 2. Outlier Detection
In [trading algorithms](../t/trading_algorithms.md), outlier detection is crucial for preventing anomalies from skewing analysis. The [weighted](../w/weighted.md) [median](../m/median.md) is a [robust](../r/robust.md) measure more resilient to outliers compared to the mean. If certain trades or data points have higher confidence, they are assigned greater weight, thereby reducing the [noise](../n/noise.md) from less reliable data.

### 3. Signal Smoothing
[Trading signals](../t/trading_signals.md) often exhibit [volatility](../v/volatility.md). By considering [weighted](../w/weighted.md) data points, the [weighted](../w/weighted.md) [median](../m/median.md) smooths these signals, making it easier to discern the [underlying](../u/underlying.md) trends. This contributes to more consistent and accurate trading decisions.

### 4. Risk Management
Different financial instruments have varying degrees of [risk](../r/risk.md) associated with them. By applying weights corresponding to [risk](../r/risk.md) levels, the [weighted](../w/weighted.md) [median](../m/median.md) helps in making informed decisions about [risk](../r/risk.md) exposure, leading to better [risk](../r/risk.md)-adjusted returns.

## Algorithms and Implementations

Several algorithms can compute the [weighted](../w/weighted.md) [median](../m/median.md) efficiently, ranging from simple sorting-based methods to more sophisticated approaches. Below are some common methods:

### Simple Sorting-Based Algorithm
This algorithm follows the steps mentioned in the calculation section and typically has a time complexity of \(O(n \log n)\) due to the sorting step.

### Partition-Based Algorithm (Quickselect)
This algorithm leverages the partition-based selection method, similar to Quickselect used for finding the k-th smallest element. It has an average-case time complexity of \(O(n)\) but can be more complex to implement.

### Heaps and Balanced Trees
Data structures like heaps and balanced binary search trees may also be used to maintain data points and their cumulative weights dynamically. These structures allow efficient insertion, deletion, and [median](../m/median.md) finding, especially useful for real-time applications in [algorithmic trading](../a/algorithmic_trading.md).

## Pseudocode: Sorting-Based Algorithm

Below is a simplified pseudocode for calculating the [weighted](../w/weighted.md) [median](../m/median.md) using the sorting-based method:

```plaintext
function weightedMedian(values, weights):
    // Zip and sort values based on data points
    zippedData = zip(values, weights).sortByValue()
    
    // Calculate total weight
    totalWeight = sum(weights)
    halfWeight = totalWeight / 2
    
    // Iterate through sorted data to find [weighted](../w/weighted.md) [median](../m/median.md)
    cumulativeWeight = 0
    for ([value](../v/value.md), weight) in zippedData:
        cumulativeWeight += weight
        if cumulativeWeight >= halfWeight:
            [return](../r/return.md) [value](../v/value.md)
```

## Practical Considerations

### Data Preprocessing
Ensure that weights are non-negative and that the sum of weights is positive. This preprocessing is vital because negative weights or zero total weight invalidate the [weighted](../w/weighted.md) [median](../m/median.md) calculation.

### Numerical Stability
When dealing with floating-point numbers, be wary of precision issues. Implement safeguards for cumulative weight calculations to avoid floating-point arithmetic errors.

### Performance Optimization
For large datasets, consider optimizing the [weighted](../w/weighted.md) [median](../m/median.md) computation using more efficient data structures and algorithms, especially in high-frequency trading where speed is critical.

## References and Further Reading

For an in-depth understanding and advanced methods, consult the following resources:
- [Quantitative Portfolio Management](https://quantitative-portfolio-management.com)
- [Algorithmic Trading Insights from QuantInsti](https://www.quantinsti.com/blog/algorithmic-trading)
- [Risk and Portfolio Management](https://www.riskportfolio.com)

In summary, the [weighted](../w/weighted.md) [median](../m/median.md) is a powerful statistical measure, enhancing the robustness and reliability of [trading algorithms](../t/trading_algorithms.md) by giving priority to more significant data points. Its applications in [portfolio management](../p/portfolio_management.md), outlier detection, [signal processing](../s/signal_processing_in_trading.md), and [risk management](../r/risk_management.md) make it an indispensable tool in the algorithmic [trader](../t/trader.md)'s toolkit.
