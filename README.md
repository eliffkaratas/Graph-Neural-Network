# Graph-Neural-Network
Graph Neural Network applied for MiniGC dataset's graph type classification

Parameter for MiniGCDataset(num_graphs,min_num_v,max_num_v, seed=0): 

num_graphs: int (Number of graphs in this dataset) 

min_num_v: int (Minimum number of nodes for graphs) 

max_num_v: int (Maximum number of nodes for graphs) 

seed : int, default is 0 

Random seed for data generation 


Attributes for MiniGCDataset: 

num_graphs : int (Number of graphs) 

min_num_v : int (The minimum number of nodes) 

max_num_v : int (The maximum number of nodes) 

num_classes : int (The number of classes) [1] 

In order to use the MiniGCDataset, we first need to import the DGLGraph from DGL (Deep Graph Library) library.

It is base graph class. It helps to create graphs. 

Node and edge features are stored as a dictionary from the feature name to the feature data (in tensor). 


DGL graph accepts graph data of multiple formats: 

NetworkX graph, 

scipy matrix, 

DGLGraph. 

If the input graph data is DGLGraph, the constructed DGLGraph only contains its graph index. 

Graph Normalization 

Before generating graphs, some normalization processes were defined. These are ensuring 
that number of nodes and number of edges take values in the range 0-1. These operations are 
done with the help of the PyTorch library.

Algorithm of the Project 

Mini graph classification dataset class is compatible with pytorch’s Dataset class. That's 
why I couldn't use TensorFlow and scikit-learn libraries for classification algorithms. In the 
project, only PyTorch was used as the classification algorithm. Therefore, the project includes 
only the neural network model.
To put it simply, it can seperate the layers in our structure into 3 main layers. Input layer, 
hidden layers and output layer. A graph will be given to the input layers and the type of that 
graph will be displayed from the output layers. Since we have 8 different graph types, our 
output layer dimension will be 8.

All of the results and information can be found in PDF file.
