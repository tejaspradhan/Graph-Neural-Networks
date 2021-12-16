# Introduction

Graph Neural Networks take the concept of Graph data structure and try to model these graphs using machine learning. Most of the real world data can be modelled as a graph. This helps in creating a lot of good structures between the data. Applying machine learning to such graph data can help in giving solutions to a lot of problems like - protein folding, drug discovery, ETA prediction based on traffic.

**Geometric Deep Learning** - The machine learning area around research related to GNNs.

**Representation Learning** - Learning neural networks for suitable representation of graph data

* A typical Graph neural network uses representation learning to transform graph data into `node level embeddings` which are vectors which contain certain structural information and features about each node. These node embedding vectors can be used to perform predictions. How we use these representations depends on the ML task we are performing.
* A key idea here is that similar nodes will lead to similar node embeddings and therefore, similar graphs will lead to similar graph embeddings.

<br>

## Graph ML Tasks
1. **Node Level Predictions** - Classify / Predict Attributes of Nodes
2. **Edge Level or Link Predictions** - Predicting whether an edge will exist between certain nodes in a graph
3. **Sub-graph Level Predictions**
4. **Complete Graph Level Predictions**

<br>

## Difficulties while creating Neural Network with Graph Input
1. Graphs can have different shapes and sizes. Neural nets, however,  need a fixed size input. 
2. Isomorphism of graphs. This means that the NN algorithm which uses graph inputs should be `permutation invariant`
3. Many metrics like euclidean distance are not defined for graphs.

<br>
<br>

# Graph Neural Networks

1. Every GNN is composed of certain `message passing layers` which help in converting the graph input into suitable graph representations with node embeddings.
2. Information about neighbouring nodes is collected and certain operations are performed on them, which is followed by updating the node feature information - `Graph Convolutions`

<img src="https://miro.medium.com/max/1838/1*0rj1Pxlzyqkg_rrZiyRDNw.png">

## What happens in Message Passing Layers?

1. Consider `node 1`. Collect node information `h1` at time step `k`.
2. For all nodes i adjacent to node 1, gather information `hi` at time step `k`.
3. Aggregate Node information.
4. Update information about node 1 based on aggregated information about neighbouring nodes for time step `k+1`

This completes one graph convolution. This 4 step process can be done multiple times - depending on the number of message passing layers in the GNN.
The number of message passing(MP) layers is a hyperparameter. Stacking too many message passing layers can cause something called `oversmoothing`
Oversmoothing causes all nodes to contain the same information. This makes the nodes indistinguishable from eachother.

<img src="https://github.com/tejaspradhan/Graph-Neural-Networks/blob/main/images/graph-conv.png">

In a nutshell, we can use the below equation to generalise the entire operation of message passing layers in a GNN

<img src="https://github.com/tejaspradhan/Graph-Neural-Networks/blob/main/images/mp-equation.png">
<br>
<br>

# Common GNN Variants
1. Graph Convolutional Network - Kipf and Welling
2. MLP as Aggregator
3. Graph Attention Networks
4. Gated GNNs

# References 
1. [Deepfindr Graph Neural Networks Playlist](https://youtube.com/playlist?list=PLV8yxwGOxvvoNkzPfCx2i8an--Tkt7O8Z)
2. [CS224W Machine Learning With Graphs](https://youtube.com/playlist?list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn)
