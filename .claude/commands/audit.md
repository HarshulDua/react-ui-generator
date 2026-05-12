Run a full project audit: check dependencies, run all tests, and write results to logs.txt.

## Steps

1. **Dependency audit** — run `npm audit` to report known vulnerabilities across all installed packages.

2. **Outdated packages** — run `npm outdated` to list packages that have newer versions available.

3. **Run all tests** — run `npx vitest run` to execute the full test suite and capture results.

4. **Write logs.txt** — create or overwrite `logs.txt` in the project root with the combined output from all three steps above, structured as:

```
=== DEPENDENCY AUDIT ===
<npm audit output>

=== OUTDATED PACKAGES ===
<npm outdated output>

=== TEST RESULTS ===
<vitest run output>
```

Use the Bash tool to run each command, capture stdout and stderr, then write everything to `logs.txt` using the Write tool. Print a short summary to the user after: how many vulnerabilities, how many outdated packages, and whether tests passed or failed.
