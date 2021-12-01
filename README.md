https://www.git-scm.com/docs/gitattributes#_filter
https://git-scm.com/book/en/v2/Customizing-Git-Git-Attributes

https://github.com/git-lfs/git-lfs/blob/main/docs/spec.md
https://github.com/git-lfs/git-lfs/blob/main/t/t-install.sh

https://github.com/tj/git-extras/tree/master/bin

https://git-scm.com/docs/gitrepository-layout
https://git-scm.com/docs/git#_git_commands
https://git-scm.com/docs/git-mergetool

```
git config filter.base64.clean 'base64 -i %f'
git config filter.base64.smudge 'base64 -Di %f'
```

or, directly on [git config](./.git/config):

```
[filter "base64"]
	clean = base64 -i %f
	smudge = base64 -Di %f
[filter "secrets"]
	clean = ./secrets-filter.js clean %f
	smudge = ./secrets-filter.js smudge %f
```
