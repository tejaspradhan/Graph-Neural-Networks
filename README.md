# Introduction

Graph Neural Networks take the concept of Graph data structure and try to model these graphs using machine learning. Most of the real world data can be modelled as a graph. This helps in creating a lot of good structures between the data. Applying machine learning to such graph data can help in giving solutions to a lot of problems like - protein folding, drug discovery, ETA prediction based on traffic.

## Table Of Contents

[1. Basics of Graph Neural Networks](https://github.com/tejaspradhan/Graph-Neural-Networks/blob/main/notes/basics.md)

[2. Graph Machine Learning Tasks in Detail]()
3. 



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

# References 
1. [Deepfindr Graph Neural Networks Playlist](https://youtube.com/playlist?list=PLV8yxwGOxvvoNkzPfCx2i8an--Tkt7O8Z)
2. [CS224W Machine Learning With Graphs](https://youtube.com/playlist?list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn)
