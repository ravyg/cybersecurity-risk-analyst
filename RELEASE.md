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

## 3. (Optional) Mint a Zenodo DOI  — **TBD**

> Marked TBD — a DOI (Hugging Face or Zenodo) will be supplied separately and pasted in afterward.

1. Sign in to <https://zenodo.org> with GitHub.
2. Go to **Settings → GitHub**, find `ravyg/cybersecurity-risk-analyst`, and flip the toggle **ON**.
3. Cut a **new** GitHub Release *after* enabling the toggle (Zenodo only archives releases created while the toggle is on — re-cut if needed).
4. Zenodo archives the release and issues a DOI (a version DOI plus a concept DOI that always points to the latest).

## 4. Add the DOI back to the repo — **TBD**

Once the DOI is minted, update these three places (all currently marked `TBD`):

- **README.md → "DOI" section:** replace `TBD — DOI to be added` with the DOI, and uncomment the badge line, filling in the DOI.
- **CITATION.cff:** uncomment and fill the top-level `doi:` field (model artifact) and/or the `preferred-citation.doi:` field (paper).
- **RELEASE.md:** mark this checklist's DOI steps done.

```bash
git add README.md CITATION.cff RELEASE.md
git commit -m "docs: add DOI"
git push
```
