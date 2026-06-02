# Architecture Overview

ScopeGuard evaluates AI-generated diffs using a deterministic, rule-based engine.

## 1. Intent Layer
Captures the developer’s request (prompt) and establishes the expected scope.

## 2. Diff Layer
Parses the AI-generated diff and extracts structural events.

## 3. Drift Engine
Classifies drift into:
- scope expansion
- structural drift
- propagation drift
- signature drift
- dependency drift

## 4. Severity Engine
Scores drift using the severity model.

## 5. Enforcement Engine
Produces one of four decisions:
- Allow
- Warning
- Approval Required
- Block

The system is model-agnostic and works with any AI coding tool.
