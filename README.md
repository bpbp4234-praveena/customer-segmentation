# Customer Segmentation Project

Segmenting mall customers based on demographics and spending behavior using K-Means clustering and a Power BI dashboard.

## Objective
Group customers into meaningful segments so the business can run targeted marketing campaigns.

## Dataset
Mall Customers dataset (200 customers).

| Column | Description |
|---|---|
| CustomerID | Unique customer ID |
| Genre | Male / Female |
| Age | Customer age |
| Income | Annual income (k$) |
| SpendingScore | Score from 1-100 assigned by the mall |

Gender split: 112 Female, 88 Male.

## Approach
1. Loaded and explored the data.
2. Applied K-Means clustering (k = 5) on Income and Spending Score.
3. Named each segment based on its average income and spending.
4. Built an interactive Power BI dashboard with slicers for Genre and Age.

## Segments and Key Findings

| Segment | Customers | Avg Age | Avg Income (k$) | Avg Spending Score |
|---|---|---|---|---|
| Average customers | 81 | 42.7 | 55.3 | 49.5 |
| Premium Customers | 39 | 32.7 | 86.5 | 82.1 |
| Untapped Potential | 35 | 41.1 | 88.2 | 17.1 |
| Budget savers | 23 | 45.2 | 26.3 | 20.9 |
| Enthusiastic Spenders | 22 | 25.3 | 25.7 | 79.4 |

- Average customers are the largest group (about 40% of all customers).
- Premium Customers are younger (avg 33) with high income and high spending.
- Untapped Potential customers earn as much as Premium Customers but spend very little, so they are the biggest growth opportunity.
- Enthusiastic Spenders are the youngest group (avg 25) and spend a lot despite low income.
- Budget savers are the oldest group (avg 45) with low income and low spending.

## Recommendations

| Segment | Strategy |
|---|---|
| Premium Customers | Loyalty programs, exclusive offers, early access to new products |
| Untapped Potential | Personalized marketing, targeted campaigns to increase spending |
| Budget savers | Discounts, value bundles |
| Enthusiastic Spenders | EMI and credit-based offers, trendy products |
| Average customers | Upsell and cross-sell |

## Dashboard
See `dashboard.png` for the Power BI dashboard.

Visuals: scatter plot (Income vs Spending Score), segment distribution donut chart, segment by gender, average age by segment, average spending score by segment, summary table, and Genre and Age slicers.

## Limitations
- The dataset has no purchase history, so Spending Score is used as a proxy for purchase behavior.
- Clustering used only Income and Spending Score. Age and Gender were used for profiling the segments.
- Dataset is small (200 customers).

## Tools Used
- Power BI
- Python (scikit-learn) for K-Means validation
- GitHub

## Files
- `Mall_Customers.csv`: original dataset
- `Mall_Customers_with_Segment_AgeGroup.csv`: dataset with Segment and Age Group
- `dashboard.png`: dashboard screenshot
