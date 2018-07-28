# MISAGA

MISAGA: An algorithm for Mining Interesting Sub-Graphs in Attributed Graphs

The software in this repository is developed based on the approach proposed in the following paper: T. He, and K.C.C. Chan, "MISAGA: An Algorithm for Mining Interesting Subgraphs in Attributed Graphs," IEEE Transactions on Cybernetics (TCYB), vol. 48, no. 5, pp. 1369-1382, 2018. Besides, the drafted version of the paper (with errata of the final version in the IEEE Xplore) is also provided. For the full text of the paper, please check http://www.ieeeexplore.ws/document/7911270/.

How to use MISAGA: To use MISAGA (MISAGA.exe) to detect clusters in an attributed graph, please firstly prepare four files, which are named as "Configuration," "edgelist," "vertex2aid," and "statistics" and put them into the directory where MISAGA.exe is. The detailed information for these files is the following:

1. edgelist: This file contains the connections in the attributed graph. There are two columns in this file which are the ids of source and target nodes. It should be noted that the starting node id must be 0.

2. vertex2aid: This file contains attributes that each vertex in the graph is associated with. There are two columns. The first column contains the vertex ids and the second column contains the ids of attributes that are labeled with each vertex. It should be noted that the starting ids for both node and attribute must be 0.

3. Configuration: This file contains the parameters used by MISAGA. There are 5 reals in this file. They are the settings related to the number of clusters, the bias between edge structure and attribute similarity in the optimization process, the maximum number of optimizing iterations, the minimum change of C between two iterations, and lambda. Here is an example: 4 0.5 300 1e-9 1 This means the initial settings of MISAGA are the following: 4 clusters, 0.5 bias, 300 iterations of optimization, 1e-9 minimum change, and lambda = 1. These parameters can be modified accordingly, or one may follow recommendations in the paper of MISAGA.

4. statistics: This file contains the information of the attributed graph. Here is an example: 500 9000 50 It means this attributed graph contained 500 vertices, 9000 edges, and 50 attributes, respectively. To help users get familiar with the files used by MISAGA, we provide the corresponding files of a set of attributed graph data which are in the directory ".\example". One may check them for the details.

After completing all the preparations, one is able to run MISAGA to perform the task of clustering in attributed graph data by running a .bat file in which contains the following codes: MISAGA.exe pause The results of clustering in the attributed graph will be written into a file after MISAGA completes the optimization process. If MISAGA cannot be executed, please check readme.txt for the requirements of running environment, which is in the zip file.

Notice: This software is permitted to use only for research and non-commercial activities. If you have any question, please feel free to contact us via tiantian.he@outlook.com.

At last, thanks very much for using MISAGA.
