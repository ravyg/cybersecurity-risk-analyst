# Hugging Face model card — "How to cite" section

Paste the block below into the HF model card at
https://huggingface.co/saki007ster/CybersecurityRiskAnalyst (Edit → README.md).

Two parts:
1. **YAML frontmatter** — add these keys to the top of the model card (between the
   `---` fences) so HF renders proper metadata and links the base model.
2. **Markdown body** — the "How to cite" section for the card body.

---

## 1) YAML frontmatter (top of the HF README, inside `---` fences)

```yaml
license: llama3.1
base_model: meta-llama/Llama-3.1-8B
library_name: transformers
pipeline_tag: text-generation
tags:
  - cybersecurity
  - risk-analysis
  - nist-csf
  - mitre-attack
  - gguf
  - ollama
```

---

## 2) "How to cite" section (paste into the card body)

```markdown
## 📄 How to cite

This model accompanies a research paper. **If you use this model in academic or
professional work, please cite the paper** — that is the primary scholarly reference.

### Cite the paper (preferred)

> Gupta, R., Kumar, S., Sharma, S., Dang, M., & Aggarwal, A. (2026).
> *An Agentic Multi-Agent Architecture for Cybersecurity Risk Management.*
> arXiv preprint arXiv:2603.20131. https://arxiv.org/abs/2603.20131

**BibTeX**

​```bibtex
@article{gupta2026agentic,
  title   = {An Agentic Multi-Agent Architecture for Cybersecurity Risk Management},
  author  = {Gupta, Ravish and Kumar, Saket and Sharma, Shreeya and Dang, Maulik and Aggarwal, Abhishek},
  journal = {arXiv preprint arXiv:2603.20131},
  year    = {2026}
}
​```

### Cite the model artifact (for reproducibility / data-availability statements)

The model was built by **Saket Kumar and Ravish Gupta**. Model DOI: `10.57967/hf/9777`.

​```bibtex
@misc{kumar2026cybersecurityriskanalyst,
  author    = {Saket Kumar and Ravish Gupta},
  title     = {CybersecurityRiskAnalyst (Revision 1842e1c)},
  year      = {2026},
  url       = {https://huggingface.co/saki007ster/CybersecurityRiskAnalyst},
  doi       = {10.57967/hf/9777},
  publisher = {Hugging Face}
}
​```

More citation formats (APA, MLA, Chicago, Harvard, Vancouver) and a `CITATION.cff`:
https://github.com/ravyg/cybersecurity-risk-analyst

⭐ Find this model useful? Star the repo and cite the paper.
```

> Note: in the block above the fenced BibTeX code blocks use a zero-width character
> (`​`) before the backticks only so this file can nest them. When you paste into
> the HF card, replace those with normal triple backticks ```` ``` ````.
