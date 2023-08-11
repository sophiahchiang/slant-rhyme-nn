# Slant Rhyme Neural Networks

How does a language model represent or understand rhyme? Is a neural network that was trained to identify normal rhymes also able to identify imperfect or slant rhymes? What might its ability or inability to do so imply about the phonetic representations and sound relationships in the model?

This repository contains the code that was used for the [paper](https://drive.google.com/file/d/1yfpcnMLyH54Aq9-75VFnoZlr6v4jpx8p/view?usp=sharing) that attempted to answer the questions above. We used two types of neural networks trained on four generated data sets of varying types of rhyming and/or non-rhyming words, two “strict” and two “expansive”. Neither model was trained on slant rhymes. We chose a feedforward neural network and a recurrent neural network, and initially hypothesized that the recurrent model would perform better in rhyming tasks because it uses discrete time-steps that could be more analogous to “sounding out” rhymes.

The structure of the set up we had to do before training or running the networks is as follows: 
1. Corpus generation
2. Conversion to IPA
3. Transformation to tensor
4. Truncate to last 6 characters and pad beginning with zeros for shorter inputs
