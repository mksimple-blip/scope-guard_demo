# Drift Taxonomy

ScopeGuard detects concrete, measurable forms of drift in AI‑generated code.  
These drift types are deterministic and model‑agnostic.

## 1. Scope Expansion
Changes made outside the requested function, class, or module.

## 2. Structural Drift
New helpers, branches, or expanded logic that increase structural complexity.

## 3. Propagation Drift
Changes spreading across multiple functions or files from a single prompt.

## 4. Signature Drift
Parameter, return type, or method signature changes that alter API behavior.

## 5. Dependency Drift
New imports, new dependencies, or changes to dependency structure.

These drift types form the foundation of ScopeGuard’s decision engine.
