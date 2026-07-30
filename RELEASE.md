# Release checklist

Steps to tag a release, publish it on GitHub, and (optionally) mint a citable DOI.

## 1. Tag v1.0.0

```bash
git tag -a v1.0.0 -m "CybersecurityRiskAnalyst v1.0.0 — initial citable release"
git push origin v1.0.0
```

## 2. Create a GitHub Release

```bash
gh release create v1.0.0 \
  --title "CybersecurityRiskAnalyst v1.0.0" \
  --notes "Initial public, citable release of the CybersecurityRiskAnalyst Ollama model. Accompanies arXiv:2603.20131."
```

(Or create it in the GitHub web UI: **Releases → Draft a new release → choose tag `v1.0.0`**.)

## 3. DOI  — ✅ minted (Hugging Face)

The model already has a Hugging Face DOI: **[`10.57967/hf/9777`](https://doi.org/10.57967/hf/9777)**.
It is wired into `README.md` (badge + DOI section) and `CITATION.cff` (top-level `doi:`).

> Optional: you may *also* mint a Zenodo DOI to archive this GitHub repo snapshot itself
> (distinct from the HF model DOI). Steps below — otherwise skip.

1. Sign in to <https://zenodo.org> with GitHub.
2. Go to **Settings → GitHub**, find `ravyg/cybersecurity-risk-analyst`, and flip the toggle **ON**.
3. Cut a **new** GitHub Release *after* enabling the toggle (Zenodo only archives releases created while the toggle is on — re-cut if needed).
4. Zenodo archives the release and issues a DOI (a version DOI plus a concept DOI that always points to the latest).

## 4. Remaining DOI TODO — arXiv DOI for the paper

The **model DOI** is set. The one field still `TBD` is the **paper's** DOI inside
`CITATION.cff` → `preferred-citation.doi`. arXiv assigns `10.48550/arXiv.2603.20131`
once the paper is live — uncomment and fill that line then:

```bash
# in CITATION.cff, under preferred-citation:
#   doi: "10.48550/arXiv.2603.20131"
git add CITATION.cff
git commit -m "docs: add arXiv paper DOI"
git push
```
