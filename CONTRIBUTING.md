# Contributing to ML Security & AI Red-Teaming Papers

Thank you for your interest in contributing to this curated reading list! Here is how you can help.

---

## Adding a New Paper

### Format Template

When adding a paper, please use the following format:

```markdown
### Paper Title
**Authors:** [Author 1, Author 2, ...] | **Year:** [YYYY] | **Venue:** [Conference/Journal/arXiv]
**Link:** [URL to paper]
**Relevance:** [1-5 stars using emoji] | **Impact:** [1-5 stars using emoji]

**Summary:** [2-3 sentence summary of the paper's contributions and findings]

**Key Takeaways:**
- [Key point 1]
- [Key point 2]
- [Key point 3]

**Code:** [Link to code repository, or "Not available"]

---
```

### Star Rating Guide

**Relevance** (how central to ML security / red-teaming):
- 1 star: Tangentially related
- 2 stars: Somewhat relevant
- 3 stars: Relevant
- 4 stars: Highly relevant
- 5 stars: Core paper in the area

**Impact** (influence on the field):
- 1 star: Early-stage or niche work
- 2 stars: Moderate interest
- 3 stars: Well-cited, solid contribution
- 4 stars: Highly cited, influential
- 5 stars: Foundational or landmark paper

---

## Review Criteria

Before submitting a paper, please verify:

1. **The paper is real.** It must be a published or preprinted paper with verifiable authors and a link.
2. **It fits a category.** The paper should belong to one of the existing categories, or you may propose a new category.
3. **The summary is accurate.** Summaries should faithfully represent the paper's contributions.
4. **No duplicates.** Check that the paper is not already listed in the repository.
5. **Correct metadata.** Verify authors, year, and venue are accurate.

---

## How to Submit via Pull Request

1. **Fork** this repository.
2. **Create a branch** with a descriptive name:
   ```bash
   git checkout -b add-paper-your-paper-name
   ```
3. **Add the paper** to the appropriate category file in `papers/<category>/README.md`.
4. **Update the root README** if the paper count changes.
5. **Commit** with a clear message:
   ```bash
   git commit -m "Add: Paper Title by Authors (Year)"
   ```
6. **Open a Pull Request** with:
   - The paper title in the PR title
   - A brief note on why this paper is relevant

---

## Proposing a New Category

If you believe a new category is needed:

1. Open an **Issue** describing the proposed category.
2. Include at least 4 papers that would belong to it.
3. Explain why existing categories do not cover them.

---

## Other Contributions

- **Improving summaries:** If you have read a paper and can improve its summary or key takeaways, PRs are welcome.
- **Fixing errors:** If you spot incorrect metadata (wrong authors, year, venue), please submit a fix.
- **Adding code links:** If a paper has released code that is not yet linked, feel free to add it.

---

## Code of Conduct

Be respectful, constructive, and academic in all interactions. This is a research-focused resource.

Thank you for helping build this reading list!
