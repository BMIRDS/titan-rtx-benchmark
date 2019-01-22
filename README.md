# Titan-RTX-benchmark

Developing deep learning research projects require powerful hardware resources such as Graphical Processing Unit (GPU) cards. Our research group has access to a GPU server including 6 Tesla K40 GPUs. Considering our lab projects growth, we recently purchased, Nvidia Titan RTX with gigantic 24GB of memory, one of the most powerful GPU card in the market at this time and the first Titan class card in the latest Turing architecture. 
We installed the GPUs on two different machines and conducted a practical test to the compare the performance of one of the older GPUs with the new one. We train one of our proposed deep neural networks on a dataset of CT images for automatic detection of osteoporotic vertebral fractures which was published in 2018 (https://www.sciencedirect.com/science/article/pii/S0010482518301185). Our experiment shows that the new Titan RTX is around 80% faster than Titan Xp on the same dataset. The model’s training took around 4 hours for Titan RTX while the same task took around 7 hours and 40 minutes on Titan Xp. The original paper was trained on an Titan Xp with 100 more epochs which took around 9 hours.
Results are summarized as below table:

| Hardware Configuration   | Time (hh:mm)  |
| -------------            |:-----:|
| Machine A with Titan RTX | 4:14 |
| Machine B with Titan Xp  | 7:40 |


||Machine A|Machine B|
|---|:---:|:---:|
|OS|Ubuntu 18.04|Ubuntu 18.04|
|CPU|Intel Core i7 7820X|Intel Xeon E5-1650|
|Memory| 32 GB (DDR4)| 64 GB (ECC-DDR3)|
|Disk Type|HDD|HDD|

Although our performance test show that Titan RTX has the best time performance compared to the other GPU, however we have not considered the difference of other hardware components such as CPUs, memory, motherboard, which any of them could have a significant effect on the running time. We have not used one of the important aspects of the Titan RTX as well, which is its 24 GB memory, and memory usage is one of our significant bottleneck in developing our deep learning models on our big medical images such as pathology images, which each image’s size is basically over hundreds of megabytes. In our current performance running time test, 11GB of memory is used to train our model. In our future test, we will consider testing the memory size and comparing the results more accurately.
