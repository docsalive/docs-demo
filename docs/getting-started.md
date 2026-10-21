# Getting started

These examples need Python 3.10 or newer and nothing else.

## Check your Python version

```bash
python3 -c "import sys; assert sys.version_info >= (3, 10), sys.version; print('ok')"
```

## Write and read a file

```python
from pathlib import Path

notes = Path("notes.txt")
notes.write_text("first line\nsecond line\n", encoding="utf-8")
lines = notes.read_text(encoding="utf-8").splitlines()
assert lines == ["first line", "second line"]
print(len(lines), "lines")
```

## Count words from the shell

```bash
printf 'docs\nalive\ndocs\n' > words.txt
sort words.txt | uniq -c | sort -rn | head -n 1
```

## Format a table

```pycon
>>> rows = [("alpha", 3), ("beta", 12)]
>>> for name, count in rows:
...     print(f"{name:<6}{count:>4}")
alpha    3
beta    12
```
