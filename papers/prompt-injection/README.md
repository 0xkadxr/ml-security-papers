# Prompt Injection Papers

A curated list of research papers on prompt injection attacks and defenses targeting LLM-integrated applications.

> Prompt injection is a class of attacks where adversarial inputs manipulate the behavior of large language models, causing them to ignore their original instructions or execute unintended actions.

---

### Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection
**Authors:** Kai Greshake, Sahar Abdelnabi, Shailesh Mishra, Christoph Endres, Thorsten Holz, Mario Fritz | **Year:** 2023 | **Venue:** AISec @ CCS 2023
**Link:** https://arxiv.org/abs/2302.12173
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** This paper introduces the concept of indirect prompt injection, where an attacker places malicious instructions in external content (e.g., web pages, emails) that an LLM-integrated application retrieves and processes. The authors demonstrate practical attacks against real systems including Bing Chat and GPT-4 powered applications, showing how adversaries can exfiltrate data, spread injections, and manipulate outputs.

**Key Takeaways:**
- Indirect prompt injection is a fundamental vulnerability in retrieval-augmented LLM applications
- Attacks can be embedded in web pages, emails, or documents that the LLM processes
- The paper demonstrates end-to-end attacks including data exfiltration and social engineering

**Code:** https://github.com/greshake/llm-security

---

### Ignore This Title and HackAPrompt: Exposing Systemic Weaknesses of LLMs Through a Global Scale Prompt Hacking Competition
**Authors:** Sander Schulhoff, Jeremy Pinto, Anaum Khan, Louis-Francois Bouchard, Chenglei Si, Sid Anber, Alber Catav, et al. | **Year:** 2023 | **Venue:** EMNLP 2023
**Link:** https://arxiv.org/abs/2311.16119
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Presents results from HackAPrompt, a large-scale prompt hacking competition with over 600,000 adversarial prompts collected from 2,800+ participants. The competition targeted OpenAI models across increasingly difficult prompt injection challenges. The authors taxonomize successful attack strategies and identify systemic weaknesses in LLM defenses.

**Key Takeaways:**
- Large-scale empirical evidence of prompt injection vulnerabilities across multiple defense strategies
- Categorizes attack techniques including context ignoring, payload splitting, and virtualization
- Demonstrates that even sophisticated prompt-based defenses are systematically breakable

**Code:** https://github.com/trigaten/Prompt_Systematic_Review

---

### Prompt Injection Attack Against LLM-Integrated Applications
**Authors:** Yi Liu, Gelei Deng, Yuekang Li, Kailong Wang, Tianwei Zhang, Yepang Liu, Haoyu Wang, Yan Zheng, Yang Liu | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2306.05499
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Provides a systematic study of prompt injection attacks on LLM-integrated applications. The authors propose a framework for understanding prompt injection in the context of applications that use LLMs as backends and demonstrate attacks against multiple real-world applications.

**Key Takeaways:**
- Formalizes prompt injection attack surfaces in LLM-integrated applications
- Evaluates attacks against real-world applications and plugins
- Proposes a taxonomy distinguishing direct and indirect injection vectors

**Code:** Not available

---

### Tensor Trust: Interpretable Prompt Injection Attacks from an Online Game
**Authors:** Sam Toyer, Olivia Watkins, Ethan Adrian Menber, Justin Svegliato, Luke Bailey, Tiffany Wang, Isaac Ong, Karim Elmaaroufi, Pieter Abbeel, Trevor Darrell, Alan Ritter, Stuart Russell | **Year:** 2023 | **Venue:** NeurIPS 2023
**Link:** https://arxiv.org/abs/2311.01011
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces Tensor Trust, an online game where players craft prompt injection attacks and defenses to steal each other's secret access codes. The game collected over 126,000 prompt injection attacks and 46,000 defenses, creating one of the largest datasets of human-generated prompt injections.

**Key Takeaways:**
- Gamified approach to collecting diverse, human-crafted prompt injection attacks
- Largest public dataset of prompt injection attacks and defenses at time of publication
- Analysis reveals common attack patterns and the fragility of prompt-based defenses

**Code:** https://github.com/HumanCompatibleAI/tensor-trust

---

### Injecting New Knowledge into Large Language Models via Supervised Fine-Tuning
**Authors:** Nick Mecklenburg, Yiyou Lin, Xiaoxiao Li, Daniel Holstein, Leonardo Nunes, Sara Malvar, Bruno Silva, Ranveer Chandra, Vijay Aski, Pavan Kumar Reddy Yannam, Tolga Aktas, Todd Hendry | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2404.00628
**Relevance:** ⭐⭐⭐ | **Impact:** ⭐⭐⭐

**Summary:** Explores how supervised fine-tuning can be used to inject new knowledge into LLMs, analyzing the conditions under which knowledge injection succeeds or fails. While primarily about knowledge injection, this work has security implications for understanding how fine-tuning can alter model behavior and potentially introduce vulnerabilities.

**Key Takeaways:**
- Fine-tuning can effectively inject new factual knowledge into LLMs
- The process can inadvertently alter safety-relevant behaviors
- Relevant context for understanding training-time attacks and data poisoning risks

**Code:** Not available

---

### Demystifying RCE Vulnerabilities in LLM-Integrated Apps
**Authors:** Tong Liu, Zizhuang Deng, Guozhu Meng, Yuekang Li, Kai Chen | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2309.02926
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Investigates remote code execution (RCE) vulnerabilities in LLM-integrated applications, demonstrating how prompt injection can be escalated to achieve arbitrary code execution. The study analyzes real-world LLM frameworks and applications, finding critical vulnerabilities that allow attackers to execute system commands through crafted prompts.

**Key Takeaways:**
- Prompt injection can escalate to full remote code execution in LLM apps with code execution capabilities
- Identifies systemic RCE vulnerability patterns across popular LLM frameworks
- Highlights the danger of giving LLMs access to code interpreters and system tools without proper sandboxing

**Code:** Not available

---

### Prompt Injection Attacks and Defenses in LLM-Integrated Applications
**Authors:** Yupei Liu, Yuqi Jia, Runpeng Geng, Jinyuan Jia, Neil Zhenqiang Gong | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2310.12815
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Provides a comprehensive study of prompt injection attacks and defenses in LLM-integrated applications. The authors propose a unified framework for evaluating both attacks and defenses, test multiple attack strategies against various defense mechanisms, and find that existing defenses provide limited protection.

**Key Takeaways:**
- Systematic evaluation framework for prompt injection attacks and defenses
- Existing defense mechanisms (instruction-based, detection-based, and input/output filtering) are insufficient
- Proposes and evaluates novel defense strategies with improved but still imperfect protection

**Code:** Not available

---

### Universal and Transferable Adversarial Attacks on Aligned Language Models
**Authors:** Andy Zou, Zifan Wang, Nicholas Carlini, Milad Nasr, J. Zico Kolter, Matt Fredrikson | **Year:** 2023 | **Venue:** arXiv preprint (presented at various workshops)
**Link:** https://arxiv.org/abs/2307.15043
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Proposes the Greedy Coordinate Gradient (GCG) attack, an automated method that generates adversarial suffixes which cause aligned LLMs to produce harmful content. The attack is universal (one suffix works across many prompts) and transferable (suffixes generated on open-source models transfer to closed-source models like GPT-4 and Claude).

**Key Takeaways:**
- Automated adversarial suffix generation using gradient-based optimization on open-source models
- Adversarial suffixes transfer across different LLM architectures and API-only models
- Demonstrates fundamental limitations of current alignment techniques against optimization-based attacks

**Code:** https://github.com/llm-attacks/llm-attacks

---

[Back to main page](../../README.md)
