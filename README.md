# RZR_Data_Analysis

# Lead Quality Analysis

## Executive Summary

This analysis evaluated 3,021 leads generated for a debt relief advertiser to answer three key business questions:

1. Is lead quality improving or declining over time?
2. What factors are associated with higher-quality leads?
3. Are there opportunities to improve lead quality and justify a higher Cost Per Lead (CPL)?

Overall, the dataset produced a lead quality rate of 13.0% and a closed rate of 8.1%, exceeding the advertiser's target quality rate of 9.6%. While lead quality fluctuated week-to-week, statistical testing found no significant long-term trend. Instead, the largest opportunities appear to come from optimizing traffic sources, creative variations, verification quality, and customer debt profiles.

---

# Question 1: Are We Seeing Lead Quality Trends Over Time?

## Trend Analysis

Lead quality was evaluated on a weekly basis using the advertiser's definition of quality:

Good Lead Outcomes:

* Closed
* EP Sent
* EP Received
* EP Confirmed

Bad Lead Outcomes:

* Unable to Contact
* Invalid Profile
* Doesn't Qualify

Unknown Outcomes:

* All remaining statuses

Weekly lead quality rates ranged from approximately 7% to 25%, with noticeable short-term fluctuations.

To determine whether quality was improving or declining over time, a logistic regression model was fitted using lead creation date as the predictor variable.

## Findings

* Regression coefficient: +0.000289
* P-value: 0.790

Because the p-value is substantially greater than 0.05, there is no statistically significant evidence that lead quality improved or declined during the observed period.

### Conclusion

Lead quality appears relatively stable over time. Short-term fluctuations exist, but there is no meaningful upward or downward trend. Improving performance will likely require operational or targeting changes rather than simply waiting for natural improvement.

---

# Question 2: What Drives Lead Quality?

## Creative Performance (Widget Analysis)

Lead quality varied substantially across ad creative variations.

Top-performing widgets:

| Widget                   | Quality Rate |
| ------------------------ | ------------ |
| yellowarrow              | 24.5%        |
| CreditSolutions (300250) | 23.7%        |
| Standard 1DC             | 16.1%        |

Lowest-performing widget:

| Widget | Quality Rate |
| ------ | ------------ |
| Head3  | 6.7%         |

### Key Insight

Creative design appears to influence lead quality significantly. Certain creatives generate nearly four times the quality rate of the weakest-performing versions.

Recommendation:

* Increase traffic allocation to Yellow Arrow and Credit Solutions creatives.
* Reduce exposure to low-performing creative variants.

---

## Marketing Campaign Performance

Significant differences were observed across acquisition campaigns.

Top campaigns:

| Campaign           | Quality Rate |
| ------------------ | ------------ |
| Financial Services | 18.7%        |
| Debt Holding Tank  | 18.1%        |
| Debt Volume        | 16.1%        |

Lowest campaigns:

| Campaign         | Quality Rate |
| ---------------- | ------------ |
| Debt General     | 8.8%         |
| DebtReductionInc | 11.3%        |

### Key Insight

Campaign selection is a meaningful driver of lead quality.

Recommendation:

* Increase investment in Financial Services and Debt Holding Tank campaigns.
* Investigate why Debt General and DebtReductionInc underperform.

---

## Geographic Performance

Quality rates varied considerably by state.

Highest-performing states:

| State         | Quality Rate |
| ------------- | ------------ |
| Oklahoma      | 26.0%        |
| Hawaii        | 21.9%        |
| Massachusetts | 17.1%        |
| Alabama       | 16.8%        |

Large-volume state:

| State      | Quality Rate |
| ---------- | ------------ |
| California | 15.8%        |

### Key Insight

Certain states consistently outperform the overall average and may justify more aggressive bidding strategies.

Recommendation:

* Consider geographic bid adjustments favoring high-performing states.
* Continue investing in California due to strong quality and substantial lead volume.

---

## Verification Scores

### Address Score

Unexpectedly, AddressScore did not show a simple linear relationship with lead quality.

| Score | Quality Rate |
| ----- | ------------ |
| 2     | 18.4%        |
| 5     | 13.8%        |
| 4     | 4.2%         |

Because some groups have relatively small sample sizes, these results should be interpreted cautiously.

### Phone Score

Phone verification displayed a clearer pattern.

| Score | Quality Rate |
| ----- | ------------ |
| 5     | 16.2%        |
| 3     | 11.7%        |
| 2     | 10.0%        |
| 4     | 7.1%         |

### Key Insight

PhoneScore appears more predictive of lead quality than AddressScore.

Recommendation:

* Prioritize leads with strong phone verification signals.
* Further investigate AddressScore behavior before using it operationally.

---

## Debt Level Analysis

Debt level emerged as one of the strongest quality indicators.

Highest-performing debt ranges:

| Debt Range | Quality Rate |
| ---------- | ------------ |
| 70k-90k    | 19.1%        |
| 10k-15k    | 18.6%        |
| 20k-30k    | 15.9%        |

Lowest-performing debt ranges:

| Debt Range     | Quality Rate |
| -------------- | ------------ |
| More than 100k | 6.8%         |
| 7.5k-10k       | 7.0%         |

### Key Insight

Lead quality is not strictly increasing with debt size. Extremely high debt levels actually produced lower-quality leads.

Recommendation:

* Prioritize debt ranges between 10k and 90k.
* Review qualification and conversion challenges among consumers reporting more than 100k in debt.

---

# Question 3: Can We Increase Lead Quality?

## Current Performance

* Current Quality Rate: 13.0%
* Advertiser Target: 9.6%

The dataset already exceeds the advertiser's stated target quality rate.

However, opportunities still exist to further improve performance while maintaining volume.

## Recommended Actions

### High Priority

1. Shift traffic toward top-performing widget designs.
2. Increase investment in Financial Services and Debt Holding Tank campaigns.
3. Prioritize traffic sources with strong PhoneScore values.
4. Focus on debt ranges between 10k and 90k.
5. Increase exposure in high-performing states such as Oklahoma, Hawaii, Massachusetts, Alabama, and California.

### Medium Priority

1. Review underperforming widgets such as Head3.
2. Investigate Debt General campaign performance.
3. Conduct A/B testing on creative elements from Yellow Arrow and Credit Solutions designs.

### Low Priority

1. Further evaluate AddressScore reliability before using it as a major optimization factor.
2. Explore interactions between state, debt level, and campaign performance.

---

# Final Recommendation

The analysis suggests that lead quality is not changing meaningfully over time, but substantial differences exist across creatives, campaigns, debt levels, and verification scores.

Because the observed quality rate already exceeds the advertiser's 9.6% target, the primary opportunity is not simply increasing quality, but scaling volume through high-performing segments while maintaining existing quality standards.

The strongest opportunities appear to be creative optimization, campaign reallocation, and improved targeting based on debt level and verification quality.
