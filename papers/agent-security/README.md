# Agent Security Papers

A curated list of research papers on security risks and vulnerabilities of LLM-based autonomous agents.

> As LLMs are deployed as autonomous agents with tool access, new security risks emerge from the interaction between language model vulnerabilities and real-world capabilities like code execution, web browsing, and API access.

---

### Identifying the Risks of LM Agents with an LM-Emulated Sandbox (ToolEmu)
**Authors:** Yangjun Ruan, Honghua Dong, Andrew Wang, Silviu Pitis, Yongchao Zhou, Jimmy Ba, Yann Dubois, Chris J. Maddison, Tatsunori Hashimoto | **Year:** 2023 | **Venue:** ICLR 2024
**Link:** https://arxiv.org/abs/2309.15817
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Introduces ToolEmu, a framework that uses LLMs to emulate tool execution for safely evaluating the risks of LLM agents. The authors identify 36 categories of potential agent failures across 144 test cases and find that even GPT-4 based agents exhibit risky behaviors in 23.9% of cases, including data leakage, unauthorized financial transactions, and system compromise.

**Key Takeaways:**
- LLM-emulated sandboxes enable safe evaluation of dangerous agent behaviors
- Even GPT-4 agents fail in nearly a quarter of safety-critical scenarios
- Categorizes 36 types of agent failures spanning data privacy, financial harm, and system integrity

**Code:** https://github.com/ryoungj/ToolEmu

---

### AgentDojo: A Dynamic Environment to Evaluate Attacks and Defenses for LLM Agents
**Authors:** Edoardo Debenedetti, Jie Zhang, Mislav Balunovic, Luca Beurer-Kellner, Marc Fischer, Florian Tramer | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2406.13352
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Presents AgentDojo, a dynamic evaluation framework designed to test the security of LLM agents against prompt injection and other attacks. The framework features realistic task suites where agents interact with tools (email, calendar, banking, etc.) while adversaries inject malicious content. The authors find that current agents and defenses fail against adaptive attacks.

**Key Takeaways:**
- Dynamic evaluation framework with realistic tool-use scenarios for agent security
- Current prompt injection defenses are ineffective against adaptive attackers
- Benchmark includes both utility metrics and security metrics to measure defense tradeoffs

**Code:** https://github.com/ethz-spylab/agentdojo

---

### InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents
**Authors:** Qiusi Zhan, Zhixiang Liang, Zifan Ying, Daniel Kang | **Year:** 2024 | **Venue:** ACL 2024 Findings
**Link:** https://arxiv.org/abs/2403.02691
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces InjecAgent, a benchmark for evaluating the vulnerability of tool-integrated LLM agents to indirect prompt injection attacks. The benchmark includes 1,054 test cases across 17 user tools and 62 attacker tools. Results show that agents based on GPT-4 are vulnerable to indirect prompt injection in up to 24% of cases, with ReAct-style agents being more susceptible than direct tool-calling agents.

**Key Takeaways:**
- First comprehensive benchmark specifically targeting indirect prompt injection in LLM agents
- ReAct-style agents are more vulnerable to prompt injection than direct function-calling agents
- Even tool-specific instructions and safety prompts provide limited protection

**Code:** https://github.com/uiuc-kang-lab/InjecAgent

---

### R-Judge: Benchmarking Safety Risk Awareness for LLM Agents
**Authors:** Tongxin Yuan, Zhiwei He, Lingzhong Dong, Yiming Wang, Ruijie Zhao, Tian Xia, Lizhen Xu, Binglin Zhou, Fangqi Li, Zhuosheng Zhang, Rui Wang, Gongshen Liu | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2401.10019
**Relevance:** ⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces R-Judge, a benchmark for evaluating whether LLMs can identify safety risks in agent interaction records. The benchmark contains 569 multi-turn interaction records across 27 risk scenarios. The study finds significant gaps in risk awareness even for advanced models, with GPT-4 achieving only 72.3% accuracy in identifying risky agent behaviors.

**Key Takeaways:**
- Benchmark for evaluating LLM safety risk awareness in agentic contexts
- Even GPT-4 struggles to identify risky agent behaviors reliably
- Multi-turn interactions create compounding risk that single-turn safety evaluations miss

**Code:** https://github.com/Lordog/R-Judge

---

### Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection
**Authors:** Kai Greshake, Sahar Abdelnabi, Shailesh Mishra, Christoph Endres, Thorsten Holz, Mario Fritz | **Year:** 2023 | **Venue:** AISec @ CCS 2023
**Link:** https://arxiv.org/abs/2302.12173
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** While primarily a prompt injection paper, this work is foundational for agent security as it demonstrates how indirect prompt injection through retrieved content (web pages, emails) can compromise LLM agents. The authors show end-to-end attacks that hijack agent behavior including data exfiltration and spreading injections through agent actions.

**Key Takeaways:**
- Indirect prompt injection is the primary threat vector for LLM agents that process external data
- Agent capabilities (email, web browsing, code execution) amplify the impact of prompt injection
- Demonstrates attack propagation where compromised agents spread injections to other systems

**Code:** https://github.com/greshake/llm-security

---

### Prompt Injection Attacks on Large Language Model-Based Agentic Systems
**Authors:** Razan Baltaji, et al. | **Year:** 2024 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2403.14610
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Provides a comprehensive analysis of prompt injection attacks specifically targeting LLM-based agentic systems. The paper categorizes attacks by the agent component they target (planning, tool use, memory) and evaluates the effectiveness of various attack strategies against different agent architectures. The authors propose a threat model specific to agentic systems.

**Key Takeaways:**
- Agent-specific threat model covering planning, tool-use, and memory components
- Different agent architectures have different vulnerability profiles
- Memory poisoning and tool manipulation create persistent attack vectors beyond single interactions

**Code:** Not available

---

[Back to main page](../../README.md)
