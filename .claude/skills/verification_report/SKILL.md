---
name: verification_report
description: >-
  Verify a focused bugfix against the issue, repository rules, and the smallest relevant execution checks.
---

# Verification report

Use this skill for issue-driven fixes, especially the `continued_fraction` regression.

1. Read the issue description, the implementation file, and any direct tests or doctests that cover the bug.
2. Confirm the fix addresses the root cause and remains narrow in scope.
3. Run only the smallest relevant verification commands needed to confirm behavior.
4. Record actual command names, exit status, and observed output.
5. Check that the patch follows the repository contribution standards in `contributing_guidelines`.
6. Report whether the fix passes, fails, or is blocked.

## Typical checks for this task

- `python3 -m doctest -v maths/continued_fraction.py`
- a focused pytest invocation covering the regression
- a direct reproduction script for the exact examples from the issue
- `python3 -m ruff check maths/continued_fraction.py` when applicable

## Output format

- Scope inspected
- Root cause and fix summary
- Commands run
- Actual results
- Repository rule compliance check
- Failures or blockers
- Final status
