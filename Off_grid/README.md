## Off-grid Fundamental Frequency Estimation

The full article can be found [here](https://github.com/JohanSward/Portfolio/tree/master/Off_grid/SwardLJ_17.pdf).

Fundamental frequency estimation is important in many applications. For instance, when modelling the human voice, the fundamental frequency (also known as the pitch) is an integral part. Another interesting application is when determining if a ball bearing machinery is at fault. A signal has a pitch structure if it can be expressed as a sum of sinusoids where each frequency is a integer multiple of the fundathe fundamental frequency. If the sum has L terms, we say that the pitch has L-1 harmonics or overtones. 

Clearly, there is a lot of structure in this problem and it is not very hard to solve it when one knows the value of L. However, if consider the more general problem where we allow for an unknown number of pitches and their respective harmonics, the problem is really difficult to sovle with the traditional methods. 

One approach that has shown in useful in other applications is to use sparse modelling by forming an optimisation problem that promotes a sparse solution. This is done by considering a large number of signal candidates, say D > > K, which in this case means that we will create D pitches with their corresponding harmonics. The fundamental frequencies thus comes from a grid of D grid points. The optimization problem is then formed such that we only select a few candidates from the dictionary such that the resulting approximation if the signal is close to the true signal. This optimization problem takes the form as

[optimization problem]


The problem with this approach is that the gridding of the fundamental frequency will of course not coinside with the true fundamental freqiencies and to get very close, one needs a very dense grid which will increase the computational burdan of the algorithm. Instead of using a grid, we propose an off the grid method that treats the fundamental frequency as a variable and then iteratively and alternativly solve for the amplitude and fundamental frequency until convergence.

Here are some results from our paper:
