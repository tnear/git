# config

`git-config` - Get and set repository or global options

## View all configs (including `user.email` and `user.name`)
```bash
git config --list
```

### View specific config
```bash
git config <configName>
git config user.name
```

## Set name and email (globally)
This is a required step for new installations of Git. Remove the `--global` flag to configure locally.

```bash
> git config --global user.email 'see here: https://github.com/settings/emails'
> git config --global user.name 'Your Name'
```

## Disable pager for `git branch`
By default, git uses a pager when listing branches. This config option changes that default.

```bash
git config --global pager.branch false
```

## Change text editor
git uses `vim` by default. To change this editor, modify the `core.editor` field:
```bash
# vim
git config --global core.editor "vim"

# vscode (note the --wait parameter)
git config --global core.editor "code --wait"
```

## Resources
- https://git-scm.com/docs/git-config
