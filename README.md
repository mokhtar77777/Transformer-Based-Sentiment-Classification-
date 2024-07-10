# Transformer Based Sentiment Classification

## What is a Transformer in Deep Learning?

In deep learning, a transformer is a type of model architecture introduced in the paper "Attention Is All You Need" by Vaswani et al. in 2017. 
Transformers are primarily designed for natural language processing (NLP) tasks, but they have also been successfully applied to various other domains such as computer vision and speech processing.

### Key Components of a Transformer
#### Self-Attention Mechanism:

The core idea behind the transformer is the self-attention mechanism, which allows the model to weigh the importance of different words in a sentence relative to each other. This mechanism enables the model to focus on relevant parts of the input sequence when making predictions.
In self-attention, each word in a sequence is represented by a query, key, and value vector. The attention scores are computed as the dot product of the query with all keys, followed by a softmax operation to obtain the attention weights. These weights are then used to compute a weighted sum of the value vectors, producing the output.
#### Multi-Head Attention:

To allow the model to jointly attend to information from different representation subspaces, the transformer uses multi-head attention. Instead of performing a single self-attention operation, it performs multiple attention operations (heads) in parallel, each with different learned linear projections. The results are concatenated and linearly transformed to form the final output.
#### Positional Encoding:

Since transformers do not inherently capture the sequential order of the input data (unlike recurrent neural networks), positional encodings are added to the input embeddings to provide information about the position of each word in the sequence. These encodings are added directly to the input embeddings before feeding them into the attention layers.
#### Feed-Forward Neural Networks:

Each position in the sequence is independently passed through a fully connected feed-forward neural network, applied to each position's output from the attention mechanism. The feed-forward network consists of two linear transformations with a ReLU activation in between.
#### Layer Normalization and Residual Connections:

Layer normalization and residual connections are used around each sub-layer (i.e., the attention layer and the feed-forward layer) to stabilize and improve the training of the model.

## Use of Transformer in Sentiment Classification
The components mentioned above outputs a 3D tensor whose size is `(M, N, F)` <br>
where `M` is the batch size, `N` is the sequence length, and `F` is the feature vector size. This tensor is averaged over this sequence
length to have a shape of `(M, F)`. Then, the output is fully connected to a sigmoid unit for classification. Attention masks
were used to mask padded tokens.

## Contact
If you have any questions or feedback, feel free to reach out to:

Name: Mokhtar Khaled Salah El Din <br>
Email: mokhtarkhaled7@yahoo.com <br>
GitHub: [mokhtar77777](https://github.com/mokhtar77777)
