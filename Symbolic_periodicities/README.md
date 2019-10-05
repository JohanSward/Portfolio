## Symbolic periodicities - what is that?

If you are interested in reading the full paper you can access it [here](https://github.com/JohanSward/Portfolio/tree/master/Symbolic_periodicities/AdalbjornssonSWJ15.pdf).

So what is a symbolic sequence and how can it have periodicities? I think that the easiest way of answering these questions is to look at an example. The most prominent example of when one is interested in finding periodicities in symbolic sequences is when one wants to study DNA sequences. The DNA sequence is made up by four different nucleotides: adenine, guanine, cytosine, and thymine. Let's denote each of these as A, G, C, and T. These nucleotides are the building block to all the genes and thus carries a lot of information. Much of that information is encoded as periodicities in the DNA, thus different combinations of the nucleotides appear periodically. 

Our goal was to create a method that could find the periodicities of nucleotides in a given sequence of DNA; or more generally, to find periodicities of symbols in a sequence of symbols. I will here demonstrate our methods using the DNA example. We have created two different methods for solving this problem. The first one is a statistically based method that merely counts the occurances of a symbol on a given index set (corresponding to different periodicities, e.g., every third element in a sequence or every sixth element in a sequence) which is then deemed significant if we can reject the null hypothesis that all the index sets are all the same. This method is fast and quite reliable, however whenever there are multiple peridoicities present in the sequence, the performance decline somewhat.



To be able to better handle the case when we have multiple periodicities, we form a more elaborate model.
