# Multimodal Attacks Papers

A curated list of research papers on adversarial attacks targeting multimodal and vision-language models.

> As AI systems increasingly process multiple modalities (text, images, audio), new attack surfaces emerge. Visual and auditory inputs can carry adversarial perturbations that bypass text-only safety measures.

---

### Visual Adversarial Examples Jailbreak Aligned Large Language Models
**Authors:** Xiangyu Qi, Kaixuan Huang, Ashwinee Panda, Peter Henderson, Mengdi Wang, Prateek Mittal | **Year:** 2023 | **Venue:** AAAI 2024
**Link:** https://arxiv.org/abs/2306.13213
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Demonstrates that adversarial images can jailbreak aligned vision-language models such as LLaVA and MiniGPT-4. By optimizing adversarial perturbations in the continuous image embedding space, the authors bypass text-based safety alignment. A single optimized adversarial image can serve as a universal jailbreak trigger across many different harmful text queries.

**Key Takeaways:**
- Visual inputs bypass text-based safety alignment in multimodal LLMs
- A single adversarial image can universally jailbreak across diverse harmful prompts
- Text-only alignment is fundamentally insufficient for multimodal model safety

**Code:** https://github.com/Unispac/Visual-Adversarial-Examples-Jailbreak-Large-Language-Models

---

### On the Adversarial Robustness of Multi-Modal Foundation Models
**Authors:** Christian Schlarmann, Matthias Hein | **Year:** 2023 | **Venue:** ICCV 2023 Workshop on Adversarial Robustness in the Real World
**Link:** https://arxiv.org/abs/2308.10741
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Systematically evaluates the adversarial robustness of multi-modal foundation models including CLIP, BLIP, and BLIP-2. The authors demonstrate that small adversarial perturbations to images can cause these models to produce arbitrary target text outputs, effectively giving attackers control over model responses through imperceptible image modifications.

**Key Takeaways:**
- Multi-modal foundation models (CLIP, BLIP, BLIP-2) are highly vulnerable to adversarial images
- Adversarial perturbations can force models to produce attacker-chosen text outputs
- Current vision encoders lack robustness, making downstream multimodal systems vulnerable

**Code:** Not available

---

### Abusing Images and Sounds for Indirect Instruction Injection in Multi-Modal LLMs
**Authors:** Eugene Bagdasaryan, Tsung-Yin Hsieh, Ben Nassi, Vitaly Shmatikov | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2307.10490
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐⭐

**Summary:** Demonstrates that adversarial images and audio can carry hidden instructions that manipulate multimodal LLMs. The authors show that perturbations invisible to humans can be embedded in images and sounds to inject instructions that override the model's original task. This extends indirect prompt injection to the visual and auditory modalities.

**Key Takeaways:**
- Adversarial perturbations in images and audio can encode hidden instructions for multimodal LLMs
- Extends indirect prompt injection beyond text to visual and auditory channels
- Attacks are imperceptible to humans but reliably control model behavior

**Code:** Not available

---

### FigStep: Jailbreaking Large Vision-Language Models via Typographic Visual Prompts
**Authors:** Yichen Gong, Delong Ran, Jinyuan Liu, Conglei Wang, Tianshuo Cong, Anyu Wang, Sisi Duan, Xiaoyun Wang | **Year:** 2023 | **Venue:** arXiv preprint
**Link:** https://arxiv.org/abs/2311.05608
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces FigStep, a simple yet effective jailbreak technique that converts harmful text instructions into images using typography. By rendering harmful queries as text within images, the attack bypasses text-based safety filters that only inspect the text input. The method is straightforward, requires no optimization, and achieves high success rates against GPT-4V, LLaVA, and other vision-language models.

**Key Takeaways:**
- Simple typographic attack: render harmful text as an image to bypass text-based safety
- No adversarial optimization required, just text-to-image rendering
- Highlights the gap between text-based and vision-based safety filtering in multimodal models

**Code:** https://github.com/ThuCCSLab/FigStep

---

### Image Hijacks: Adversarial Images Can Control Generative Models at Runtime
**Authors:** Luke Bailey, Euan Ong, Stuart Russell, Scott Emmons | **Year:** 2023 | **Venue:** ICML 2024
**Link:** https://arxiv.org/abs/2309.00236
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Introduces the concept of image hijacks, where adversarial images gain control over the text generation of vision-language models at runtime. The authors present a general framework for crafting images that force specific model behaviors, including prompt injection through images, forcing specific text outputs, and diverting conversations to attacker-chosen topics.

**Key Takeaways:**
- Adversarial images can hijack text generation in vision-language models at inference time
- General framework encompasses multiple attack goals: injection, output forcing, and context manipulation
- Demonstrates that image inputs are a powerful and underexplored attack surface for LLMs

**Code:** https://github.com/euanong/image-hijacks

---

### Jailbreak in Pieces: Compositional Adversarial Attacks on Multi-Modal Language Models
**Authors:** Erfan Shayegani, Yue Dong, Nael Abu-Ghazaleh | **Year:** 2024 | **Venue:** ICLR 2024
**Link:** https://arxiv.org/abs/2307.14539
**Relevance:** ⭐⭐⭐⭐⭐ | **Impact:** ⭐⭐⭐⭐

**Summary:** Proposes compositional adversarial attacks that distribute harmful content across text and image modalities so that neither modality alone appears harmful. The model combines the benign-looking text and image components to produce harmful outputs. This exploits the cross-modal reasoning capabilities of vision-language models to circumvent per-modality safety filters.

**Key Takeaways:**
- Harmful intent can be split across modalities, evading unimodal safety filters
- The model's cross-modal reasoning ability is exploited to reassemble harmful content
- Per-modality safety checks are insufficient; cross-modal safety reasoning is required

**Code:** Not available

---

[Back to main page](../../README.md)
