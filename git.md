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
git commit -a -m <message>
```

#### Short status
```console
git status -s
```

#### Push a branch
```console
git push <remote-name> <local-branch-name>[:<remote-branch-name>]
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

