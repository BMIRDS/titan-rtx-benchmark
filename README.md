# Titan-RTX-benchmark

GPU cards are the most important hardware for deep learning research. Our research group recently bought a new computer equiped with Nvidia Titan RTX, the first Titan class card in the lastest Turing architecture. We are very excited about this new card, which is one of the most powerful graphics cards in the market with gigantic 24GB of memory. We conducted some tests to see how much benefit we can get from this expense. Although our test results are not measured under scientific regorousness, the outcome is impressive and satisfied us. 

We measured practical wall-time of model training on two machines under the setting of one of our publication [Deep neural networks for automatic detection of osteoporotic vertebral fractures on CT scans](https://www.sciencedirect.com/science/article/pii/S0010482518301185). For the details of training, please refer to the *Section 3.3, Feature extraction training*.

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

A machine A with Titan RTX finished training in about 4 hours, while another machine B with Titan Xp took 7 hours and 40 mins. Surprisingly the new machine (A) runs 80% faster than our old machine (B). This is really a big deal especially for some experiements that requires a week of training. Shorter training time give us more opportunity to condut the variety of experiments, and thus affects our quality and productivity of research. Both machines runs faster than the code at the time of publication, which took 9 hrs, due to multiple code optimizations and deep learning library's upgrade. By considering the large gap in time it took between two computers, we think that not only GPUs but also other components, such as CPU, memory, and motherboard, have affected to the results, so it's not simple to say the RTX is 80% faster than Xp. However, since it's hard to predict the bottleneck of training pipeline beforehand, always getting the lastest GPU and high performance computer would make sense to unlock the full potential of the research. Another bottleneck of typical deep learning could be the GPU memory size; the RTX comes with 24 GB of memory which is double since previous main stream. We haven't used much memory this time (e.g. both training used up to 11 GB), but other projects require significantly larger memory and we look forward to get benefit of the new GPU on those projects.


