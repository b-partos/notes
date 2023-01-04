# Configure the `ssh-client` to use a custom key and host configuration

When there are more than 1 ssh keyfiles, git operations on github may fail because the git client will try to use one that is not registered in the github account.

As a workaround, a config file can be created in the `.ssh` directory.

```config
# ~/.ssh/config

Host personal-github # The custom host name
  HostName github.com
  IdentityFile ~/.ssh/personal_github_key # The keyfile name
  User git

Host other-github # The custom host name
  HostName github.com
  IdentityFile ~/.ssh/other_github_key # The keyfile name
  User git

```

Then the custom host can be used to clone the repository.

```
$ git clone git@personal-github:my-name/repo-name.git
```

It can also be set for an existing repository as well.

```
$ git remote remove origin
$ git remote add origin git@personal-github:my-name/repo-name.git
```

## Referenes:
[StackExchange answer](https://superuser.com/a/1519694)

