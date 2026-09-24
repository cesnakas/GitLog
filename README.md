# Git Log

Git history and branch management for Cursor & VS Code.

Manage branches, browse commit history, inspect changed files, and perform common Git operations directly from the editor.

**Git graph** · **Branch management** · **Search & filters** · **Changed files** · **Merge / Rebase / Push**

> This repository is the public home for Git Log releases, documentation, bug reports, and feature requests. The source code is maintained separately and is not published in this repository.

## Highlights

- **Branch management** — browse local and remote branches, create, checkout, rename, delete, merge, rebase, update, and push.
- **Commit graph** — explore commit history with branch and tag references, authors, dates, and hashes.
- **Powerful search and filters** — filter by branch, user, date, path, text, or commit hash, with case-sensitive and regex search.
- **Changed files and diffs** — inspect files changed by a commit and open diffs directly in the editor.
- **Branch comparison** — compare branch histories or diff a branch against the working tree.
- **Remote state** — fetch remotes and see ahead/behind state for tracked branches.
- **Fast workflow** — open Git Log from the bottom panel, status bar, Command Palette, or keyboard shortcut.

## Installation

Git Log is currently distributed as a `.vsix` package through GitHub Releases.

1. Open the **Releases** section of this repository.
2. Download the `.vsix` file from the latest release.
3. Open the Extensions view in Cursor or VS Code.
4. Open the Extensions menu (`...`).
5. Choose **Install from VSIX...**
6. Select the downloaded package.

You can also install it from the command line.

### Cursor

```bash
cursor --install-extension git-log-<version>.vsix
```

### VS Code

```bash
code --install-extension git-log-<version>.vsix
```

Extension ID: `cesnakas.git-log`

## Features

### Branches

- Browse local and remote branches
- Group branches by directory
- Show Git tags in the branches pane
- Mark frequently used branches as favorites
- Create a branch from any branch or ref
- Checkout local and remote branches
- Smart checkout for worktrees with uncommitted changes
- Rename and delete branches
- Merge branches
- Rebase the current branch onto another branch
- Checkout another branch and rebase it onto the current branch
- Update branches using merge or rebase
- Push branches
- Force push safely with `--force-with-lease`
- Compare a branch with the current branch
- Show a branch diff against the working tree
- Fetch all remotes
- View ahead/behind state for tracked branches

### Commit history

- Browse commit history with a Git graph
- View branch and tag references on commits
- View commit author, date, and hash
- Search by commit message, author, ref, or commit hash
- Match case when searching
- Use regular expressions when searching
- Filter by branch
- Filter by author
- Filter by date
- Filter by file or directory path
- Sort by commit date or topologically
- Show first-parent history
- Hide merge commits
- Collapse linear branches

### Changed files

- View files changed by the selected commit
- Inspect added, modified, deleted, and renamed files
- Open commit diffs directly in Cursor or VS Code
- Compare a branch with the working tree
- Swap diff direction
- Get an individual file from another branch into the working tree

### Repository integration

- Dedicated **Git Log** bottom panel
- Status bar branch indicator and quick access
- Automatic refresh when Git refs, HEAD, tags, or repository state change
- Integration with the built-in VS Code Git extension
- Automatic background fetch
- Live ahead/behind indicators

## Usage

Open a folder containing a Git repository, then open **Git Log** using any of these methods:

- Open the **Git Log** tab in the bottom panel
- Click the Git branch indicator in the status bar
- Run **Git Log: Open** from the Command Palette
- Press `Cmd+Shift+G`, then `L` on macOS
- Press `Ctrl+Shift+G`, then `L` on Windows/Linux

The interface is organized around three main areas:

- **Branches** — browse and manage local branches, remote branches, and tags
- **Log** — explore, search, and filter commit history
- **Changes** — inspect files changed by the selected commit or branch comparison

Right-click a branch to access branch-specific Git operations.

## Search and filters

The Git Log toolbar provides filters for:

- **Branch**
- **User**
- **Date**
- **Paths**
- **Text or commit hash**

Search supports case-sensitive matching and regular expressions.

Graph options include:

- Sort by commit date
- Topological sort
- First-parent history
- Hide merge commits
- Collapse linear branches

## Settings

### Update method

`gitLog.updateMethod`

Controls how incoming changes are integrated when an update cannot be fast-forwarded.

| Value | Behavior |
| --- | --- |
| `merge` | Merge incoming changes into the local branch using `git pull --no-rebase` |
| `rebase` | Rebase local commits on top of incoming changes using `git pull --rebase` |

Default: `merge`

## Requirements

- Cursor or Visual Studio Code compatible with VS Code API `1.85.0` or newer
- Git installed and available on the system
- An opened workspace containing a Git repository
- The built-in VS Code Git extension

## Commands

| Command | Description |
| --- | --- |
| `Git Log: Open` | Open and focus the Git Log panel |
| `Git Log: Refresh` | Refresh branches and commit history |

## Releases

Ready-to-install builds are published in the **Releases** section of this repository.

See [CHANGELOG.md](CHANGELOG.md) for notable changes between versions.

## Feedback & Issues

Found a bug or have an idea for Git Log?

- Use **Bug report** for reproducible problems.
- Use **Feature request** to suggest improvements or new workflows.

Please check existing issues before opening a new one.

## Support

If Git Log saves you time, you can support its development at [support.cesnakas.com](https://support.cesnakas.com).

## License

Git Log is proprietary software.

The distributed extension may be installed and used subject to the terms in [LICENSE](LICENSE). The source code is not licensed for public use or distribution.
