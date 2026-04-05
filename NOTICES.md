# Z.AI Adapter Modifications

This fork of Claurst includes modifications to support the Z.AI coding platform.

## Changes from upstream (Kuberwastaken/claurst)

### Provider: Z.AI / Zhipu AI (`openai_compat_providers.rs`)

The `zhipu()` provider factory was enhanced to support the Z.AI coding platform:

- When `ZAI_API_KEY` is set, the provider routes to `https://api.z.ai/api/coding/paas/v4`
- Falls back to standard Zhipu API (`open.bigmodel.cn`) when only `ZHIPU_API_KEY` is present
- Added `reasoning_field: Some("reasoning_content")` quirk for GLM-5.1 reasoning output
- Default model: `glm-5.1`

### .gitignore

Added `target/` exclusion to prevent build artifacts from being tracked.

## Upstream

- Repository: https://github.com/Kuberwastaken/claurst
- License: GNU General Public License v3.0
- Copyright: Kuberwastaken and contributors

## This fork

- Repository: https://github.com/schwabauerbriantomas-gif/claurst
- License: GNU General Public License v3.0 (same as upstream, per GPLv3 requirements)
