# ReadMe Page for MSDS692_BatmanSA
## Batman Movie Analysis Project

![image](https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/30e35112-0d7e-4177-a8cf-fe9b9f88e139)
![image](https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/ba5e5d0e-59e0-406b-a1aa-6b7d16127945)


### Project Overview
This project aims to compare two Batman movies, *Batman* (1989) and *The Dark Knight* (2008), through Natural Language Processing (NLP) and sentiment analysis. The goal is to determine which Batman movie is the "darkest," most complex (subjective), and most popular based on the movie scripts and reviews.

### Motivation
Batman movies are known for their complex characters and dark themes. This project seeks to explore these aspects by analyzing the dialogues and reviews of the movies. The insights gained can inform future movie productions by highlighting elements that resonate with audiences.

### Data Sources
- **Movie Scripts**: PDF files of the scripts for Batman (1989) and The Dark Knight (2008).
- **Movie Reviews**: Reviews for the two movies scraped from Rotten Tomatoes.

<img width="479" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/3448754f-756b-49c7-b058-cf9f0dc504fb">

### Tools and Libraries
- **Python Libraries**: pdfplumber, re, nltk, pandas, matplotlib, seaborn, TextBlob, and selenium.
- **Data Extraction**: Used pdfplumber to extract text from PDF files and selenium for web scraping movie reviews.

### Data Preprocessing
1. **Extracted text** from PDFs using pdfplumber.
2. **Removed non-dialogue elements** (scene descriptions) using regex patterns.
3. **Tokenized text** and removed stopwords using nltk.
4. **Cleaned reviews** by removing punctuation, converting to lowercase, and tokenizing.

### Exploratory Data Analysis (EDA)
1. **Word Count Analysis**: Calculated the average word count per dialogue and reviewed.
2. **Vocabulary Richness**: Measured the richness of vocabulary in the dialogues and reviews.
3. **Sentiment Distribution**: Analyzed the distribution of sentiment polarity and subjectivity scores.
4. **Word Co-occurrence**: Created heatmaps to visualize the interactions between characters.
5. **Adjective Frequency**: Identified the most common adjectives used to describe the characters.

A selection of EDA visualizations below:

Movies were similar in their common words, common adjectives, and character count:
**Number of Unique Characters in Each Movie:**
*Batman*: 149, *The Dark Knight*: 143

<img width="439" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/63410bc5-6fa6-4957-a148-c5c78a1f6793">

In *Batman*, Bruce Wayne had more dialogue than Batman. In *The Dark Knight*, Bruce spoke about as often in his role of Bruce Wayne as in his role as Batman:
<img width="636" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/0bb97381-47d3-460f-a89d-cb215b8272f1">

<img width="418" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/a8421525-21d6-4844-8fc8-a59606a7a3fc">
<img width="415" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/c681d573-438c-4745-9408-d41341a1b04b">

<img width="625" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/a5e1f888-4e14-48bf-8228-4884b1335620">

<img width="441" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/f69b0259-2eab-44e7-a954-b3143416ec89">




   

### Sentiment Analysis
- **TextBlob**: Used for calculating polarity and subjectivity scores of the dialogues and reviews.
- **VADER**: Used to analyze sentiment in social media and informal text.

### Comparative Analysis
1. **Overall Sentiment Trends**: Compared the average sentiment scores across the two movies.
2. **Hero vs. Villain Sentiment**: Analyzed the sentiment of dialogues between Batman/Bruce Wayne and the main villains.
3. **Supporting Characters Sentiment**: Compared the sentiment of supporting characters' dialogues.

### Visualizations
1. **Box Plot of Sentiment Polarity Distribution**: Showed the spread of sentiment scores.
2. **Heatmap of Sentiment Over Time**: Visualized sentiment changes throughout the movie.
3. **Violin Plot of Sentiment Subjectivity**: Displayed the distribution of subjectivity scores.
4. **Scatter Plot of Sentiment Polarity vs. Subjectivity**: Correlated sentiment polarity with subjectivity.
5. **Line Plot of Sentiment Trends Over Time**: Tracked sentiment changes across the movie.



### Findings
- **Darkness**: *Batman* is darker based on the sentiment analysis of the movie scripts, while *The Dark Knight* is darker based on the reviews.
- **Subjectivity**: *Batman* is more subjective based on both the script and review analysis.
- **Sentiment**: Both movies have generally positive reviews, with *Batman* having slightly higher positive sentiment.

### Challenges and Solutions
- **Scraping Reviews**: Overcame the challenge of repeatedly clicking the "Load More" button by automating the process with selenium.
- **Handling Complex Dialogues**: Improved sentiment analysis by using multiple models (TextBlob and VADER) to capture nuanced language.

### Future Work
1. **Explore Character Interactions**: Create conversation maps to visualize character dynamics and interactions.
2. **Evaluate Sentiment Analysis**: Improve models to better detect sarcasm and tone.
3. **Custom Sentiment Lexicon**: Develop a custom lexicon tailored to Batman movies.
4. **Character-Specific Analysis**: Perform sentiment analysis on a per-character basis.
5. **Temporal Analysis**: Conduct temporal analysis of sentiment to observe character emotion evolution.
6. **Additional Movie Analysis**: Extend the analysis to include more Batman movies for comparative insights.

### Repository Contents
- **Presentation PDF**: [BatmanNLP_Presentation_CSmith.pdf](./BatmanNLP_Presentation_CSmith.pdf)
- **Jupyter Notebooks**:
  - [ReviewMostPopular.ipynb](./ReviewMostPopular.ipynb)
  - [ScriptReviewSentimentipynb.ipynb](./ScriptReviewSentimentipynb.ipynb)
  - [BatmanDialogue.ipynb](./BatmanDialogue.ipynb)
  - [ScrapingRottenTomatoes.ipynb](./ScrapingRottenTomatoes.ipynb)

This project showcases the power of NLP and sentiment analysis in uncovering the hidden aspects of movies. By comparing different elements of the Batman movies, I gained insights into the themes and character dynamics that contribute to their popularity and impact.
