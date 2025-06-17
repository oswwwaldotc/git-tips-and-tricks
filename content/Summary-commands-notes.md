# Git: Tips & Tricks 🧑‍💻

> Summary

## Configuration and Aliases ⚙️

### Exercises and Solutions

```bash
# Viewing configuration settings
git config --list

# Setting a global configuration value
git config --global user.name "Your Name"

# Reading a global configuration value
git config --global user.name

# Setting a local configuration value
git config user.email "your.email@example.com"

# Reading a configuration value
git config user.email
```

### Code Exercises and Solutions

```bash
# Creating an alias
git config --global alias.co checkout
# Now you can use `git co` instead of `git checkout`
git co <branch-name>

# Alias to add all changes and commit with message in one command
# Usage: git acommit "your commit message"
git config --global alias.acommit '!git add -A && git commit -m'

# Shortened status command showing changes concisely
git config --global alias.st "status --short"

# Compact log view with branch graph
git config --global alias.lg "log --oneline --graph --decorate --all"

# Detailed colored log with author and timestamp
git config --global alias.flog "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

# Simplified colored log with author name
git config --global alias.slog "log --graph --pretty='format:%C(red)%d%C(reset) %C(yellow)%h%C(reset) %ar %C(green)%aN%C(reset) %s'"
```

---

## Most common commands 📋

| Command                    | Description                                                   | Example                               |
|----------------------------|---------------------------------------------------------------|---------------------------------------|
| `git init`                 | Initializes a new Git repository.                             | `git init`                            |
| `git clone [url]`          | Clones a repository from a given URL.                         | `git clone https://github.com/user/repo.git` |
| `git status`               | Shows the status of changes in the current repository.        | `git status`                          |
| `git add [file/directory]` | Adds changes in the specified file/directory to the staging area. | `git add .`                           |
| `git commit -m "[message]"`| Commits the staged changes with a descriptive message.        | `git commit -m "Add new feature"`     |
| `git branch [branch-name]` | Creates a new branch.                                         | `git branch feature-branch`           |
| `git checkout [branch-name]`| Switches to the specified branch.                             | `git checkout feature-branch`         |
| `git merge [branch-name]`  | Merges the specified branch into the current branch.          | `git merge feature-branch`            |
| `git push [remote] [branch]`| Pushes the committed changes to the specified remote repository and branch. | `git push origin main`                |
| `git pull [remote] [branch]`| Fetches and merges changes from the specified remote repository and branch. | `git pull origin main`                |
| `git log`                  | Displays the commit history.                                  | `git log`                             |
| `git reset [commit-hash]`  | Resets the current HEAD to the specified commit.              | `git reset abc123`                    |
| `git rebase [branch-name]` | Reapplies commits from the current branch onto the specified branch. | `git rebase main`                      |
| `git stash`                | Temporarily saves changes that are not ready to be committed. | `git stash`                           |
| `git stash pop`            | Restores the most recently stashed changes.                  | `git stash pop`                       |
| `git remote add [name] [url]` | Adds a remote repository.                                | `git remote add origin https://github.com/user/repo.git` |
| `git diff`                 | Shows differences between staged changes and working directory. | `git diff`                            |