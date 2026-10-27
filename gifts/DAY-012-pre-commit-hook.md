# A five-line pre-commit hook for agent commits

An agent will commit code that does not type-check unless something stops it. A pre-commit hook runs before every commit, from you or from an agent, and refuses the commit when a check fails. Five lines are enough.

## The five lines

These are the lines from the first night, for a TypeScript project that uses Husky. Save them as `.husky/pre-commit`:

```sh
# TypeScript check (fails fast if types are broken)
npx tsc --noEmit

# Lint-staged (runs ESLint on staged files)
npx lint-staged
```

Husky 9 runs this file with `sh -e`, so the first command that fails stops the commit. Use `bunx` or `pnpm exec` in place of `npx` if that is your package manager.

## Set it up

1. Add the tools: `husky` and `lint-staged` as dev dependencies.
2. Add `"prepare": "husky"` to the `scripts` in `package.json`, then run your install once so the hooks folder is wired.
3. Tell lint-staged what to run on staged files, in `package.json`:

```json
"lint-staged": {
  "*.{ts,tsx}": ["eslint --fix"],
  "*.{js,jsx,json,md}": ["prettier --write"]
}
```

4. Save the five lines as `.husky/pre-commit`.

## Without Husky

A plain git hook works too. If the `.git/hooks` folder is missing, make it with `mkdir -p .git/hooks`. Then save this as `.git/hooks/pre-commit` and make it executable with `chmod +x .git/hooks/pre-commit`:

```sh
#!/bin/sh
set -e
# Type check (fails fast if types are broken)
npx tsc --noEmit
# Lint (replace with your own linter)
npx eslint .
```

Keep the `set -e` line. Without it the script's result is its last command, so a failed type check above a passing lint still lets the commit through.

## Check that it can say no

A hook you have never seen fail is a hook you have not tested.

1. Add a file with a type error, for example `const n: number = "oops"; export {n};`
2. Stage it and try to commit. The commit should be refused with the type error printed.
3. Delete the file and commit again. It should go through.

If your git has a shared hooks folder for every repo, git ignores `.git/hooks`. Run `git config --global --get core.hooksPath` to see. If it prints a folder, the hooks in that folder run for every repo you have, so do not overwrite what is there. Run the plain hook yourself before you commit, with `sh .git/hooks/pre-commit`, or call it from the shared hook.

## What it caught the first time

The commit that added these five lines first fixed the more than 20 TypeScript errors that had piled up without one, so the hook started from zero.
