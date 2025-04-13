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

## Features

- Composable layout creation via CLI flags
- Save and load layouts from files
- Auto-attach options
- Dry-run mode for previewing commands
- Minimal config support
- Simple management with `init` and `list` commands

## Usage

**Commands:**
- `tmax init` - creates default config and layouts folder
- `tmax list` - lists saved layouts

**Options:**
- `-v:<width>` - split vertically with given width
- `-h:<height>` - split horizontally with given height
- `-c:<command>` - run a command in the current window or split
- `-w:<name>` - create a new named window
- `-s:<name>` - name the session
- `-a` - auto attach to the session

**Session file options:**
- `--file:<file>` - run session from a tmax file
- `--save:<name>` - save layout to a file
- `--load:<name>` - load layout by name

**Other:**
- `--dry-run` - print tmux command without executing them
- `-h`, `--help` - show usage info

## Layouts & Config

- Layouts are stored in `~/.config/tmax/layouts/`
- Default config is stored in `~/.config/tmax/config`
- Run `tmax init` to create both
