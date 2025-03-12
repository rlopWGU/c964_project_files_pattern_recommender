KNIT AND CROCHET PATTERN RECOMMENDATION PROGRAM
v.1.0
------------
11 March 2025
Lopez, Raelynn
S010616837
Computer Science C964 Capstone Project


PROGRAM DESCRIPTION
------------
This program is designed to process user input queries for knitting or crochet patterns and return the top 5 resulting pattern suggestions. The program contains scripts that gather and process a significant volume of pattern data from a public, popular pattern source known as Ravelry. The goal of this data processing (which includes POS tagging, TF-IDF, Word Embeddings, and Cosine Similarity) is to produce a well rounded matrix of the pattern data organized according to their similarities. User input queries are then processed similarly and the top five most similar pattern results are returned to the terminal in a table.

INFORMATION FOR USE
------------
Instructions on how to use the application. The application is ready to use in a Jupyter Lab environment upon downloading its files. 
1. Install Jupyter Lab (if not already installed on your machine).
  - Open the command line, type “pip install jupyterlab”, and press enter.
  - Wait for the installation to complete.
2. Open the project in the Jupyter Lab environment.
  - Open the command line, type "jupyter lab", and press enter.
  - Navigate to main.ipynb in the project files and open the file.
3. Run the main.ipynb script
  - This script performs any necessary installations of tools and libraries needed to use the program.
4. Interact with the program's UI using the terminal.
  - There are several options in the UI, including: submitting a pattern search query, menu, execute data collection and processing, view data visualizations, and exit the program.
5. To close the program, type "menu" in the terminal and press enter, followed by "3" and press enter.
6. To view the search results log, open "search_results.csv".

SCRIPTS
------------
Description of scripts.

DATA COLLECTION
1. url_extraction.ipynb (automatic retrieval of Ravelry URLs)
2. data_scraper.ipynb (automatic scraping of pattern data from Ravelry URLs)

DATA PROCESSING
3. data_preprocessor.ipynb (data cleaning/POS tagging)
4. data_tfidf.ipynb (applies TF-IDF to preprocessed data)
5. data_word_embedding.ipynb (applies Word2Vec word embedding to preprocessed data)
6. data_cosim_tfidf.ipynb (applies Cosine Similarity to TF-IDF data)
7. data_cosim_word_embedding.ipynb (applies Cosine Similarity to word embedding data)
8. data_normalize_matrices.ipynb (combines tf-idf and word2vec matrices after normalizing their values)

USER QUERY PROCESSING
9. input_preprocess.ipynb (takes input for a query and returns top five similar results)

DATA VISUALIZATIONS
10. data_visualizer.ipynb (generates 2D and 3D graphs of pattern data at different intervals in the data processing sequence)

PROGRAM MANAGERS
11. control_data_processing.ipynb (calls scripts 1-8 to sequentially perform pattern URL extraction, data scraping, and all data processing)
12. ui.ipynb (contains user interface functionality)
13. main.ipynb (controller)

DATA FILES
------------
All files produced and stored by the program.

DATA COLLECTION
1. ravelry_pattern_urls.csv (stores scraped URLs of knitting and crochet patterns from Ravelry)
2. patterns_raw.csv (contains raw scraped pattern data, including names, designers, descriptions, and attributes)

DATA PROCESSING
3. patterns_pos.csv (preprocessed pattern descriptions with POS-tagged and filtered keywords for analysis)
4. patterns_tfidf.csv (TF-IDF representation of filtered patter keywords for similarity calculations)
5. tfidf_matrix.pkl (Pickle file storing the trained TF-IDF matrix for reuse in similarity computations)
6. tfidf_vectorizer.pkl (Pickle file storing the trained TF-IDF vectorizer for transforming new inputs)
7. patterns_cosim_embedding.csv (cosine similarity matrix computed from Word2Vec embeddings of pattern descriptions)
8. patterns_with_vectors.csv (stores pattern data with corresponding word embeddings for similarity analysis)
9. patterns_cosim_tfidf.csv (cosine similarity matrix computed using TF-IDF feature vectors)
10. patterns_cosim_hybrid.csv (hybrid cosine similarity matrix combining TF-IDF and Word2Vec-based similarities)
11. patterns_word2vec.model (model created from patterns data word embeddings)

USER QUERIES
12. search_results.csv (logs user search queries, corresponding pattern recommendations, and timestamps for monitoring)

DATASET ATTRIBUTION
This project utilizes publicly available knitting and crochet pattern metadata collected from [Ravelry](https://www.ravelry.com). The dataset consists of pattern titles, designer names, descriptions, fiber types, skill levels, and tags, which were scraped from publicly accessible pattern pages.
All pattern designs, names, and metadata remain the intellectual property of their respective creators. This dataset was collected solely for research and educational purposes to improve search capabilities using natural language processing (NLP) techniques.
If you are a designer and have concerns about your pattern metadata being included in this dataset, please contact us for removal.

SUPPORT
------------
For program support, performance issues, or errors, please reach out to the developer via rlop373@wgu.edu and include a detailed description.
