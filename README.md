Approach followed :-
TextBlob - This library iterates through a list of cleaned reviews, calculates the sentiment polarity for each review using TextBlob, and appends the polarity scores. Further sentiment is assigned based on polarity score. 
GloVe (Global Vectors for Word Representation) embeddings are loaded from a file named 'glove.6B.100d.txt'. It iterates through each line of the file, splits the line to separate the word and its corresponding vector representation, converts the vector representation into a NumPy array of type float32, and stores each word along with its embedding vector in the 'embeddings_index' dictionary.
A function is created that computes the document embedding by averaging the GloVe embeddings of tokens present in the document, excluding tokens not found in the embeddings index. If the document has no valid tokens, it returns a zero vector.
Themes for different reviews are created which are converted into vector embeddings
Cosine Similarity - This function assigns a theme to a given review vector by computing the cosine similarity between the review vector and pre-defined theme vectors. It returns the theme with the highest cosine similarity, indicating the most similar theme for the review.
Using similar method , priority level is assigned to each review
Another feature added is using semantic search system that can find the most relevant text entries from a dataset based on their semantic similarity to a given query, leveraging pre-trained sentence embedding models from the txtai library.
Further analysis is conducted based on classifications and these insights can be used by airlines industry
The above method can be used by Airlines industry , Hospitality and service industries , E-commerce and retail , Government and public services
