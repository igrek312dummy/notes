## Table of Contents
- [Configuration](#configuration)
    - [Useful git global configs](#useful-git-global-configs)
- [Editing](#editing)
    - [Rename/move a file](#renamemove-a-file)
- [Commits](#commits)
    - [Commit after adding all files to staging area](#commit-after-adding-all-files-to-staging-area)
    - [Short status](#short-status)
    - [Push a branch](#push-a-branch)
    - [Push a branch and update upstream info for later pulls](#push-a-branch-and-update-upstream-info-for-later-pulls)
- [Branching](#branching)
    - [Create a branch and switch to it](#create-a-branch-and-switch-to-it)
    - [Create a branch from remote and switch to it](#create-a-branch-from-remote-and-switch-to-it)
    - [Create a branch from a tag and switch to it](#create-a-branch-from-a-tag-and-switch-to-it)
- [Remote Work](#remote-work)
    - [Track a remote branch from a local branch](#track-a-remote-branch-from-a-local-branch)
    - [List all remote tracking branches](#list-all-remote-tracking-branches)
    - [Fetch all remote repositories](#fetch-all-remote-repositories)
    - [Delete a remote branch](#delete-a-remote-branch)
- [Merging and Rebasing](#merging-and-rebasing)
    - [Rebase without checking out](#rebase-without-checking-out)
    - [Rebase onto](#rebase-onto)
- [Tags](#tags)
    - [Create a tag](#create-a-tag)
    - [Push a tag or all newly-created tags](#push-a-tag-or-all-newly-created-tags)
- [Logging](#logging)
    - [Useful flags](#useful-flags)

### Configuration

#### Useful git global configs
```console
git config --global <config> <value>
    user.name
    user.email
    core.editor
    merge.tool <toolname>
    merge.<toolname>.path
    alias.<command-name>
```

### Editing

#### Rename/move a file
```console
git mv <oldfile> <newfile>
```

### Commits

#### Commit after adding all files to staging area
```console
git commit -am <message>
```

#### Short status
```console
git status -s
```

#### Push a branch
```console
git push <remote-name> <local-branch-name>[:<remote-branch-name>]
```

#### Push a branch and update upstream info for later pulls
This creates a new branch on the remote server if none is found with the name, to push a branch as another branch's name, see above.
```console
git push -u <remote-name> <local-branch-name>
```

### Branching

#### Create a branch and switch to it
```console
git checkout -b <branch-name>
```

#### Create a branch from remote and switch to it
```console
git checkout <remote-branch-name>
git checkout --track <remote-name>/<branch-name>
git checkout -b <local-branch-name> <remote-name>/<remote-branch-name>
```

#### Create a branch from a tag and switch to it
```console
git checkout -b <branch-name> <tag-name>
```

### Remote Work

#### Track a remote branch from a local branch
```console
git branch -u <remote-name>/<branch-name>
```

#### List all remote tracking branches
```console
git branch -vv
```

#### Fetch all remote repositories
```console
git fetch --all
```

#### Delete a remote branch
```console
git push <remote-name> --delete <remote-branch-name>
```

### Merging and Rebasing

#### Merge squash
This will perform the merge and stage the changes as a single commit (deleting the merge history)
```console
git merge --squash <branch>
```

#### Rebase without checking out
```console
git rebase <target> <source>
```

#### Rebase onto
This rebases by taking changes from when `source` diverged from `parent` and applies it to `target`.
```console
git rebase --onto <target> <parent> <source>
```

### Tags

#### Create a tag
```console
git tag <tag-name> [<commit-number>] [-a] [-m] <annotated-tag-message>
```

#### Push a tag or all newly-created tags
```console
git push <remote-name> <tag-name>
git push <remote-name> --tags
```

### Logging

#### Useful flags
| Flag            | Description                                    |
| --------------- | ---------------------------------------------- |
| `relative-date` | Uses relative dates instead of full timestamps |
| `stat`          | Shows file change stats                        |
| `abbrev-commit` | Shows only first 5 chars of the hash           |
| `graph`         | Shows branch graph                             |
| `oneline`       | Shows only hash and commit messages            |


