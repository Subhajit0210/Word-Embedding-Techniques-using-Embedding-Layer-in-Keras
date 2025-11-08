# Word-Embedding-Techniques-using-Embedding-Layer-in-Keras

Word embeddings provide a dense representation of words and their relative meanings. They are an improvement over sparse representations used in simpler bag-of-words models. Word embeddings can be learned from text data and reused among projects. They can also be understood as part of fitting a neural network on text data.

## Table of Contents
- [Project Overview](#project-overview)
- [Dependencies](#dependencies)
- [Data Collection](#data-collection)
- [Data Preparation](#data-preparation)
- [CNN Model](#cnn-model)
- [Results and Insights](#results-and-insights)
- [Usage](#usage)
- [Contributing](#contributing)


Overview
The notebook covers the following steps:

Import Libraries: Imports necessary libraries from TensorFlow and Keras.
Example Sentences: Defines a list of sample sentences for demonstration.
One Hot Representation: Converts the sentences into a one-hot encoding representation based on a defined vocabulary size.
Word Embedding Representation:
Uses the Embedding layer to create word embeddings.
Utilizes pad_sequences to ensure all input sequences have the same length.
Builds a Sequential model with an Embedding layer.
Compiles the model.
Shows the model summary.
Predicts the embedded representation of the example sentences.
Requirements
TensorFlow 2.0+
Keras (integrated within TensorFlow)
Numpy

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




## Code Explanation
1. **one_hot(words, voc_size)**: Converts a word into its one-hot representation based on the vocabulary size.
2. **pad_sequences(onehot_repr, padding='pre', maxlen=sent_length)**: Pads the one-hot encoded sequences to a fixed length (sent_length) by adding zeros at the beginning (padding='pre').
3. **Embedding(voc_size, dim, input_length=sent_length)**: Creates an embedding layer with voc_size as the input dimension (vocabulary size), dim as the output dimension (embedding size), and input_length as the fixed length of input sequences.
4. **Sequential()**: Initializes a Keras Sequential model.
5. **model.add(...)**: Adds layers to the sequential model.
6. **model.compile('adam', 'mse')**: Configures the model for training (although no training is performed in this example).
7. **model.summary()**: Prints a summary of the model architecture.
8. **model.predict(embedded_docs)**: Generates the word embeddings for the padded sequences.





Reference Link - https://machinelearningmastery.com/use-word-embedding-layers-deep-learning-keras/
