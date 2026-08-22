## Amazon Product Recommendation System using NLP


### 🛍️ Introduction
This project is a Streamlit web application that acts as a search and product recommendation engine using TF-IDF and cosine similarity.
It analyzes product titles and descriptions from an Amazon dataset to recommend the most relevant products based on a user query.


### 📂 Project Structure
```
product.py               # Main Streamlit app
amazon_product.csv       # Dataset with product details
ima.jpg                  # Banner image for the web app
```


### ⚙️ Features

- 🔍 Search for products by name or description  
- 🧠 Text processing using NLTK’s Snowball Stemmer  
- 📊 TF-IDF Vectorization for feature extraction  
- 🤝 Cosine Similarity to rank products by relevance  
- 🌐 Interactive Streamlit interface with image banner  


### 🧾 Dependencies

Install the required libraries before running the app:

```
pandas
numpy
nltk
scikit-learn
streamlit
Pillow
```

You can install them all with:

```
pip install -r requirements.txt
```


### 🚀 How to Run the App

Clone this repository:

```
git clone https://github.com/archna13/Amazon-Product-Recommendation-System-using-NLP.git
```

Make sure the dataset (`amazon_product.csv`) and image (`ima.jpg`) are in the same directory as `product.py`.

Run the Streamlit application:

```
streamlit run product.py
```

Open the app in your browser at:

```
http://localhost:8501
```


### 🧠 How It Works

#### Preprocessing:
- Tokenizes and stems text (titles + descriptions) using NLTK.  
- Creates stemmed tokens for each product.

#### Feature Extraction:
- Converts text data into numerical TF-IDF vectors.

#### Similarity Calculation:
- Calculates cosine similarity between the query and product data.  
- Ranks the top 10 most similar products.

#### Output:
- Displays matching products (title, description, category) in the Streamlit interface.


### 🧩 Example Output

| Title | Description | Category |
|-------|--------------|----------|
| Amazon Basics Mouse | Wireless optical mouse with ergonomic design | Electronics |
| Logitech Keyboard | Compact design with fast response keys | Accessories |


### 🧱 Future Enhancements

- Integrate product images into recommendations.  
- Add sentiment analysis for customer reviews.  
- Include product price and rating filters.  
- Deploy on Streamlit Cloud or Hugging Face Spaces.


### 👩‍💻 Author

**Archana Manivannan**  

