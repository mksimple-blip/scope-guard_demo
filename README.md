![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-prototype-blue)
![Version](https://img.shields.io/badge/version-v0.1.0-orange)

# ScopeGuard Demo

AI writes code. ScopeGuard keeps it aligned.

Code review evaluates the code. ScopeGuard evaluates whether the code stayed within the requested scope.

---

## 🚀 Thesis

Human review doesn’t scale at the same rate as AI‑generated code.  
ScopeGuard identifies unexpected transformations *before* they reach your repository.

---

## ⭐ Origin Story

AI coding assistants can restructure files, introduce helpers, expand logic, or modify business rules from a single prompt.

These transformations are powerful — but they also create a new challenge: verifying that the AI stayed aligned with the developer’s intent.

Across tools and community reports, a consistent pattern emerged:

- small prompts triggering broad refactors  
- new helper functions appearing without request  
- unrelated modules being modified  
- schema‑level changes generated from ambiguous instructions  
- logic that satisfies the prompt but alters behavior elsewhere  

The code often met the request while introducing additional changes the developer never intended.

That’s when ScopeGuard became clear:

**We need a governance layer — an automated reviewer focused on intent alignment.**

Not a coding assistant.  
Not a static analyzer.  
A companion layer built for AI‑generated code.

---

## ⭐ Example Output From the Prototype

### Prompt:
“Improve error handling in JSON encoder.”

**Result:**  
✓ ALLOW  
**Severity:** None  
No drift detected.

---

### Prompt:
“Refactor the entire header resolution pipeline.”

**Result:**  
⚠ REVIEW REQUIRED  
**Severity:** High  

Detected:

- new helper function  
- structural expansion  
- propagation across multiple functions  

Approval recommended.

*(Only real prototype outputs are shown.)*

---

## ⭐ What ScopeGuard Detects

ScopeGuard focuses on concrete, measurable drift types:

- **Scope Expansion** — changes outside the requested area  
- **Structural Drift** — new helpers, branches, or expanded logic  
- **Propagation Drift** — changes spreading across files or modules  
- **Signature Drift** — parameter or return‑type changes  
- **Dependency Drift** — new imports or dependency changes  

These drift types already work in the prototype.

---

## ⭐ Severity Model

| Severity | Decision          | Meaning                          |
|---------|--------------------|----------------------------------|
| None    | Allow             | No drift detected                |
| Low     | Allow             | Minor non‑functional drift       |
| Medium  | Warning           | Limited unexpected changes       |
| High    | Approval Required | Significant drift detected       |
| Critical| Block             | Unsafe or destructive drift      |

---

## ⭐ How It Works

1. Developer writes a prompt in any AI coding tool  
2. The AI generates code  
3. ScopeGuard analyzes the diff  
4. Drift Engine evaluates:  
   - scope expansion  
   - structural drift  
   - propagation drift  
   - signature drift  
   - dependency drift  
5. Severity Engine scores the risk  
6. Enforcement Engine returns:  
   - Allow  
   - Warning  
   - Approval Required  
   - Block  

Simple for the developer.  
Deterministic under the hood.

---

## ⭐ Why Existing Tools Aren’t Enough

Existing tools focus on correctness, quality, and security.  
They generally do **not** evaluate whether an AI‑generated change stayed aligned with the original request.

ScopeGuard fills that gap by analyzing **intent‑to‑change alignment**, a dimension traditional tools don’t cover.

---

## ⭐ Why Now

AI coding assistants are becoming standard developer tools.  
The more code they generate, the more important it becomes to verify that changes stay aligned with intent.

---

## ⭐ What ScopeGuard Is Not

- Not a replacement for code review  
- Not a static analyzer  
- Not a linter  
- Not a coding assistant  
- Not tied to any specific model  

ScopeGuard verifies whether AI‑generated changes stayed within the intended scope.

---

## ⭐ Current Status

### Prototype Capabilities
✓ Scope expansion detection  
✓ Structural drift detection  
✓ Propagation drift detection  
✓ Signature drift detection  
✓ Dependency drift detection  
✓ Severity scoring  
✓ Explainable decisions  

### In Development
• Semantic drift analysis  
• Multi‑file governance  
• IDE integrations  
• Model‑agnostic diff adapters  

---

## ⭐ Who It’s For

- Engineers using any AI coding assistant  
- Teams adopting AI‑assisted development  
- CTOs who need safety + auditability  
- Companies with compliance or governance requirements  
- Anyone who wants to prevent AI‑generated regressions  

---

## ⭐ Maker’s Comment

Hey everyone — I’m Mani 👋

I built ScopeGuard after repeatedly seeing AI assistants modify logic I never asked them to touch.

From helper functions appearing out of nowhere to multi‑file propagation from a one‑line prompt — the patterns were too consistent to ignore.

ScopeGuard isn’t another AI coding assistant.  
It’s a reviewer for AI‑generated code — focused on whether the change stayed within the intended scope.

I’d love your feedback, ideas, and thoughts on where this should go next.

Thank you for checking it out ❤️

---

## ⭐ Call to Action

- Try the demo  
- Join the early access list  
- Share your drift examples  
- Tell me how your team uses AI for coding  

