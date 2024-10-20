# config

`git-config` - Get and set repository or global options

## View all configs (including `user.email` and `user.name`)
```
git config --list
```

### View specific config
```
git config <configName>
git config user.name
```

## Set name and email (globally)
This is a required step for new installations of Git. Remove the `--global` flag to configure locally.

```
> git config --global user.email 'see here: https://github.com/settings/emails'
> git config --global user.name 'Your Name'
```

## Disable pager for `git branch`
By default, git uses a pager when listing branches. This config option changes that default.

```
git config --global pager.branch false
```

## Resources
- https://git-scm.com/docs/git-config
