## Neural Machine Translation by Jointly Learning to Align and Translate

Tensorflow implementation of the [Neural Machine Translation by Jointly Learning to Align and Translate]https://arxiv.org/abs/1409.0473 paper.

As a part of our Advanced Machine Learning project we re-implemented the neural machine translation paper , the paper introduced a model that translates one sentence from a source language into a sentence in a target language. This model consists of 3 major parts, an encoder that reads the input sentence and encodes it into a sequence of vectors of variable length, and a decoder that outputs the translated sentence in the target language and the attention, placed in between the previous parts to take in consideration the context of a word in the input sentence depending on its previous and next words 

Neural machine translation is a recently proposed approach to machine translation. Unlike the traditional statistical machine translation, the neural machine translation aims at building a single neural network that can be jointly tuned to maximize the translation performance.

#### Introduction
Neural machine translation is a task that is becoming more and more essential for many industries of today’s world. The overwhelming majority of the machine translation models are of the encoderdecoder type.Till now, we have known 3 types of models of the machine translation task which are a sequence to sequence based on encoder-decoder model, a sequence to sequence with attention and finally, state of art model known as transformers. Researched were looking for a solution to bypass the fixed length limitation and try to have better results using a variable length context vector. Our role in this project is to reverse engineer the results obtained in the paper ”NEURAL MACHINE TRANSLATION BY JOINTLY LEARNING TO ALIGN AND TRANSLATE” by Bahdanau, Cho and Bengio. The paper introduces an innovation to the classic encoder-decoder model by learning to align and translate jointly, using a variable length attention vector while the encoderdecoder based model uses a fixed length attention vector corresponding to the last hidden states of
the encoder.


#### Dataset
The WMT’ 14 dataset contains approximately 850M words, during our research the time needed for our model to train on the totallity of the dataset would be closer to 6 days. Evidently, we chose at first to shrink the dataset to a couple hundred thousand words, to facilitate the process and make sure our python code was correct before moving into the full dataset. We chose to concatenate the Europarl dataset with the IWSLT-17 dataset to form our mini-set. We were later able to treat th entire dataset which totaled a whopping 14GO of english sentences and their translation in french.



