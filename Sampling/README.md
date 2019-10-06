## How to sample a signal

If you want to read the full paper you can find it [here](https://github.com/JohanSward/Portfolio/blob/master/Sampling/SwardEJ18.pdf).

In most signal processing problems we are interested in finding estimates of a certain set of parameters given a measured signal. It is clear that the quality of the estimates depends on when the signal is sampled. The question is then how does the sampling effect the estimation. This question is not only interesting from a theoretical point of view but is also a very important in many applications such as in Nuclear Magnetic Resonance (NMR) where one often knows the values of most of the parameters. NMR signals are often measured in many dimensions which makes the aqcusion time quite long (from days to weeks). Our goal is to analyse the sampling problem from a theoretical point of view as well as answer the question: "How should I sample a signal to make the estimation error as small as possible". This makes it possible to drastically decrease the acquision time of, e.g., NMR measuremts thus allowing for a much more efficient research process.

To this end, we use the Cramér-Rao Lower Bound (CRLB) of the signal model and we choose the samples that minimizes the CRLB of each considered parameter. As an example, let's consider a simple sinosoid with a damped amplitude. What is the best way of sampling this signal? Is the best way to acquire all the samples in the beginning of the signal? This makes sense since it is where the signal has most power. However, using our method we can see that it is not the optimal way. Instead the optimal sampling scheme looks like this:

[image]

Thus the best way of sampling a damped signal is to first sample where the signal is as most powerful and then wait and sample when the signal has declined slightly.


Our approach can take any signal model and return the optimal sampling scheme.

