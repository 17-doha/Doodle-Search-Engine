Name
=======
**Search Engine Project**

Description
=======
•	Text-analysis-based project that combines NLP, ML, and IR concepts to generate an accurate search engine with a simple GUI for displaying the outputs.  
  


**Used Tools:**  
 * Python    
 * TF-IDF 
 * BM25 
 * BERT  
 * Web-Scraping 
 * Python-terrier 
 * Streamlit 

**Data Collection:**  
 * I prepared the collection through scrapping wikipedia documents + some other documents from google of total 115 terms and around 5 documents for each one and total corpus contains 529 document.
* Colab for preparing data: https://colab.research.google.com/drive/1azsLGr0y3G-wUPrp04BW8mHwE265DdIA?usp=sharing
  
**Preprocessing:**
* Preprocessing took place for cleaning using regex library, tokenization, stemming, remove stop words, removing duplicates, and removing additional unnecessary spaces.
  
 **Indexing:**
* Indexing took place through python terrier library to prepare index and inverted index of the whole corpus.
* Got a list of the unique terms to be used later in retrieval.
* Prepared list with each document and the freq of the word inside it for each word.
  
**Query Processing:**
* Implemented a preprocessing function that does nearly the same functionality for preprocessing documents but on a single query.
* Tried a simple and more complex query.
* Retrieved using TF-IDF algorithm for ranking.
* Printed a list of the documents with all the terms presented (common list).
* Printed a list of the documents that are relevant to the query (document list).
* Printed the top ten relevant documents to a query using the document_rank dictionary that contains each “document_id” as the key and the “docno” and “rank” as the values
  
**Query expansion:**
* Applied the BM25 model for retrieval.
* Applied relevance feedback using rochiio algorithm by apply “RM3” model for query expansion and then searching again by using BM25 model.
* Appended the results to the “res” list.
* Made the search_bert function that uses bert model to rerank the documents that resulted from the search that was done after BM25.
  
**User Interface:**
* Developed user interface using streamlit library from google colab that takes the whole code and runs it inside it and uses the search_bert function.
  
**Evaluation:**
* Evaluated some of the queries that could be searched about such as : ["Standup Comedy", "Gaza","Egypt", "Zewail City", "Covid"] and prepared a list of the relevant documents that should appear on the search for these queries and calculated the ndcg to calculate the accuracy of the search.
* Evaluated the speed of the search using time library from python.

**Interface:**

![image](https://github.com/17-doha/Doodle-Search-Engine/assets/65771031/86be75fb-ec64-4144-ba79-82e13c0c0b84)




