# vec2vec
Download model weights and test dataset here: https://huggingface.co/gaodrew/vec2vec
Since the seminal Word2Vec paper in 2013, vector embeddings have become ubiquitous and powerful tools for many language-related tasks. A leading embeddings model is OpenAI’s text-ada-002 which can embed up to approximately 6,000 words into a 1,536-dimensional vector. While powerful, text-ada-002 is not open source and is only available via API. Thus, users must have an Internet connection to query their text-ada-002 databases. Additionally, API costs can add up and users are locked in to OpenAI. We trained a simple neural network to convert open-source 768-dimensional MPNet embeddings into text-ada-002 embeddings. We compiled a subset of 50,000 reviews from Stanford’s Amazon Fine Foods dataset. We calculated MPNet and text-ada-002 embeddings for each review and trained a simple neural network for 75 epochs. Our model achieved an average cosine similarity of 0.932 on 10,000 unseen reviews in our held-out test dataset. Given the high dimension (1,536) of text-ada-002 embeddings, 0.932 is quite impressive. Finally, we manually assessed the quality of our predicted “synthetic” embeddings for vector search over text-ada-002-embedded reviews. While not as good as real text-ada-002 embeddings, predicted embeddings were able to retrieve highly relevant reviews. Our final model, “Vec2Vec”, is lightweight (<80 MB) and fast. Future steps include training a neural network with a more sophisticated architecture and a larger dataset of paired embeddings to achieve greater performance. The ability to convert between and align embedding spaces may be helpful for interoperability, limiting dependence on proprietary models, protecting data privacy, reducing costs, and offline operations.
