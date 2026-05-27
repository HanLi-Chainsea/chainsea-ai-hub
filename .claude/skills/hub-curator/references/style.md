# Style & Rubric

## Language & Tone

- Traditional Chinese by default.
- Keep English terms such as `MCP`, `agent`, `workflow`, `coverage`, `mutation testing`, `CI`, `PRD` when they are clearer.
- Avoid over-translating tool names and framework names.
- Practical. Specific. Calm about risks. No hype.

## Good Entry Shape

1. Why it is listed.
2. Where it belongs.
3. What ChainSea could use it for.
4. When not to use it.
5. What risks or adoption blockers exist.
6. What was verified.
7. What the next check should be.

Do not rewrite the original project's README. Keep only the minimum context needed for indexing, adoption judgment, and future maintenance.

## Status

- `Experimental`：看起來有價值，但尚未在內部情境驗證。
- `Useful`：已確認能解決具體問題，可在特定情境使用。
- `Production-used`：已在實際專案或流程中使用。
- `Deprecated`：不再建議使用，但保留歷史脈絡。

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

## Time-Aware Notes

For development experience notes, do not erase old context just because later information changed. Add a `Later Updates` section and preserve the original date.

This lets the hub show natural iteration instead of pretending every note was written with perfect hindsight.