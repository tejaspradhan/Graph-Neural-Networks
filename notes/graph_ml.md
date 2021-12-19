# Graph Machine Learning Tasks

1. Node Classification / Prediction
2. Link Prediction
3. Graph/ Sub-graph Prediction

<img src="https://github.com/tejaspradhan/Graph-Neural-Networks/blob/main/images/graph-ml.png">


## Node Classification/ Prediction

* Classify every node of the graph based on its node features
* Predict value of a node based on its features

## Link Prediction

* Predict new links / edges between nodes in a graph based on previous existing links.
* 2 main Approaches
  1. Predict missing links at random
  2. Predict missing links over time - The links might not be present in the graphs at timestep `t` but will be present later (predicted) 

### Link Level Features
1. **Distanced based Features** - Shortest path distance (Dijktra's) between 2 nodes. Do not calculate overlaps. (distance is not the only sufficient metric).
2. **Local Neighbourhood Overlap** - How many neighbours do 2 nodes have in common
   * Common Neighbors
   * Jaccard Co-efficient
   * Adamic Adar Index
4. **Global Neigbourhood Overlap** - Considers 2 hop / k-hop neighbours if there are no immediate neighbours. Solves the 0 neighbour problem 

## Graph Level Prediction

* Extract characteristics and features of the entire graphs. Use them for prediction/ classification
* Kernel Methods are used. 
* Kernel matrices measure similarity between data and return a real value.

### Graph Kernels

**1. Graphlet Kernel**

* Count the number of graphlets in the graph of size k. Graphlets need not be connected or rooted.
* [More on Graphlet Kernel](https://ethz.ch/content/dam/ethz/special-interest/bsse/borgwardt-lab/documents/slides/BNA09_3_4.pdf)
* Problem is that calculating graphlets is computationally complex.



**2. Weisfeiler-Lehman Kernel**

* Based on color refinement
* Computationally efficient 
* [More on WL Kernes](https://jmlr.csail.mit.edu/papers/volume12/shervashidze11a/shervashidze11a.pdf)
