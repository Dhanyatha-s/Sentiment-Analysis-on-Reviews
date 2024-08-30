# Sentiment Analysis on Amazon Food Reviews  


### Overview  
This project focuses on performing sentiment analysis on the Amazon Food Reviews dataset using two different models: VADER (Valence Aware Dictionary and sEntiment Reasoner) and RoBERTa (Robustly Optimized BERT Pretraining Approach). The goal is to analyze the sentiments of the reviews, compare the performance of both models, and explore the distribution of positive, negative, and neutral sentiments.  

### Dataset  
The dataset used for this project is the Amazon Food Reviews dataset, which contains reviews and ratings of various food products sold on Amazon.  

Number of Reviews: ~500,000  
#### Features:  
ProductId: Unique identifier for the product.    
UserId: Unique identifier for the user.  
ProfileName: Name of the user.  
HelpfulnessNumerator: Number of users who found the review helpful.  
HelpfulnessDenominator: Number of users who indicated whether they found the review helpful.  
Score: Rating given by the user (1 to 5).  
Time: Timestamp for the review.  
Summary: Short summary of the review.  
Text: Full review text.  

### Methodology
#### 1. Sentiment Analysis using VADER:  
VADER is a rule-based model that is specifically attuned to sentiments expressed in social media.  
It provides scores for positive, negative, neutral sentiments, and a compound score, which indicates the overall sentiment.  
#### 2. Sentiment Analysis using RoBERTa:  
RoBERTa is a transformer-based model that has been fine-tuned on large datasets for sentiment analysis tasks.  
It outputs probabilities for positive, negative, and neutral sentiments for each review.  
#### 3. Comparison of Results:  
Both models were applied to the Amazon Food Reviews dataset.  
The results were compared based on the distribution of positive, negative, and neutral sentiments.  
#### 4. Evaluation:  
The sentiment scores from both models were compared to the original ratings provided in the dataset.    
A comparison was made between the models to assess which one aligns more closely with the human-assigned ratings.

#### Results
Distribution of Sentiments 
> Positive Sentiment: 
>'Hey, the description says 360 grams - that is roughly 13 ounces at under $4.00 per can. No way - that is the approximate price for a 100 gram can.'  

> Negative Sentiment:  
>'this was sooooo deliscious but too bad i ate em too fast and gained 2 pds! my fault'

> Neutral Sentiment:
> VADER identified more neutral reviews compared to RoBERTa, which was more decisive in categorizing reviews as either positive or negative.  

### Model Performance  
#### VADER:  

Strengths: Fast, rule-based, good at handling social media text.  
Weaknesses: Less nuanced, particularly in reviews with mixed sentiments.  


#### RoBERTa:  

Strengths: Powerful, deep learning model with strong performance on sentiment analysis tasks.  
Weaknesses: Computationally intensive, may require fine-tuning for specific datasets.  

## Conclusion
Comparison: RoBERTa provided a more accurate and nuanced analysis of sentiments in the Amazon Food Reviews compared to VADER. However, VADER is still a good option for quick and efficient sentiment analysis, especially in contexts where computational resources are limited.  

### Final Thoughts: The choice between VADER and RoBERTa should depend on the specific requirements of the task, including accuracy needs and available computational power.

How to Run the Code
Clone the Repository:

bash
```
git clone https://github.com/yourusername/sentiment-analysis-amazon-reviews.git
cd sentiment-analysis-amazon-reviews
````
Install Dependencies: Ensure you have Python 3.x installed. Then, install the required Python packages:

bash
```
pip install -r requirements.txt
```
Run the Sentiment Analysis:

bash
```
python sentiment_analysis.py
```
View the Results: The results will be saved in the results/ directory, with comparisons and visualizations included.

Files in the Repository
sentiment_analysis.ipynb: Main script to run sentiment analysis using VADER and RoBERTa.  

data/: Directory containing the Amazon Food Reviews dataset on kaggle.  
results/: Directory where results and visualizations are stored.
README.md: This file.  


### Future Work  
Fine-tuning RoBERTa: Fine-tune the RoBERTa model on a subset of the Amazon reviews to improve accuracy.  
Model Ensemble: Explore an ensemble of VADER and RoBERTa to leverage the strengths of both models.  
Additional Features: Incorporate more features from the reviews, such as review length, helpfulness score, etc., into the analysis.  

### License
This project is licensed under the MIT License - see the LICENSE file for details.  

Acknowledgments  
Thanks to Kaggle for providing the Amazon Food Reviews dataset.  
The Hugging Face team for creating the amazing transformers library.  
