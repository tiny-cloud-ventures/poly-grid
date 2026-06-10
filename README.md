<div align="center">

<img src="assets/poly-grid-logo.png" alt="Poly Grid" width="320" />

### Stop setting up. Start working.

One-click AI agent workspaces for macOS. Save your whole rig — agents, layout,
working directories, initial prompts — and load it back in a click.
Like `tmuxinator`, except your agents are already running.

[![Latest release](https://img.shields.io/github/v/release/tiny-cloud-ventures/poly-grid?label=download&color=22c55e)](https://github.com/tiny-cloud-ventures/poly-grid/releases/latest)
[![Buy — $20](https://img.shields.io/badge/buy-%2420%20%C2%B7%203%20machines-22c55e)](https://tinycloud.lemonsqueezy.com/checkout/buy/23ac2124-877b-4d75-8687-e063ef2c51e1)
[![macOS](https://img.shields.io/badge/macOS-11%2B-lightgrey)](https://github.com/tiny-cloud-ventures/poly-grid/releases/latest)

</div>

---

<div align="center">
  <img src="assets/showcase.gif" alt="Poly Grid demo — broadcast prompts across three AI agents at once" />
</div>

---

> You've typed `cd ~/projects/foo && claude` four hundred times. Stop.

## What it does

| | |
|---|---|
| **Presets** | Save the whole grid — agents, layout, working directories, per-pane initial prompts — as a named bundle. Load it later and the whole grid spins up. Agents already running. |
| **Macros** | The commands you retype forty times a day, one click away. Pin `/clear`, `make test`, `git status` to a pane header — send to the focused pane or the broadcast group. |
| **Spaces** | Every project's rig, saved. Switch between projects, agent roles, or workflows without losing pane state. |
| **Broadcast** | Type once, send to every selected pane. Same prompt, three agents, instant compare. |
| **`@mentions`** | `@pane2:50` pulls the last 50 lines of that pane's output into your prompt. Hand context between agents without copy-paste. |
| **MCP server** | Local HTTP server (`127.0.0.1` only, bearer-token auth) exposes panes to Claude Desktop, Cursor, and Cline. Read/write panes from any MCP client. |
| **Cross-pane search** | Find any string across every pane's live buffer and scrollback history (`⌘⇧F`). |
| **Worktree panes** | `New worktree pane…` runs `git worktree add` and spawns a pane there, labeled with the branch. Cleanup on close. |
| **Pane attention** | Free in-app activity dots. Pro out-of-app delivery (OS notifications, dock bounce, sound) when an idle pane needs you. |
| **Power-user surface** | Command palette (`⌘⇧P`), `⌘1`–`⌘9` pane focus, `⌘⌥H/J/K/L` vim-style direction nav, `?` for the full shortcut sheet. |

---

## Why not just tmux?

tmux is free, scriptable, and great. If you've already wired up a `tmuxrc` plus `tmuxinator` for your AI workflow, you probably don't need this.

Poly Grid is for the rest of us — people who want the rig pre-built, not scripted. Presets in a dropdown, macros as buttons, no `.conf` to maintain. And because it's GUI-native, the same workspace your terminal sees is also reachable from Claude Desktop, Cursor, and Cline over MCP — no socket-passing, no `tmux send-keys` glue.

---

## Install

1. Download the latest DMG from **[Releases](https://github.com/tiny-cloud-ventures/poly-grid/releases/latest)**:
   - `Poly-Grid-1.0.0-arm64.dmg` — Apple Silicon
   - `Poly-Grid-1.0.0.dmg` — Intel
2. Open the DMG and drag **Poly Grid.app** into your Applications folder.
3. Launch. The first time, macOS may ask you to confirm the app — it's signed and notarized by Apple, so right-click → Open is enough.

The app **auto-updates** via `electron-updater`. New versions install themselves in the background and prompt to restart when ready.

---

## Pricing

- **Free forever:** the base multi-pane grid. Spawn panes, set layouts, type into them. That's yours.
- **7-day free trial** of the orchestration features above (presets, macros, spaces, broadcast, `@mentions`, MCP server, attention notifications, scrollback search).
- **$20 one-time, 3 machines** to unlock everything after the trial.

**[→ Buy a license](https://tinycloud.lemonsqueezy.com/checkout/buy/23ac2124-877b-4d75-8687-e063ef2c51e1)**

Activation lives in `~/.poly-grid-license` (encrypted via macOS Keychain), so reinstalling or upgrading macOS won't reset your trial or activation slot.

---

## System requirements

- macOS 11 (Big Sur) or later
- Apple Silicon or Intel
- ~150 MB disk
- Internet for license activation and auto-updates (7-day offline grace built in)

Linux and Windows builds are on the roadmap — Linux first, once the macOS funnel is healthy.

---

## Privacy

Poly Grid ships with **opt-in** product analytics (powered by [Aptabase](https://aptabase.com/), open-source and privacy-first). First launch asks you explicitly; you can toggle it any time from **Help → Privacy…**.

When on, the app sends:

- A random install ID, app version, OS family
- Six named funnel events (`app_launched`, `pane_command_typed`, `pro_feature_attempted`, `license_modal_opened`, `license_activated`, `app_quit`)
- Small counters (trial days left, session count, panes open)

It **never** sends:

- Pane contents, commands you type, or terminal output
- File paths, working directories, or git remotes
- License keys, your email, or your machine's hostname

A hardened redactor at the boundary drops the entire event if anything path-shaped, license-shaped, email-shaped, or homedir-leaking sneaks in. The full policy lives at [poly-grid.com/privacy](https://poly-grid.com/privacy).

---

## Support

- Feature requests + bug reports: [open an issue](https://github.com/tiny-cloud-ventures/poly-grid/issues)
- Direct support for license holders: email the address on your purchase receipt

---

## License

Poly Grid is **proprietary software**, sold via Lemon Squeezy. The source code is closed; this repository hosts the public release binaries, documentation, and asset previews only.

**© Tiny Cloud Ventures.** All rights reserved.
