This was stolen from https://www.atlassian.com/git/tutorials/dotfiles

## Install your dotfiles onto a new system (or migrate to this setup)

If you already store your configuration/dotfiles in a [Git repository](https://www.atlassian.com/git), on a new system you can migrate to this setup with the following steps:

-   Prior to the installation make sure you have committed the alias to your `.bashrc` or `.zsh`:

```bash
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```

-   And that your source repository ignores the folder where you'll clone it, so that you don't create weird recursion problems:

```bash
echo ".cfg" >> .gitignore
```

-   Now clone your dotfiles into a [bare](http://www.saintsjd.com/2011/01/what-is-a-bare-git-repository/) repository in a "_dot_" folder of your `$HOME`:

```bash
git clone --bare <git-repo-url> $HOME/.cfg
```

-   Define the alias in the current shell scope:

```bash
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```

-   Checkout the actual content from the bare repository to your `$HOME`:

```undefined
config checkout
```

-   The step above might fail with a message like:

```js
error: The following untracked working tree files would be overwritten by checkout:
    .bashrc
    .gitignore
Please move or remove them before you can switch branches.
Aborting
```

This is because your `$HOME` folder might already have some stock configuration files which would be overwritten by Git. The solution is simple: back up the files if you care about them, remove them if you don't care. I provide you with a possible rough shortcut to move all the offending files automatically to a backup folder:

```bash
mkdir -p .config-backup && \
config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | \
xargs -I{} mv {} .config-backup/{}
```

-   Re-run the check out if you had problems:

```undefined
config checkout
```

-   Set the flag `showUntrackedFiles` to `no` on this specific (local) repository:

```bash
config config --local status.showUntrackedFiles no
```

-   You're done, from now on you can now type `config` commands to add and update your dotfiles:

```bash
config status
config add .vimrc
config commit -m "Add vimrc"
config add .bashrc
config commit -m "Add bashrc"
config push
```

Again as a shortcut not to have to remember all these steps on any new machine you want to setup, you can create a simple script, [store it as Bitbucket snippet](https://bitbucket.org/snippets/nicolapaolucci/7rE9K) like I did, [create a short url](http://bit.do/) for it and call it like this:

```bash
curl -Lks http://bit.do/cfg-install | /bin/bash
```

For completeness this is what I ended up with (tested on many freshly minted [Alpine Linux](http://www.alpinelinux.org/) containers to test it out):

```bash
git clone --bare https://bitbucket.org/durdn/cfg.git $HOME/.cfg
function config {
   /usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME $@
}
mkdir -p .config-backup
config checkout
if [ $? = 0 ]; then
  echo "Checked out config.";
  else
    echo "Backing up pre-existing dot files.";
    config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | xargs -I{} mv {} .config-backup/{}
fi;
config checkout
config config status.showUntrackedFiles no
```