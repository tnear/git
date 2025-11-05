# submodule

`git-submodule` - Initialize, update or inspect submodules

A submodule is a git repository which is a sub-directory of another git repository.

## Initialize
`git submodule update --init` will initialize initializes repositories defined in `.gitmodules`.

`git submodule update --init --recursive` initializes nested submodules.

These commands are useful after pulling the repository for the first time.

## Get latest changes from remote
Run `git module update --remote` to pull newest changes from submodule's remote repository.

Add `--recursive` to do it recursively.

## Resources
- https://git-scm.com/docs/git-submodule
- https://git-scm.com/book/en/v2/Git-Tools-Submodules
