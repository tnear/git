# ls-files

`git-ls-files` - Show information about files in the index and the working tree

`ls-files` honors `.gitignore` and is recommended over `find` for searching a repository.

## List all files tracked by git repository
```bash
git ls-files
```

### List files with extension
```bash
git ls-files '*.cpp'

# multiple extensions
git ls-files '*.h' '*.hpp'

# specified directory
git ls-files 'src/'
```

### Search file contents by extension
```bash
# search all '.h' files which are missing (-L) include guard
git ls-files '*.h' | xargs grep -L '#pragma once'
```

## Search by attribute
```bash
# list modified files
git ls-files -m

# list deleted files
git ls-files -d
```

## Resources
- https://git-scm.com/docs/git-ls-files
