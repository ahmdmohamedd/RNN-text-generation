# Shakespeare Text Generation using RNNs (LSTM)

This project utilizes Recurrent Neural Networks (RNNs) with Long Short-Term Memory (LSTM) layers to generate text that mimics the style of Shakespeare. The model is trained on a corpus of Shakespeare's works, learning the sequences of characters and their contextual relationships, and is capable of generating original passages in Shakespearean style.

## Table of Contents
- [Overview](#overview)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Training Details](#training-details)
- [Results](#results)
- [Future Improvements](#future-improvements)


## Overview
This project aims to replicate the writing style of William Shakespeare by training a text generation model using RNNs with LSTM units. After training on Shakespeare's collected works for 30 epochs, the model can generate text that resembles lines from Shakespeare's plays and sonnets. The temperature parameter is used to control the creativity of the generated text.

## Model Architecture
The model uses a Recurrent Neural Network with LSTM layers, which allows it to maintain context over longer sequences of text. The architecture consists of the following:
- **Embedding Layer**: Converts input characters into dense vectors of a fixed size.
- **LSTM Layer**: Enables the model to capture long-term dependencies in the text.
- **Dense Layer**: Outputs logits corresponding to each character in the vocabulary.

### Key Parameters:
- **Vocabulary Size**: Number of unique characters in the text.
- **Embedding Dimension**: Size of the vector space in which characters are embedded.
- **RNN Units**: Number of LSTM units used in the RNN layer.
- **Batch Size**: Size of input sequences processed in each step of training.

## Dataset
The model is trained on a dataset comprising the complete works of William Shakespeare, which includes:
- **Plays**: Comedies, tragedies, and historical plays.
- **Sonnets**: Shakespeare’s collection of sonnets.

The dataset was preprocessed to remove unnecessary characters and was tokenized into individual characters to form the basis of the input sequences.

## Installation
To run the project, you'll need Python 3 and the following libraries:
- `tensorflow`
- `numpy`
- `keras`
- `matplotlib`

You can install these dependencies by running:
```bash
pip install tensorflow numpy keras matplotlib
```

## Usage
1. **Clone the repository**:
   ```bash
   git clone https://github.com/ahmdmohamedd/RNN-text-generation.git
   cd RNN-text-generation
   ```

2. **Run the Jupyter Notebook**:
   Open the `Shakespeare_Text_Generation.ipynb` notebook in Jupyter and run all the cells sequentially. The notebook includes:
   - Data preprocessing
   - Model architecture
   - Training
   - Text generation using the trained model

3. **Generate Text**:
   After training the model, you can generate new Shakespeare-like text by providing a starting string and specifying the desired number of characters to generate.

## Training Details
The model was trained using 30 epochs with a batch size of 64 and a sequence length of 100 characters. The Adam optimizer was used with a learning rate of 0.001. A temperature parameter of 0.5 was set during text generation to balance between creative and coherent outputs.

### Training Time:
- The training was done over approximately 30 epochs, with each epoch taking around 15 minutes on an NVIDIA GeForce MX550 GPU.

## Results
The model generates creative Shakespearean-style text. Here's an example of the output:

```
ROMEO: I fain about your highness to my wife.

BAPTISTA:
Now, good my lord, let me hear him.

Shepherd:
None, sir; I know you fare you well, for I must wed;
But I will bring thee tidings...
```

The generated text is fluent and maintains Shakespearean phrasing. With further training or larger datasets, the output could become even more coherent and contextually relevant.

## Future Improvements
- **Training for More Epochs**: Training the model for additional epochs could enhance the output quality and coherence.
- **Using a Larger Dataset**: Including a more extensive Shakespearean corpus or similar literary works could improve the model’s diversity in text generation.
- **Different RNN Architectures**: Experimenting with architectures like GRU or using bidirectional LSTMs could yield interesting results.
