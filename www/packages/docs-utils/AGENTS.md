# docs-utils

Shared MDX/frontmatter, sidebar, slug and API-reference path utilities live here; React components belong in docs-ui. Preserve the [manifest's](package.json) ESM entry and separate global-config CJS/ESM exports; changes affect preparation and rendering across apps.

From `www/packages/docs-utils/`: `yarn test --run` runs Vitest once, but its script uses `--passWithNoTests`, so success alone does not prove coverage. Non-emitting checks: `yarn exec tsc --noEmit --incremental false` and `yarn exec tsc --project tsconfig.cjs.json --noEmit --incremental false`. No lint script exists here. `yarn build` cleans/emits files and marks the CJS directory; it is not a read-only check. Follow [workspace restrictions](../../AGENTS.md).
