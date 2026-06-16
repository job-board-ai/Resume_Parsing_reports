# Resume Parse Quality Reports

Human-readable side-by-side reports: raw extracted text vs structured parse output.

Each report shows every resume in the corpus with:
- **Left panel** — raw text the parser extracted from the PDF/DOCX
- **Right panel** — full parsed output: name, every experience with bullet points,
  all skills as chips, education, contact links

Generated automatically by CI on every change to `services/ai/`.

## Reports

| Date | Link |
|------|------|
| [2026-06-16](./2026-06-16.html) | [View report](./2026-06-16.html) |

## How to read

- ✅ **PASS** — all invariants satisfied (non-empty title, company, no homoglyph chars)
- 🟡 **XFAIL** — expected weakness; tier-1 alone can't parse this resume cleanly
  (LLM fallback handles it in production)
- ❌ **FAIL** — regression detected; an invariant that previously held is now broken
- ⚠️ **ERROR** — parse threw an unexpected exception

## Regenerate locally

```bash
# from services/ai/
venv/bin/python tests/golden/generate_report.py
```
