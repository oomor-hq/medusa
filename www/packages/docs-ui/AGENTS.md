# docs-ui

Shared documentation components, layouts, providers and hooks used across www apps; keep shared rendering here. [Exports](package.json) support CJS and ESM plus component subpaths: preserve both when changing public components. Utilities shared outside React belong in docs-utils.

From `www/packages/docs-ui/`: `yarn test --run` runs Vitest once; `yarn exec eslint src` checks without fixing. `yarn exec tsc --project tsconfig.cjs.json --noEmit --incremental false` and the same command with `tsconfig.esm.json` check both type targets without emit. `yarn lint` uses `--fix`; `yarn build` cleans and emits both formats, not a read-only check. Follow [workspace restrictions](../../AGENTS.md).
