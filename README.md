Here were 5 challenges I faced

1. Handling Invalid Input in Custom Functions
In the Z.prop.test() function, if users enter a proportion p1 or p2 that leads to np ≤ 5 or n(1−p) ≤ 5, the Z-test becomes unreliable. Handling these edge cases (e.g., through better error messages or fallback logic) is tricky and important.

2. Dealing with Missing or Invalid Data
The dataset may contain NA values or non-numeric entries. While na.omit() helps, it can silently drop rows, potentially biasing results if too much data is removed. Pre-cleaning or diagnostics may be necessary before modeling.

3. Log-Transforming Zero or Negative Values
Taking the log of MaxLongevity_m or Brain_Size_Species_Mean assumes all values are strictly positive. If any value is zero or negative, log() will return -Inf or NaN, breaking your linear model.

4. Confusing Prediction vs. Confidence Intervals
It’s easy to mix up confidence intervals (mean estimate range) with prediction intervals (individual outcome range). Both are plotted, but interpreting or reporting them correctly can be a challenge, especially in explanatory text or reports.

5. Hardcoded File Paths Limit Portability
Using absolute paths like "C:\\Users\\jzeng21\\Desktop\\..." makes your script break on other machines or systems. Switching to relative paths or prompting users to select a file dynamically would improve flexibility.
