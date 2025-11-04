### setup 
| Command                                    | What it does                       | Example                                              |
| ------------------------------------------ | ---------------------------------- | ---------------------------------------------------- |
| `git config --global user.name "<name>"`   | Set your global commit author name | `git config --global user.name "Atul Parmar"`        |
| `git config --global user.email "<email>"` | Set your global commit email       | `git config --global user.email "atul@example.com"`  |
| `git config --global color.ui auto`        | Enable colored CLI output          | `git config --global color.ui auto`                  |

### Setup & Init
| Command           | What it does                     | Example                                              |
| ----------------- | -------------------------------- | ---------------------------------------------------- |
| `git init`        | Initialize a repo in current dir | `cd ~/Desktop/BYTEXL && git init`                    |
| `git clone <url>` | Clone an existing repo           | `git clone https://github.com/aspparmar/bytexl.git`  |

### Stage & Snapshot
| Command                 | What it does                 | Example                                         |
| ----------------------- | ---------------------------- | ----------------------------------------------- |
| `git status`            | Show changes & staging state | `git status` in `BYTEXL` to see `lpu-dsa-II/*`  |
| `git add <file>`        | Stage a file                 | `git add lpu-dsa-II/binary-tree.txt`            |
| `git add .`             | Stage everything             | `git add .` in `BYTEXL`                         |
| `git reset <file>`      | Unstage but keep changes     | `git reset lpu-dsa-II/binary-tree.txt`          |
| `git diff`              | Unstaged changes diff        | `git diff` after editing `binary-tree.txt`      |
| `git diff --staged`     | Diff of staged changes       | `git diff --staged` before commit               |
| `git commit -m "<msg>"` | Create a snapshot            | `git commit -m "Add binary tree notes"`         |
 
### Branch & Merge

| Command               | What it does        | Example                                      |
| --------------------- | ------------------- | -------------------------------------------- |
| `git branch`          | List branches       | `git branch` shows `* main`                  |
| `git branch <name>`   | Create branch       | `git branch docs-btree`                      |
| `git checkout <name>` | Switch branches     | `git checkout docs-btree`                    |
| `git merge <branch>`  | Merge into current  | `git checkout main && git merge docs-btree`  |
| `git log`             | View commit history | `git log --oneline --graph --decorate`       |
### Share & Update (Remotes)
| Command                        | What it does                  | Example                                                          |
| ------------------------------ | ----------------------------- | ---------------------------------------------------------------- |
| `git remote add <alias> <url>` | Add remote                    | `git remote add origin https://github.com/aspparmar/bytexl.git`  |
| `git fetch <alias>`            | Download branches             | `git fetch origin`                                               |
| `git merge <alias>/<branch>`   | Merge remote branch           | `git merge origin/main`                                          |
| `git push <alias> <branch>`    | Push commits                  | `git push origin main`                                           |
| `git pull`                     | Fetch + merge tracking branch | `git pull` on `main` (tracks `origin/main`)                      |
### Tracking Path Changes
| Command              | What it does           | Example                                                               |
| -------------------- | ---------------------- | --------------------------------------------------------------------- |
| `git rm <file>`      | Delete & stage removal | `git rm lpu-dsa-II/old.txt`                                           |
| `git mv <old> <new>` | Rename/move & stage    | `git mv lpu-dsa-II/binary-tree.txt lpu-dsa-II/binary-tree-notes.txt`  |
| `git log --stat -M`  | Logs with renames      | `git log --stat -M -- lpu-dsa-II`                                     |
### Temporary Commits (Stash)
| Command          | What it does     | Example                                     |
| ---------------- | ---------------- | ------------------------------------------- |
| `git stash`      | Save WIP changes | Edit files in `lpu-dsa-II/*` → `git stash`  |
| `git stash list` | List stashes     | `git stash list`                            |
| `git stash pop`  | Reapply & drop   | `git stash pop` to restore edits            |
| `git stash drop` | Discard a stash  | `git stash drop stash@{0}`                  |
### rewrite-history
| Command                     | What it does                    | Example                                  |
| --------------------------- | ------------------------------- | ---------------------------------------- |
| `git rebase <branch>`       | Replay commits on top of target | `git rebase main` while on `docs-btree`  |
| `git reset --hard <commit>` | Reset working tree & index      | `git reset --hard HEAD~1` (dangerous)    |
### inspect and compare

| Command                      | What it does           | Example                                              |
| ---------------------------- | ---------------------- | ---------------------------------------------------- |
| `git log`                    | Show history           | `git log -- lpu-dsa-II/binary-tree-notes.txt`        |
| `git log branchB..branchA`   | Commits in A not in B  | `git log main..docs-btree`                           |
| `git log --follow <file>`    | History across renames | `git log --follow lpu-dsa-II/binary-tree-notes.txt`  |
| `git diff branchB...branchA` | Diff A not in B        | `git diff main...docs-btree`                         |
| `git show <SHA>`             | Show an object         | `git show abc1234`                                   |
### Ignoring Patterns
| Command / Pattern                              | What it does       | Example                                                                   |
| ---------------------------------------------- | ------------------ | ------------------------------------------------------------------------- |
| `git config --global core.excludesfile <file>` | Global ignore file | `git config --global core.excludesfile ~/.gitignore_global`               |
| `.gitignore` patterns                          | Ignore files/dirs  | In `BYTEXL/.gitignore` add: `.DS_Store`, `logs/`, `*.notes`, `pattern*/`  |
