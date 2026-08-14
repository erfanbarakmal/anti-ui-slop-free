# RTL and Persian UI Rules

## Direction
- Use `dir="rtl"` at an appropriate container or document boundary for Persian-first interfaces.
- Keep code, URLs, file paths, email addresses, numbers with units, and mixed technical tokens readable with appropriate bidi handling.
- Do not mirror icons whose meaning is not directional.
- Mirror directional navigation icons only when the interaction meaning changes with direction.

## Layout
- Place primary reading flow and text alignment according to RTL expectations.
- Do not mechanically reverse every visual relationship.
- Preserve logical grouping and platform conventions.
- Test mixed Persian and English labels, numbers, dates, and technical strings.

## Persian Text
- Never use U+200C ZERO WIDTH NON-JOINER.
- Use U+0020 SPACE instead.
- Before final output, scan generated text files for U+200C and replace it with U+0020.

Suggested validation command:

```bash
python - <<'PY'
from pathlib import Path
root = Path('.')
for p in root.rglob('*'):
    if p.is_file():
        try:
            s = p.read_text(encoding='utf-8')
        except Exception:
            continue
        if '\u200c' in s:
            print(p)
PY
```
