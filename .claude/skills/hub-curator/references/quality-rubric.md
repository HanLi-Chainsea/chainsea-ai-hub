# Quality Rubric

Use this rubric to decide whether a resource belongs in the main hub, watchlist, or nowhere for now.

## Fit

- Does it solve a recurring ChainSea engineering problem?
- Does it improve AI-assisted engineering, QA, documentation, automation, or integration?
- Can more than one project or engineer reuse it?
- Does it have a clear owner, maintainer, or community?

## Maturity

- `Experimental`: interesting, incomplete, or not yet verified internally.
- `Useful`: works for a clear use case, but may still need manual review or setup.
- `Production-used`: used in a real project or workflow.
- `Deprecated`: no longer recommended; keep only for historical context.

## Integration Difficulty

- `Low`: can be tried with minimal setup and low risk.
- `Medium`: needs configuration, credentials, or project-specific adaptation.
- `High`: changes architecture, permissions, CI/CD, data flows, or team process.

## Recommended Priority

- `High`: likely to save meaningful engineering time soon.
- `Medium`: useful but needs more evaluation.
- `Low`: worth noting but not ready for promotion.

## Risks To Check

- Security and permission scope.
- Data sensitivity and external service exposure.
- License compatibility.
- Maintenance activity.
- Documentation quality.
- Setup complexity.
- Lock-in or dependency risk.
- Whether generated output still requires human review.

## Decision

- Add to main hub when fit is clear and risk is manageable.
- Add to watchlist when value is plausible but not verified.
- Reject when the use case is unclear, the project is abandoned, or risk is too high for the expected benefit.
