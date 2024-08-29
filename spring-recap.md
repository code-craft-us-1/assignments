# Recap of starter

## double or float

```cpp
Stats Statistics::ComputeStatistics(const std::vector<___>& )
```

## Rationale for epsilon

>Why can't we check equality?

```cpp
TEST(Statistics, ReportsAverageMinMax) {
    auto computedStats = Statistics::ComputeStatistics({1.5, 8.9, 3.2, 4.5});
    float epsilon = 0.001; // Why this number?
    EXPECT_LT(std::abs(computedStats.average - 4.525), epsilon);
    EXPECT_LT(std::abs(computedStats.max - 8.9), epsilon);
    EXPECT_LT(std::abs(computedStats.min - 1.5), epsilon);
}
```
