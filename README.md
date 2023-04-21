# distributed-clustering

## Assignment

Write two programs using MPI technology for distributed clustering performance 
evaluation.
 
Before you write the programs, prepare a dataset 
with numerical values and no less than 1000 rows (for example, you can use Brooklyn sales map 
dataset).
 
Process 0 (root) reads data from file into an array and sends the data to all the processes in the 
communicator. Each other process starts K-means clustering algorithm and finds a solution. 
When solution is obtained, it is evaluated by using a clustering index. You can select any.
 
Process 0 collects the performance indices from all the processes and finds the best clustering 
solution based on Min or Max criteria. Process 0 outputs the best solution and its clusters’ 
centroids.
 
First version of program uses only point-to-point communication functions (like MPI_Send and 
MPI_Recv) for data transmission. Second version of program is based on collective 
communication (MPI_Bcast or MPI_Reduce). Compare the time performance of both versions 
and make conclusions.
 
