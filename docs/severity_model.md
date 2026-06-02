# Severity Model

ScopeGuard assigns a severity score based on the type and magnitude of drift.

| Severity | Decision           | Meaning                               |
|----------|--------------------|----------------------------------------|
| None     | Allow              | No drift detected                      |
| Low      | Allow              | Minor non-functional drift             |
| Medium   | Warning            | Limited unexpected changes             |
| High     | Approval Required  | Significant drift detected             |
| Critical | Block              | Unsafe or destructive drift            |

Severity is computed deterministically from drift events.
