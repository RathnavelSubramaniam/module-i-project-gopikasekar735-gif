[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/D94-Q8ry)
1. Import libraries, load stock_news.csv
2. Exploratory Data Analysis (EDA)
   - Sentiment distribution, correlations, price trends, news length by sentiment
3. Preprocessing
   - Store target y = Label
   - Tokenize news text (list of word lists)
4. Word2Vec Embedding
   - Train Word2Vec on tokenized text
   - Build word→vector dictionary
   - Average word vectors → document-level DataFrame (word2vec_df)
5. Sentence Transformer Embeddings
   - Load BAAI/bge-base-en-v1.5 → encode → embedding_matrix (768-dim)
   - Load all-MiniLM-L6-v2 → encode → minilm_embedding_matrix (384-dim)
6. Model Building (repeated for each embedding: Word2Vec, BGE, MiniLM)
   - Random Forest: split → fit → predict → evaluate → confusion matrix
   - Neural Network: split → remap labels (0,1,2) → build/compile model → train → predict → evaluate
7. Model Performance Summary
   - Concatenate all 6 models' metrics into train/test comparison tables
8. Conclusions & Recommendations
   - Identify best embedding + model combination
   - Business recommendations for deployment
