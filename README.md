# backup-automation

This is a set of scripts that can be used to back things up in Git.

## Usage

### add

```bash
% add absolute_path [local_path]
```

Adds an entry to the list of tracked files (henceforth, "listfile"). Each given path must be absolute. If local path is omitted, it defaults to the basename of the file/dir.

Upon successul addition, adds the listfile to the working index.

### remove

```bash
% remove absolute_path
```

Removes all entries with the given local absolute path from the listfile, and adds the listfile to the working index.

Assumes that the entry was added, pulled, and committed prior to being removed. If you want to remove something you just added but didn't commit, you'll have to do it manually.

### pull

Copies each file/directory in the listfile to the local repository and adds the contents to the working index.

Finishes up with a run of 'git status'.

### push

Propagates each file/directory in the listfile out to the filesystem from the repository.

