# Documentation workspace

This is a separate Yarn 3.2.1 workspace ([manifest](package.json)), not the commerce root. Read the app/package guide before choosing checks; preserve existing guides.

From `www/`: `yarn prep` runs package preparation and writes generated content; it is not a read-only check. `yarn test` runs workspace tests once. App `lint` and `lint:content`, and docs-ui `lint`, use `--fix`; do not use them for non-mutating verification. The app guides give direct ESLint checks without fixes and type checks without emit. Preparation may be needed before those checks; missing generated files are not a pass.

Do not run deploy, upload (including `upload:r2`), Cloudflare preview or publishing commands on your own initiative. Builds and prep can generate files or invoke subprocesses; inspect their scripts first. No builds, installs or application checks on this docs-only task.
