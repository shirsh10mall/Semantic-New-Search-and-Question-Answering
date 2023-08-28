# Semantic Search based News Recommendation and Wikipedia Articles Question Answering System

Main Notebook: https://www.kaggle.com/code/shirshmall/project-ir-semantic-search-summarize-qna/notebook


Failed Attempts and Previous Codes:
1. https://www.kaggle.com/code/shirshmall/project-ir-part-1-keywords-extraction/notebook
2. https://www.kaggle.com/code/shirshmall/task-ir-part-2-search-and-summarize-keywords
3. https://www.kaggle.com/code/shirshmall/fine-tuning-t5-for-cnn-news-articles-summarization 
4. https://www.kaggle.com/code/shirshmall/project-ir-part-4-faiss-semantic-search

Dataset: 
1. Web-Scraped Reuters News Articles: https://www.kaggle.com/datasets/shirshmall/reuters-news-article-and-summary-web-scraping
2. CNN Daily News Articles Embedding: https://www.kaggle.com/code/shirshmallwork/project-ir-add-embeddings/output


# Semantic Search-based News Recommendation and Wikipedia Articles Question Answering System

## Introduction
In the era of information explosion, finding relevant news articles and obtaining accurate answers to questions from a sea of online content can be challenging. This project aims to address this issue by creating an innovative Semantic Search-based News Recommendation and Wikipedia Articles Question Answering System. By leveraging cutting-edge natural language processing (NLP) techniques, this system provides users with an efficient and user-friendly way to explore news articles and access accurate information.

## Dataset Collection
To build a robust and diverse system, data collection is essential. This project harnesses the power of various datasets:
1. **Web Scraped Reuters News Articles**: The project starts by scraping news articles from Reuters, a reputable news agency. These articles encompass full-length news pieces alongside corresponding summaries. The scraping process is facilitated by the Selenium library, allowing the collection of up-to-date and relevant news content.
2. **CNN News Articles**: In addition to Reuters, the CNN News Articles dataset from Hugging Face datasets is incorporated. This dataset adds depth and variety to the range of news content.
3. **Dynamic Wikipedia Articles Extraction**: To further enrich the user experience, Wikipedia articles are extracted dynamically using the BeautifulSoup and Wikipedia Python packages. This ensures that users have access to authoritative and comprehensive information.

**Semantic Search Approach**
Embracing advanced Natural Language Processing techniques, the project's Semantic Search approach enhances news retrieval. Utilizing BART embeddings, the system captures article semantics, enabling a FAISS index for precise semantic search, presenting users contextually aligned news articles.

**News Articles Embeddings and Semantic Search**
To attain deeper insights into news articles, the project leverages BART embeddings, empowering efficient semantic search through the FAISS index. This technology enhances user experience by offering contextually relevant news articles with ease.

**Question Answering System**
Expanding beyond news articles, the project integrates a robust question answering system. It employs fine-tuned models to provide accurate answers to user queries, combining BERT embeddings and brute force search for context generation, revolutionizing information access.

## Fine-Tuning Summarization Model
The project relies on the fine-tuning of two powerful summarization models: T5 and BART. These models are pre-trained on a substantial amount of text data and can generate concise summaries of longer articles. The fine-tuning process involves adapting these models to generate summaries specifically for news articles and their corresponding pairs.

## News Articles Embeddings and Semantic Search
One of the key features of the system is semantic search, which enables users to find articles related to their interests efficiently. After obtaining the news articles, the BART model is employed to create embeddings of the articles. These embeddings capture the semantic essence of the content, allowing for a deeper understanding of the text. The generated embeddings are then utilized to construct a FAISS index—a high-performance library for similarity search. This index facilitates the rapid retrieval of semantically related articles, streamlining the recommendation process.

## Question Answering System
The project extends its functionality beyond news articles by incorporating a robust question answering system. This system allows users to ask questions about a given topic and receive accurate answers. Here's how the process unfolds:
1. **Input Topic**: Users begin by providing a topic or subject they are interested in.
2. **Semantic Search**: Leveraging the FAISS index, the system performs a semantic search to identify the most relevant news articles related to the input topic. This ensures that users receive a tailored selection of articles.
3. **Summarization**: The selected news articles are passed through the fine-tuned summarization models (T5 and BART) to generate concise and informative summaries. These summaries offer users a quick overview of the articles' content.
4. **Wikipedia Articles Extraction**: To further enhance the user experience, the system extracts Wikipedia articles related to the input topic. This is achieved through Wikipedia's search engine, ensuring that users have access to comprehensive information.
5. **Question Input**: Users are prompted to input a question related to the chosen topic.
6. **Embeddings and Context Generation**: The sentences from the Wikipedia articles and the user's question are converted into embeddings. Using a brute force approach, the system identifies the top 25 sentences most relevant to the question and combines them into a context.
7. **Question Answering Model**: The question and context are fed into a question answering model, which produces accurate answers to the user's query.

## Model Deployment
To make the Semantic Search-based News Recommendation and Question Answering System accessible and user-friendly, the project culminates in the creation of an interactive app. Gradio, a Python library for creating UIs, is utilized to develop an intuitive and responsive user interface. This app empowers users to effortlessly navigate news articles, access summaries, and receive answers to their questions.

<be>

![example 3](https://github.com/shirsh10mall/Semantic-News-Search-and-Question-Answering-Wiki-Articles/assets/87264071/40867f26-c0ee-44b5-b5a6-5f79c8180983)

![example 2](https://github.com/shirsh10mall/Semantic-News-Search-and-Question-Answering-Wiki-Articles/assets/87264071/b801fd7c-39e1-4f1e-a645-c646753f9556)

![example 1](https://github.com/shirsh10mall/Semantic-News-Search-and-Question-Answering-Wiki-Articles/assets/87264071/8010036d-61df-4863-8b3b-a5d78356dfbf)
<br>

## Conclusion
In an era of information overload, the Semantic Search-based News Recommendation and Wikipedia Articles Question Answering System emerges as a beacon of innovation. By combining semantic search, summarization, and question answering techniques, this project equips users with a versatile tool to explore news articles and access reliable information. This system not only enhances user experience but also showcases the transformative potential of NLP in catering to the evolving needs of information seekers.



## Failed Process:

**Failed Process 1: News Search based on Keywords and Summarization**

1. **Drop Irrelevant and Repetitive Columns**: Initially, attempted to streamline the dataset by removing unnecessary and duplicated columns to simplify subsequent processes.
2. **Extract Keywords from Various Columns**: Employed a combination of manual programming, Named Entity Recognition (NER) systems, and Knowledge Graph techniques to extract relevant keywords from different columns in the news data.
3. **Input Keywords and Search with Inverted Index**: Designed a system to input extracted keywords and search for documents containing these keywords using an inverted index. Intended to narrow down relevant articles based on keyword matches.
4. **Filtering and Grouping by Date**: The extracted documents were filtered based on keyword relevance and then grouped by date to facilitate chronological organization.
5. **Sorting Documents by Date**: In an attempt to prioritize recent news, sorted the documents based on their publication date.
6. **Selecting Past Dates and Creating Summaries**: The idea was to select the most recent past 10 (or fewer) dates and create concise summaries for the news articles published on those dates.
7. **Content-Based News Recommendations**: As an additional feature, aimed to enhance user experience by suggesting 5-6 news articles related to the user's selected content using content-based recommendation techniques.

**Failed Process 2: Extracting Keywords and Key Phrases**

1. **Keyword Extraction Algorithms**: Initially, attempted to utilize various keyword extraction algorithms to automatically identify the most important keywords within the news articles.
2. **Named Entity Recognition (NER) Techniques**: Explored the use of NER techniques to identify named entities such as people, organizations, and locations within the text as potential keywords.
3. **Document Matrix and Inverted Index Approach**: Experimented with creating a document-term matrix and building an inverted index for words in the news articles. This approach aimed to enable word-level matching for efficient keyword-based searches.

In both failed attempts, the challenges lay in achieving accurate keyword extraction and developing efficient search mechanisms. These challenges resulted in suboptimal search results and inadequacies in providing meaningful news recommendations. As a result, the decision was made to pivot the project towards a Semantic Search-based approach, which proved to be more effective in delivering relevant news articles and information to users. This pivot enabled the project to overcome the limitations faced in the failed processes and achieve its objectives more successfully.
