[README.md](https://github.com/user-attachments/files/31185590/README.md)
# Code-Aware Auditor Credential

An interactive, self-paced training system that teaches traditional IT auditors how to audit modern, code-defined, cloud-native environments — **without requiring them to write any code.**

Most IT audit training still assumes a slow-moving environment where a quarterly screenshot is a reasonable piece of evidence. Modern environments deploy dozens of times a day through Git, CI/CD pipelines, infrastructure-as-code, and policy-as-code — and the auditor's job has to change with it: read the configuration, trace it through the pipeline, and validate it against the logs, rather than trusting a static export or a manager's assurance that "it's fine."

This is a single self-contained HTML file — no build step, no server, no dependencies. Open it in a browser and it runs.

**[Live demo](#)** — *enable GitHub Pages (see below) and drop the link here once it's live.*

## What's inside

- **12 modules**, each following the same disciplined structure: Learning Objectives → Real-World Audit Scenario → Core Concepts → **How to Read & Interpret** (real, annotated JSON / YAML / HCL / Rego / log snippets, with "what an engineer sees" vs. "what an auditor should ask" side by side) → Auditor Validation Lens → Sample Artifacts (a compliant-vs-non-compliant toggle over real code) → a Hands-On interpretation exercise → a decision-based "What Would You Do" audit judgment scenario → Red Flags & False Assurance Risks → Audit Documentation Guidance → an interactive Deliverables Checklist.
- **Topics covered**: reading JSON/YAML/HCL, CI/CD pipelines as control systems, Git & GitHub as audit evidence, Terraform (IaC), policy-as-code (OPA/Sentinel-style), cloud-native audit logs (CloudTrail-style), sampling in automated/system-generated populations, evidence reliability (logs vs. exports vs. screenshots), configuration drift detection, end-to-end control traceability, and audit documentation/reporting.
- **Capstone simulation**: a fictional repository review (`checkout-service`) with real Terraform, pipeline YAML, and cloud-log artifacts that tell one connected story — work through a sampling exercise, draft an audit opinion, and take a scored 10-question certification exam (80% pass threshold).
- **Reference library**: an audit workpaper template, an evidence-reliability scale, and a sampling worksheet template.
- Progress, quiz answers, and checklist state persist locally in the browser (`localStorage`) — no account, no backend, no data collection.
- Light and dark theme support, responsive layout.

## Running it

Just open `index.html` in any modern browser — double-click it, or:

```bash
open index.html      # macOS
start index.html      # Windows
```

No installation, no dependencies, nothing to build.

### Hosting it live (GitHub Pages)

Since the file is already named `index.html`, GitHub Pages will serve it directly with no configuration beyond turning it on:

1. On the repo page, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Pick the `main` branch and the `/ (root)` folder, then **Save**.
4. GitHub will publish it at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Status & disclaimer

This was built as a training/portfolio artifact. The technical examples (IAM policy JSON, Terraform/HCL, Rego policy-as-code, CloudTrail-style log fields) and framework references are accurate to the best of current knowledge, but this has **not** been reviewed by a security engineer or audit professional and should be treated as a strong draft rather than certified training material.

## License

MIT — see [LICENSE](LICENSE).
