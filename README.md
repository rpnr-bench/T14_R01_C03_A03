# Local Web Baseline Scan

A local web security review project using OWASP ZAP baseline scanning against a demo application and sample report fixtures.

## Project layout

- `app.py` — Minimal local demo application.
- `zap/` — Baseline scan configuration.
- `sample_data/` — Sample ZAP baseline JSON.
- `reports/` — Generated scan summaries.
- `scripts/` — Baseline scan and report conversion helpers.

## Quick start

```bash
make validate
```
```bash
python3 scripts/zap_json_to_markdown.py
```

## Baseline review workflow

1. Run or inspect the local demo application.
2. Review ZAP policy files before changing alert handling.
3. Convert JSON outputs into Markdown summaries for review.
4. Keep endpoint scope documentation current.

The scan helper is scoped to local demo targets.

## Maintenance notes

The ZAP runner only allows localhost, 127.0.0.1, or host.docker.internal targets.

## Contributing

Keep changes focused, update documentation when behavior changes, and run the validation commands before submitting a pull request.
