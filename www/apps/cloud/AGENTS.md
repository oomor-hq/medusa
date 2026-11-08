# cloud

Owns Medusa Cloud deployment/hosting documentation; content lives in `app` MDX, navigation in `sidebar.mjs`. See the [local manifest](package.json) and [preparation source](scripts/prepare.mjs). Shared rendering belongs in docs-ui, not duplicated app components.

From `www/apps/cloud/`:

- `yarn prep` writes generated content; also generates the changelog manifest. Inspect changes after preparation.
- Non-emitting type check: `yarn exec tsc --noEmit --incremental false` (requires prepared dependencies/generated types).
- Non-fixing code check: `yarn exec eslint app pages components lib src --no-error-on-unmatched-pattern`.
- Non-fixing content check: `yarn exec eslint --no-config-lookup -c .content.eslintrc.mjs 'app/**/*.mdx' --quiet`.

The manifest's `lint` and `lint:content` scripts add `--fix`. `build:cloudflare` prepares/builds deployment artifacts; `deploy` and `upload` contact Cloudflare. Follow the [workspace restrictions](../../AGENTS.md); do not run these on your own initiative.
