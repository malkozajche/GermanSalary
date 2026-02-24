## Cursor Cloud specific instructions

This is a purely static HTML/CSS/JS project (German Salary Calculator) with **no dependencies, no build system, no package manager, no linter, and no automated tests**.

### Running the app

Serve files locally with Python's built-in HTTP server (see `README.md`):

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html` in Chrome.

There is also a secondary page at `bg-salary-calculator.html` (Bulgarian landing page).

### Key caveats

- There is no `package.json`, no npm/pnpm/yarn, and no Node.js tooling.
- There are no lint, test, or build commands — all logic is inline in the HTML files.
- The only CI is `.github/workflows/greetings.yml` (a first-time contributor greeting; not relevant for development).
- All JavaScript and CSS is inlined in the HTML files; there are no separate `.js` or `.css` files to edit.
