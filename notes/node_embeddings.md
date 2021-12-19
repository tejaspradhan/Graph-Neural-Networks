# Node Embeddings

* The main objective of node embeddings is to come up with a feature vector for every node in the graph. 
* Node embedding vectors should be task independent. 
* Essentially, we map every node to a `d-dimensional vector space` which will have `d` node features. Node features should be such that they should give information about the nodes as well as the structure of the graph. 
* Similar nodes / nodes which are close together should have similar node embeddings. 
* These nodes will be used to further perform machine learning tasks.
* Learning node embeddings is an unsupervised / self-supervised task.

## Encoder Decoder Architecture of Learning Node Embeddings 

1. Encoder encodes the node into a lower dimensional vector space. - Encoded value is the node embedding
2. Decoder calculates similarity score of the embedding.
3. If the similar nodes dont have a good similarity score, the embeddings are optimised. 

<img src="">
