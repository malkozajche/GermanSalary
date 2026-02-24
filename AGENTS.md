# AGENTS.md

## Cursor Cloud specific instructions

This is a zero-dependency static HTML/CSS/JS project (German Salary Calculator). There is no build step, no package manager, no linter, and no automated test suite.

### Running the application

Serve the files with any static HTTP server. The simplest approach:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html` in a browser. See `README.md` for details.

### Key files

- `index.html` — main calculator (all HTML, CSS, and JS are inline)
- `bg-salary-calculator.html` — Bulgarian landing page linking to an external hosted version

### Testing

There are no automated tests. Manual testing is done by opening the calculator in a browser, changing inputs (gross salary, tax class, state, etc.), and verifying the live-updating results panel computes plausible values.
