# Multiclass QCNN Research (Fully Quantum)
Implementation of multi-class quantum convolutional neural network (without classical layers). I not only implement 4-class MNIST Digit Classification, but I also compare with implementations of 2-Class MNIST QCNN Classifier and different loss functions. I also test numerous gradient and gradient-free algorithms. Labels are on IPYNB Files.

Quick Navigation to Best Version:
* [Gradient Based Optimizer](<GPU/V4 (FINAL TESTING)/Gradient Testing/Circuit1/4 Classes/4Qubits(One_Hot)_ADAM_256_95Epoch.ipynb>) - Gradient Based Optimizer Test (Best Performing)
* [Gradient Free Optimizer](<GPU/V4 (FINAL TESTING)/Circuit 1/Estimator 4 Classes Circuit 1 (256 Batch)/4Qubits(NoEndConv).ipynb>) - Gradient Free Optimizer Test (Best Performing)

We use multiple circuits tested in the GPU File under the V4 (Final Testing) under different categories. Rest of directories are tests and represent the iterative work.
All Circuits Tested Accesible Below (Folders)
* [Gradient Free Optimizer](<GPU/V4 (FINAL TESTING)>) - Gradient Free Optimizer Testing
* [Gradient Based Optimizer](<GPU/V4 (FINAL TESTING)/Gradient Testing>) - Gradient Based Optimizer Testing (ReverseGradientEstimator)
### Paper Link (In Progress)
Note: This is a draft paper and has not yet been properly reviewed or completed.

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
    <td><img src="images/circuit.png" alt="Sample Circuit Decomposed" width="1000" height="1700"></td>
  </tr>
</table>


## Algorithms
[Gradient Free Optimizer](<GPU/V4 (FINAL TESTING)/Circuit 1/Estimator 4 Classes Circuit 1 (256 Batch)/4Qubits(NoEndConv).ipynb>) - Gradient Free Optimizer Test (Best Performing)
<table>
  <tr>
    <td><img src="images/GradientFree4ClassesAccuracy.png" alt="Gradient Free 4 Classes Accuracy" width="300" height="225"></td>
    <td><img src="images/GradientFree4ClassesLoss.png" alt="Gradient Free 4 Classes Loss" width="300" height="225"></td>
  </tr>
</table>

<br>

[Gradient Based Optimizer](<GPU/V4 (FINAL TESTING)/Gradient Testing/Circuit1/4 Classes/4Qubits(One_Hot)_ADAM_256_95Epoch.ipynb>) - Gradient Based Optimizer Test (Best Performing)
<table>
  <tr>
    <td><img src="images/GradientImage4ClassesAccuracy.png" alt="Gradient Image 4 Classes Loss" width="300" height="225"></td>
    <td><img src="images/GradientImage4ClassesLoss.png" alt="Gradient Image 4 Classes" width="300" height="225"></td>
  </tr>
</table>

## Output
<table>
  <tr>
    <td><img src="images/output.png" alt="Sample Output (Best Performance Enhanced Circuit)" width="600" height="650"></td>
  </tr>
</table>

## Future Aim / Next Steps
--To Be Filled Later--

## Works Cited
Modified from (https://qiskit-community.github.io/qiskit-machine-learning/tutorials/11_quantum_convolutional_neural_networks.html)
To Be Filled Out Soon.
