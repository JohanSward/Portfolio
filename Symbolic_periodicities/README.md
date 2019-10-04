## Symbolic periodicities - what is that?

If you are interested in reading the full paper you can access it [here](https://github.com/JohanSward/Portfolio/tree/master/Symbolic_periodicities/AdalbjornssonSWJ15.pdf).

So what is a symbolic sequence and how can it have periodicities? I think that the easiest way of answering these questions is to look at an example and the most prominent example is that of a DNA sequence. The DNA sequence is made up by four different nucleotides: adenine, guanine, cytosine, and thymine. Let's denote each of these as A, G, C, and T. These nucleotides are the building block to all the genes and thus carries a lot of information. Much of that information is encoded as periodicities in the DNA, thus different combinations of the nucleotides appear periodically. 

Our goal was to create a method that could find the periodicities of nucleotides in a given sequence of DNA; or more generally to find periodicities of symbols in a sequence of symbols. We created two different methods. The first one is a statistically based method that merely counts the occurances of a symbol on a given set of indices and are then tested if significant by forming a hypothesis test. This method is fast and quite reliable, however whenever there are multiple peridoicities present in the sequence, the performance decline somewhat. To 
