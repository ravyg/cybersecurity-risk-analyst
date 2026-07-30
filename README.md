# CybersecurityRiskAnalyst

> ⭐ **Find this useful? Clone it, [star the repo](https://github.com/ravyg/cybersecurity-risk-analyst), and cite the paper.** If you use this model in academic or professional work, please cite [arXiv:2603.20131](https://arxiv.org/abs/2603.20131) (see [How to cite](#how-to-cite)). Model DOI: [`10.57967/hf/9777`](https://doi.org/10.57967/hf/9777).

**CybersecurityRiskAnalyst** is a custom fine-tuned Large Language Model (LLM) designed to act as a senior cybersecurity risk assessor and strategist. It is published on Ollama and has **1,400+ downloads**. This repository makes the model formally citable and links it to the research paper it accompanies.

- **Model:** [`saki007ster/CybersecurityRiskAnalyst`](https://ollama.com/saki007ster/CybersecurityRiskAnalyst) on Ollama
- **Base model:** Llama 3.1 8B (`llama` architecture, 8.03B parameters)
- **Quantization:** Q4_0 · **Size:** 4.7 GB · **Context window:** 128K
- **Tags:** text, cybersecurity, risk assessment

### What it does

- **Risk Posture Evaluation** — assesses an organization's overall security posture
- **Framework Mapping** — NIST CSF, CIS Controls, MITRE ATT&CK, ISO/IEC 27001
- **Threat Intelligence Awareness**
- **Gap Analysis**
- **Prioritized Recommendations**
- **Human-Centric Reports** — clear, decision-ready output
- **Explainability** — reasoning you can follow and audit

---

## DOI

[![DOI](https://img.shields.io/badge/DOI-10.57967%2Fhf%2F9777-blue)](https://doi.org/10.57967/hf/9777)

**Model DOI (Hugging Face):** [`10.57967/hf/9777`](https://doi.org/10.57967/hf/9777)

---

## Install & Use

Requires [Ollama](https://ollama.com/download).

```bash
# Pull the model
ollama pull saki007ster/CybersecurityRiskAnalyst

# Or pull-and-run in one step
ollama run saki007ster/CybersecurityRiskAnalyst
```

### Minimal usage example

```bash
ollama run saki007ster/CybersecurityRiskAnalyst \
  "We run a 200-person fintech on AWS with no formal incident response plan. \
   Assess our top cyber risks and map them to NIST CSF."
```

Or via the Ollama HTTP API:

```bash
curl http://localhost:11434/api/generate -d '{
  "model": "saki007ster/CybersecurityRiskAnalyst",
  "prompt": "Perform a NIST CSF gap analysis for a small healthcare provider storing PHI in a single on-prem server.",
  "stream": false
}'
```

Python:

```python
import ollama

response = ollama.chat(
    model="saki007ster/CybersecurityRiskAnalyst",
    messages=[{
        "role": "user",
        "content": "Prioritize remediation for an org with exposed RDP, no MFA, and unpatched VPN.",
    }],
)
print(response["message"]["content"])
```

---

## How to cite

This model accompanies the paper below — **if you use the model in academic or professional work, please cite the paper.**

> Gupta, Ravish; Kumar, Saket; Sharma, Shreeya; Dang, Maulik; and Aggarwal, Abhishek (2026).
> *An Agentic Multi-Agent Architecture for Cybersecurity Risk Management.* arXiv preprint arXiv:2603.20131.

<details open>
<summary><b>APA</b></summary>

```
Gupta, R., Kumar, S., Sharma, S., Dang, M., & Aggarwal, A. (2026). An Agentic Multi-Agent Architecture for Cybersecurity Risk Management. arXiv preprint arXiv:2603.20131.
```
</details>

<details>
<summary><b>MLA</b></summary>

```
Gupta, Ravish, et al. "An Agentic Multi-Agent Architecture for Cybersecurity Risk Management." arXiv preprint arXiv:2603.20131 (2026).
```
</details>

<details>
<summary><b>Chicago</b></summary>

```
Gupta, Ravish, Saket Kumar, Shreeya Sharma, Maulik Dang, and Abhishek Aggarwal. "An Agentic Multi-Agent Architecture for Cybersecurity Risk Management." arXiv preprint arXiv:2603.20131 (2026).
```
</details>

<details>
<summary><b>Harvard</b></summary>

```
Gupta, R., Kumar, S., Sharma, S., Dang, M. and Aggarwal, A., 2026. An Agentic Multi-Agent Architecture for Cybersecurity Risk Management. arXiv preprint arXiv:2603.20131.
```
</details>

<details>
<summary><b>Vancouver</b></summary>

```
Gupta R, Kumar S, Sharma S, Dang M, Aggarwal A. An Agentic Multi-Agent Architecture for Cybersecurity Risk Management. arXiv preprint arXiv:2603.20131. 2026.
```
</details>

<details>
<summary><b>BibTeX</b></summary>

```bibtex
@article{gupta2026agentic,
  title   = {An Agentic Multi-Agent Architecture for Cybersecurity Risk Management},
  author  = {Gupta, Ravish and Kumar, Saket and Sharma, Shreeya and Dang, Maulik and Aggarwal, Abhishek},
  journal = {arXiv preprint arXiv:2603.20131},
  year    = {2026}
}
```
</details>

A machine-readable [`CITATION.cff`](CITATION.cff) is also provided — GitHub will render a "Cite this repository" button from it.

---

## Authors & attribution

This model and the accompanying paper are the work of:

- **Ravish Gupta**
- **Saket Kumar** — *model author / maintainer* ([`saki007ster` on Ollama](https://ollama.com/saki007ster))
- **Shreeya Sharma**
- **Maulik Dang**
- **Abhishek Aggarwal**

---

## License

This model is a fine-tuned derivative of **Meta Llama 3.1 8B** and is therefore governed by the **[Llama 3.1 Community License Agreement](LICENSE)** (Version Release Date: July 23, 2024).

- Built with Llama. Use is subject to Meta's [Acceptable Use Policy](https://www.llama.com/llama3_1/use-policy/).
- The base-model license terms are inherited by this derivative; see [LICENSE](LICENSE) for the full text.

---

## Related

- 📄 **Paper:** [An Agentic Multi-Agent Architecture for Cybersecurity Risk Management](https://arxiv.org/abs/2603.20131) (arXiv:2603.20131)
- 🤖 **Model (Ollama):** [saki007ster/CybersecurityRiskAnalyst](https://ollama.com/saki007ster/CybersecurityRiskAnalyst)
- 🤗 **Model (Hugging Face):** [saki007ster/CybersecurityRiskAnalyst](https://huggingface.co/saki007ster/CybersecurityRiskAnalyst) · DOI [`10.57967/hf/9777`](https://doi.org/10.57967/hf/9777)
- 🛠 **Modelfile:** [Modelfile](Modelfile) in this repo
