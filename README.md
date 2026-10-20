# Grokking Deep Learning: Summary Notes

<a style="width: 400px" href="https://www.manning.com/books/grokking-deep-learning"><img alt="Grokking Deep Learning Cover" src="./Grokking Deep Learning Cover.png" style="width: 400px; height: auto; padding: 10px;"></a>

**Original Author:** Andrew W. Trask

This repository contains a collection of Jupyter Notebooks summarizing the concepts and code of *Grokking Deep Learning*. The book builds neural networks from scratch, first with plain Python and NumPy, and only later with a small framework of its own. These notes follow the same path: each chapter is paraphrased in a short academic summary, and the code listings of the book are reproduced so that every idea can be run and inspected, one step at a time.

## 📂 Repository Structure

The summaries are divided into 16 modules, one for each chapter of the book:

* **`01.introducing-deep-learning.ipynb`**
    Why deep learning is worth learning, what the book assumes from the reader, and how to approach the chapters that follow.
* **`02.fundamental-concepts.ipynb`**
    How machines learn: deep learning within the wider fields of artificial intelligence and machine learning, supervised and unsupervised learning, and parametric and nonparametric models.
* **`03.introduction-to-neural-prediction.ipynb`**
    Forward propagation and the predict, compare, learn pattern. Covers a simple network, networks with multiple inputs and outputs, stacked layers, and a short NumPy primer.
* **`04.introduction-to-neural-learning.ipynb`**
    Comparing predictions with targets, hot and cold learning, and gradient descent for a single weight, including the role of the derivative and of the learning rate `alpha`.
* **`05.learning-multiple-weights-at-a-time.ipynb`**
    Generalizing gradient descent to many weights: multiple inputs, multiple outputs, and both at once. Also introduces MNIST and shows how to interpret learned weights through dot products.
* **`06.building-your-first-deep-neural-network.ipynb`**
    The streetlight problem, matrices, and full, batch, and stochastic gradient descent. Explains correlation, overfitting, conflicting pressure, and indirect correlation, then builds the first deep network with nonlinearity and backpropagation.
* **`07.how-to-picture-neural-networks.ipynb`**
    A simplified way to draw networks (layers and weight matrices as bricks), and a notation that links these pictures to variable names, code, and algebra.
* **`08.learning-signal-and-ignoring-noise.ipynb`**
    Overfitting, memorization versus generalization, early stopping, dropout, why dropout works as an ensemble, and batch gradient descent.
* **`09.modeling-probabilities-and-nonlinearities.ipynb`**
    Activation functions and their constraints (relu, sigmoid, tanh, softmax), choosing the output layer, computing slopes for backpropagation, and upgrading the MNIST network.
* **`10.neural-learning-about-edges-and-corners.ipynb`**
    Reusing weights in many places: convolutional layers and kernels, how they reduce overfitting, and a simple NumPy implementation.
* **`11.neural-networks-that-understand-language.ipynb`**
    Natural language processing with IMDB movie reviews: capturing word correlation, the embedding layer, comparing word embeddings, filling in the blank, and word analogies (king − man + woman).
* **`12.neural-networks-that-write-like-shakespeare.ipynb`**
    Recurrent layers for variable-length data: averaged word vectors, identity and transition matrices, and forward and backward propagation through a recurrent network on a question-answering task.
* **`13.introducing-automatic-optimization.ipynb`**
    Building a small deep learning framework: tensors, automatic gradient computation (autograd), optimizers, layer types, loss functions, nonlinearities, the embedding layer, cross-entropy, and a recurrent cell.
* **`14.learning-to-write-like-shakespeare-lstm.ipynb`**
    Character language modeling, truncated backpropagation, vanishing and exploding gradients, LSTM cells and their gates, and tuning the model to generate text.
* **`15.deep-learning-on-unseen-data.ipynb`**
    Privacy in deep learning: federated learning on a spam-detection task, how updates can leak data, secure aggregation, and homomorphic encryption.
  
## 🖼️ Figures

The book's figures are included in the notebooks as screenshots. Each notebook refers to them with a relative path, so the images need to sit next to the notebooks in this structure:

```
pictures/
└── chapter N/
    └── picture N.x.png
```

Here `N` is the chapter number and `x` is the order of the figure within that chapter (for example, `pictures/chapter 6/picture 6.1.png`). Chapters without figures (such as Chapter 15 and Chapter 16) have no folder.

## 🛠️ System Requirements

The notebooks are written to run in Google Colab, where most of the packages below are already installed. To run them locally, set up a Python environment with:
* `numpy`
* `keras` and `tensorflow` (load MNIST)
* `phe` (homomorphic encryption example)
* `jupyter`

The remaining imports in the code (`sys`, `math`, `random`, `collections`, `copy`, `codecs`) belong to the Python standard library.

---

## ⚠️ Disclaimer

This repository was created purely as personal study notes and a summary of the concepts and code in *Grokking Deep Learning*.

All concepts, theoretical frameworks, code listings, figures, and the general flow of the material discussed herein remain the intellectual property of their respective original authors and publisher. This repository is not intended to serve as a substitute for formal educational material, but rather as a study aid and a supplementary code summary. For a comprehensive and in-depth understanding of the subject matter, it is highly recommended to refer to the original book, **"Grokking Deep Learning"** by Andrew W. Trask (Manning Publications, 2019).
