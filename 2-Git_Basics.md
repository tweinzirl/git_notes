### Getting a git repository
There are two ways set up a local repository:
  - clone it using `git clone https://github.com/user/some_repo`
  - Make a local directory into a git repository with
```bash
git init
git add .  # '.' means local working directory; can also add files separately
git commit -m 'commit message'
```

### File states
There are two kinds of files in git: `tracked` (meaning the file was present in the last commit snapshot) and `untracked`.
Tracked files can be Unmodified, Modified, or Staged. [Figure 8](https://git-scm.com/book/en/v2/images/lifecycle.png)
from the book shows how files may transition between these labels. The figure says that:
  - Untracked files become Staged with `git add`
  - Unmodified files become Modified if they are edited
  - A Modified file is Staged with `git add`
  - Staged files become Unmodified after `git commit`
  - Undo Modified status with `git checkout` or `git restore`


### File status

### File differences

### Commiting files
git commit

### Remove file

### Undoing changes

### Fetching and pulling from remote servers

### Pushing to the server

### Git log
