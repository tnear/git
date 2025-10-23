# restore

`git-restore` - Restore working tree files

**Note**: this command can discard changes without prompting.

## Delete changes
```bash
git restore file.txt              # discard changes to file.txt
git restore src/path/to/file.txt  # full path

# Restore multiple files
git restore file1.txt file2.txt
git restore *.txt                 # Restore all .txt files
```

## Move out of staging area
```bash
# Restore to staging area (staged changes)
git restore --staged file.txt     # Unstage file.txt
git restore --staged .            # Unstage all changes
```

## Apply specific files in a stash
```bash
# apply most recent stash
git restore --source=stash -- path/to/file

# apply specific stash
git restore --source=stash@{2} -- path/to/file
```

## Resources
- https://git-scm.com/docs/git-restore
