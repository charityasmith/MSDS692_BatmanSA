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
<br/>
Movies were similar in their common words, common adjectives, and character count:
**Number of Unique Characters in Each Movie:**
*Batman*: 149, *The Dark Knight*: 143

<img width="439" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/63410bc5-6fa6-4957-a148-c5c78a1f6793">

<br/>

**Bruce Wayne or Batman?**
In *Batman*, Bruce had more lines in his role as Bruce Wayne than as Batman.
In *The Dark Knight*, Bruce spoke about as often in his role of Bruce Wayne as in his role as Batman:
<img width="636" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/0bb97381-47d3-460f-a89d-cb215b8272f1">

<br/>

**Word Co-occurrence Heatmaps**
Characters like Bruce, Vicki, Dent, and Joker have strong interactions, as shown by the high co-occurrence frequencies.
The presence of frequent co-occurrences between key characters (e.g., Bruce and Vicki, Bruce and Joker) highlights pivotal relationships and interactions that drive the storyline.
<br/>
<img width="418" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/a8421525-21d6-4844-8fc8-a59606a7a3fc">
<img width="415" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/c681d573-438c-4745-9408-d41341a1b04b">

<br/>

**Dialogue Count in Movie Scripts:**
In both movies, The Joker had the most lines, followed by Batman/Bruce Wayne:
<img width="625" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/a5e1f888-4e14-48bf-8228-4884b1335620">

<br/>

**Most Common Words in Movie Reviews:**
<br/>
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
<img width="316" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/e0717f28-6057-40ef-8694-c502d825c0f4">

2. **Visualization of Sentiment Over Time**: Visualized sentiment changes throughout the movie. <img width="334" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/6682066e-3a6e-4fdd-9c8b-6a94bed567ed">

3. **Scatter Plot of Sentiment Polarity vs. Subjectivity**: Correlated sentiment polarity with subjectivity.
 <img width="327" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/28b7089c-4696-477d-928a-fa6bb450208a">

4. **Average Sentiment for Main Characters**: Bar plot to display average sentiment for main characters using TextBlob and VADER.
**TextBlob Results:**

<img width="421" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/34135851-ffd1-4ef7-bfcb-23479353e40f">

**VADER Results:**

<img width="424" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/1683cb0c-7bb5-4c05-b052-24b35e6ce819">



### Findings
- **Darkness**: *Batman* is darker based on the sentiment analysis of the movie scripts, while *The Dark Knight* is darker based on the reviews.
- **Subjectivity**: *Batman* is more subjective based on both the script and review analysis.
- **Sentiment**: Both movies have generally positive reviews, with *Batman* having slightly higher positive sentiment.
<img width="337" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/beba3fe7-b91d-4a64-b960-8baeb270ccc9">


### Challenges and Solutions
- **Scraping Reviews**: Overcame the challenge of repeatedly clicking the "Load More" button by automating the process with selenium. I also implemented a loop to click the "Load More" button until all reviews were loaded.

- **Handling Complex Dialogues**: Improved sentiment analysis by using multiple models (TextBlob and VADER) to capture nuanced language. Used patterns to identify and remove scene descriptions (e.g., INT., EXT., FADE IN). Identified character names by detecting uppercase lines with limited words.
<img width="464" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/9dab1d26-9ab3-4b72-b47a-755228f129e3">



### Challenges that Remain Open
The Joker's dialogues, as analyzed through TextBlob and VADER, show a neutral or slightly positive sentiment score. However, The Joker often uses complex and nuanced language that can mask the underlying dark intent. His dialogues are laced with sarcasm, irony, and a playful tone that may be interpreted by sentiment analysis models as neutral or slightly positive. Additionally, The Joker's dialogues often contain dark humor, which can be perceived as humorous or playful. This can skew the sentiment analysis towards neutral or positive, even though the content is dark and disturbing! Given these factors, the neutral or slightly positive sentiment scores for the Joker's dialogues can be understood as a limitation of the sentiment analysis models in capturing the full context and nuance of his speech.

<img width="245" alt="image" src="https://github.com/charityasmith/MSDS692_BatmanSA/assets/20384712/79559b01-6973-4a18-8676-fb4a76cdb3e7">




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
