# Multiclass QCNN Research Abstract (Fully Quantum)
This paper explores the implementation and optimization of fully quantum convolutional neural networks (QCNNs) for multi-class image classification. Building upon existing QCNN architectures, we investigate the viability of these models for complex classification tasks using the MNIST handwritten digits dataset. A key focus is the analysis of both gradient-based (ADAM) and gradient-free (COBYLA) optimization methods for training QCNNs. We examine the impact of various factors, including data set size, loss function, and circuit modifications, on the performance of binary and multi-class (4-class) classification. Our results demonstrate the potential of QCNNs for achieving comparable accuracy to classical CNNs, particularly with gradient-based optimization, while also highlighting the challenges associated with gradient-free optimization in higher dimensional Hilbert spaces. Furthermore, we observe a potential advantage of QCNNs in mitigating overfitting compared to classical counterparts. We also investigate the impact of hybrid quantum-classical architectures, where a classical linear layer is incorporated after the quantum circuit. Finally, we discuss future research directions, including dense encoding, optimization algorithm development, architectural changes, and noise analysis, to further enhance the efficiency and accuracy of QCNNs. All code and testing details are available on Github.

Quick Navigation to Best Version:
* [Gradient Based Optimizer](<GPU/V4 (FINAL TESTING)/Gradient Testing/Circuit1/4 Classes/4Qubits(One_Hot)_ADAM_256_95Epoch.ipynb>) - Gradient Based Optimizer Test (Best Performing)
* [Gradient Free Optimizer](<GPU/V4 (FINAL TESTING)/Circuit 1/Estimator 4 Classes Circuit 1 (256 Batch)/4Qubits(NoEndConv).ipynb>) - Gradient Free Optimizer Test (Best Performing)

We use multiple circuits tested in the GPU File under the V4 (Final Testing) under different categories. Rest of directories are tests and represent the iterative work.
All Circuits Tested Accessible Below (Folders)
* [Gradient Free Optimizer](<GPU/V4 (FINAL TESTING)>) - Gradient Free Optimizer Testing
* [Gradient Based Optimizer](<GPU/V4 (FINAL TESTING)/Gradient Testing>) - Gradient Based Optimizer Testing (ReverseGradientEstimator)
### Paper Link (Draft)
Note: This is a draft paper and has not yet been properly reviewed or completed. Edits are in progress and will be updated here.

[QCNN Paper PDF](<./QCNN Research Project - Fourth Draft.pdf>)

## Goal
Implementing and comparing different quantum circuit architectures and analyzing current constraints in gradient calculation of quantum circuits.

## Input
Input in all cases is an MNIST dataset consisting of handwritten digits. To represent the classical data for quantum processing, we reduce the image dimensions from 28x28 image
<table>
  <tr>
    <td><img src="images/fullImage.png" alt="28x28 Image" width="350" height="300"></td>
  </tr>
</table>

to 4x4 image so that we can use 16 qubits to represent 1 image. The images are processed through the ZFeatureMap, which encodes classical data into a quantum representation that can then be processed by the quantum algorithm.
<table>
  <tr>
    <td><img src="images/smallImage.png" alt="4x4 Image" width="350" height="300"></td>
  </tr>
</table>

## Sample Circuit Used
<table>
  <tr>
    <td><img src="images/circuit.png" alt="Sample Circuit Decomposed" width="1200" height="1700"></td>
  </tr>
</table>


## Sample Algorithms
[Gradient Free Optimizer](<GPU/V4 (FINAL TESTING)/Circuit 1/Estimator 4 Classes Circuit 1 (256 Batch)/4Qubits(NoEndConv).ipynb>) - Gradient Free Optimizer Test (Best Performing)
<table>
  <tr>
    <td><img src="images/GradientFree4ClassesAccuracy.png" alt="Gradient Free 4 Classes Accuracy" width="310" height="225"></td>
    <td><img src="images/GradientFree4ClassesLoss.png" alt="Gradient Free 4 Classes Loss" width="310" height="225"></td>
  </tr>
</table>

<br>

[Gradient Based Optimizer](<GPU/V4 (FINAL TESTING)/Gradient Testing/Circuit1/4 Classes/4Qubits(One_Hot)_ADAM_256_95Epoch.ipynb>) - Gradient Based Optimizer Test (Best Performing)
<table>
  <tr>
    <td><img src="images/GradientImage4ClassesAccuracy.png" alt="Gradient Image 4 Classes Loss" width="310" height="225"></td>
    <td><img src="images/GradientImage4ClassesLoss.png" alt="Gradient Image 4 Classes" width="310" height="225"></td>
  </tr>
</table>

## Output
<table>
  <tr>
    <td><img src="images/output.png" alt="Sample Output (Best Performance Enhanced Circuit)" width="600" height="650"></td>
  </tr>
</table>

## Future Aim / Next Steps
Experimenting with dense encoding (check 8.1), testing/developing new optimizers, architectural changes, further analysis of bottleneck in gradient-free optimizers, and the effect of noise on our models.

## Works Cited
1. Cong, I., Choi, S., & Lukin, M. D. (2018, October 9). [1810.03787] Quantum Convolutional Neural Networks. arXiv. Retrieved February 14, 2025, from https://arxiv.org/abs/1810.03787
2. IBM Quantum. (n.d.). The Quantum Convolution Neural Network - Qiskit Machine Learning 0.8.2. GitHub Pages. Retrieved February 14, 2025, from https://qiskit-community.github.io/qiskit-machine-learning/tutorials/11_quantum_convolutional_neural_networks.html
3. Vatan, F., & Williams, C. (2024, November 26). quant-ph/0308006v3 25 Mar 2004. arXiv. Retrieved February 14, 2025, from https://arxiv.org/pdf/quant-ph/0308006
