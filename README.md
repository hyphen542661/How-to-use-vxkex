# Windows 7 Modern Software Compatibility Guide

A practical, tested guide for running modern software on Windows 7 — for people keeping older machines alive and useful in 2026.

Most "modern app on old OS" guides online are outdated, incomplete, or just wrong. This repo documents **exact versions, exact download links, and exact steps that have actually been tested and confirmed working**, mostly using [VxKex Next](https://github.com/vxsz/VxKex) as a compatibility shim.

## Why this exists

Windows 7 machines are still out there — low-RAM laptops, old desktops, machines that can't (or shouldn't) be upgraded. Most modern apps assume Windows 10/11 APIs and refuse to install or run. This guide collects working solutions in one place instead of scattered forum posts.

## What's covered

| App | Status | Notes |
|---|---|---|
| [VxKex Next setup](vxkex-setup.md) | ✅ Required first step | Compatibility layer for most entries below |
| [Discord](apps/discord.md) | ✅ Working | Archived Win7-compatible installer |
| [Dropbox](apps/dropbox.md) | ✅ Working | Specific older version required |
| [Notion](apps/notion.md) | ✅ Working | Specific version required |
| [Browsers](apps/browsers.md) | ✅ Working | Opera, Pale Moon, Midori, Vivaldi |
| [Godot Engine](apps/godot.md) | ✅ Working | Needs a launch flag |
| [Perplexity Desktop](apps/perplexity.md) | ✅ Working | Via VxKex |

## Quick start

1. Read [`vxkex-setup.md`](vxkex-setup.md) first — most entries assume it's installed.
2. Pick the app you need from the table above.
3. Follow the exact version + steps listed. Using a different version than the one documented is the #1 reason these stop working.

## Contributing

If you've gotten something else running on Windows 7, open an issue or PR with:
- The exact app version that worked
- Whether VxKex was required
- Any launch flags, registry tweaks, or gotchas

## Disclaimer

Windows 7 is out of support from Microsoft. This guide doesn't cover security implications of running an unsupported OS — that's a separate conversation. This is purely a technical compatibility reference.

## License

MIT — use, share, and adapt freely.
