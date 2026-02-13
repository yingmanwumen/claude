# Claude Code Configuration

Personal Claude Code configuration, including custom skills and plugins.

## Structure

```
.claude/
├── skills/           # Custom skills
├── plugins/          # Plugin cache directories
├── .gitignore        # Git ignore rules
└── CLAUDE.md         # Claude Code documentation
```

## Custom Skills

### review-commit-push
Automated workflow for reviewing, committing, and pushing code changes.

**Features:**
- Runs linter/formatter before committing
- Reviews code diffs for correctness
- Uses conventional commit style
- Commits and pushes in one step

**Usage:** Invoked automatically via `/review-commit-push` command.

### peon-ping-toggle
Toggle peon-ping sound notifications on/off.

**Usage:**
```bash
bash "${CLAUDE_CONFIG_DIR:-$HOME/.claude}"/hooks/peon-ping/peon.sh toggle
```

### peon-ping-config
Update peon-ping configuration settings (volume, pack rotation, categories, etc.).

**Config location:** `${CLAUDE_CONFIG_DIR:-$HOME/.claude}/hooks/peon-ping/config.json`

## Setup

1. Clone this repository to your Claude Code config directory:
   ```bash
   git clone git@github.com:yingmanwumen/claude.git ~/.claude
   ```

2. Restart Claude Code to load the configuration.
