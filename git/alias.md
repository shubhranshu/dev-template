# Git Aliases Setup

This documentation provides a set of Git commands to create useful aliases to streamline your workflow.

## Aliases

1. **main**: Stash changes, checkout the main branch, get the latest changes, and apply the stash.
2. **sps**: Stash changes, get the latest changes, and apply the stash.
3. **fp**: Fetch and prune branches.
4. **lga**: Show logs with a graph view for all branches.
5. **lgb**: Show logs with a graph view for the current branch.

## Commands

Run the following commands in your terminal to set up these aliases:

```bash
# Alias 'main': stash, checkout main, get latest, apply stash
git config --global alias.main "!git stash push -m 'Auto-stash before main' && git checkout main && git pull origin main && git stash pop"

# Alias 'sps': stash, get latest, apply stash
git config --global alias.sps "!git stash push -m 'Auto-stash before sps' && git pull origin && git stash pop"

# Alias 'fp': fetch and prune
git config --global alias.fp 'fetch --prune'

# Alias 'lga': log with graph and all branches
git config --global alias.lga "log --oneline --graph --all --decorate"

# Alias 'lgb': log with graph for the current branch
git config --global alias.lgb "log --oneline --graph --decorate"

# Set alias for git status
git config --global alias.st status

# Set alias for git commit
git config --global alias.ci commit

# Set alias for git checkout
git config --global alias.co checkout

# Set alias for git branch
git config --global alias.br branch

# Set alias for git log with graph view
git config --global alias.lg "log --oneline --graph --all --decorate"

# Set alias for git diff
git config --global alias.df diff

# Set alias for git pull
git config --global alias.pl pull

# Set alias for git push
git config --global alias.ph push

# Set alias for git fetch
git config --global alias.f fetch

# Set alias for git merge
git config --global alias.mg merge

# Set alias for git rebase
git config --global alias.rb rebase

# Set alias for git reset
git config --global alias.rs reset

# Set alias for git add
git config --global alias.a add

# Set alias for git commit --amend
git config --global alias.amend 'commit --amend'

# Set alias for git log with pretty format
git config --global alias.l "log --pretty=format:'%C(yellow)%h%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
