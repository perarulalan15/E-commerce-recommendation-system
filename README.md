# E-commerce Products Recommendation System

This project demonstrates a recommendation system for beauty products based on user ratings. The system uses collaborative filtering and matrix factorization techniques to suggest products that a user might like.

## Dataset

The dataset used is `ratings_Beauty.csv`, which contains user ratings for various beauty products. It includes the following columns:
- `UserId`: Unique identifier for each user.
- `ProductId`: Unique identifier for each product.
- `Rating`: Rating given by the user to the product.

## Steps

1. **Data Preprocessing**:
   - The data is loaded and cleaned by dropping missing values.
   - A subset of the data (`amazon_ratings1`) containing the first 10,000 rows is selected for processing.

2. **Utility Matrix**:
   - A utility matrix is created using a pivot table where rows represent users, columns represent products, and values are the ratings.

3. **Dimensionality Reduction**:
   - The utility matrix is transposed and subjected to Truncated SVD (Singular Value Decomposition) to reduce dimensionality.

4. **Correlation Matrix**:
   - A correlation matrix is computed from the decomposed matrix to find similar products.

5. **Product Recommendation**:
   - Given a product ID, the system recommends similar products with a high correlation score.

## Running the Code

1. Clone the repository and navigate to the project directory.
2. Ensure you have Python and the required libraries installed. You can install the dependencies using:
   ```bash
   pip install numpy pandas matplotlib scikit-learn
