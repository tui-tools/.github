<img src="https://raw.githubusercontent.com/tui-tools/.github/main/profile/assets/logo.png" alt="tui-tools" width="300">

Terminal tools for Linux that show you the system as it is, and **preview the
exact command line of every change before running it**.

Each one is a **single static binary**. No daemon, no state of its own, nothing
left running after you quit. They share a palette, a key language and one
promise: the command in the confirm dialog is the command that executes.

**[tui-tools.github.io](https://tui-tools.github.io)** — every tool, with
screenshots, install commands per package manager, checksums and what each one
can do to your machine. It is built from each repository's own `tool.json`, so
a new tool appears there on its first release without anyone editing a page.

## The tools

| Tool | What it does | |
| --- | --- | --- |
| [**tui-firewall**](https://github.com/tui-tools/tui-firewall) | The system firewall: rules, policies, logging. ufw today, firewalld planned. | [![CI](https://github.com/tui-tools/tui-firewall/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-firewall/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-firewall?label=release)](https://github.com/tui-tools/tui-firewall/releases) |
| [**tui-systemd**](https://github.com/tui-tools/tui-systemd) | systemd units: what failed, the journal that explains why, timers, boot times. | [![CI](https://github.com/tui-tools/tui-systemd/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-systemd/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-systemd?label=release)](https://github.com/tui-tools/tui-systemd/releases) |
| [**tui-snapper**](https://github.com/tui-tools/tui-snapper) | btrfs snapshots, managed by snapper: the history, what changed between any two, and undo. | [![CI](https://github.com/tui-tools/tui-snapper/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-snapper/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-snapper?label=release)](https://github.com/tui-tools/tui-snapper/releases) |

| Also here | |
| --- | --- |
| [**tui-kit**](https://github.com/tui-tools/tui-kit) | The shared foundation: theme, widgets, config loader, command runner. [![CI](https://github.com/tui-tools/tui-kit/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-kit/actions/workflows/ci.yml) |
| [**tui-template**](https://github.com/tui-tools/tui-template) | A working skeleton for a new tool. Press **Use this template**. |

## Try one without a machine to risk

```sh
tui-firewall --demo
tui-systemd --demo
tui-snapper --demo
```

`--demo` runs against sample data. Every key works, every command is built and
previewed for real, and nothing touches your system.

## The rules

They hold for every tool here.

- **Preview, then confirm.** No tool changes anything without first showing the
  exact command line. The confirm dialog is the only path to a mutation, and the
  value it displays is the value that runs.
- **Read-only by default.** Starting a tool only reads state.
- **No daemon, no state of its own.** The system is the source of truth; the
  tools re-read it after every change.
- **Runs as you.** Reads work unprivileged wherever the underlying tool allows
  it; only an action escalates, through `sudo -n`, which never prompts.
- **Backend behind an interface.** The UI never names a binary, which is what
  lets `tui-firewall` grow a firewalld backend without touching its screens.
- **Responsive.** Layouts adapt from a 40-column pane to a full screen.

## Naming

Every tool is **`tui-<target>`**: the repository, the Go module, the binary and
the config directory all carry that one name, with **no aliases**. `tui-<name>-<solution>`
only when a target genuinely needs disambiguating.

## Theme

The default palette is **Tokyo Night**. If you run [Omarchy](https://omarchy.org),
the tools read your active desktop theme from
`~/.config/omarchy/current/theme/colors.toml` and follow it, so switching your
desktop theme switches every tool. `TUI_THEME` overrides, and `NO_COLOR` drops
color while keeping layout.

**Unofficial.** These tools follow the Omarchy visual style and read its theme
files. They are **not** part of the Omarchy project and are not endorsed by its
maintainers.

## Roadmap

Next, in this order:

1. **tui-network**: interfaces, addresses, routes and DNS. systemd-networkd and
   resolved first; NetworkManager and netplan later.
2. **tui-secure**: one screen for the machine's security posture (Secure Boot,
   SELinux or AppArmor mode and recent denials, firewall, sshd, pending
   updates), with each fix handed to the tool that owns it.
3. **tui-update**: package updates with the restart classifier and, where the
   filesystem allows it, a snapshot before and a rollback after.
Then: **tui-users** (accounts, groups, authorized keys, sudo), **tui-ssh**
(`sshd_config` with `sshd -t` before apply, sessions, failed logins),
**tui-disk** (btrfs subvolumes and maintenance, `lsblk`, `fstab`, SMART),
**tui-logs** (the journal, split out of tui-systemd), **tui-docker** /
**tui-podman**, **tui-cron**, **tui-cert**, **tui-samba** (shares, users and live
connections for a file server).

Want one sooner, or a different one? Open an issue on
[tui-tools/.github](https://github.com/tui-tools/.github/issues).

## Status

Early, under validation. Expect rough edges, and please report them — a bug
report from a real machine, with the output the tool showed, is the most useful
thing anyone can send right now.

## License

MIT, per repository.
