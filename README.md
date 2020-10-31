# text-summarization
There are two main types of how to summarize text in NLP:
1) Extraction-based summarization

The extractive text summarization technique involves pulling keyphrases from the source document and combining them to make a summary. The extraction is made according to the defined metric without making any changes to the texts.
2) Abstraction-based summarization

The abstraction technique entails paraphrasing and shortening parts of the source document. When abstraction is applied for text summarization in deep learning problems, it can overcome the grammar inconsistencies of the extractive method.
The abstractive text summarization algorithms create new phrases and sentences that relay the most useful information from the original text — just like humans do.
Therefore, abstraction performs better than extraction. However, the text summarization algorithms required to do abstraction are more difficult to develop; that’s why the use of extraction is still popular.

In this project, we have used both types.
for a user query we have extracted the semantic similar sentences from the corpus using the Sentence Transformer framework.

https://www.sbert.net/

In SentenceTransformer framework we have used bert pre-trained model('distilbert-base-nli-mean-tokens') to find the top similar sentences.

Merged the sentences if the cosine score is greater than 0.4

Output of extractive model is further sent to a T5 model (Text-to-Text-transformer) for an abstractive summary.

Note: these models perform well on most of the data. if u still feel u can improve it, then you can train the models with your corpus data and change the embeddings value in it.

