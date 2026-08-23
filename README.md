## Amazon Product Recommendation System using NLP


### 🛍️ Introduction
This project is an NLP-based product search and recommendation system built using Amazon product data. It analyzes product titles and descriptions to identify products that are most relevant to a user's search query. The system uses text preprocessing, TF-IDF vectorization, and cosine similarity to calculate product relevance and rank the top matching products. A Streamlit interface provides an interactive way for users to search and explore recommended products.

### 🌐 Technologies Used

- Python
- Pandas
- NumPy
- NLTK
- Scikit-learn
- Streamlit
- Pillow


### 🧾 Installation

#### Clone the Repository
```
git clone https://github.com/archna13/Amazon-Product-Recommendation-System-using-NLP.git
```

#### Create a Virtual Environment
```
python -m venv .venv
```

#### Activate the Environment
```
.venv\Scripts\activate     # Windows
source .venv/bin/activate  # Linux/Mac
```

#### Install Dependencies
```
pip install -r requirements.txt
```

**Note:** Make sure the dataset (`amazon_product.csv`) and image (`ima.jpg`) are in the same directory as `product.py`.

#### Run the Streamlit application:

```
streamlit run product.py
```

#### Open the app in your browser at:

```
http://localhost:8501
```


### 🧠 Features

- **Data Collection & Cleaning:** The Amazon product dataset is loaded from `amazon_product.csv` using Pandas and prepared for recommendation analysis. Unnecessary fields such as the product ID are removed, while relevant product information is retained.

- **Text Preprocessing:** Product titles and descriptions are converted to lowercase, tokenized, and processed using NLTK's Snowball Stemmer. The processed title and description text is combined into a standardized representation for similarity analysis.

- **Feature Engineering:** The processed title and description are combined into a single text feature for each product. This allows the recommendation system to consider both product names and descriptions when determining relevance.

- **TF-IDF Feature Extraction:** The processed product text is converted into numerical vectors using *TF-IDF vectorization*. This represents the importance of words across the product dataset and enables mathematical comparison between user queries and products.

- **Similarity Calculation:** Cosine similarity is used to compare the vector representation of the user's search query with the product vectors. Products with higher similarity scores are considered more relevant to the user's query.

- **Product Ranking & Recommendation:** Similarity scores are sorted in descending order to identify the most relevant products. The system selects the top 10 matching products and extracts their title, description, and category for display.

- **Streamlit Search Interface:** A Streamlit web application provides an interactive search interface where users can enter product-related queries and view the recommended products in a structured format. A banner image is also displayed as part of the application interface.


### 🧩 Example Output

| Title | Description | Category |
|-------|--------------|----------|
| Amazon Basics Mouse | Wireless optical mouse with ergonomic design | Electronics |
| Logitech Keyboard | Compact design with fast response keys | Accessories |


### 🧱 Future Enhancements

- **Product Images:** Integrate product images directly into the recommendation results.
*- **Review Sentiment:** Add sentiment analysis of customer reviews to provide additional product insights.
- **Price & Rating Filters:** Allow users to filter recommendations based on product price and customer ratings.
- **Cloud Deployment:** Deploy the application using Streamlit Cloud or Hugging Face Spaces for public access.


### 📂 Project Structure
```
product.py               # Main Streamlit app
amazon_product.csv       # Dataset with product details
ima.jpg                  # Banner image for the web app
README.md                # Project documentation
LICENSE                  # Project license
```


### 📊 Conclusion

This project demonstrates how NLP techniques can be used to build a practical product search and recommendation system. By combining text preprocessing, TF-IDF, and cosine similarity, the system identifies and ranks products based on their relevance to user queries. The Streamlit interface makes the recommendation process simple, interactive, and accessible to users.

