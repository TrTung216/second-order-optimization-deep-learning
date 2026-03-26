# Research on Second-Order Optimization Algorithms in Deep Learning

This repository contains the research paper:

**"Research on Some Second-Order Optimization Algorithms in Deep Learning Model Training"**

## Authors
- Vu Van Doc
- Nguyen Khac Hieu
- Tran Trong Tung
- Trinh Trung Hoang

## Abstract
This research analyzes and compares first-order and second-order optimization algorithms used in deep learning training. The study focuses on the effectiveness of second-order methods such as **L-BFGS** and **K-FAC** compared with traditional optimizers like **SGD** and **Adam**.

Experiments were conducted using **CNN** and **RNN** architectures on the **CIFAR-10 dataset**. Results show that second-order methods can achieve faster convergence and improved stability, though with higher computational cost.

## Experiments
Framework: **PyTorch**

Dataset:
- CIFAR-10

Optimizers evaluated:
- SGD
- Adam
- L-BFGS
- K-FAC

Models:
- CNN
- RNN

## Results
The experiments demonstrate a trade-off between convergence speed and computational cost.  
Among the evaluated methods, **K-FAC shows a balanced performance across CNN and RNN architectures.**

## Paper
You can read the full paper here:

📄 `paper/second_order_optimization_deep_learning.pdf`

## License
This repository is for academic and research purposes.
