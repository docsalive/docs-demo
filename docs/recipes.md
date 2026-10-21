# Recipes

Small, self-contained data tasks using the Python standard library.

## Summary statistics

```pycon
>>> import statistics
>>> data = [2, 4, 4, 4, 5, 5, 7, 9]
>>> statistics.mean(data)
5
>>> statistics.median(data)
4.5
>>> statistics.pstdev(data)
2.0
```

## Parse CSV text

```python
import csv
import io

text = "name,qty\napples,3\npears,5\n"
rows = list(csv.DictReader(io.StringIO(text)))
total = sum(int(r["qty"]) for r in rows)
assert total == 8
print("total:", total)
```

## Check whether a value is a mapping

> **Deliberately out of date.** This example uses an import that was removed in Python 3.10.
> It's kept on purpose so the DocsAlive check has a real problem to report. The current import is
> `from collections.abc import Mapping`.

```python
from collections import Mapping

print(isinstance({"a": 1}, Mapping))
```

## Dates

```pycon
>>> from datetime import date
>>> (date(2026, 12, 25) - date(2026, 12, 1)).days
24
>>> date(2026, 10, 20).isoformat()
'2026-10-20'
```
