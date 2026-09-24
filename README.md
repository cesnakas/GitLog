# Git Log

Git history and branch management for Cursor & VS Code.

Manage branches, browse commit history, inspect changed files, and perform common Git operations directly from the editor.

> Screenshot coming soon.

## Features

### Branch management

- Browse local and remote branches
- Group branches by directory
- Mark frequently used branches as favorites
- Create branches from any branch or ref
- Checkout local and remote branches
- Rename and delete branches
- Merge branches
- Rebase the current branch onto another branch
- Checkout a branch and rebase it onto the current branch
- Update branches using merge or rebase
- Push branches, including force push with `--force-with-lease`
- Compare a branch with the current branch
- Show a branch diff against the working tree
- Fetch all remotes
- View ahead/behind state for tracked branches

### Commit history

- Browse commit history with a Git graph
- View branches, refs, tags, authors, dates, and commit hashes
- Search by commit message, author, ref, or commit hash
- Match case or use regular expressions when searching
- Filter history by branch
- Filter by author
- Filter by date
- Filter by file or directory path
- Sort by commit date or topologically
- Show first-parent history
- Hide merge commits
- Collapse linear branches
- Compare branch histories

### Changed files

- View files changed by the selected commit
- Open diffs directly in the editor
- Inspect added, modified, deleted, and renamed files
- View differences between a branch and the working tree
- Get an individual file from another branch

### Workflow integration

- Opens as a dedicated **Git Log** panel
- Refreshes when Git refs, HEAD, tags, or repository state change
- Integrates with the built-in VS Code Git extension
- Automatically fetches remote changes in the background
- Keeps branch state and ahead/behind indicators up to date
- Supports repositories with uncommitted changes during checkout using safe checkout/stash flows

## Installation

### Cursor

Install **Git Log** from the Extensions view in Cursor.

### VS Code

Install **Git Log** from the Extensions view in Visual Studio Code.

You can also install a `.vsix` package manually:

```bash
code --install-extension git-log-<version>.vsix
```

For Cursor:

```bash
cursor --install-extension git-log-<version>.vsix
```

## Usage

Open a folder containing a Git repository, then open **Git Log** using any of these methods:

- Open the **Git Log** panel
- Click the Git branch icon in the status bar
- Run **Git Log: Open** from the Command Palette
- Use `Cmd+Shift+G`, then `L` on macOS
- Use `Ctrl+Shift+G`, then `L` on Windows/Linux

The interface is organized around three main areas:

- **Branches** — browse and manage local and remote branches
- **Log** — explore, search, and filter commit history
- **Changes** — inspect files changed by a commit or branch comparison

Right-click a branch to access branch-specific Git operations.

## Search and filters

The Git Log toolbar provides filters for:

- **Branch**
- **User**
- **Date**
- **Paths**
- **Text or commit hash**

Graph options include topological/date sorting, first-parent history, hiding merges, and collapsing linear branches.

## Settings

### Update method

`gitLog.updateMethod`

Controls how incoming changes are integrated when an update cannot be fast-forwarded.

Available values:

- `merge` — merge incoming changes into the local branch
- `rebase` — rebase local commits on top of incoming changes

Default: `merge`

## Requirements

- Cursor or Visual Studio Code `1.85.0` or newer
- Git installed and available on the system
- An opened workspace containing a Git repository
- The built-in VS Code Git extension

## Commands

| Command | Description |
| --- | --- |
| `Git Log: Open` | Open and focus the Git Log panel |
| `Git Log: Refresh` | Refresh branches and commit history |

## Feedback & Issues

Bug reports and feature requests are welcome. Please open an issue in the GitHub repository.

## License

Released under the [MIT License](LICENSE).
