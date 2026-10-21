# DocsAlive docs demo

This repository is a small, public demo of [DocsAlive](https://docsalive.com). DocsAlive runs the code
examples in a project's documentation and reports the ones that no longer work.

Every push to this repository triggers a **DocsAlive docs** check. Open the latest commit and select
**Checks** to see the result, with notes on the exact lines that need attention.

The pages in [`docs/`](docs/) contain short, working Python and shell examples that use only the Python
standard library. One example in [`docs/recipes.md`](docs/recipes.md) is **deliberately out of date** so
that the check has a real problem to report. It is clearly marked, and it's kept as is on purpose.

## Quick example

```pycon
>>> import json
>>> json.dumps({"status": "alive"}, sort_keys=True)
'{"status": "alive"}'
```

## Pages

- [Getting started](docs/getting-started.md): Python and shell basics.
- [Recipes](docs/recipes.md): small data tasks, including the planted out-of-date example.

## About

DocsAlive is a product of MRSLM Group LLC. Questions: hello@docsalive.com.
The examples in this repository are released under the [MIT License](LICENSE).
