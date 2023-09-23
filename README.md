# ScratchGPT
Bigram transformer model from scratch (Shakespearean corpus)

Essentially, transformers are encoder-decoder models
That is, they take an input (user prompt) --> encode it (tokenization) --> let the tokens talk between each other (self and cross attention) --> decode it (generate next most probable set of words).
This is how chatgpt works: it encodes the user prompt, makes sense of what the encoded data is, tries to find a relation between each token (each token has a weight-->how much probable it is to appear after the previous token), and finally generates a sequence of tokens in a probabilistic manner.

The Shakespeare model is technically half of GPT... its trained on a corpus of Shakespearean text and asked to generate random text based on the weights and biases it has learned during model compile.
This phase is called pretraining ---> the first half of model training.

The second half is finetuning ---> changing the parameters (like temperature, num_tokens, categorization) to generate better tokens to a user prompt.
This is why chatgpt responds more like a human than a chatbot

The data used for training the model is the total collection of all Shakespearean works available in a 1MB file [input.txt](input.txt).
[train.ipynb](train.ipynb) is just a breakdown of the transformer architecture I wrote for future editing. [bigram.py](bigram.py) provides a more concise and condensed format of training the model. It uses over 10 million parameters in training, depending on how you modulate your usage of hyperparameters in the code. [MODEL.py](MODEL.py) is probably what you are looking for, as it loads the pre-trained model straight out of the directory and generates text upon execution.

Notes:

Switch device to 'cpu' if no CUDA device available.
If you are training from the boilerplate code, I suggest running it on Colab's T4 (or if you're brave, on the A100).
Playing with the block_size and batch_size should generate some interesting results.

Joi will require an encoder and decoder segment.
And she will have to be trained on a larger, more conversational corpus of information.
Au Revoir.
