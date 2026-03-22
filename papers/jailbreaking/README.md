# Jailbreaking Papers

A curated list of research papers on jailbreaking techniques that bypass LLM safety training and alignment measures.

> Jailbreaking refers to techniques that circumvent the safety guardrails of aligned language models, causing them to generate content they were trained to refuse.

---

### Jailbroken: How Does LLM Safety Training Fail?
**Authors:** Alexander Wei, Nika Haghtalab, Jacob Steinhardt | **Year:** 2023 | **Venue:** NeurIPS 2023
**Link:** https://arxiv.org/abs/2307.02483
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Provides a systematic analysis of why LLM safety training fails against jailbreak attacks. The authors identify two fundamental failure modes: competing objectives (where the model's helpfulness objective conflicts with safety) and mismatched generalization (where safety training fails to generalize to novel attack distributions). They evaluate jailbreak techniques against GPT-4 and Claude.

**Key Takeaways:**
- Two fundamental failure modes explain most successful jailbreaks: competing objectives and mismatched generalization
- Safety training via RLHF has inherent limitations that cannot be easily patched
- Provides a theoretical framework for understanding why jailbreaks succeed

**Code:** Not available

---

### Do Anything Now: Characterizing and Evaluating In-The-Wild Jailbreak Prompts on Large Language Models
**Authors:** Xinyue Shen, Zeyuan Chen, Michael Backes, Yun Shen, Yang Zhang | **Year:** 2023 | **Venue:** CCS 2024
**Link:** https://arxiv.org/abs/2308.03825
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Conducts the first large-scale measurement study of in-the-wild jailbreak prompts. The authors collected 6,387 jailbreak prompts from December 2022 to December 2023 from Reddit, Discord, and dedicated websites. They find that jailbreak prompts are evolving rapidly, with community-driven development cycles that outpace model provider patches.

**Key Takeaways:**
- First large-scale empirical study of real-world jailbreak prompts (6,387 prompts collected)
- Community-driven jailbreak development evolves faster than provider-side defenses
- Categorizes jailbreak strategies including role-playing, privilege escalation, and prompt leaking

**Code:** https://github.com/verazuo/jailbreak_llms

---

### AutoDAN: Generating Stealthy Jailbreak Prompts on Aligned Large Language Models
**Authors:** Xiaogeng Liu, Nan Xu, Muhao Chen, Chaowei Xiao | **Year:** 2023 | **Venue:** ICLR 2024
**Link:** https://arxiv.org/abs/2310.04451
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces AutoDAN, a method that uses a hierarchical genetic algorithm to automatically generate stealthy jailbreak prompts. Unlike GCG-style attacks that produce gibberish suffixes, AutoDAN generates semantically meaningful jailbreaks that evade perplexity-based detection filters while maintaining high attack success rates.

**Key Takeaways:**
- Genetic algorithm-based approach generates readable jailbreak prompts that bypass perplexity filters
- Demonstrates that defenses based on detecting unnatural inputs are insufficient
- Automated generation enables scalable red-teaming of LLM safety

**Code:** https://github.com/SheltonLiu-N/AutoDAN

---

### Prompt Automatic Iterative Refinement (PAIR)
**Authors:** Patrick Chao, Alexander Robey, Edgar Dobriban, Hamed Hassani, George J. Pappas, Eric Wong | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2310.08419
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Proposes PAIR, an algorithm that uses an attacker LLM to automatically generate jailbreak prompts for a target LLM through iterative refinement. PAIR requires only black-box access to the target model and generates semantic jailbreaks in under twenty queries on average, making it highly efficient for automated red-teaming.

**Key Takeaways:**
- Black-box jailbreak generation requiring only API access to the target model
- Uses an attacker LLM to iteratively refine prompts based on target model responses
- Highly efficient, typically succeeding in fewer than 20 queries

**Code:** https://github.com/patrickrchao/JailbreakingLLMs

---

### Tree of Attacks: Jailbreaking Black-Box LLMs with Crafted Prompts
**Authors:** Anay Mehrotra, Manolis Zampetakis, Paul Kassianik, Blaine Nelson, Hyrum Anderson, Yaron Singer, Amin Karbasi | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2312.02119
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces Tree of Attacks with Pruning (TAP), a method that uses tree-of-thought reasoning to generate jailbreak prompts. TAP employs an attacker LLM that explores multiple attack paths in parallel, pruning unsuccessful branches, and refining promising ones. The method achieves high success rates against GPT-4, GPT-4-Turbo, and Llama-2 with limited queries.

**Key Takeaways:**
- Tree-based search strategy explores diverse attack paths simultaneously
- Achieves high success rates with fewer queries than iterative methods
- Demonstrates effectiveness against state-of-the-art aligned models including GPT-4

**Code:** https://github.com/RICommunity/TAP

---

### Many-shot Jailbreaking
**Authors:** Anthropic (Cem Anil, Esin Durmus, et al.) | **Year:** 2024 | **Venue:** Anthropic Research Blog / arXiv
**Link:** https://arxiv.org/abs/2404.04495
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Demonstrates that large context windows enable a new class of jailbreak attacks. By including many examples of the desired harmful behavior in a long prompt (many-shot), the model's in-context learning overrides its safety training. The attack is simple, requires no optimization, and scales in effectiveness with context window size.

**Key Takeaways:**
- Larger context windows create new attack surfaces through in-context learning exploitation
- Simple attack requiring only many examples of harmful Q&A pairs in the prompt
- Effectiveness scales with the number of shots and context window size

**Code:** Not available

---

### DeepInception: Hypnotize Large Language Model to Be Jailbreaker
**Authors:** Xuan Li, Zhanke Zhou, Jianing Zhu, Jiangchao Yao, Tongliang Liu, Bo Han | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2311.03191
**Relevance:** ⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Proposes DeepInception, a jailbreak technique inspired by the movie Inception that creates nested fictional scenarios to bypass LLM safety. By embedding harmful requests within multiple layers of hypothetical role-playing contexts, the attack exploits the model's tendency to maintain narrative consistency over safety guidelines.

**Key Takeaways:**
- Nested fictional scenarios create psychological distance that bypasses safety training
- Exploits the tension between helpfulness in creative writing and safety refusal
- Simple to execute and effective across multiple LLMs without requiring optimization

**Code:** https://github.com/tmlr-group/DeepInception

---

### Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation
**Authors:** Yangsibo Huang, Samyak Gupta, Mengzhou Xia, Kai Li, Danqi Chen | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2310.06987
**Relevance:** ⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Reveals that manipulating the generation process of open-source LLMs (e.g., modifying sampling parameters, generation configurations, or decoding strategies) can catastrophically break safety alignment. The authors show that simple changes to temperature, top-k, or the addition of a few guided tokens can cause aligned models to produce harmful content.

**Key Takeaways:**
- Safety alignment of open-source LLMs can be broken by manipulating generation hyperparameters
- Even small changes to decoding strategies can bypass safety training entirely
- Highlights that weight-level access provides fundamentally different attack capabilities than API-only access

**Code:** Not available

---

[Back to main page](../../README.md)
