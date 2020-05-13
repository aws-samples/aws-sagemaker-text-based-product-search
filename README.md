## Text Based Item/Product Search

This repository guides users through creating a text based item search using Amazon SageMaker and Amazon Elasticsearch


## How does it work?

we have used pre-trained BERT model(distilbert-base-nli-stsb-mean-tokens) from sentence-transformers to generate fixed length sentence 768 embedding  on Multi-modal Corpus of Fashion Images from *__feidegger__*, a *__zalandoresearch__* dataset. Then those feature vectors will be imported in Amazon Elasticsearch KNN Index as a reference.

![diagram](../master/pic1.png)


When we present a new query text/sentence, it's computing the related embedding from Amazon SageMaker hosted PyTorch model and query Amazon Elasticsearch KNN index to find similar text/sentence and corresponds to the actual Product which is stored in Amazon S3

![diagram](../master/pic2.png)

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
