## Git Setup and Configuration

| Code | Description |
|------|-------------|
| `git init` | Initializes a new Git repository in the current directory. |
| `git init --bare` | Initializes a new bare Git repository without a working directory. |
| `git init --quiet` | Initializes a new Git repository without output. |
| `git init --template=template_dir` | Initializes a new Git repository using a custom template directory. |
| `git init --separate-git-dir=git_dir` | Initializes a new Git repository with the .git directory at a custom location. |
| `git clone repository [directory]` | Clones a repository into a specified directory. |
| `git clone --local repository [directory]` | Clones a local repository. |
| `git clone --no-local repository [directory]` | Clones a repository without optimizing for local repositories. |
| `git clone --depth depth repository [directory]` | Creates a shallow clone with a history truncated to the specified number of commits. |
| `git clone --branch branch repository [directory]` | Clones a specific branch from a repository. |
| `git clone --tag tag repository [directory]` | Clones a specific tag from a repository. |
| `git clone --single-branch repository [directory]` | Clones only the history leading to a single branch. |
| `git clone --no-single-branch repository [directory]` | Clones all branches from a repository. |
| `git clone --mirror repository [directory]` | Creates a mirror clone of a repository. |
| `git clone --no-checkout repository [directory]` | Clones a repository without checking out the working tree. |
| `git clone --recurse-submodules repository [directory]` | Clones a repository and all its submodules. |
| `git clone --no-recurse-submodules repository [directory]` | Clones a repository without its submodules. |
| `git clone --shallow-submodules repository [directory]` | Clones a repository with shallow submodules. |
| `git clone --no-shallow-submodules repository [directory]` | Clones a repository with full submodules. |
| `git clone --reference repository repository [directory]` | Clones a repository using a reference repository to speed up the clone. |
| `git clone --dissociate repository [directory]` | Clones a repository and makes the clone independent of the reference repository. |
| `git clone --quiet repository [directory]` | Clones a repository without output. |
| `git clone --progress repository [directory]` | Clones a repository with progress output. |
| `git clone --no-progress repository [directory]` | Clones a repository without progress output. |
| `git clone --verbose repository [directory]` | Clones a repository with verbose output. |
| `git clone --no-hardlinks repository [directory]` | Clones a repository without using hard links. |
| `git config user.name "Name"` | Sets the Git username for commits. |
| `git config user.email "email@example.com"` | Sets the Git email for commits. |
| `git config --global user.name "Name"` | Sets the global Git username for commits. |
| `git config --global user.email "email@example.com"` | Sets the global Git email for commits. |
| `git config --local user.name "Name"` | Sets the local Git username for commits. |
| `git config --system user.name "Name"` | Sets the system Git username for commits. |
| `git config --global core.editor "editor"` | Sets the global Git editor. |
| `git config --global core.pager "pager"` | Sets the global Git pager. |
| `git config --global init.defaultBranch main` | Sets the default branch name for new repositories. |
| `git config --global color.ui true` | Enables colored output. |
| `git config --global color.ui auto` | Auto-detects colored output support. |
| `git config --global color.ui never` | Disables colored output. |
| `git config --global alias.co checkout` | Creates a Git alias for checkout. |
| `git config --global alias.ci commit` | Creates a Git alias for commit. |
| `git config --global alias.br branch` | Creates a Git alias for branch. |
| `git config --global alias.st status` | Creates a Git alias for status. |
| `git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"` | Creates a custom log alias. |
| `git config --global core.autocrlf input` | Sets the line ending conversion to input. |
| `git config --global core.autocrlf output` | Sets the line ending conversion to output. |
| `git config --global core.autocrlf true` | Sets the line ending conversion to true. |
| `git config --global core.safecrlf true` | Enables safe CRLF handling. |
| `git config --global core.safecrlf false` | Disables safe CRLF handling. |
| `git config --global core.safecrlf warn` | Warns about CRLF line endings. |
| `git config --global core.fileMode true` | Enables file mode changes. |
| `git config --global core.fileMode false` | Disables file mode changes. |
| `git config --global core.symlinks true` | Enables symbolic links. |
| `git config --global core.symlinks false` | Disables symbolic links. |
| `git config --global core.ignorecase true` | Enables case-insensitive file system support. |
| `git config --global core.ignorecase false` | Disables case-insensitive file system support. |
| `git config --global core.trustctime false` | Disables trust of file modification times. |
| `git config --global core.preloadindex true` | Enables preloading of the index. |
| `git config --global gc.auto 6700` | Sets the auto garbage collection threshold. |
| `git config --global gc.pruneExpire now` | Sets the garbage collection prune expiration time. |
| `git config --global fetch.prune true` | Enables automatic pruning during fetch. |
| `git config --global pull.rebase true` | Enables rebase for pull operations. |
| `git config --global pull.ff only` | Sets pull to fast-forward only. |
| `git config --global rebase.autoStash true` | Enables automatic stashing during rebase. |
| `git config --global merge.ff only` | Sets merge to fast-forward only. |
| `git config --global merge.tool vimdiff` | Sets the merge tool to vimdiff. |
| `git config --global mergetool.vimdiff.path "vimdiff"` | Sets the path for the vimdiff merge tool. |
| `git config --global diff.tool vimdiff` | Sets the diff tool to vimdiff. |
| `git config --global difftool.vimdiff.path "vimdiff"` | Sets the path for the vimdiff diff tool. |
| `git config --global credential.helper cache` | Sets the credential helper to cache. |
| `git config --global credential.helper "cache --timeout=3600"` | Sets the credential helper to cache with a timeout. |
| `git config --global credential.helper store` | Sets the credential helper to store. |
| `git config --global credential.helper osxkeychain` | Sets the credential helper to OSX Keychain. |
| `git config --global credential.helper libsecret` | Sets the credential helper to libsecret. |
| `git config --global credential.helper manager` | Sets the credential helper to manager. |
| `git config --global credential.helper wincred` | Sets the credential helper to Windows Credential Manager. |
| `git config --list` | Lists all Git configuration settings. |
| `git config --global --list` | Lists all global Git configuration settings. |
| `git config --local --list` | Lists all local Git configuration settings. |
| `git config --system --list` | Lists all system Git configuration settings. |
| `git config --get user.name` | Gets the value of a specific configuration setting. |
| `git config --get-regexp "user\..*"` | Gets all configuration settings matching a regex. |
| `git config --get-all user.name` | Gets all values for a configuration setting. |
| `git config --unset user.name` | Unsets a Git configuration setting. |
| `git config --global --unset user.name` | Unsets a global Git configuration setting. |
| `git config --local --unset user.name` | Unsets a local Git configuration setting. |
| `git config --system --unset user.name` | Unsets a system Git configuration setting. |
| `git config --replace-all user.name "New Name"` | Replaces all values for a configuration setting. |
| `git config --global --replace-all user.name "New Name"` | Replaces all global values for a configuration setting. |
| `git config --rename-section old_name new_name` | Renames a configuration section. |
| `git config --remove-section section_name` | Removes a configuration section. |

---
## Basic Git Workflow

| Code | Description |
|------|-------------|
| `git status` | Shows the working tree status. |
| `git status -s` | Shows the working tree status in short format. |
| `git status -sb` | Shows the working tree status with branch information. |
| `git status --short` | Shows the working tree status in short format. |
| `git status --branch` | Shows the working tree status with branch information. |
| `git status --porcelain` | Shows the working tree status in a machine-readable format. |
| `git status --porcelain=1` | Shows the working tree status in porcelain v1 format. |
| `git status --porcelain=2` | Shows the working tree status in porcelain v2 format. |
| `git status --ignored` | Shows ignored files in the status output. |
| `git status --no-ignored` | Hides ignored files in the status output. |
| `git status --ignored=matching` | Shows ignored files matching patterns. |
| `git status --ignored=traditional` | Shows ignored files using traditional ignore rules. |
| `git status --untracked-files` | Shows untracked files in the status output. |
| `git status --untracked-files=normal` | Shows untracked files using normal mode. |
| `git status --untracked-files=all` | Shows all untracked files. |
| `git status --untracked-files=no` | Hides untracked files in the status output. |
| `git status --column` | Shows the status output in columns. |
| `git status --no-column` | Shows the status output without columns. |
| `git status --ahead-behind` | Shows the ahead/behind count in the status output. |
| `git status --no-ahead-behind` | Hides the ahead/behind count in the status output. |
| `git status --renames` | Detects renames in the status output. |
| `git status --no-renames` | Disables rename detection in the status output. |
| `git status --find-renames` | Forces rename detection in the status output. |
| `git add file1 file2` | Stages specified files for commit. |
| `git add .` | Stages all modified and new files in the current directory and subdirectories. |
| `git add -A` | Stages all modified, new, and deleted files. |
| `git add -u` | Stages all modified and deleted files (but not new files). |
| `git add --all` | Stages all files (same as -A). |
| `git add --patch` | Interactively stages hunks of files. |
| `git add --interactive` | Interactively stages files. |
| `git add -i` | Interactively stages files. |
| `git add -p` | Interactively stages hunks of files. |
| `git add -N file` | Stages a file without adding its content (for empty files). |
| `git add --intent-to-add file` | Stages a file without adding its content (same as -N). |
| `git add --renormalize .` | Re-normalizes line endings for all files. |
| `git add --refresh` | Refreshes the staged files. |
| `git add --ignore-errors` | Ignores errors when staging files. |
| `git add --ignore-missing` | Ignores missing files when staging. |
| `git add --sparse` | Stages files in a sparse checkout. |
| `git add --no-warn-embedded-repo` | Disables warnings about embedded repositories. |
| `git add --chmod=+x file` | Stages a file and marks it as executable. |
| `git add --chmod=-x file` | Stages a file and marks it as non-executable. |
| `git reset` | Resets the current HEAD to the specified state. |
| `git reset --soft HEAD~1` | Soft reset to the previous commit (keeps changes staged). |
| `git reset --mixed HEAD~1` | Mixed reset to the previous commit (keeps changes unstaged). Default mode. |
| `git reset --hard HEAD~1` | Hard reset to the previous commit (discards all changes). |
| `git reset --merge HEAD~1` | Merge reset to the previous commit (discards unstaged changes). |
| `git reset --keep HEAD~1` | Keep reset to the previous commit (keeps local changes). |
| `git reset HEAD file` | Unstages a file. |
| `git reset -- file1 file2` | Unstages specified files. |
| `git reset --patch` | Interactively unstages hunks of files. |
| `git reset --interactive` | Interactively unstages files. |
| `git reset -p` | Interactively unstages hunks of files. |
| `git reset --recurse-submodules` | Resets submodules. |
| `git reset --no-recurse-submodules` | Resets without affecting submodules. |
| `git commit` | Commits staged changes. |
| `git commit -m "message"` | Commits staged changes with a message. |
| `git commit -a -m "message"` | Stages all modified files and commits with a message. |
| `git commit --amend` | Amends the most recent commit. |
| `git commit --amend --no-edit` | Amends the most recent commit without editing the message. |
| `git commit --amend -m "New message"` | Amends the most recent commit with a new message. |
| `git commit --allow-empty` | Creates an empty commit. |
| `git commit --allow-empty-message` | Allows an empty commit message. |
| `git commit --author="Name <email@example.com>" -m "message"` | Commits with a custom author. |
| `git commit --date="2023-01-01T00:00:00" -m "message"` | Commits with a custom date. |
| `git commit --no-verify` | Commits without running pre-commit hooks. |
| `git commit --no-gpg-sign` | Commits without a GPG signature. |
| `git commit --gpg-sign` | Commits with a GPG signature. |
| `git commit --gpg-sign=key-id` | Commits with a GPG signature using a specific key. |
| `git commit --signoff` | Commits with a sign-off. |
| `git commit --no-signoff` | Commits without a sign-off. |
| `git commit --file file` | Commits with a message from a file. |
| `git commit --template file` | Commits with a message template from a file. |
| `git commit --cleanup=default` | Commits with default message cleanup. |
| `git commit --cleanup=strip` | Commits with strip message cleanup. |
| `git commit --cleanup=whitespace` | Commits with whitespace message cleanup. |
| `git commit --cleanup=verbatim` | Commits with verbatim message cleanup. |
| `git commit --status` | Includes the status output in the commit message. |
| `git commit --no-status` | Excludes the status output from the commit message. |
| `git commit --verbose` | Commits with verbose output. |
| `git commit --quiet` | Commits without output. |
| `git rm file1 file2` | Removes files from the working tree and stages the deletion. |
| `git rm -r directory` | Recursively removes a directory and stages the deletion. |
| `git rm --cached file` | Removes a file from the staging area but keeps it in the working tree. |
| `git rm --ignore-unmatch file` | Ignores files that do not exist when removing. |
| `git rm -f file` | Force removes a file. |
| `git rm -n file` | Dry-run removal of a file (shows what would happen). |
| `git rm -v file` | Verbosely removes a file. |
| `git rm --quiet file` | Removes a file without output. |
| `git mv old new` | Renames or moves a file and stages the change. |
| `git mv -n old new` | Dry-run rename or move (shows what would happen). |
| `git mv -v old new` | Verbosely renames or moves a file. |
| `git mv -f old new` | Force renames or moves a file. |
| `git mv --dry-run old new` | Dry-run rename or move (shows what would happen). |

---
## Branching

| Code | Description |
|------|-------------|
| `git branch` | Lists all branches. |
| `git branch -r` | Lists all remote branches. |
| `git branch -a` | Lists all local and remote branches. |
| `git branch -v` | Lists branches with their associated commit messages. |
| `git branch -vv` | Lists branches with their associated commit messages and remote tracking branches. |
| `git branch --list` | Lists all branches. |
| `git branch --list "pattern*"` | Lists branches matching a pattern. |
| `git branch --contains commit` | Lists branches that contain a specific commit. |
| `git branch --merged` | Lists branches that have been merged into the current branch. |
| `git branch --merged branch` | Lists branches that have been merged into a specific branch. |
| `git branch --no-merged` | Lists branches that have not been merged into the current branch. |
| `git branch --no-merged branch` | Lists branches that have not been merged into a specific branch. |
| `git branch --show-current` | Shows the current branch name. |
| `git branch --remote` | Lists remote branches. |
| `git branch --all --format="%(refname:short)"` | Lists all branches with a custom format. |
| `git branch branch_name` | Creates a new branch. |
| `git branch branch_name commit` | Creates a new branch at a specific commit. |
| `git branch -f branch_name commit` | Force creates a new branch at a specific commit. |
| `git branch -d branch_name` | Deletes a branch. |
| `git branch -D branch_name` | Force deletes a branch. |
| `git branch -m old_name new_name` | Renames a branch. |
| `git branch -M old_name new_name` | Force renames a branch. |
| `git branch -c branch_name` | Creates a new branch and checks it out. |
| `git branch -C branch_name` | Creates or resets a branch and checks it out. |
| `git branch --set-upstream-to=origin/branch` | Sets the upstream branch for the current branch. |
| `git branch --unset-upstream` | Unsets the upstream branch for the current branch. |
| `git branch --edit-description` | Edits the description of the current branch. |
| `git branch --no-edit-description` | Does not edit the description of the current branch. |
| `git checkout branch_name` | Switches to a branch. |
| `git checkout -b branch_name` | Creates a new branch and switches to it. |
| `git checkout -b branch_name commit` | Creates a new branch at a specific commit and switches to it. |
| `git checkout -B branch_name` | Creates or resets a branch and switches to it. |
| `git checkout --track origin/branch` | Creates a new branch that tracks a remote branch. |
| `git checkout --no-track origin/branch` | Creates a new branch without tracking a remote branch. |
| `git checkout -` | Switches to the previous branch. |
| `git checkout --detach` | Detaches HEAD at the current commit. |
| `git checkout commit` | Detaches HEAD at a specific commit. |
| `git checkout --ours file` | Checks out the local version of a file. |
| `git checkout --theirs file` | Checks out the remote version of a file. |
| `git checkout --patch` | Interactively checks out changes. |
| `git checkout --ignore-other-worktrees` | Ignores other worktrees when checking out. |
| `git checkout --recurse-submodules` | Checks out submodules. |
| `git checkout --no-recurse-submodules` | Checks out without affecting submodules. |
| `git switch branch_name` | Switches to a branch. |
| `git switch -c branch_name` | Creates a new branch and switches to it. |
| `git switch -C branch_name` | Creates or resets a branch and switches to it. |
| `git switch --detach` | Detaches HEAD at the current commit. |
| `git switch --detach commit` | Detaches HEAD at a specific commit. |
| `git switch --discard-changes` | Discards local changes when switching branches. |
| `git switch --merge` | Merges local changes when switching branches. |
| `git switch --no-guess` | Disables guessing the branch name. |
| `git switch --guess` | Enables guessing the branch name. |
| `git switch --no-track` | Switches without setting upstream. |
| `git restore file` | Restores a file in the working tree. |
| `git restore --staged file` | Restores a staged file. |
| `git restore --worktree file` | Restores a file in the working tree. |
| `git restore --source=HEAD file` | Restores a file from HEAD. |
| `git restore --source=commit file` | Restores a file from a specific commit. |
| `git restore --patch` | Interactively restores changes. |
| `git restore --ignore-unmatch` | Ignores files that do not exist when restoring. |
| `git restore --recurse-submodules` | Restores submodules. |
| `git restore --no-recurse-submodules` | Restores without affecting submodules. |

---
## Merging and Rebasing

| Code | Description |
|------|-------------|
| `git merge branch_name` | Merges a branch into the current branch. |
| `git merge --no-ff branch_name` | Merges a branch without fast-forwarding. |
| `git merge --ff-only branch_name` | Merges a branch only if it can be fast-forwarded. |
| `git merge --squash branch_name` | Merges a branch and squashes the commits into one. |
| `git merge --no-commit branch_name` | Merges a branch but does not commit. |
| `git merge --no-squash branch_name` | Merges a branch without squashing. |
| `git merge --commit branch_name` | Merges a branch and commits automatically. |
| `git merge --stat branch_name` | Merges a branch and shows file statistics. |
| `git merge --no-stat branch_name` | Merges a branch without showing file statistics. |
| `git merge --summary branch_name` | Merges a branch and shows a summary. |
| `git merge --no-summary branch_name` | Merges a branch without showing a summary. |
| `git merge --abort` | Aborts the current merge. |
| `git merge --continue` | Continues the current merge after resolving conflicts. |
| `git merge --quiet` | Merges with quiet output. |
| `git merge --verbose` | Merges with verbose output. |
| `git merge --progress` | Merges with progress output. |
| `git merge --no-progress` | Merges without progress output. |
| `git merge -Xours` | Merges with a strategy option to prefer our changes. |
| `git merge -Xtheirs` | Merges with a strategy option to prefer their changes. |
| `git merge -Xignore-all-space` | Merges while ignoring whitespace changes. |
| `git merge -Xignore-space-change` | Merges while ignoring changes in the amount of whitespace. |
| `git merge -Xrename-threshold=50` | Merges with a rename threshold. |
| `git merge --strategy=ours branch_name` | Merges using the ours strategy. |
| `git merge --strategy=theirs branch_name` | Merges using the theirs strategy. |
| `git merge --strategy=octopus branch1 branch2 branch3` | Merges using the octopus strategy. |
| `git merge --strategy=resolve branch_name` | Merges using the resolve strategy. |
| `git merge --strategy=recursive branch_name` | Merges using the recursive strategy. |
| `git merge-file file1 file2 file3` | Performs a three-way merge of files. |
| `git merge-file -p file1 file2 file3` | Performs a three-way merge of files with a custom marker. |
| `git merge-file --marker-size=7 file1 file2 file3` | Performs a three-way merge of files with a custom marker size. |
| `git mergetool` | Runs merge conflict resolution tools to resolve merge conflicts. |
| `git mergetool --tool-help` | Shows a list of available merge tools. |
| `git mergetool -y` | Runs mergetool without prompting. |
| `git mergetool --no-prompt` | Runs mergetool without prompting. |
| `git mergetool -t vimdiff` | Runs mergetool with a specific tool. |
| `git mergetool --tool=vimdiff` | Runs mergetool with a specific tool. |
| `git mergetool -g` | Runs mergetool with a GUI tool. |
| `git mergetool --gui` | Runs mergetool with a GUI tool. |
| `git mergetool --no-gui` | Runs mergetool without a GUI tool. |
| `git mergetool --prompt` | Runs mergetool with prompting. |
| `git mergetool --write` | Runs mergetool and writes the result to the working tree. |
| `git mergetool --no-write` | Runs mergetool without writing the result to the working tree. |
| `git rebase branch_name` | Rebases the current branch onto another branch. |
| `git rebase -i branch_name` | Interactively rebases the current branch. |
| `git rebase -i HEAD~3` | Interactively rebases the last 3 commits. |
| `git rebase -i commit` | Interactively rebases onto a specific commit. |
| `git rebase --continue` | Continues the current rebase after resolving conflicts. |
| `git rebase --abort` | Aborts the current rebase. |
| `git rebase --skip` | Skips the current commit during rebase. |
| `git rebase --edit-todo` | Edits the rebase todo list. |
| `git rebase --onto new_base branch_name` | Rebases onto a new base. |
| `git rebase --onto new_base commit` | Rebases a range of commits onto a new base. |
| `git rebase --root` | Rebases all commits onto the new base. |
| `git rebase --autostash` | Automatically stashes and applies changes during rebase. |
| `git rebase --no-autostash` | Disables automatic stashing during rebase. |
| `git rebase --committer-date-is-author-date` | Uses the author date as the committer date. |
| `git rebase --ignore-whitespace` | Rebases while ignoring whitespace changes. |
| `git rebase -Xours` | Rebases with a strategy option to prefer our changes. |
| `git rebase -Xtheirs` | Rebases with a strategy option to prefer their changes. |
| `git rebase --keep-empty` | Keeps empty commits during rebase. |
| `git rebase --no-keep-empty` | Removes empty commits during rebase. |
| `git rebase --empty=drop` | Drops empty commits during rebase. |
| `git rebase --empty=keep` | Keeps empty commits during rebase. |
| `git rebase --empty=ask` | Asks what to do with empty commits during rebase. |
| `git rebase --rebase-merges` | Rebases merge commits. |
| `git rebase --no-rebase-merges` | Does not rebase merge commits. |
| `git cherry-pick commit` | Applies the changes from a specific commit. |
| `git cherry-pick -n commit` | Applies the changes from a commit without committing. |
| `git cherry-pick --abort` | Aborts the current cherry-pick. |
| `git cherry-pick --continue` | Continues the current cherry-pick after resolving conflicts. |
| `git cherry-pick --skip` | Skips the current commit during cherry-pick. |
| `git cherry-pick -Xours commit` | Cherry-picks with a strategy option to prefer our changes. |
| `git cherry-pick -Xtheirs commit` | Cherry-picks with a strategy option to prefer their changes. |
| `git cherry-pick --no-commit commit` | Cherry-picks without committing. |
| `git cherry-pick --edit commit` | Cherry-picks and edits the commit message. |
| `git cherry-pick --no-edit commit` | Cherry-picks without editing the commit message. |
| `git cherry-pick --signoff commit` | Cherry-picks with a sign-off. |
| `git cherry-pick --ff commit` | Cherry-picks with fast-forward. |
| `git cherry-pick --allow-empty commit` | Cherry-picks and allows empty commits. |
| `git cherry-pick --keep-redundant-commits commit` | Cherry-picks and keeps redundant commits. |
| `git cherry-pick --mainline parent-number commit` | Cherry-picks a merge commit with a specific parent. |
| `git revert commit` | Creates a new commit that undoes the changes from a specific commit. |
| `git revert --no-commit commit` | Reverts without committing. |
| `git revert --abort` | Aborts the current revert. |
| `git revert --continue` | Continues the current revert. |
| `git revert -n commit1..commit2` | Reverts a range of commits. |
| `git revert --no-ff` | Reverts without fast-forwarding. |
| `git revert --edit` | Reverts and edits the commit message. |
| `git revert --no-edit` | Reverts without editing the commit message. |
| `git revert --signoff` | Reverts with a sign-off. |
| `git revert --gpg-sign` | Reverts with a GPG signature. |

---
## Remote Operations

| Code | Description |
|------|-------------|
| `git remote` | Lists all remote repositories. |
| `git remote -v` | Lists all remote repositories with their URLs. |
| `git remote show origin` | Shows information about a remote repository. |
| `git remote show -n origin` | Shows information about a remote repository without contacting it. |
| `git remote add origin url` | Adds a new remote repository. |
| `git remote add --fetch origin url` | Adds a new remote repository and fetches it. |
| `git remote add --push origin url` | Adds a new remote repository with a push URL. |
| `git remote add --fetch origin url --push-url push_url` | Adds a new remote with separate fetch and push URLs. |
| `git remote add --track branch origin url` | Adds a new remote and tracks a branch. |
| `git remote add --no-track branch origin url` | Adds a new remote without tracking a branch. |
| `git remote rename old new` | Renames a remote repository. |
| `git remote remove origin` | Removes a remote repository. |
| `git remote rm origin` | Removes a remote repository (alias). |
| `git remote set-url origin new_url` | Changes the URL of a remote repository. |
| `git remote set-url --push origin push_url` | Changes the push URL of a remote repository. |
| `git remote set-url --add origin new_url` | Adds a new URL to a remote repository. |
| `git remote set-url --delete origin url` | Deletes a URL from a remote repository. |
| `git remote set-head origin -a` | Sets the default branch for a remote repository. |
| `git remote set-head origin --delete` | Deletes the default branch for a remote repository. |
| `git remote set-branches origin branch1 branch2` | Sets the branches to track for a remote repository. |
| `git remote set-branches --add origin branch` | Adds a branch to track for a remote repository. |
| `git remote set-branches --delete origin branch` | Deletes a branch to track for a remote repository. |
| `git remote get-url origin` | Gets the URL of a remote repository. |
| `git remote get-url --push origin` | Gets the push URL of a remote repository. |
| `git remote get-url --all origin` | Gets all URLs of a remote repository. |
| `git remote prune origin` | Prunes stale remote-tracking branches. |
| `git remote prune -n origin` | Dry-run pruning of stale remote-tracking branches. |
| `git remote prune -v origin` | Verbosely prunes stale remote-tracking branches. |
| `git remote update` | Fetches updates from all remotes. |
| `git remote update origin` | Fetches updates from a specific remote. |
| `git remote update --prune` | Fetches updates and prunes stale branches. |
| `git fetch` | Downloads objects and refs from another repository. |
| `git fetch origin` | Downloads objects and refs from the origin remote. |
| `git fetch --all` | Downloads objects and refs from all remotes. |
| `git fetch --prune` | Prunes stale remote-tracking references after fetching. |
| `git fetch --prune --all` | Prunes stale references for all remotes after fetching. |
| `git fetch --dry-run` | Performs a dry-run fetch. |
| `git fetch --no-tags` | Fetches without downloading tags. |
| `git fetch --tags` | Fetches only tags. |
| `git fetch --force` | Forces the fetch to overwrite local references. |
| `git fetch --unshallow` | Converts a shallow repository to a complete one. |
| `git fetch --depth=1` | Fetches with a depth limit of 1. |
| `git fetch --update-head-ok` | Allows updating HEAD during fetch. |
| `git fetch --no-recurse-submodules` | Fetches without updating submodules. |
| `git fetch --recurse-submodules` | Fetches and updates submodules. |
| `git fetch --recurse-submodules=yes` | Fetches and updates all submodules. |
| `git fetch --recurse-submodules=no` | Fetches without updating submodules. |
| `git fetch --recurse-submodules=on-demand` | Fetches and updates submodules on demand. |
| `git fetch --jobs=4` | Fetches with 4 parallel jobs. |
| `git fetch --no-jobs` | Fetches without parallel jobs. |
| `git pull` | Fetches from and integrates with another repository or a local branch. |
| `git pull origin branch` | Pulls from a specific remote and branch. |
| `git pull --rebase` | Pulls and rebases the current branch on top of the fetched branch. |
| `git pull --no-rebase` | Pulls without rebasing. |
| `git pull --ff-only` | Pulls only if it can be fast-forwarded. |
| `git pull --squash` | Pulls and squashes the commits into one. |
| `git pull --no-commit` | Pulls but does not commit. |
| `git pull --autostash` | Automatically stashes and applies changes during pull. |
| `git pull --no-autostash` | Disables automatic stashing during pull. |
| `git pull --recurse-submodules` | Pulls and updates submodules. |
| `git pull --recurse-submodules=no` | Pulls without updating submodules. |
| `git pull --recurse-submodules=yes` | Pulls and updates all submodules. |
| `git pull --recurse-submodules=on-demand` | Pulls and updates submodules on demand. |
| `git pull --no-recurse-submodules` | Pulls without updating submodules. |
| `git pull --allow-unrelated-histories` | Allows pulling from unrelated histories. |
| `git pull --no-allow-unrelated-histories` | Disallows pulling from unrelated histories. |
| `git pull --verbose` | Pulls with verbose output. |
| `git pull --quiet` | Pulls without output. |
| `git pull --progress` | Pulls with progress output. |
| `git pull --no-progress` | Pulls without progress output. |
| `git push` | Updates remote refs along with associated objects. |
| `git push origin branch` | Pushes to a specific remote and branch. |
| `git push -u origin branch` | Pushes to a remote branch and sets upstream. |
| `git push --set-upstream origin branch` | Pushes to a remote branch and sets upstream (alias). |
| `git push --all` | Pushes all branches. |
| `git push --tags` | Pushes all tags. |
| `git push --force` | Force pushes. |
| `git push --force-with-lease` | Force pushes with a lease check. |
| `git push --force-if-includes` | Force pushes if the remote ref is an ancestor of the local ref. |
| `git push --dry-run` | Performs a dry-run push. |
| `git push --no-thin` | Pushes without using thin pack. |
| `git push --thin` | Pushes using thin pack. |
| `git push --prune` | Prunes stale remote-tracking references. |
| `git push --no-prune` | Pushes without pruning. |
| `git push --delete origin branch` | Deletes a remote branch. |
| `git push --delete origin tag` | Deletes a remote tag. |
| `git push --follow-tags` | Pushes only tags that are ancestors of pushed commits. |
| `git push --no-follow-tags` | Pushes without following tags. |
| `git push --atomic` | Pushes all refs as a single atomic transaction. |
| `git push --no-atomic` | Pushes refs as individual transactions. |
| `git push --recurse-submodules=check` | Pushes and checks submodules. |
| `git push --recurse-submodules=on-demand` | Pushes and updates submodules on demand. |
| `git push --recurse-submodules=yes` | Pushes and updates all submodules. |
| `git push --recurse-submodules=no` | Pushes without updating submodules. |
| `git push --verbose` | Pushes with verbose output. |
| `git push --quiet` | Pushes without output. |
| `git push --progress` | Pushes with progress output. |
| `git push --no-progress` | Pushes without progress output. |

---
## Inspection and Comparison

| Code | Description |
|------|-------------|
| `git log` | Shows the commit logs. |
| `git log -n 10` | Shows the last 10 commits. |
| `git log -10` | Shows the last 10 commits. |
| `git log --oneline` | Shows the commit logs in a compact one-line format. |
| `git log --graph` | Shows the commit logs with a graph. |
| `git log --decorate` | Shows the commit logs with branch and tag decorations. |
| `git log --all` | Shows the commit logs for all branches. |
| `git log --author="Name"` | Shows the commit logs for a specific author. |
| `git log --grep="pattern"` | Shows the commit logs matching a pattern. |
| `git log --grep="pattern" --invert-grep` | Shows the commit logs not matching a pattern. |
| `git log --since="2023-01-01"` | Shows the commit logs since a specific date. |
| `git log --until="2023-01-01"` | Shows the commit logs until a specific date. |
| `git log --before="2023-01-01"` | Shows the commit logs before a specific date. |
| `git log --after="2023-01-01"` | Shows the commit logs after a specific date. |
| `git log --before="1 week ago"` | Shows the commit logs before 1 week ago. |
| `git log --after="1 week ago"` | Shows the commit logs after 1 week ago. |
| `git log --stat` | Shows the commit logs with file statistics. |
| `git log --name-status` | Shows the commit logs with file status. |
| `git log --name-only` | Shows the commit logs with file names only. |
| `git log --patch` | Shows the commit logs with patches. |
| `git log --patch-with-stat` | Shows the commit logs with patches and statistics. |
| `git log --word-diff` | Shows the commit logs with word diff. |
| `git log --word-diff=color` | Shows the commit logs with colored word diff. |
| `git log --word-diff=porcelain` | Shows the commit logs with porcelain word diff. |
| `git log --follow file` | Shows the commit logs for a file, including renames. |
| `git log --all --full-history -- file` | Shows the full history for a file. |
| `git log --pretty=format:"%h - %an, %ar : %s"` | Shows the commit logs with a custom format. |
| `git log --pretty=fuller` | Shows the commit logs with a fuller format. |
| `git log --abbrev-commit` | Shows the commit logs with abbreviated commit hashes. |
| `git log --relative-date` | Shows the commit logs with relative dates. |
| `git log --date=short` | Shows the commit logs with short dates. |
| `git log --date=local` | Shows the commit logs with local dates. |
| `git log --date=iso` | Shows the commit logs with ISO dates. |
| `git log --date=rfc` | Shows the commit logs with RFC dates. |
| `git log --date=unix` | Shows the commit logs with Unix timestamps. |
| `git log --date=human` | Shows the commit logs with human-readable dates. |
| `git log --parents` | Shows the commit logs with parent information. |
| `git log --children` | Shows the commit logs with child information. |
| `git log --left-right` | Shows the commit logs with left/right information. |
| `git log --cherry-pick` | Shows the commit logs with cherry-pick information. |
| `git log --cherry-mark` | Shows the commit logs with cherry-mark information. |
| `git log --cherry` | Shows the commit logs with cherry information. |
| `git log --left-only` | Shows the commit logs for commits only in the left branch. |
| `git log --right-only` | Shows the commit logs for commits only in the right branch. |
| `git log --merges` | Shows the commit logs for merge commits only. |
| `git log --no-merges` | Shows the commit logs excluding merge commits. |
| `git log --first-parent` | Shows the commit logs following only the first parent. |
| `git log --no-walk` | Shows the commit logs without walking the commit history. |
| `git log --do-walk` | Shows the commit logs with walking the commit history. |
| `git log --simplify-merges` | Simplifies merge commits in the commit logs. |
| `git log --simplify-by-decoration` | Simplifies the commit logs by decoration. |
| `git log --full-history` | Shows the full history in the commit logs. |
| `git log --dense` | Shows a dense history in the commit logs. |
| `git log --sparse` | Shows a sparse history in the commit logs. |
| `git log --simplify-empty` | Simplifies empty commits in the commit logs. |
| `git log --all-match` | Shows commits that match all --grep patterns. |
| `git log --invert-grep` | Shows commits that do not match --grep patterns. |
| `git log --basic-regexp="pattern"` | Uses basic regex for --grep. |
| `git log --extended-regexp="pattern"` | Uses extended regex for --grep. |
| `git log --fixed-strings="pattern"` | Uses fixed strings for --grep. |
| `git log --perl-regexp="pattern"` | Uses Perl regex for --grep. |
| `git log --regexp-ignore-case="pattern"` | Uses case-insensitive regex for --grep. |
| `git log --all --grep="pattern"` | Searches all branches for commits matching a pattern. |
| `git show` | Shows objects (commits, tags, trees, blobs). |
| `git show commit` | Shows a commit. |
| `git show commit:file` | Shows a file from a commit. |
| `git show --stat` | Shows a commit with file statistics. |
| `git show --name-only` | Shows a commit with file names only. |
| `git show --name-status` | Shows a commit with file status. |
| `git show --patch` | Shows a commit with patches. |
| `git show --format=fuller` | Shows a commit with a fuller format. |
| `git show --abbrev-commit` | Shows a commit with an abbreviated hash. |
| `git show HEAD` | Shows the latest commit. |
| `git show HEAD:file` | Shows a file from the latest commit. |
| `git show --text` | Shows a blob as plain text. |
| `git show --no-text` | Shows a blob without text conversion. |
| `git show --binary` | Shows a blob as binary. |
| `git show --no-binary` | Shows a blob without binary conversion. |
| `git diff` | Shows changes between commits, commit and working tree, etc. |
| `git diff --cached` | Shows staged changes. |
| `git diff --staged` | Shows staged changes (alias). |
| `git diff HEAD` | Shows changes between HEAD and working tree. |
| `git diff HEAD~1` | Shows changes between HEAD~1 and working tree. |
| `git diff commit1 commit2` | Shows changes between two commits. |
| `git diff --stat` | Shows changes with file statistics. |
| `git diff --name-only` | Shows changes with file names only. |
| `git diff --name-status` | Shows changes with file status. |
| `git diff --color` | Shows changes with colors. |
| `git diff --color-words` | Shows changes with colored words. |
| `git diff --word-diff` | Shows changes with word diff. |
| `git diff --word-diff=color` | Shows changes with colored word diff. |
| `git diff --word-diff=porcelain` | Shows changes with porcelain word diff. |
| `git diff --word-diff-regex=.` | Shows changes with word diff using a custom regex. |
| `git diff --unified=5` | Shows changes with 5 lines of context. |
| `git diff -U5` | Shows changes with 5 lines of context (short form). |
| `git diff --patch-with-stat` | Shows changes with patches and statistics. |
| `git diff --reverse` | Shows changes in reverse. |
| `git diff --no-prefix` | Shows changes without source/destination prefixes. |
| `git diff --src-prefix=a/` | Shows changes with a custom source prefix. |
| `git diff --dst-prefix=b/` | Shows changes with a custom destination prefix. |
| `git diff --no-ext-diff` | Disables external diff tools. |
| `git diff --binary` | Shows changes in binary files. |
| `git diff --ignore-cr-at-eol` | Shows changes while ignoring carriage returns at end of line. |
| `git diff --ignore-space-at-eol` | Shows changes while ignoring spaces at end of line. |
| `git diff --ignore-space-change` | Shows changes while ignoring changes in the amount of whitespace. |
| `git diff --ignore-all-space` | Shows changes while ignoring all whitespace. |
| `git diff --ignore-blank-lines` | Shows changes while ignoring blank lines. |
| `git diff --indent-heuristic` | Uses an indent heuristic for diff. |
| `git diff --no-indent-heuristic` | Disables the indent heuristic for diff. |
| `git diff --patience` | Uses the patience diff algorithm. |
| `git diff --histogram` | Uses the histogram diff algorithm. |
| `git diff --minimal` | Uses the minimal diff algorithm. |
| `git diff --diff-algorithm=algorithm` | Uses a custom diff algorithm. |
| `git difftool` | Shows changes using an external diff tool. |
| `git difftool --tool-help` | Shows a list of available diff tools. |
| `git difftool -y` | Runs difftool without prompting. |
| `git difftool --no-prompt` | Runs difftool without prompting. |
| `git difftool -t vimdiff` | Runs difftool with a specific tool. |
| `git difftool --tool=vimdiff` | Runs difftool with a specific tool. |
| `git difftool --cached` | Shows staged changes using an external diff tool. |
| `git difftool HEAD` | Shows changes between HEAD and working tree using an external diff tool. |
| `git difftool commit1 commit2` | Shows changes between two commits using an external diff tool. |
| `git difftool --dir-diff` | Runs difftool in directory diff mode. |
| `git difftool --no-dir-diff` | Disables directory diff mode. |
| `git difftool --symlinks` | Uses symlinks for difftool. |
| `git difftool --no-symlinks` | Disables symlinks for difftool. |
| `git difftool --trust-exit-code` | Trusts the exit code from difftool. |
| `git difftool --no-trust-exit-code` | Does not trust the exit code from difftool. |

---
## Tagging

| Code | Description |
|------|-------------|
| `git tag` | Lists all tags. |
| `git tag -l` | Lists all tags. |
| `git tag -l "v1.*"` | Lists tags matching a pattern. |
| `git tag -l --sort=-creatordate` | Lists tags sorted by creation date (newest first). |
| `git tag -l --sort=-taggerdate` | Lists tags sorted by tagger date (newest first). |
| `git tag -l --sort=-version:refname` | Lists tags sorted by version. |
| `git tag -l --sort=refname` | Lists tags sorted by refname. |
| `git tag -l --sort=taggerdate` | Lists tags sorted by tagger date. |
| `git tag -l --sort=creatordate` | Lists tags sorted by creation date. |
| `git tag light` | Creates a lightweight tag. |
| `git tag -a tag_name` | Creates an annotated tag. |
| `git tag -a tag_name -m "message"` | Creates an annotated tag with a message. |
| `git tag -a tag_name commit` | Creates an annotated tag at a specific commit. |
| `git tag -s tag_name -m "message"` | Creates a signed tag with a message. |
| `git tag -u GPG_KEY -s tag_name -m "message"` | Creates a signed tag with a specific GPG key. |
| `git tag -u GPG_KEY tag_name -m "message"` | Creates a signed tag with a specific GPG key (short form). |
| `git tag -d tag_name` | Deletes a tag. |
| `git tag -D tag_name` | Force deletes a tag. |
| `git show tag_name` | Shows a tag. |
| `git show tag_name:file` | Shows a file from a tag. |
| `git describe` | Shows the most recent tag reachable from a commit. |
| `git describe --tags` | Shows the most recent tag reachable from a commit, considering all tags. |
| `git describe --abbrev=0` | Shows the most recent tag reachable from a commit with full hash. |
| `git describe --long` | Shows the most recent tag reachable from a commit with long format. |
| `git describe --all` | Shows the most recent tag reachable from a commit, considering all refs. |
| `git describe --exact-match` | Shows the most recent tag that matches the commit exactly. |
| `git describe --dirty` | Shows the most recent tag with a dirty suffix if there are changes. |
| `git describe --broken` | Shows the most recent tag even if it is broken. |
| `git describe --contains` | Shows the most recent tag that contains the commit. |
| `git describe --no-contains` | Shows the most recent tag without checking if it contains the commit. |
| `git verify-tag tag_name` | Verifies the GPG signature of a tag. |
| `git verify-tag --verbose tag_name` | Verifies the GPG signature of a tag with verbose output. |
| `git push origin tag_name` | Pushes a tag to a remote. |
| `git push origin --tags` | Pushes all tags to a remote. |
| `git push --delete origin tag_name` | Deletes a tag from a remote. |
| `git push origin :refs/tags/tag_name` | Deletes a tag from a remote (alternative syntax). |
| `git fetch origin tag tag_name` | Fetches a specific tag from a remote. |
| `git fetch origin --tags` | Fetches all tags from a remote. |
| `git fetch origin --prune-tags` | Fetches and prunes stale tags from a remote. |
| `git fetch origin --no-prune-tags` | Fetches without pruning tags from a remote. |

---
## Stashing

| Code | Description |
|------|-------------|
| `git stash` | Stashes changes in the working directory. |
| `git stash push` | Stashes changes in the working directory. |
| `git stash push -m "message"` | Stashes changes with a message. |
| `git stash push --all` | Stashes all changes, including ignored and untracked files. |
| `git stash push --include-untracked` | Stashes changes, including untracked files. |
| `git stash push --index` | Stashes changes, including staged changes. |
| `git stash push -p` | Interactively stashes changes. |
| `git stash push --patch` | Interactively stashes changes (alias). |
| `git stash push --keep-index` | Stashes changes but keeps the index. |
| `git stash push --no-keep-index` | Stashes changes and does not keep the index. |
| `git stash list` | Lists all stashes. |
| `git stash list --format="%gd: %s"` | Lists stashes with a custom format. |
| `git stash show` | Shows the changes in the most recent stash. |
| `git stash show -p` | Shows the changes in the most recent stash with patches. |
| `git stash show stash@{n}` | Shows the changes in a specific stash. |
| `git stash show -p stash@{n}` | Shows the changes in a specific stash with patches. |
| `git stash show --name-only` | Shows the changes in the most recent stash with file names only. |
| `git stash show --name-status` | Shows the changes in the most recent stash with file status. |
| `git stash show --stat` | Shows the changes in the most recent stash with statistics. |
| `git stash apply` | Applies the most recent stash. |
| `git stash apply stash@{n}` | Applies a specific stash. |
| `git stash apply --index` | Applies a stash and restages the staged changes. |
| `git stash apply --no-index` | Applies a stash without restaging the staged changes. |
| `git stash pop` | Applies and removes the most recent stash. |
| `git stash pop stash@{n}` | Applies and removes a specific stash. |
| `git stash drop` | Removes the most recent stash. |
| `git stash drop stash@{n}` | Removes a specific stash. |
| `git stash clear` | Removes all stashes. |
| `git stash branch branch_name` | Creates a new branch from a stash. |
| `git stash branch branch_name stash@{n}` | Creates a new branch from a specific stash. |
| `git stash create` | Creates a stash without storing it in the stash list. |
| `git stash store` | Stores a stash in the stash list. |
| `git stash save "message"` | Stashes changes with a message (deprecated, use `git stash push -m`). |
| `git stash --keep-index` | Stashes changes but keeps the index. |
| `git stash --no-keep-index` | Stashes changes and does not keep the index. |
| `git stash --include-untracked` | Stashes changes, including untracked files. |
| `git stash --all` | Stashes all changes, including ignored and untracked files. |

---
## Working with Patches

| Code | Description |
|------|-------------|
| `git apply patch` | Applies a patch to the working tree. |
| `git apply --check patch` | Checks if a patch can be applied. |
| `git apply --index patch` | Applies a patch and stages the changes. |
| `git apply --cached patch` | Applies a patch to the staging area. |
| `git apply --reverse patch` | Applies a patch in reverse. |
| `git apply --reject patch` | Applies a patch and leaves rejected hunks in .rej files. |
| `git apply --whitespace=fix patch` | Applies a patch and fixes whitespace errors. |
| `git apply --whitespace=warn patch` | Applies a patch and warns about whitespace errors. |
| `git apply --whitespace=error patch` | Applies a patch and errors on whitespace errors. |
| `git apply --whitespace=error-all patch` | Applies a patch and errors on all whitespace errors. |
| `git apply --ignore-space-change patch` | Applies a patch while ignoring changes in the amount of whitespace. |
| `git apply --ignore-whitespace patch` | Applies a patch while ignoring all whitespace. |
| `git apply --ignore-blank-lines patch` | Applies a patch while ignoring blank lines. |
| `git apply --unidiff-zero` | Applies a patch with zero lines of context. |
| `git apply --no-prefix` | Applies a patch without removing path prefixes. |
| `git apply -3 patch` | Applies a patch with a 3-way merge. |
| `git apply --3way patch` | Applies a patch with a 3-way merge (alias). |
| `git apply --index --cached patch` | Applies a patch to the staging area and index. |
| `git am patch` | Applies a patch from a mailbox. |
| `git am patch1 patch2` | Applies patches from multiple mailboxes. |
| `git am < mailbox` | Applies patches from a mailbox file. |
| `git am --signoff` | Applies patches and adds a Signed-off-by line. |
| `git am --keep-cr` | Applies patches and preserves carriage returns. |
| `git am --no-keep-cr` | Applies patches and removes carriage returns. |
| `git am --abort` | Aborts the current am operation. |
| `git am --continue` | Continues the current am operation after resolving conflicts. |
| `git am --skip` | Skips the current patch during am. |
| `git am --3way` | Uses 3-way merge when applying patches. |
| `git am --no-3way` | Does not use 3-way merge when applying patches. |
| `git am --reject` | Applies patches and leaves rejected hunks in .rej files. |
| `git am --interactive` | Interactively applies patches. |
| `git am --committer-date-is-author-date` | Uses the author date as the committer date. |
| `git am --ignore-date` | Uses the current date as the committer date. |
| `git am --ignore-space-change` | Applies patches while ignoring changes in the amount of whitespace. |
| `git am --ignore-whitespace` | Applies patches while ignoring all whitespace. |
| `git am --whitespace=fix` | Applies patches and fixes whitespace errors. |
| `git am --whitespace=warn` | Applies patches and warns about whitespace errors. |
| `git am --whitespace=error` | Applies patches and errors on whitespace errors. |
| `git am --whitespace=error-all` | Applies patches and errors on all whitespace errors. |
| `git am -C n` | Applies patches with n lines of context. |
| `git am --directory=dir` | Applies patches with a custom directory. |
| `git am --exclude=pattern` | Applies patches excluding files matching a pattern. |
| `git am --include=pattern` | Applies patches including only files matching a pattern. |
| `git format-patch` | Prepares patches for email submission. |
| `git format-patch -1` | Prepares a patch for the last commit. |
| `git format-patch -3` | Prepares patches for the last 3 commits. |
| `git format-patch HEAD~3` | Prepares patches for the last 3 commits. |
| `git format-patch --stdout` | Prepares patches and prints to stdout. |
| `git format-patch --attach` | Prepares patches with attachments. |
| `git format-patch --inline` | Prepares patches inline. |
| `git format-patch --no-thread` | Prepares patches without threading. |
| `git format-patch --thread` | Prepares patches with threading. |
| `git format-patch --in-reply-to=Message-ID` | Prepares patches as a reply to a message. |
| `git format-patch --subject-prefix="PREFIX"` | Prepares patches with a custom subject prefix. |
| `git format-patch --signature="signature"` | Prepares patches with a custom signature. |
| `git format-patch --signature-file=file` | Prepares patches with a signature from a file. |
| `git format-patch --to=email@example.com` | Prepares patches with a specific recipient. |
| `git format-patch --cc=email@example.com` | Prepares patches with a specific CC recipient. |
| `git format-patch --from=email@example.com` | Prepares patches with a specific sender. |
| `git format-patch --add-header="header"` | Prepares patches with a custom header. |
| `git format-patch --no-numbered` | Prepares patches without numbered files. |
| `git format-patch --numbered` | Prepares patches with numbered files. |
| `git format-patch --start-number n` | Prepares patches starting from number n. |
| `git format-patch --numbered-files` | Prepares patches with numbered files. |
| `git format-patch --no-numbered-files` | Prepares patches without numbered files. |
| `git format-patch --suffix=.txt` | Prepares patches with a custom suffix. |
| `git format-patch --output-indicator-context=">"` | Prepares patches with a custom output indicator context. |
| `git format-patch --no-output-indicator-context` | Prepares patches without an output indicator context. |
| `git format-patch --notes` | Prepares patches with notes. |
| `git format-patch --no-notes` | Prepares patches without notes. |

---
## Submodules

| Code | Description |
|------|-------------|
| `git submodule` | Shows the status of submodules. |
| `git submodule status` | Shows the status of submodules. |
| `git submodule status --cached` | Shows the status of submodules in the index. |
| `git submodule status --recursive` | Shows the status of submodules recursively. |
| `git submodule add repository [path]` | Adds a submodule. |
| `git submodule add -b branch repository [path]` | Adds a submodule at a specific branch. |
| `git submodule add -f repository [path]` | Forces the addition of a submodule. |
| `git submodule add --name name repository [path]` | Adds a submodule with a custom name. |
| `git submodule add --reference repository reference [path]` | Adds a submodule with a reference repository. |
| `git submodule add --depth depth repository [path]` | Adds a submodule with a shallow clone. |
| `git submodule add --no-depth repository [path]` | Adds a submodule without a shallow clone. |
| `git submodule init` | Initializes submodules. |
| `git submodule init [path]` | Initializes a specific submodule. |
| `git submodule update` | Updates submodules. |
| `git submodule update --init` | Initializes and updates submodules. |
| `git submodule update --recursive` | Updates submodules recursively. |
| `git submodule update --remote` | Updates submodules to the latest remote commit. |
| `git submodule update --merge` | Updates submodules and merges changes. |
| `git submodule update --rebase` | Updates submodules and rebases changes. |
| `git submodule update --checkout` | Updates submodules and checks out the latest commit. |
| `git submodule update --force` | Forces the update of submodules. |
| `git submodule update --depth=1` | Updates submodules with a shallow clone. |
| `git submodule update --no-depth` | Updates submodules without a shallow clone. |
| `git submodule foreach command` | Executes a command in each submodule. |
| `git submodule foreach --recursive command` | Executes a command in each submodule recursively. |
| `git submodule foreach --quiet command` | Executes a command in each submodule quietly. |
| `git submodule foreach --copy` | Copies the command output for each submodule. |
| `git submodule foreach --no-copy` | Does not copy the command output for each submodule. |
| `git submodule sync` | Synchronizes submodule URLs with the superproject. |
| `git submodule sync --recursive` | Synchronizes submodule URLs recursively. |
| `git submodule sync --no-recursive` | Synchronizes submodule URLs without recursing. |
| `git submodule absorbgitdirs` | Absorbs nested .git directories. |
| `git submodule absorbgitdirs --prefix=prefix` | Absorbs nested .git directories with a prefix. |
| `git submodule deinit` | Deinitializes submodules. |
| `git submodule deinit -f` | Forces the deinitialization of submodules. |
| `git submodule deinit [path]` | Deinitializes a specific submodule. |
| `git submodule deinit --all` | Deinitializes all submodules. |
| `git submodule deinit --all -f` | Forces the deinitialization of all submodules. |
| `git rm -f path/to/submodule` | Removes a submodule from the working tree and .gitmodules. |
| `git rm -f --cached path/to/submodule` | Removes a submodule from the index and .gitmodules. |
| `git config -f .gitmodules submodule.path.url new_url` | Changes the URL of a submodule. |
| `git config -f .gitmodules submodule.path.update none` | Disables updates for a submodule. |
| `git config -f .gitmodules submodule.path.update normal` | Enables normal updates for a submodule. |
| `git config -f .gitmodules submodule.path.update checkout` | Enables checkout updates for a submodule. |
| `git config -f .gitmodules submodule.path.update rebase` | Enables rebase updates for a submodule. |
| `git config -f .gitmodules submodule.path.update merge` | Enables merge updates for a submodule. |
| `git config -f .gitmodules submodule.path.ignore` | Ignores a submodule path. |
| `git config -f .gitmodules submodule.path.noIgnore` | Does not ignore a submodule path. |

---
## Repository Maintenance

| Code | Description |
|------|-------------|
| `git gc` | Runs garbage collection to optimize the repository. |
| `git gc --aggressive` | Runs aggressive garbage collection. |
| `git gc --auto` | Runs garbage collection automatically. |
| `git gc --prune=now` | Runs garbage collection and prunes unreachable objects. |
| `git gc --prune=all` | Runs garbage collection and prunes all unreachable objects. |
| `git gc --no-prune` | Runs garbage collection without pruning. |
| `git gc --quiet` | Runs garbage collection without output. |
| `git gc --verbose` | Runs garbage collection with verbose output. |
| `git repack` | Repacks unpacked objects into packs. |
| `git repack -a` | Repacks all unpacked objects into packs. |
| `git repack -d` | Repacks and removes redundant packs. |
| `git repack -f` | Repacks and forces a full repack. |
| `git repack -F` | Repacks and uses a more aggressive delta compression. |
| `git repack --max-pack-size=100m` | Repacks with a maximum pack size of 100MB. |
| `git repack --window=10` | Repacks with a window size of 10. |
| `git repack --depth=50` | Repacks with a depth of 50. |
| `git repack --threads=4` | Repacks with 4 threads. |
| `git repack --no-threads` | Repacks without threads. |
| `git repack -l` | Lists objects in packs. |
| `git repack -L n,m` | Limits the repack to objects with depth n and window m. |
| `git prune` | Removes unreachable objects from the object database. |
| `git prune -n` | Performs a dry-run prune. |
| `git prune -v` | Prunes with verbose output. |
| `git prune --expire now` | Prunes objects expired now. |
| `git prune --expire=2.weeks.ago` | Prunes objects expired 2 weeks ago. |
| `git prune --unreachable` | Prunes unreachable objects. |
| `git prune --no-unreachable` | Does not prune unreachable objects. |
| `git fsck` | Verifies the connectivity and validity of the objects in the database. |
| `git fsck --full` | Performs a full fsck. |
| `git fsck --strict` | Performs a strict fsck. |
| `git fsck --unreachable` | Shows unreachable objects. |
| `git fsck --no-unreachable` | Does not show unreachable objects. |
| `git fsck --no-reflogs` | Performs fsck without checking reflogs. |
| `git fsck --root` | Shows root objects. |
| `git fsck --tags` | Shows tags. |
| `git fsck --cache` | Shows cached objects. |
| `git fsck --verbose` | Performs fsck with verbose output. |
| `git fsck --connectivity-only` | Checks only connectivity. |
| `git fsck --no-connectivity` | Does not check connectivity. |
| `git reflog` | Shows the reference logs. |
| `git reflog show` | Shows the reflog. |
| `git reflog show branch` | Shows the reflog for a specific branch. |
| `git reflog expire` | Expires reflog entries. |
| `git reflog expire --expire=now` | Expires all reflog entries. |
| `git reflog expire --expire-unreachable=now` | Expires unreachable reflog entries. |
| `git reflog expire --all` | Expires all reflog entries. |
| `git reflog expire --dry-run` | Performs a dry-run expiration of reflog entries. |
| `git reflog expire --verbose` | Expires reflog entries with verbose output. |
| `git reflog delete` | Deletes reflog entries. |
| `git reflog delete --all` | Deletes all reflog entries. |
| `git reflog delete --dry-run` | Performs a dry-run deletion of reflog entries. |
| `git reflog delete --verbose` | Deletes reflog entries with verbose output. |
| `git reflog expire --stale-fix` | Expires reflog entries and fixes stale entries. |
| `git worktree` | Lists all working trees. |
| `git worktree add path branch` | Adds a new working tree. |
| `git worktree add path -b branch` | Adds a new working tree and creates a new branch. |
| `git worktree add path --detach` | Adds a new working tree in detached HEAD state. |
| `git worktree add path --checkout` | Adds a new working tree and checks out files. |
| `git worktree add path --no-checkout` | Adds a new working tree without checking out files. |
| `git worktree add path --lock` | Adds a new working tree and locks it. |
| `git worktree add path --no-lock` | Adds a new working tree without locking it. |
| `git worktree list` | Lists all working trees. |
| `git worktree list --porcelain` | Lists all working trees in porcelain format. |
| `git worktree remove path` | Removes a working tree. |
| `git worktree remove -f path` | Force removes a working tree. |
| `git worktree prune` | Prunes dead working trees. |
| `git worktree prune --dry-run` | Performs a dry-run prune of working trees. |
| `git worktree prune --verbose` | Prunes working trees with verbose output. |
| `git worktree lock path` | Locks a working tree. |
| `git worktree lock --reason "reason" path` | Locks a working tree with a reason. |
| `git worktree unlock path` | Unlocks a working tree. |
| `git worktree move path new_path` | Moves a working tree. |
| `git worktree repair` | Repairs working trees. |

---
## Git Internals and Plumbing Commands

| Code | Description |
|------|-------------|
| `git cat-file -t object` | Shows the type of an object. |
| `git cat-file -p object` | Pretty-prints the contents of an object. |
| `git cat-file -s object` | Shows the size of an object. |
| `git cat-file -e object` | Exits with zero status if the object exists. |
| `git cat-file -t <sha1` | Shows the type of a blob, tree, or commit object. |
| `git cat-file blob sha1` | Shows the contents of a blob object. |
| `git cat-file tree sha1` | Shows the contents of a tree object. |
| `git cat-file commit sha1` | Shows the contents of a commit object. |
| `git cat-file tag sha1` | Shows the contents of a tag object. |
| `git cat-file --batch` | Shows the type, size, and contents of multiple objects. |
| `git cat-file --batch-check` | Shows the type and size of multiple objects. |
| `git cat-file --batch-all-objects` | Shows all objects in batch mode. |
| `git hash-object -w file` | Computes the object ID of a file and writes it to the object database. |
| `git hash-object file` | Computes the object ID of a file. |
| `git hash-object --stdin` | Computes the object ID from stdin. |
| `git hash-object --no-filters` | Computes the object ID without applying filters. |
| `git hash-object --path=file` | Computes the object ID with a custom path. |
| `git index-pack file.pack` | Builds an index file for a pack. |
| `git index-pack -v file.pack` | Builds an index file for a pack with verbose output. |
| `git index-pack --stdin` | Builds an index file from stdin. |
| `git index-pack --fix-thin` | Fixes thin packs when building an index. |
| `git index-pack --keep-idx` | Keeps the index file when building an index. |
| `git index-pack --strict` | Uses strict mode when building an index. |
| `git mktree` | Creates a tree object from a ls-tree formatted text. |
| `git mktag` | Creates a tag object. |
| `git ls-tree sha1` | Lists the contents of a tree object. |
| `git ls-tree -r sha1` | Recursively lists the contents of a tree object. |
| `git ls-tree -z sha1` | Lists the contents of a tree object with null-terminated entries. |
| `git ls-tree --name-only sha1` | Lists only the names of the contents of a tree object. |
| `git ls-tree --name-status sha1` | Lists the names and status of the contents of a tree object. |
| `git ls-tree --full-name sha1` | Lists the full names of the contents of a tree object. |
| `git ls-tree --full-tree sha1` | Lists the full tree of the contents of a tree object. |
| `git ls-tree --abbrev sha1` | Lists the abbreviated names of the contents of a tree object. |
| `git ls-remote url` | Lists references available from a remote repository. |
| `git ls-remote --heads url` | Lists head references from a remote repository. |
| `git ls-remote --tags url` | Lists tag references from a remote repository. |
| `git ls-remote --refs url` | Lists all references from a remote repository. |
| `git ls-remote --upload-pack url` | Lists references using git-upload-pack. |
| `git ls-remote --quiet url` | Lists references without output. |
| `git ls-remote --symref url` | Lists references with symbolic ref information. |
| `git peek-remote url` | Lists references available from a remote repository (deprecated). |
| `git receive-pack url` | Receives a pack from a remote repository. |
| `git upload-pack url` | Sends a pack to a remote repository. |
| `git upload-archive url` | Sends an archive to a remote repository. |
| `git http-fetch` | Fetches objects from a remote repository over HTTP. |
| `git http-push` | Pushes objects to a remote repository over HTTP. |
| `git parse-remote` | Parses a remote URL. |
| `git get-tar-commit-id` | Gets the commit ID from a tar archive. |
| `git shell` | Restricted login shell for Git-only SSH access. |
| `git instaweb` | Instantly browses a working copy in a web browser. |
| `git instaweb --httpd=webrick` | Instantly browses a working copy using WEBrick. |
| `git instaweb --httpd=lighttpd` | Instantly browses a working copy using lighttpd. |
| `git instaweb --httpd=apache2` | Instantly browses a working copy using Apache2. |
| `git instaweb --start` | Starts the web server. |
| `git instaweb --stop` | Stops the web server. |
| `git instaweb --restart` | Restarts the web server. |
| `git instaweb --browse` | Opens the working copy in a web browser. |
| `git archive` | Creates an archive of a repository. |
| `git archive --format=tar HEAD` | Creates a tar archive of the HEAD commit. |
| `git archive --format=tar --prefix=project/ HEAD` | Creates a tar archive with a prefix. |
| `git archive --format=zip HEAD` | Creates a zip archive of the HEAD commit. |
| `git archive --format=tar --output=file.tar HEAD` | Creates a tar archive and saves it to a file. |
| `git archive --format=tar --remote=origin HEAD` | Creates an archive from a remote repository. |
| `git archive --format=tar --remote=origin --exec=git-upload-archive HEAD` | Creates an archive from a remote repository using git-upload-archive. |
| `git archive --list` | Lists available archive formats. |
| `git var GIT_AUTHOR_IDENT` | Shows the author identity. |
| `git var GIT_COMMITTER_IDENT` | Shows the committer identity. |
| `git var GIT_EDITOR` | Shows the editor. |
| `git var GIT_PAGER` | Shows the pager. |
| `git interpret-trailers` | Interprets Git trailers. |
| `git interpret-trailers --parse` | Parses Git trailers. |
| `git interpret-trailers --in-trailer` | Shows the in-trailer format. |
| `git interpret-trailers --unfold` | Unfolds Git trailers. |
| `git check-ref-format ref` | Checks if a reference name is valid. |
| `git check-ref-format --branch ref` | Checks if a branch name is valid. |
| `git check-ref-format --tag ref` | Checks if a tag name is valid. |
| `git symbolic-ref ref` | Shows the symbolic reference for a reference. |
| `git symbolic-ref HEAD` | Shows the symbolic reference for HEAD. |
| `git symbolic-ref --short HEAD` | Shows the short symbolic reference for HEAD. |
| `git rev-parse HEAD` | Shows the object name for HEAD. |
| `git rev-parse HEAD~1` | Shows the object name for HEAD~1. |
| `git rev-parse --verify HEAD` | Verifies the object name for HEAD. |
| `git rev-parse --short HEAD` | Shows the short object name for HEAD. |
| `git rev-parse --abbrev-ref HEAD` | Shows the abbreviated reference for HEAD. |
| `git rev-parse --abbrev-ref=strict HEAD` | Shows the abbreviated reference for HEAD with strict mode. |
| `git rev-parse --symbolic HEAD` | Shows the symbolic reference for HEAD. |
| `git rev-parse --symbolic-full-name HEAD` | Shows the full symbolic reference for HEAD. |
| `git rev-parse --git-dir` | Shows the path to the .git directory. |
| `git rev-parse --show-toplevel` | Shows the top-level directory of the repository. |
| `git rev-parse --show-cdup` | Shows the relative path from the current directory to the top-level directory. |
| `git rev-parse --is-inside-work-tree` | Checks if the current directory is inside the working tree. |
| `git rev-parse --is-inside-git-dir` | Checks if the current directory is inside the .git directory. |
| `git rev-parse --is-bare-repository` | Checks if the repository is bare. |
| `git rev-parse --is-shallow-repository` | Checks if the repository is shallow. |
| `git update-server-info` | Updates server info files. |
| `git verify-pack` | Verifies the integrity of pack files. |
| `git verify-pack -v file.pack` | Verifies a pack file with verbose output. |
| `git verify-pack --stat file.pack` | Verifies a pack file and shows statistics. |
| `git pack-objects --all` | Creates a pack with all objects. |
| `git pack-objects --unpacked` | Creates a pack with unpacked objects. |
| `git pack-objects --incremental` | Creates an incremental pack. |
| `git pack-objects --stdout` | Creates a pack and writes it to stdout. |
| `git pack-objects --stdout --all > pack.pack` | Creates a pack with all objects and saves it to a file. |
| `git pack-objects --revs` | Creates a pack with objects from revision arguments. |
| `git pack-objects --exclude=pattern` | Creates a pack excluding objects matching a pattern. |
| `git pack-objects --include=pattern` | Creates a pack including only objects matching a pattern. |
| `git pack-objects --indexed-objects` | Creates a pack with indexed objects. |
| `git unpack-objects` | Unpacks objects from a pack. |
| `git unpack-objects < pack.pack` | Unpacks objects from a pack file. |
| `git unpack-objects --strict` | Unpacks objects with strict mode. |
| `git index-pack` | Builds an index file for a pack. |
| `git prune-packed` | Removes objects that are already in packs. |
| `git get-tar-commit-id` | Gets the commit ID from a tar archive. |
| `git mailinfo` | Extracts patch and author information from an email. |
| `git mailinfo --message-id` | Extracts patch and author information from an email and shows the message ID. |
| `git mailinfo --scissors` | Extracts patch and author information from an email and respects scissors lines. |
| `git mailsplit` | Splits a mailbox into individual message files. |
| `git mailsplit -ooutputdir -b -f n` | Splits a mailbox into individual message files starting from message n. |
| `git mailsplit --max-msg-size=size` | Splits a mailbox with a maximum message size. |
| `git strip-space` | Removes trailing whitespace from lines. |
| `git strip-space -s` | Removes trailing whitespace and compresses blank lines. |
| `git strip-space --comment-lines` | Removes trailing whitespace from comment lines. |

---
## Git Credential Helpers

| Code | Description |
|------|-------------|
| `git credential-cache` | Cache for Git credentials. |
| `git credential-cache exit` | Exits the credential cache daemon. |
| `git credential-cache --timeout=3600` | Runs the credential cache with a timeout of 3600 seconds. |
| `git credential-cache --socket=/path/to/socket` | Runs the credential cache with a custom socket path. |
| `git credential-store` | Store for Git credentials. |
| `git credential-store --file=/path/to/file` | Uses a custom file for storing credentials. |
| `git credential-manager` | Manager for Git credentials. |
| `git credential-manager get` | Gets credentials from the manager. |
| `git credential-manager store` | Stores credentials in the manager. |
| `git credential-manager erase` | Erases credentials from the manager. |
| `git credential-manager-core` | Core credential manager for Git. |
| `git credential-manager-core get` | Gets credentials from the core manager. |
| `git credential-manager-core store` | Stores credentials in the core manager. |
| `git credential-manager-core erase` | Erases credentials from the core manager. |
| `git credential osxkeychain` | OSX Keychain credential helper for Git. |
| `git credential osxkeychain get` | Gets credentials from the OSX Keychain. |
| `git credential osxkeychain store` | Stores credentials in the OSX Keychain. |
| `git credential osxkeychain erase` | Erases credentials from the OSX Keychain. |
| `git credential libsecret` | libsecret credential helper for Git. |
| `git credential libsecret get` | Gets credentials from libsecret. |
| `git credential libsecret store` | Stores credentials in libsecret. |
| `git credential libsecret erase` | Erases credentials from libsecret. |
| `git credential wincred` | Windows credential helper for Git. |
| `git credential wincred get` | Gets credentials from the Windows credential manager. |
| `git credential wincred store` | Stores credentials in the Windows credential manager. |
| `git credential wincred erase` | Erases credentials from the Windows credential manager. |

---
## Git Hooks

| Code | Description |
|------|-------------|
| `pre-commit` | Runs before a commit is finalized. |
| `pre-commit.sample` | Sample pre-commit hook. |
| `pre-push` | Runs before a push is executed. |
| `pre-rebase` | Runs before a rebase is executed. |
| `post-checkout` | Runs after a checkout is performed. |
| `post-commit` | Runs after a commit is finalized. |
| `post-merge` | Runs after a merge is performed. |
| `post-receive` | Runs after a push is received. |
| `post-rewrite` | Runs after commands that rewrite commits. |
| `post-update` | Runs after a branch is updated via push. |
| `pre-applypatch` | Runs before a patch is applied. |
| `pre-receive` | Runs before a push is received. |
| `prepare-commit-msg` | Runs before the commit message editor is fired up. |
| `commit-msg` | Runs after the commit message editor is fired up. |
| `fsmonitor-watchman` | Runs when the watchman file system monitor is used. |
| `p4-changelist` | Runs when using Git with Perforce. |
| `p4-prepare-changelist` | Runs when preparing a changelist with Perforce. |
| `p4-post-changelist` | Runs after a changelist is submitted with Perforce. |
| `p4-pre-submit` | Runs before a changelist is submitted with Perforce. |
| `pre-auto-gc` | Runs before a garbage collection is performed. |
| `post-auto-gc` | Runs after a garbage collection is performed. |
| `sendemail-validate` | Runs when validating emails with git-send-email. |
| `push-to-checkout` | Runs when pushing to a branch that is checked out. |
| `pre-merge-commit` | Runs before a merge commit is created. |
| `push--pre` | Runs before a push is executed (client-side). |
| `fetch--pre` | Runs before a fetch is executed (client-side). |
| `rebase--interactive` | Runs during an interactive rebase. |

---
## Git Environment Variables

| Code | Description |
|------|-------------|
| `GIT_AUTHOR_NAME` | Author name to use for commits. |
| `GIT_AUTHOR_EMAIL` | Author email to use for commits. |
| `GIT_AUTHOR_DATE` | Author date to use for commits. |
| `GIT_COMMITTER_NAME` | Committer name to use for commits. |
| `GIT_COMMITTER_EMAIL` | Committer email to use for commits. |
| `GIT_COMMITTER_DATE` | Committer date to use for commits. |
| `GIT_EDITOR` | Editor to use for commit messages. |
| `GIT_PAGER` | Pager to use for Git output. |
| `GIT_DIR` | Path to the .git directory. |
| `GIT_WORK_TREE` | Path to the working tree. |
| `GIT_PREFIX` | Prefix to prepend to Git output. |
| `GIT_ASKPASS` | Program to use for prompting for a password. |
| `GIT_SSH` | SSH command to use for Git operations. |
| `GIT_SSH_COMMAND` | SSH command to use for Git operations. |
| `GIT_SSH_VARIANT` | SSH variant to use (auto, ssh, plink, simple). |
| `GIT_TRACE` | Enables tracing for Git commands. |
| `GIT_TRACE_PACKET` | Enables packet tracing for Git commands. |
| `GIT_TRACE_PERFORMANCE` | Enables performance tracing for Git commands. |
| `GIT_TRACE_SETUP` | Enables setup tracing for Git commands. |
| `GIT_TRACE_SHALLOW` | Enables shallow tracing for Git commands. |
| `GIT_CURL_VERBOSE` | Enables verbose output for curl. |
| `GIT_HTTP_USER_AGENT` | User agent to use for HTTP requests. |
| `GIT_HTTP_LOW_SPEED_LIMIT` | Low speed limit for HTTP requests. |
| `GIT_HTTP_LOW_SPEED_TIME` | Low speed time for HTTP requests. |
| `GIT_HTTP_NO_SSL_VERIFY` | Disables SSL verification for HTTP requests. |
| `GIT_SSL_NO_VERIFY` | Disables SSL verification. |
| `GIT_SSL_CAINFO` | Path to the CA bundle for SSL. |
| `GIT_SSL_CAPATH` | Path to the CA directory for SSL. |
| `GIT_SSL_CERT` | Path to the SSL certificate. |
| `GIT_SSL_KEY` | Path to the SSL key. |
| `GIT_SSL_CERT_PASSWORD_PROTECTED` | Indicates that the SSL certificate is password-protected. |
| `GIT_SSL_NO_CRLF` | Disables CRLF conversion for SSL. |
| `GIT_TERMINAL_PROMPT` | Disables terminal prompt for Git commands. |
| `GIT_INTERACTIVE_REBASE` | Enables interactive rebase. |
| `GIT_SEQUENCE_EDITOR` | Editor to use for editing todo lists in interactive rebase. |
| `GIT_DIFF_OPTS` | Default options for git-diff. |
| `GIT_MERGE_AUTOEDIT` | Disables auto-editing of merge messages. |
| `GIT_MERGE_VERBOSITY` | Verbosity level for merge output. |
| `GIT_PAGER_IN_USE` | Indicates that a pager is in use. |
| `GIT_LITERAL_PATHSPECS` | Treats pathspecs literally. |
| `GIT_GLOB_PATHSPECS` | Treats pathspecs as glob patterns. |
| `GIT_NOGLOB_PATHSPECS` | Treats pathspecs as literal paths. |
| `GIT_ICASE_PATHSPECS` | Treats pathspecs as case-insensitive. |
| `GIT_REFLOG_ACTION` | Action for reflog entries. |
| `GIT_NOTES_REF` | Ref to use for notes. |
| `GIT_NOTES_REWRITE_REF` | Ref to use for notes rewrite. |
| `GIT_NOTES_REWRITE_MODE` | Mode to use for notes rewrite. |
| `GIT_NOTES_DISPLAY_REF` | Ref to use for notes display. |
| `GIT_NOTES_MERGE_STRATEGY` | Strategy to use for notes merge. |
| `GIT_WORK_TREE` | Path to the working tree. |
| `GIT_INDEX_FILE` | Path to the index file. |
| `GIT_OBJECT_DIRECTORY` | Path to the object directory. |
| `GIT_ALTERNATE_OBJECT_DIRECTORIES` | Paths to alternate object directories. |
| `GIT_NO_REPLACE_OBJECTS` | Disables replacement of objects. |
| `GIT_REPLACE_REF_BASE` | Ref to use as the base for replacement refs. |
| `GIT_REPLACE_REF_PREFIX` | Prefix to use for replacement refs. |
| `GIT_FETCH_OPTIONS` | Options to use for fetch. |
| `GIT_PUSH_OPTIONS` | Options to use for push. |
| `GIT_TRANSFER_TRACE` | Enables tracing for Git transfer. |
| `GITMAINWORKTREE` | Path to the main working tree. |
| `GIT_DISCOVERY_ACROSS_FILESYSTEM` | Enables discovery across filesystems. |
| `GIT_PROTOCOL_FROM_USER` | Protocol to use for Git operations. |
| `GIT_OPTIONAL_LOCKS` | Disables mandatory file locking. |
| `GIT_REDACT_COOKIES` | Redacts cookies in Git output. |
| `GIT_REDACT_HTTP_HEADER` | Redacts HTTP headers in Git output. |

---
## Git Attributes

| Code | Description |
|------|-------------|
| `text` | Marks files as text. |
| `-text` | Marks files as binary. |
| `text=auto` | Automatically detects text files. |
| `text=eol` | Sets the end-of-line type for text files. |
| `eol=crlf` | Sets the end-of-line type to CRLF. |
| `eol=lf` | Sets the end-of-line type to LF. |
| `eol=native` | Sets the end-of-line type to native. |
| `working-tree-encoding=utf-8` | Sets the working tree encoding to UTF-8. |
| `ident` | Expands $Id$ keywords. |
| `-ident` | Disables $Id$ keyword expansion. |
| `filter` | Specifies a filter for the file. |
| `filter=clean` | Specifies a clean filter for the file. |
| `filter=smudge` | Specifies a smudge filter for the file. |
| `diff` | Specifies a diff driver for the file. |
| `diff=driver` | Specifies a custom diff driver for the file. |
| `merge` | Specifies a merge driver for the file. |
| `merge=driver` | Specifies a custom merge driver for the file. |
| `linguist-language=language` | Specifies the language for Linguist. |
| `linguist-vendored` | Marks files as vendored for Linguist. |
| `linguist-generated` | Marks files as generated for Linguist. |
| `linguist-documentation` | Marks files as documentation for Linguist. |
| `export-ignore` | Ignores files when exporting. |
| `export-subst` | Expands keywords when exporting. |

---
## Git Ignore Patterns

| Code | Description |
|------|-------------|
| `*.log` | Ignores all files with the .log extension. |
| `temp/` | Ignores all files in the temp directory. |
| `temp/*.txt` | Ignores all .txt files in the temp directory. |
| `build/` | Ignores all files in the build directory. |
| `!important.log` | Does not ignore important.log. |
| `*.txt` | Ignores all .txt files. |
| `!important.txt` | Does not ignore important.txt. |
| `**/temp` | Ignores all files named temp in any directory. |
| `doc/*.txt` | Ignores all .txt files in the doc directory. |
| `doc/**/*.txt` | Ignores all .txt files in the doc directory and its subdirectories. |
| `/temp` | Ignores the temp file in the root directory. |
| `temp` | Ignores all files and directories named temp. |
| `temp/` | Ignores only the temp directory. |
| `*.[oa]` | Ignores all files ending with .o or .a. |
| `*~` | Ignores all files ending with ~. |
| `*.swp` | Ignores all swap files. |
| `._*` | Ignores all files starting with ._. |
| `*.un~` | Ignores all files ending with .un~. |
| `[abc]` | Ignores all files with a single character a, b, or c. |
| `[!abc]` | Ignores all files with a single character not a, b, or c. |
| `[0-9]` | Ignores all files with a single digit. |
| `??*` | Ignores all files with two arbitrary characters followed by any characters. |
| `a/**/b` | Ignores all files matching a/b, a/x/b, a/x/y/b, etc. |
| `a/**/b.txt` | Ignores all .txt files matching a/b.txt, a/x/b.txt, a/x/y/b.txt, etc. |
| `**/foo` | Ignores all files named foo in any directory. |
| `foo/**` | Ignores all files in the foo directory and its subdirectories. |
| `/*` | Ignores all files in the root directory. |
| `/*/` | Ignores all directories in the root directory. |
| `/**` | Ignores all files in any directory. |