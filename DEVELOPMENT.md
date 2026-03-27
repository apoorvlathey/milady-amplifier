# Development

## Core Commands

```bash
pnpm run build
pnpm run typecheck
pnpm run test
pnpm run check:pfp -- <avatar-url>
```

## Chrome Debugging

Launch Chrome with a persistent local debug profile:

```bash
pnpm run debug:chrome:launch-local-profile
```

Attach to that running Chrome session:

```bash
pnpm run debug:chrome:attach
```

Keep the CDP attachment open:

```bash
pnpm run debug:chrome:attach:keep-open
```

## Alternate Profile Helpers

Launch against a system Chrome profile named `Extension`:

```bash
pnpm run debug:chrome:launch-extension-profile
```

Legacy extension debug helpers:

```bash
pnpm run debug:extension
pnpm run debug:extension:default-profile
pnpm run debug:extension:extension-profile
pnpm run debug:extension:seed-extension-profile
```

## Asset Preparation

Download the Milady image corpus:

```bash
pnpm run download:images
pnpm run download:images:aria2
```

Generate the legacy local assets:

```bash
pnpm run generate:hashes
pnpm run generate:model
pnpm run prepare:assets
```

## Training Pipeline

```bash
pnpm run ingest:avatars -- cache/milady-shrinkifier-avatars-<timestamp>.json
pnpm run download:avatars
pnpm run label:heuristic
pnpm run review:avatars
pnpm run build:dataset
pnpm run train:classifier
pnpm run score:classifier -- --run-id <run-id>
pnpm run export:classifier -- --run-id <run-id>
```
