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
| [**tui-network**](https://github.com/tui-tools/tui-network) | Links, addresses, routes and DNS: systemd-networkd and resolved, with the .network file behind each link. | [![CI](https://github.com/tui-tools/tui-network/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-network/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-network?label=release)](https://github.com/tui-tools/tui-network/releases) |
| [**tui-secure**](https://github.com/tui-tools/tui-secure) | The machine's security posture: Secure Boot, SELinux or AppArmor, the firewall, sshd, updates and accounts, each with the command behind its verdict. | [![CI](https://github.com/tui-tools/tui-secure/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-secure/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-secure?label=release)](https://github.com/tui-tools/tui-secure/releases) |
| [**tui-users**](https://github.com/tui-tools/tui-users) | Local accounts, groups, authorized keys and sudo: who exists, what each one can do, and what is worth a second look. | [![CI](https://github.com/tui-tools/tui-users/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-users/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-users?label=release)](https://github.com/tui-tools/tui-users/releases) |
| [**tui-update**](https://github.com/tui-tools/tui-update) | Pending package updates across pacman, apt and dnf: what they restart or reboot, what is a security fix, and a snapshot before. | [![CI](https://github.com/tui-tools/tui-update/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-update/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-update?label=release)](https://github.com/tui-tools/tui-update/releases) |
| [**tui-disk**](https://github.com/tui-tools/tui-disk) | Disks, mounts and fstab crossed against each other, btrfs filesystems in full and the SMART health of every drive. | [![CI](https://github.com/tui-tools/tui-disk/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-disk/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-disk?label=release)](https://github.com/tui-tools/tui-disk/releases) |
| [**tui-ssh**](https://github.com/tui-tools/tui-ssh) | The SSH server as it really is: the effective sshd_config with a verdict per setting, live sessions, failed logins and host keys. | [![CI](https://github.com/tui-tools/tui-ssh/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-ssh/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-ssh?label=release)](https://github.com/tui-tools/tui-ssh/releases) |
| [**tui-logs**](https://github.com/tui-tools/tui-logs) | The systemd journal: every filter a journalctl argument, the command it adds up to on screen, and vacuuming previewed before it runs. | [![CI](https://github.com/tui-tools/tui-logs/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-logs/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-logs?label=release)](https://github.com/tui-tools/tui-logs/releases) |
| [**tui-cron**](https://github.com/tui-tools/tui-cron) | Every scheduled job on one screen, systemd timers and cron together, with each schedule read back in English next to the expression. | [![CI](https://github.com/tui-tools/tui-cron/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-cron/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-cron?label=release)](https://github.com/tui-tools/tui-cron/releases) |
| [**tui-cert**](https://github.com/tui-tools/tui-cert) | Every TLS certificate on the machine, worst first: what expires when, whose key is not its key, and what a server is really serving. | [![CI](https://github.com/tui-tools/tui-cert/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-cert/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-cert?label=release)](https://github.com/tui-tools/tui-cert/releases) |
| [**tui-containers**](https://github.com/tui-tools/tui-containers) | Every container on one screen, docker and podman together: what is wrong first, one container in full, and its log. | [![CI](https://github.com/tui-tools/tui-containers/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-containers/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-containers?label=release)](https://github.com/tui-tools/tui-containers/releases) |
| [**tui-samba**](https://github.com/tui-tools/tui-samba) | The Samba file server: shares worst first with the Unix permissions behind them, the accounts, and who is connected right now. | [![CI](https://github.com/tui-tools/tui-samba/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-samba/actions/workflows/ci.yml) [![release](https://img.shields.io/github/v/release/tui-tools/tui-samba?label=release)](https://github.com/tui-tools/tui-samba/releases) |

| Also here | |
| --- | --- |
| [**tui-kit**](https://github.com/tui-tools/tui-kit) | The shared foundation: theme, widgets, config loader, command runner. [![CI](https://github.com/tui-tools/tui-kit/actions/workflows/ci.yml/badge.svg)](https://github.com/tui-tools/tui-kit/actions/workflows/ci.yml) |
| [**tui-template**](https://github.com/tui-tools/tui-template) | A working skeleton for a new tool. Press **Use this template**. |

## Try one without a machine to risk

```sh
tui-firewall --demo
tui-systemd --demo
tui-snapper --demo
tui-network --demo
tui-secure --demo
tui-users --demo
tui-update --demo
tui-disk --demo
tui-ssh --demo
tui-logs --demo
tui-cron --demo
tui-cert --demo
tui-containers --demo
tui-samba --demo
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

The list the family set out to build is complete: every tool above exists, runs
and has a `--demo`. What comes next is depth rather than breadth — a
**firewalld backend for tui-firewall**, so Fedora and RHEL-family machines get
the same screens ufw users have today.

Which means the next tool is whichever one somebody asks for. If there is a
part of a Linux machine you keep reading through four commands and a manual
page, open an issue on
[tui-tools/.github](https://github.com/tui-tools/.github/issues) and say so.

## Status

Early, under validation. Expect rough edges, and please report them — a bug
report from a real machine, with the output the tool showed, is the most useful
thing anyone can send right now.

## License

MIT, per repository.
