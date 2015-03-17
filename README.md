# backup-automation

This is a set of scripts that can be used to back things up in Git.

## Known Limitations

Can't track any file called 'list', 'add', 'remove', 'push', 'pull', or 'README.md'.

## Usage

### add

Adds an entry to the tracked file list, and adds the list to the working index.

### remove

Removes an entry from the tracked file list, and adds the list to the working index.

Assumes that the entry was added, pulled, and committed prior to being removed. If you want to remove something you just added but didn't commit, you'll have to do it manually.

### pull

Copies each file/directory in the file list to the local repository and adds the contents to the working index.

Finishes up with a run of 'git status'.

### push

Propagates each file/directory in the file list out to the filesystem from the repository.

