# EduDeepGraph
Graphs in Machine Learning (MVA) project about using Deep Learning on Graph between Educational Contents.  
The aim of this project is to predict a student's answer to an educational question using a knowledge base.  
With this base, we are building a similarity graph and graph convolutions for the predictions.   
  
Dataset : lelivrescolaire dataset (questions/answers for each student)  
Advisor : Julien Seznec (lelivrescolaire).  

### Building the graph
[Jupyter notebook file](https://github.com/SharoneDayan/EduDeepGraph/blob/master/Graph%20construction.ipynb)    
We have m(~25k) students and n(~15k) questions.  
Adjacency matrix (W) / Graph : 
- nodes = questions
- edges = correlations between questions (difficulty/success/spentTime mean over all students) using L1-norm  

W is a n x n matrix.

### Graph Convolutional Network (GCN)
[Jupyter notebook file](https://github.com/SharoneDayan/EduDeepGraph/blob/master/GCN.ipynb)   
We are using T. Kipf's [paper](http://arxiv.org/abs/1609.02907) and [implementation](https://github.com/tkipf/gcn).  
Train set : 
- Adjacency matrix (W, n x n matrix) 
- History matrix : students' answers to the questions (H, n x m matrix, sparse matrix)

