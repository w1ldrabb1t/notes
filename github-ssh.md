`sudo ssh-copy-id -i github-personal-key w1ldrabb1t@linux-lite-vm`
This didn't work so good.


`git remote add origin git@github:your-username/your-repo.git`
where git@github matches the Host config at `~/.ssh/config`
like so...

```
Host github
        Hostname github.com
        User git
        IdentityFile ~/.ssh/github-username-key

```
