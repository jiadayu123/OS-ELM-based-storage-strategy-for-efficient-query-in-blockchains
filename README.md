# OS-ELM-based-storage-strategy-for-efficient-query-in-blockchains

## Architecture

<img src="https://github.com/jiadayu123/OS-ELM-based-storage-strategy-for-efficient-query-in-blockchains/blob/master/figs/f2.png" width="400px">

The architecture of the hot block storage strategy consists of three modules, as shown in this figure, namely the sharding-based blockchain module (the left part); the feature extraction module (the upper right part) and the classifier module (the upper right part).

In the sharding-based blockchain module, the blockchain system adopts different sharding strategies to realize that resource-constrained nodes join the consensus of the blockchain system. This paper takes ElasticChain as an example to describe the working process of the module in detail. 

In the feature extraction module, the verification nodes will analyze the attributes of the blocks and obtain the knowledge of blocks. Then, the verification nodes calculate the feature values of each block for a storage node according to the knowledge. 

In the classifier module, the features of blocks are used as the input of the latest classifier based on OS-ELM, and the output result is the hot block or non-hot block for a node. Then, the node stores the hot blocks locally. The training process of OS-ELM classifier is shown in Steps [1]-[3] in this figure. In the beginning, according to a small amount of training data, an original classifier model is obtained. Moreover, with the operation of the blockchain system, new blocks continue to increase and new training data will be generated. Based on the existing classifier model, OS-ELM method will train the new training set and quickly get the latest classifier to accurately classify the hot blocks.
