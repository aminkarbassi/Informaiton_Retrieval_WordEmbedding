# Informaiton_Retrieval_WordEmbedding

Introduction

As part of a search task, 50 queries on a collection of over 20'000 documents are evaluated. The queries represent information needs, which are sometimes formulated in keywords, but also as complete sentences. in keywords, but also as complete sentences. 

Systems Used and Motivation

For this project, the text-embedding-ada-002 model from OpenAI was utilized. This pre-trained word embedding model offers powerful capabilities for representing textual data in a high-dimensional space. The motivation behind using such a model was to leverage the semantic information encoded within the embeddings, enabling more accurate comparisons and similarity measurements between documents and queries.

Index Structure

The index in this project was constructed using the text-embedding-ada-002 model. The embedding vectors generated for both the collection documents and the query list served as the basis for the index. Each document and query was transformed into a fixed-length vector of 1536 dimensions. These vectors capture the semantic meaning and context of the respective text elements, allowing for efficient comparison and retrieval.

Ranking list

To evaluate the similarities between the collection documents and the queries, cosine similarity was employed. Cosine similarity measures the cosine of the angle between two vectors from each document and each query and provides a metric to assess their similarity. By calculating the cosine similarity between the embedding vectors of each query and the collection documents, a ranking list of document-query pairs was generated. The higher the cosine similarity value, the more similar the document and query are considered to be.

Results Interpretation

The generated ranking list provides a quantitative assessment of the similarities between the collection documents and the queries. Higher cosine similarity values indicate stronger semantic similarity between document-query pairs. Consequently, documents appearing at the top of the ranking list are deemed more relevant to the corresponding query.

Conclusion

This experiment utilized the text-embedding-ada-002 model to create an index of embedding vectors for both the collection documents and the queries. By employing cosine similarity, the experiment evaluated the similarities between the documents and queries, resulting in a ranking list. The utilization of pre-trained word embedding models facilitates accurate measurement of semantic similarities and enables efficient retrieval of relevant documents based on user queries.

It should be noted that word embedding the documents and queries is very time consuming. therefore, the whole process for the applied method here would be slower in finding relevant documents when the number of documents is large. It worth stating that the embedding process has to be done once and the results would be stored locally to avoid repetition of time consuming calculations. After the documents are vectorized, the remaining part of the process is very fast.
