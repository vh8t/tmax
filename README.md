<p align="center">
  <img src="logo.png" alt="tmax logo" width="100" style="border-radius: 8px;" />
</p>

<h1 align="center">tmax</h1>

<p align="center">
  A declarative and composable <code>tmux</code> wrapper for lightning-fast session management.<br>
  Minimal, scriptable, and written entirely in POSIX shell.
</p>

<p align="center">
  <code>tmux</code> power with simplicity. Define layouts, run commands, and get productive—fast.
</p>

## Why tmax?
`tmax` removes the friction from using `tmux`. Whether you’re managing a complex dev environment or just want to automate your favorite layout, `tmax` gives you:
- **Declarative layouts** using simple flags or config files
- **Scriptable workflows** for automation and bootstrapping
- **Readable dry-run summaries** for visibility and safety
- **No magic**, no dependencies — just portable shell

## Installation
1. Clone the repo
```sh
git clone https://github.com/vh8t/tmax.git ~/.local/shar/tmax
```

2. Add to your PATH (e.g., in `.bashrc`, `.zshrc`, or `.profile`):
```sh
export PATH="$HOME/.local/share/tmax:$PATH"
```

3. Reload your shell:

4. (Optional) initialize tmax folders:
```sh
tmax init
```
This sets up the config and layout directories at `~/.config/tmax`

## Features
- Composable layout creation via CLI flags
- Save and load layouts from files
- Auto-attach options
- Dry-run mode for previewing commands
- Minimal config support
- Simple management with `init` and `list` commands

## Usage
**Commands:**
- `tmax init` - Create default config and layouts folder
- `tmax list` - List saved layouts

**Session options:**
- `-s, --session:<name>` - Name the tmux session"
- `-a, --attach` - Automatically attach to the session after creation"
- `-m, --summary` - Print a detailed session summary before execution"

**Layout options:**
- `-v, --vertical[:<width>]` - Split vertically with optional width"
- `-h, --horizontal[:<height>]` - Split horizontally with optional height"
- `-w, --window[:<name>]` - Create a new (optionally named) window"
- `-c, --command:<command>` - Run a command in the current window or split"

**Session file options:**
- `-f, --file:<file>` - Run session from a tmax file"
- `-S, --save:<name>` - Save current layout to a file"
- `-l, --load:<name>` - Load layout by name"

**Other options:**
- `-d, --dry-run` - Show tmux commands without executing them"
- `-H, --help` - Show this help message"
- `-V, --version` - Show current tmax version"

## Layouts & Config
- Layouts are stored in `~/.config/tmax/layouts/`
- Default config is stored in `~/.config/tmax/config`
- Run `tmax init` to create both
