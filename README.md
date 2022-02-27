# Sporadic Log

a.k.a., random notes.

GitHub Pages site:

- https://sporadically.github.io/log/

Source repository

- https://github.com/sporadically/log

## Git Config

### Account-level Git Config

```bash
git config --global user.email your@email.com
git config --global user.name "Your Name"
```

The result of the above commands is stored in `~/.gitconfig` file.

On the command line,
`git config --global --list` returns account-wide config.

### Repository-specific Git Config

To use repository-specific `user.email` and `user.name`,
go to the local repository folder and
use `git config user.email` and `git config user.name`
without the `--global` option.

```bash
cd <local_repository>
git config user.email your@email.com
git config user.name "Your Name"
```

The result of the above commands is stored in
`.git/config` file in the repository.

## If Permission Denied by Git Push

If you receive the "**Permission denied (publickey)**" error
from `git push`,
try the following.
This will open the browser and
GtiHub Credential Manager lets you set up the access.

```bash
git remote set-url origin https://<username>@github.com/<username>/<repo>.git
```

The result of the above command is stored in
the `[remote "origin"]` section of `.git/config` file.
