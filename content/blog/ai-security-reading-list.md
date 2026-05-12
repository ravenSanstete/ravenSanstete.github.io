---
title: "A Nostalgia Reading List for Beginners on AI Security"
date: 2025-02-06
tags: ["AI Security", "Reading List"]
description: "Missing the innocent time but we must move forward for bigger challenges"
---

## 1. Adversarial Attacks

### 1.1. Adversarial Examples (AE) & Defenses

#### 1.1.1. Survey

- **Wild patterns: Ten years after the rise of adversarial machine learning** — A survey covering AI security research before 2018, focusing primarily on adversarial examples and poisoning attacks.

#### 1.1.2. Attack Side

- **FGSM** — the first AE
- **PGD** — the first iterative AE generation algorithm
- **C&W** — systematization work
- **TextBugger** — AE attacks on NLP models
- **Black-box Adversarial Attacks on Commercial Speech Platforms with Minimal Information** — AE on audio models

#### 1.1.3. Empirical Defense

- **MagNet: a Two-Pronged Defense against Adversarial Examples** (CCS'17) — manifold-based, unsupervised approach
- **Obfuscated Gradients Give a False Sense of Security** (ICML'18 Best Paper) — surveys pre-2018 defenses and breaks them; circumventing defenses to adversarial examples

#### 1.1.4. Certified Defense

- **SoK: Certified Robustness for Deep Neural Networks** — a survey
- **Certified Adversarial Robustness via Randomized Smoothing** (ICML'19) — an early work on randomized smoothing
- **AI2: Safety and Robustness Certification of Neural Networks with Abstract Interpretation** (S&P'18) — deterministic certification based on ideas from program verification

### 1.2. Backdoor Attacks & Defenses

#### 1.2.1. Survey

- **TrojanZoo** — huge engineering efforts with an open-sourced framework

#### 1.2.2. Attack Side

- **TrojanNN** (NDSS'17) — neuron-based injection
- **BadNet** (IEEE Access) — data-based injection, classic
- **Latent Backdoor** (CCS'19) — extending the backdoor attack to pretrained encoders, via feature alignment
- **Input-Aware Backdoor** (NeurIPS'20) — the first dynamic trigger backdoor
- **Hidden Trigger Backdoor Attack on NLP Models via Linguistic Style Manipulation** (Security'22) — the first dynamic backdoor on NLP models *(Ours)*
- **Towards Backdoor Attack on Deep Learning based Time Series Classification** (ICDE'22) — the first effective backdoor attack on time series models *(Ours)*

#### 1.2.3. Defense Side

- **Fine-pruning** (RAID'18) — pruning and finetuning, based on the hypothesized differences in activation patterns
- **STRIP** (ACSAC'19) — detection based on the hypothesis that triggered input is resilient to noise
- **Neural Cleanse** (S&P'19) — strong link between backdoor behavior and static trigger pattern
- **ABS** (CCS'19) — neuron-level inspection

### 1.3. Poisoning Attacks

#### 1.3.1. Clean-Label Attacks

- **Poison Frogs! Targeted Clean-Label Poisoning Attacks on Neural Networks** (NIPS'18) — present the idea of clean-label attack, feature-level alignment
- **Bullseye Polytope** (EuroS&P'21) — enhancing the attack effectiveness from a geometric view, simple yet effective
- **Label-consistent backdoor attack** — another approach towards clean-label attack

### 1.4. Byzantine Attacks

- **The Hidden Vulnerability of Distributed Learning in Byzantium (Krum)** (NIPS'17) — Statistics-based defense
- **Justinian's GAAvernor: Robust Distributed Learning with Gradient Aggregation Agent** (Security'20) — RL-based defense *(Ours)*

## 2. Privacy Attacks

### 2.1. Membership Inference

#### 2.1.1. Survey

- **Membership Inference Attacks on Machine Learning: A Survey** (ACM Computing Surveys)

#### 2.1.2. Attack Side

- **Membership Inference Attacks against Machine Learning Models** (S&P'17) — the earliest MIA
- **ML-Leaks** (NDSS'18) — a minimalist

#### 2.1.3. Defense Side

- **MemGuard** (CCS'19) — defense by logit-level obfuscation

### 2.2. Property Inference

#### 2.2.1. Global Property

- A CCS'18 paper on inference based on model weights

#### 2.2.2. Individual Property

- **Exploiting Unintended Feature Leakage in Collaborative Learning** (S&P'19) — feature inference based on the embedding or gradient in federated learning scenarios
- **Privacy risks of general-purpose language models** (S&P'20) — reconstructing the privacy semantics from the text embeddings of LLMs *(Ours)*

### 2.3. Data Reconstruction

#### 2.3.1. Gradient-Based

- **Deep Leakage from Gradients (DLG)** (NeurIPS'19) — the earliest
- **GradInversion** (CVPR'21) — incorporate data priors into the reconstruction
- **Exploring the Security Boundary of Data Reconstruction via Neuron Exclusivity Analysis** (Security'22) — equation-solving-based reconstruction, pixel-level reconstruction *(Ours)*

#### 2.3.2. Weight-Based

- **Model Inversion Attacks that Exploit Confidence Information and Basic Countermeasures** (CCS'15) — present the idea of model inversion
- **Dreaming to Distill: Data-free Knowledge Transfer via DeepInversion** (CVPR'20) — distilling (synthetic) training data from the pretrained model only
- **Extracting Training Data from Large Language Models** (USENIX Security'21) — extracting training data from GPT-2 based on MIA

### 2.4. Model Extraction/Stealing

#### 2.4.1. Attack Side

- **Stealing machine learning models via prediction APIs** (Security'16) — the earliest attack based on distilling
- **High Accuracy and High Fidelity Extraction of Neural Networks** (Security'20) — propose the notion of fidelity and exploit the ReLU property
- **Matryoshka: Stealing Functionality of Private ML Data by Hiding Models in Model** (TPAMI'24) — stealing by steganography *(Ours)*

#### 2.4.2. Defense Side

- **PRADA: Protecting against DNN Model Stealing Attacks** (EuroS&P'19) — a classic one

## 3. Copyright Protection

### 3.1. Model Watermarking

#### 3.1.1. Survey

- **SoK: How Robust is Image Classification Deep Neural Network Watermarking?** (S&P'22) — a good survey
- **A Systematic Review on Model Watermarking for Neural Networks**

#### 3.1.2. White-box Watermarking

- **Embedding Watermarks into Deep Neural Networks** (ICME'17) — the earliest white-box watermarking scheme
- **Cracking White-box DNN Watermarks via Invariant Neuron Transforms** (KDD'23) — Weight-based Obfuscation Attack *(Ours)*
- **Rethinking White-Box Watermarks on Deep Learning Models under Neural Structural Obfuscation** (USENIX Security'23) — Structure-based Obfuscation Attack *(Ours)*

#### 3.1.3. Black-box Watermarking

- **Turning Your Weakness Into a Strength: Watermarking Deep Neural Networks by Backdooring** (USENIX Security'18) — one of the earliest black-box watermarking
- **Neural Dehydration: Effective Erasure of Black-box Watermarks from DNNs with Limited Data** (CCS'24) — cracking nine mainstream black-box watermarking schemes *(Ours)*

### 3.2. Model Fingerprinting

- **IPGuard: Protecting Intellectual Property of Deep Neural Networks via Fingerprinting the Classification Boundary** (AsiaCCS'21) — one of the earliest fingerprinting algorithms for classifiers
- **TAFA: A Task-Agnostic Fingerprinting Algorithm for Neural Networks** (ESORICS'21) — task-agnostic *(Ours)*
- **MetaV: A Meta-Verifier Approach to Task-Agnostic Model Fingerprinting** (KDD'22) — more generic *(Ours)*
