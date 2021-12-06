# build-knowledge-graph-from-the-legal-corpus
The objective of this project is to create a Knowledge graph from unstructured data. 

Steps are as follows:

●	Due to the time consuming process of annotation of data we have utilized fake sentence generators for auto labeling and generation of data.

●	The labeled data was used to do NER and RE which is provided in the CoNNlu format.

●	Flair framework was used to perform NER and RE, with a legal-bert-base-uncased embedding model.

●	The models created were used to predict entities and Relation in test set data as that data is unseen by the trainer.

●	Once we had head and tail along with relations, we created the triples to generate a Knowledge graph and visualized the Knowledge Graph in Neo4j Bloom.

●	We used various graph embedding results including Node2vec, Graphsage, attri2vec and GCN to train link prediction models and obtained acceptable auc-roc scores on the test dataset(graph).

AUC-ROC of Each Link Prediction Model:	        

Node2Vec:	                      0.771417

Attri2Vec:	                      0.812228

GraphSAGE:                      0.895163

GCN:	                            0.927841

