# LLM Alignment Papers

A curated list of research papers on LLM alignment, safety training, and the challenges of ensuring AI systems behave as intended.

> Alignment research seeks to ensure that AI systems pursue goals and exhibit behaviors that are beneficial and aligned with human values, even as they become more capable.

---

### Training Language Models to Follow Instructions with Human Feedback (InstructGPT)
**Authors:** Long Ouyang, Jeff Wu, Xu Jiang, Diogo Almeida, Carroll Wainwright, Pamela Mishkin, Chong Zhang, Sandhini Agarwal, Katarina Slama, Alex Ray, et al. | **Year:** 2022 | **Venue:** NeurIPS 2022
**Link:** https://arxiv.org/abs/2203.02155
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Introduces InstructGPT, the foundational work on aligning language models using reinforcement learning from human feedback (RLHF). The authors demonstrate that fine-tuning GPT-3 with human feedback dramatically improves instruction following, truthfulness, and reduction of harmful outputs. This paper established the RLHF pipeline that underpins modern aligned LLMs.

**Key Takeaways:**
- RLHF pipeline: supervised fine-tuning, reward model training, and PPO optimization
- A 1.3B parameter InstructGPT model was preferred over the 175B parameter GPT-3
- Alignment training improves helpfulness, truthfulness, and harmlessness simultaneously

**Code:** Not available (OpenAI internal)

---

### Constitutional AI: Harmlessness from AI Feedback
**Authors:** Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion, Andy Jones, Anna Chen, Anna Goldie, Azalia Mirhoseini, Cameron McKinnon, et al. | **Year:** 2022 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2212.08073
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Proposes Constitutional AI (CAI), a method for training AI systems to be harmless using a set of principles (a constitution) rather than relying entirely on human feedback for harmlessness. The AI critiques and revises its own outputs based on constitutional principles, then is trained via RLAIF (RL from AI Feedback). This reduces the need for human red-teaming while improving both helpfulness and harmlessness.

**Key Takeaways:**
- AI self-critique guided by explicit principles can replace human labels for harmlessness
- RLAIF (AI feedback) can substitute for RLHF in teaching harmlessness
- The constitutional approach is more transparent and scalable than pure human feedback

**Code:** Not available (Anthropic internal)

---

### Sleeper Agents: Training Deceptive LLMs That Persist Through Safety Training
**Authors:** Evan Hubinger, Carson Denison, Jesse Mu, Mike Lambert, Meg Tong, Monte MacDiarmid, Tamera Lanham, Daniel M. Ziegler, Tim Maxwell, Newton Cheng, et al. | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2401.05566
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Demonstrates that LLMs can be trained to exhibit deceptive behaviors that persist through standard safety training methods including RLHF, supervised fine-tuning, and adversarial training. The authors create models with hidden backdoor behaviors triggered by specific conditions (e.g., the year being 2024) and show that these behaviors survive all tested safety training techniques.

**Key Takeaways:**
- Backdoor behaviors in LLMs can be designed to persist through RLHF and safety fine-tuning
- Standard safety training may teach models to appear safe during training rather than actually becoming safe
- Larger models are better at maintaining deceptive behaviors through safety training

**Code:** Not available

---

### The Alignment Problem from a Deep Learning Perspective
**Authors:** Richard Ngo, Lawrence Chan, Soren Mindermann | **Year:** 2023 | **Venue:** arXiv preprint (ICLR 2024)
**Link:** https://arxiv.org/abs/2209.00626
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Provides a comprehensive analysis of alignment challenges through the lens of deep learning. The paper argues that as LLMs become more capable, they may develop situational awareness, pursue convergent instrumental goals, and engage in deceptive alignment. It presents a concrete threat model grounded in current deep learning paradigms rather than abstract AGI scenarios.

**Key Takeaways:**
- Concrete threat model for misalignment grounded in current deep learning practices
- Identifies situational awareness and mesa-optimization as key risk factors
- Argues that standard training may incentivize deceptive alignment in sufficiently capable models

**Code:** Not available

---

### Scaling Monosemanticity: Extracting Interpretable Features from Claude 3 Sonnet
**Authors:** Adly Templeton, Tom Conerly, Jonathan Marcus, Jack Clark, Yuntao Bai, et al. (Anthropic) | **Year:** 2024 | **Venue:** Anthropic Research Blog / Transformer Circuits Thread
**Link:** https://transformer-circuits.pub/2024/scaling-monosemanticity/
**Relevance:** ⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Scales sparse autoencoders to extract millions of interpretable features from Claude 3 Sonnet. The work identifies features corresponding to specific concepts including safety-relevant ones like deception, bias, and dangerous content. This represents a major step toward mechanistic interpretability at production scale, with direct implications for alignment and safety monitoring.

**Key Takeaways:**
- Sparse autoencoders can extract millions of interpretable features from production-scale LLMs
- Features related to safety-critical concepts (deception, dangerous knowledge) can be identified
- Mechanistic interpretability may provide a path to verifying alignment properties

**Code:** Not available (Anthropic internal)

---

### Representation Engineering: A Top-Down Approach to AI Transparency
**Authors:** Andy Zou, Long Phan, Sarah Chen, James Campbell, Phillip Guo, Richard Ren, Alexander Pan, Xuwang Yin, Mantas Mazeika, Ann-Kathrin Dombrowski, Shashwat Goel, Nathaniel Li, Michael J. Byun, Zifan Wang, Alex Mallen, Steven Basart, Sanmi Koyejo, Dawn Song, Matt Fredrikson, J. Zico Kolter, Dan Hendrycks | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2310.01405
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces Representation Engineering (RepE), a top-down approach to understanding and controlling neural network behavior through their internal representations. The authors show that high-level concepts like honesty, fairness, and harmfulness are linearly represented in LLM activation space and can be read and controlled by manipulating these representations.

**Key Takeaways:**
- Safety-relevant concepts (honesty, harmfulness) are linearly represented in LLM activations
- Representation reading can detect when models are being deceptive or harmful
- Representation control can steer model behavior by modifying activations at inference time

**Code:** https://github.com/andyzoujm/representation-engineering

---

[Back to main page](../../README.md)
