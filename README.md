# Second-Order Optimization in Deep Learning

**Research on Some Second-Order Optimization Algorithms in Deep Learning Model Training**

---

## Overview

This repository presents a research study on optimization methods in deep learning, focusing on both first-order and second-order algorithms.

The work investigates how curvature information, represented through the Hessian matrix and its approximations, affects convergence speed, stability, and computational efficiency in training neural networks.

---

## Authors

* Vu Van Doc
* Nguyen Khac Hieu
* Tran Trong Tung
* Trinh Trung Hoang

---

## Objectives

* Compare first-order methods (SGD, Adam) with second-order methods (L-BFGS, K-FAC)
* Analyze convergence behavior and training stability
* Quantify the trade-off between performance and computational cost
* Provide practical insights for optimizer selection

---

## Methods

### First-Order Methods

* Stochastic Gradient Descent (SGD)
* Adam

### Second-Order Methods

* L-BFGS
* K-FAC

---

## Experimental Setup

* Framework: PyTorch
* Dataset: CIFAR-10 (60,000 images, 10 classes)
* Hardware: NVIDIA RTX 2050 (4GB VRAM)
* Random seed: 42

### Models

* CNN: 2 convolution layers (6, 16 filters), ReLU, MaxPooling, Fully Connected (6882 parameters)
* RNN: Input size 96, hidden size 128, output size 10

### Training Configuration

* CNN: 20 epochs, batch size 256
* RNN: 15 epochs, batch size 128
* Gradient clipping: 1.0

---

## Results

### Final Results (CNN & RNN)

| Optimizer | Loss (CNN) | Loss (RNN) | Accuracy CNN (%) | Accuracy RNN (%) | Time CNN (s) | Time RNN (s) |
| --------- | ---------- | ---------- | ---------------- | ---------------- | ------------ | ------------ |
| SGD       | 1.0079     | 1.5434     | 62.60            | 42.88            | 232.8        | 229.8        |
| Adam      | 1.0826     | 1.3805     | 60.48            | 47.57            | 225.1        | 229.2        |
| L-BFGS    | 0.9427     | 1.7503     | **64.63**        | 33.19            | 620.2        | 87.2         |
| K-FAC     | **0.9270** | **1.1379** | 63.45            | **50.90**        | 265.6        | 338.0        |

---

## Key Findings

* Second-order methods achieve faster loss reduction per iteration
* Computational cost is significantly higher compared to first-order methods
* K-FAC provides the best balance between accuracy and stability across both CNN and RNN
* L-BFGS achieves the highest accuracy on CNN (64.63%) but fails on RNN (33.19%) due to instability
* Performance of second-order methods strongly depends on model architecture

---

## Repository Structure

```id="0v9j3g"
.
├── paper/
│   └── Nghiên cứu một số thuật toán tối ưu bậc hai trong huấn luyện mô hình học sâu.pdf
│
├── figures/
│   ├── cnn.png
│   ├── rnn.png
│   ├── picture3.png
│   ├── picture4.png
│   ├── picture5.png
│   ├── picture6.png
│   ├── picture7.png
│   ├── table1.png
│   └── table2.png
│
└── README.md
```

---

## Paper

The full paper is available at:

`paper/Nghiên cứu một số thuật toán tối ưu bậc hai trong huấn luyện mô hình học sâu.pdf`

---

## Discussion

The experiments demonstrate a clear trade-off:

* Second-order methods (K-FAC, L-BFGS) improve convergence efficiency
* However, they introduce higher computational overhead due to matrix operations
* K-FAC remains stable across architectures, while L-BFGS is highly sensitive to non-linear loss surfaces (especially in RNNs)

---

## Future Work

* Apply second-order methods to larger architectures (e.g., Transformers)
* Develop hybrid optimizers combining Adam and K-FAC
* Improve scalability and memory efficiency
* Conduct experiments on larger datasets

---

## References

See full references in the paper.

---

## License

This repository is intended for academic and research purposes.

---

## Citation

```id="y6ivhz"
Tran Trong Tung et al.,
"Research on Some Second-Order Optimization Algorithms in Deep Learning Model Training"
```
