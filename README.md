# Iris_NN
 A simple single-layer neural network in Excel using the Iris dataset. You can modify the learning rate and then iterate through epochs one at a time using the VBA buttons. To the right of the calculations is a visualisation of the neural net, and confustion matixes for the three outputs.

### Neural Network Architecture

This neural network is designed to classify the Iris dataset into three classes: Iris-setosa, Iris-versicolor, and Iris-virginica. The network consists of a single input layer and a single output layer.

#### Input Layer

- **Number of Neurons**: 4
- **Features**: 
  - Sepal length
  - Sepal width
  - Petal length
  - Petal width

#### Output Layer

- **Number of Neurons**: 3
- **Classes**:
  - Iris-setosa
  - Iris-versicolor
  - Iris-virginica
- **Activation Function**: Softmax

#### Weights and Biases

- **Weights**:
  - There are \(4 \times 3 = 12\) weights, connecting each input feature to each output neuron.
  - Represented as a 4x3 matrix \(W\):

    $`\[
    W = \begin{bmatrix}
    W_{11} & W_{12} & W_{13} \\
    W_{21} & W_{22} & W_{23} \\
    W_{31} & W_{32} & W_{33} \\
    W_{41} & W_{42} & W_{43}
    \end{bmatrix}
    \]
    `$

- **Biases**:
  - Each output neuron has its own bias term, resulting in 3 bias terms in total.
  - Represented as a vector \(b\):

    \[
    b = \begin{bmatrix}
    b_1 \\
    b_2 \\
    b_3
    \end{bmatrix}
    \]

#### Forward Pass

During the forward pass, the network performs the following computations for each data point:

1. **Linear Combination**:
   - For each output neuron \(j\), the linear combination of inputs is computed as:

     \[
     z_j = \sum_{i=1}^{4} W_{ij} \cdot x_i + b_j
     \]

     Where:
     - \(W_{ij}\) is the weight connecting input \(i\) to output \(j\)
     - \(x_i\) is the input feature
     - \(b_j\) is the bias for output \(j\)

2. **Activation (Softmax)**:
   - The softmax function is applied to the linear combinations to obtain the output probabilities:

     \[
     \text{softmax}(z_j) = \frac{e^{z_j}}{\sum_{k=1}^{3} e^{z_k}}
     \]

     This ensures that the outputs are probabilities that sum to 1.

#### Summary of the Architecture

1. **Input Layer**:
   - 4 neurons (sepal length, sepal width, petal length, petal width)

2. **Output Layer**:
   - 3 neurons (Iris-setosa, Iris-versicolor, Iris-virginica)
   - Softmax activation function

3. **Connections**:
   - 12 weights (4 input features × 3 output classes)
   - 3 biases (one for each output neuron)


