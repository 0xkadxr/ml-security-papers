# Adversarial ML Papers

A curated list of research papers on adversarial machine learning, covering adversarial examples, robustness, and certified defenses.

> Adversarial ML studies how machine learning models can be attacked through carefully crafted inputs and how to build models that are robust to such attacks.

---

### Intriguing Properties of Neural Networks
**Authors:** Christian Szegedy, Wojciech Zaremba, Ilya Sutskever, Joan Bruna, Dumitru Erhan, Ian Goodfellow, Rob Fergus | **Year:** 2013 | **Venue:** ICLR 2014
**Link:** https://arxiv.org/abs/1312.6199
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** The foundational paper that discovered adversarial examples in neural networks. The authors demonstrate that imperceptible perturbations to inputs can cause deep neural networks to misclassify with high confidence. This paper launched the entire field of adversarial machine learning.

**Key Takeaways:**
- First demonstration that neural networks are vulnerable to adversarial perturbations
- Adversarial examples are imperceptible to humans but cause confident misclassification
- Adversarial examples transfer between models with different architectures

**Code:** Not available

---

### Explaining and Harnessing Adversarial Examples (FGSM)
**Authors:** Ian J. Goodfellow, Jonathon Shlens, Christian Szegedy | **Year:** 2014 | **Venue:** ICLR 2015
**Link:** https://arxiv.org/abs/1412.6572
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Introduces the Fast Gradient Sign Method (FGSM), a simple and efficient one-step method for generating adversarial examples. The paper argues that the linear nature of neural networks in high-dimensional spaces is the primary cause of adversarial vulnerability, rather than model nonlinearity or overfitting. Also proposes adversarial training as a defense.

**Key Takeaways:**
- FGSM provides a fast, single-step method for generating adversarial examples
- The linear hypothesis explains adversarial vulnerability as a consequence of high-dimensional dot products
- Adversarial training (training on adversarial examples) improves robustness

**Code:** Widely reimplemented (see CleverHans, Foolbox, ART)

---

### Towards Deep Learning Models Resistant to Adversarial Attacks (PGD)
**Authors:** Aleksander Madry, Aleksandar Makelov, Ludwig Schmidt, Dimitris Tsipras, Adrian Vladu | **Year:** 2017 | **Venue:** ICLR 2018
**Link:** https://arxiv.org/abs/1706.06083
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Proposes Projected Gradient Descent (PGD) adversarial training as a principled defense against adversarial attacks. The paper frames adversarial robustness as a min-max optimization problem and demonstrates that PGD adversarial training with random restarts produces models with strong empirical robustness. PGD became the gold standard for evaluating adversarial robustness.

**Key Takeaways:**
- PGD attack is the strongest first-order adversary and the standard benchmark for robustness evaluation
- Adversarial training framed as saddle point (min-max) optimization
- Models trained with PGD adversarial training achieve reliable robustness against first-order attacks

**Code:** https://github.com/MadryLab/mnist_challenge

---

### Certified Adversarial Robustness via Randomized Smoothing
**Authors:** Jeremy Cohen, Elan Rosenfeld, J. Zico Kolter | **Year:** 2019 | **Venue:** ICML 2019
**Link:** https://arxiv.org/abs/1902.02918
**Relevance:** ⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Introduces randomized smoothing as a scalable method for certifying adversarial robustness. By classifying inputs based on the majority vote of predictions under Gaussian noise, the method provides provable L2 robustness guarantees. This was the first certified defense to scale to ImageNet-scale models.

**Key Takeaways:**
- First certified defense that scales to large-scale image classification (ImageNet)
- Provides tight L2 robustness certificates via the Neyman-Pearson lemma
- Randomized smoothing can be applied to any base classifier without architectural changes

**Code:** https://github.com/locuslab/smoothing

---

### Adversarial Examples Are Not Bugs, They Are Features
**Authors:** Andrew Ilyas, Shibani Santurkar, Dimitris Tsipras, Logan Engstrom, Brandon Tran, Aleksander Madry | **Year:** 2019 | **Venue:** NeurIPS 2019
**Link:** https://arxiv.org/abs/1905.02175
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Presents a paradigm-shifting perspective that adversarial examples arise from models relying on non-robust but highly predictive features in the data. The authors demonstrate that models trained on adversarially perturbed data (where labels are flipped) still generalize, because adversarial perturbations introduce useful but non-robust features. This reframes adversarial vulnerability as a feature, not a bug.

**Key Takeaways:**
- Adversarial vulnerability stems from models using non-robust but predictive features
- Datasets can be decomposed into robust and non-robust feature components
- Robustness may require an inherent tradeoff with standard accuracy

**Code:** https://github.com/MadryLab/constructed-datasets

---

### RobustBench: A Standardized Adversarial Robustness Benchmark
**Authors:** Francesco Croce, Maksym Andriushchenko, Vikash Sehwag, Edoardo Debenedetti, Nicolas Flammarion, Mung Chiang, Prateek Mittal, Matthias Hein | **Year:** 2021 | **Venue:** NeurIPS 2021 (Datasets and Benchmarks Track)
**Link:** https://arxiv.org/abs/2010.09670
**Relevance:** ⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Introduces RobustBench, a standardized benchmark for evaluating adversarial robustness. The benchmark uses AutoAttack (an ensemble of parameter-free attacks) as the evaluation standard and maintains a continuously updated leaderboard. RobustBench has become the de facto standard for measuring and comparing adversarial robustness of image classifiers.

**Key Takeaways:**
- Standardized evaluation protocol eliminates issues with weak attack evaluations
- AutoAttack ensemble provides reliable robustness assessment without parameter tuning
- Maintains a living leaderboard tracking state-of-the-art robust models

**Code:** https://github.com/RobustBench/robustbench

---

### Adversarial Attacks on Multimodal Agents
**Authors:** Chen Henry Wu, Jing Yu Koh, Ruslan Salakhutdinov, Daniel Fried, Aditi Raghunathan | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2406.12814
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Demonstrates adversarial attacks against multimodal agents that operate in web and computing environments. The authors show that adversarial perturbations to images and web page elements can cause agents to take incorrect or harmful actions, such as navigating to malicious URLs or executing unintended commands.

**Key Takeaways:**
- Multimodal agents inherit adversarial vulnerabilities from their vision components
- Adversarial perturbations in the environment can redirect agent behavior
- Highlights unique risks when adversarial ML meets autonomous agents

**Code:** Not available

---

### Visual Adversarial Examples Jailbreak Aligned Large Language Models
**Authors:** Xiangyu Qi, Kaixuan Huang, Ashwinee Panda, Peter Henderson, Mengdi Wang, Prateek Mittal | **Year:** 2023 | **Venue:** AAAI 2024
**Link:** https://arxiv.org/abs/2306.13213
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Demonstrates that adversarial images can jailbreak vision-language models like LLaVA and MiniGPT-4. By optimizing adversarial perturbations in the image input, the authors bypass the text-based safety alignment of multimodal LLMs. A single adversarial image can universally jailbreak the model across many harmful text prompts.

**Key Takeaways:**
- Visual inputs provide a new attack vector that bypasses text-based safety alignment
- Adversarial images can serve as universal jailbreak keys across diverse harmful queries
- Safety alignment that focuses only on text inputs is fundamentally incomplete for multimodal models

**Code:** https://github.com/Unispac/Visual-Adversarial-Examples-Jailbreak-Large-Language-Models

---

[Back to main page](../../README.md)
