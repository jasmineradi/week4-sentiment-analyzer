# Sentiment Analysis System
## Overview

This project implements sentiment analysis for product reviews using Natural Language
Processing (NLP) techniques from Chapter 23.

## Features

- **Two Analysis Methods:**
- Simple: Word counting based on positive/negative word lists
- Advanced: Machine learning using TextBlob
- **REST API** for easy integration
- **Visualization** of sentiment distributions
- **Text preprocessing** including tokenization and stop word removal

## How to Run

### 1. Install Requirements
```bash
pip install -r requirements.txt
```
### 2. Test the Analyzer
```bash
python test_sentiment.py
```
### 3. Start the API Server
```bash
python api_server.py
```
Then visit http://localhost:5000

## API Usage Example
```python
import requests
response = requests.post('http://localhost:5000/analyze',
json={'text': 'This product is amazing!'})
print(response.json())
```
## Understanding NLP Concepts

### Tokenization

Breaking text into words: "I love this" → ["I", "love", "this"]

### Stop Words
Common words we filter out: "the", "is", "at", "which"

### Sentiment Analysis
Determining if text is positive, negative, or neutral

## Challenges Encountered
One challenge I faced was understanding how all the different files connected to each other. At first, I wasn’t sure what the API or sentiment analyzer actually did or how they worked together. I also had some trouble with installing the required packages and figuring out how to run each file in the right folder. Once I slowed down and ran each step one at a time, I started to see how the project fit together and what the code was doing behind the scenes.

## Real-World Applications
1. Companies like to issue surveys regularly and use sentiment analysis to determine positive or negative sentiment about products or services.

2. Some financial firms will analyze reports and online activity to guess how a stock market might react.

3. Some HR departments will analyze surveys to determine how employees are performing in their positions.

## What I Learned
I learned about Natural Language Processing (NLP), which is how computers can understand and analyze human language. I saw how text can be cleaned and broken down into smaller pieces (like words) before being analyzed for meaning. I also learned that NLP tools, such as TextBlob, can detect the tone of a message and decide whether it sounds positive, negative, or neutral. This helped me understand how programs can process language data and use it in real-world applications like chatbots, product reviews, and social media analysis.

## Example Input and Output
**Input:**  
"This product is absolutely amazing!"

**Output:**  
Positive sentiment detected with 92% confidence.