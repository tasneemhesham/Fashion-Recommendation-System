# Fashion-Recommendation-System
# Fashion Recommendation System

## Overview
The Fashion Recommendation System is designed to recommend the most trending fashion products based on user search queries. For example, if a user searches for "Kurti," the system will recommend the most trending or highly-rated Kurtis available on the platform. The system leverages a dataset of fashion products collected from Myntra to provide relevant recommendations.

## Dataset
The dataset used for building the recommendation system includes the following information about fashion products:

- **Brand Name**: The brand of the product.
- **Product URL**: A link to the product page on Myntra.
- **Image URL**: A link to the product image.
- **Ratings**: Ratings given to the product on Myntra.
- **Total Number of Ratings**: The total number of ratings the product has received.
- **Product Information**: Descriptive information about the product.
- **Selling Price**: The current selling price of the product.
- **Original Price**: The original price before any discounts.
- **Discount**: The discount applied to the product.

## Recommendation Strategy
To recommend the most trending fashion products, we use a weighted average of ratings rather than content-based filtering. Content-based filtering is useful for recommending similar products, but for trending recommendations, we use the following approach:

### Weighted Score Calculation
The weighted score of a product is calculated using the formula:

\[ \text{score} = \left(\frac{n}{n + m} \times a\right) + \left(\frac{m}{m + n} \times mr\right) \]

Where:
- \( n \) = Total number of ratings for the product
- \( m \) = Minimum number of ratings required to consider a product
- \( a \) = Average rating of the product
- \( mr \) = Mean rating of all products

### Process
1. **Calculate Mean Rating**: Compute the mean rating (mr) of all products in the dataset.
2. **Compute Weighted Scores**: For each product, calculate the weighted score using the above formula.
3. **Rank Products**: Rank products based on their weighted scores to recommend the top-rated or trending items.


