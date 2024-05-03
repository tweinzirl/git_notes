[Section 2.1](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)

### Getting a git repository
There are two ways set up a local repository:
  - clone it using `git clone https://github.com/user/some_repo`
  - Make a local directory into a git repository with
```bash
git init
git add .  # '.' means local working directory; can also add files separately
git commit -m 'commit message'
```

[Section 2.2](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)

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
Use `git status` or `git status -s` to summarize the status of files in the working directory.

### Viewing differences in Modified and Staged files
Use `git diff` to list changes in files that have been Modified but not yet Staged.
To compare Staged files with the last commit, use `git diff --staged`.

### Commiting files
Common usages of `git commit`:
  - The most straightforward way to commit Staged files is `git commit - 'commit message'`
  - To automatically stage every tracked file before committing, use `git commit -a -m 'commit message'`
  - To update the previous commit with any currently staged files, use `git commit --amend`. The use case is like
```bash
git commit -m 'Initial commit'
git add forgotten_file
git commit --amend
```

### Remove file
  - To remove a file from the index and filesystem: `git rm <file>`
  - To remove from the index only: `git rm --cached <file>`

### Undoing changes

### Fetching and pulling from remote servers

### Pushing to the server

### Git log
