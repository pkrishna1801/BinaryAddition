# Binary Addition Using Recurrent Neural Networks

This project implements a **Recurrent Neural Network (RNN)** to learn **binary addition** at the bit level.  
The model processes two binary numbers sequentially and predicts both the **sum bit** and the **carry bit** at each timestep.

---

## Overview

Binary addition is a classic sequential reasoning task that requires memory of previous states (carry propagation).  
This project demonstrates how an RNN can learn this temporal dependency using supervised learning.

---

## Architecture

**BinaryAdditionRNN (2–16–2)**  
- **Input size:** 2 (two binary digits per timestep)  
- **Hidden layer:**  
  - 1 RNN layer  
  - 16 hidden units  
  - ReLU activation  
- **Output size:** 2  
  - Carry bit  
  - Sum bit  
- **Sequence output:** Enabled (returns output at every timestep)  
- **Loss function:** Binary Cross-Entropy with Logits  

---

## Dataset

**BinaryAdditionDataset**
- Generates random binary numbers
- Inputs:
  - Binary representation of two numbers
  - Shape: `(sequence_length, 2)`
- Targets:
  - Carry bit and sum bit at each timestep
  - Shape: `(sequence_length, 2)`

This formulation allows the model to learn **carry propagation over time**, not just final outputs.

---

## Training

- Framework: **PyTorch**
- Optimizer: Adam
- Loss: `BCEWithLogitsLoss`
- Task: Sequence-to-sequence prediction of binary addition

---

## Key Learning Objectives

- Understanding sequential learning with RNNs
- Modeling arithmetic reasoning using neural networks
- Learning temporal dependencies (carry handling)
- Designing custom datasets for sequence problems

---

## Applications & Extensions

- Multi-digit arithmetic tasks
- Comparison with LSTM / GRU architectures
- Curriculum learning for longer bit-widths
- Analysis of sequence-level accuracy vs bit-level accuracy

---

## Author

**Prarthana**  
Machine Learning & Neural Networks  
