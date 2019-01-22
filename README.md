# Titan-RTX-benchmark

Training deep learning models requires powerful hardware resources such as Graphical Processing Unit (GPU) cards. Considering the current growth in computational needs of our lab, we recently purchased an Nvidia Titan RTX GPU card, which is the most powerful GPU card on the market at this time and the first Titan class card in the latest Turing architecture. 
To evaluate this new GPU, we conducted a quick experiment to compare the performance of one of our older GPUs with Titan RTX. We trained our proposed deep neural network (CNN + LSTM) on a dataset of CT images for automatic detection of osteoporotic vertebral fractures as it was presented in our 2018 paper (https://www.sciencedirect.com/science/article/pii/S0010482518301185). We trained the model using different GPU cards for 300 epochs on the same dataset. Our experiment showed that the training process is more than 80% faster with the new Titan RTX GPU in comparison to Titan Xp. The model training took around 4 hours on Titan RTX while the same task took around 7 hours and 40 minutes on Titan Xp. These results are summarized below:

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

Of note, two GPU cards were installed on two different machines and we did not consider the effect of other hardware components, such as CPUs, memory, and motherboard, on the running time.
In the past, GPU memory had been a significant bottleneck in our research for training deep neural networks on medical images, particularly for high-resolution pathology images. Considering Titan RTX's 24 GB memory and this preliminary comparison, we expect Titan RTX will considerably boost our model development efforts and cut the training time. 
