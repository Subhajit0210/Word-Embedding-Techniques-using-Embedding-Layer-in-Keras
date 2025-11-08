# Word-Embedding-Techniques-using-Embedding-Layer-in-Keras

***Word Embeddings*** provide a dense representation of words and their relative meanings. They are an improvement over sparse representations used in simpler ***Bag-of-Words*** models. Word Embeddings can be learned from text data and reused among projects. They can also be understood as part of fitting a neural network on text data.

Reference Link - https://machinelearningmastery.com/use-word-embedding-layers-deep-learning-keras/

## Table of Contents
- [Import Libraries](#import-libraries)
- [Example Sentences](#example-sentences)
- [One Hot Representation](#one-hot-representation)
- [Word Embedding Representation](#word-embedding-representation)
- [Requirements](#requirements)
- [Code Explanation](#code-explanation)
- [Usage](#usage)
- [Contributing](#contributing)

## Import Libraries
Imports necessary ***TensorFlow*** and ***Keras*** libraries.

## Example Sentences
Defines a list of sample sentences for demonstration.

## One Hot Representation
Converts the sentences into a ***One-Hot Encoding*** representation based on a defined vocabulary size.

## Word Embedding Representation
1. Uses the Embedding layer to create word embeddings.
2. Utilizes pad_sequences to ensure all input sequences have the same length.
3. Builds a Sequential model with an Embedding layer.
4. Compiles the model.
5. Shows the model summary.
6. Predicts the embedded representation of the example sentences.

## Requirements
1. ***TensorFlow 2.0+***
2. ***Keras (integrated within TensorFlow)***
3. ***NumPy***

## Code Explanation
1. ***one_hot(words, voc_size)***: Converts a word into its one-hot representation based on the vocabulary size.
2. ***pad_sequences(onehot_repr, padding='pre', maxlen=sent_length)***: Pads the one-hot encoded sequences to a fixed length (sent_length) by adding zeros at the beginning (padding='pre').
3. ***Embedding(voc_size, dim, input_length=sent_length)***: Creates an embedding layer with voc_size as the input dimension (vocabulary size), dim as the output dimension (embedding size), and input_length as the fixed length of input sequences.
4. ***Sequential()***: Initializes a Keras Sequential model.
5. ***model.add(...)***: Adds layers to the sequential model.
6. ***model.compile('adam', 'mse')***: Configures the model for training (although no training is performed in this example).
7. ***model.summary()***: Prints a summary of the model architecture.
8. ***model.predict(embedded_docs)***: Generates the word embeddings for the padded sequences.


## Usage
To run the project, follow these steps:
1. Clone the repository:
```bash
git clone https://github.com/yourusername/Face-Mask-Detection-using-CNN.git
```
2. Navigate to the project directory:
```bash
cd Face-Mask-Detection-using-CNN
```
4. Run the Jupyter notebook:
```bash
jupyter notebook Face_Mask_Detection_using_CNN.ipynb
```
Run the notebook cells sequentially to see the text processing and embedding steps.

## Contributing
Contributions are welcome! Please create a new branch for any changes and submit a pull request for review.
