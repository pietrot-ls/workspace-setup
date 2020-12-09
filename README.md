# WORKSPACE SETUP

## MACBOOK

#### 1. BASICS

- [Install Chrome](https://www.google.com/intl/en_ca/chrome/)
- [Install Zoom](https://zoom.us/)
- [Install 1Password](https://1password.com/downloads/mac/) 
  > Store the emergency kit saftely (ie. Google Drive)

#### 2. CLI

- [Install iTerm](https://iterm2.com/)
- [Install OhMyZsh](https://github.com/ohmyzsh/ohmyzsh)
- [Configure OhMyZsh Theme](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#half-life)
- [Install Homebrew](https://brew.sh/)

#### 3. PYTHON ENVIRONMENT

**Install pip**

```
$ sudo easy_install pip
```

**Install pyenv**

```
$ brew update && brew install pyenv
```

Append the following to ~/.zshrc

```
# pyenv ----
# To use Homebrew's directories rather than ~/.pyenv
export PYENV_ROOT="/usr/local/var/pyenv"

# To enable shims and autocompletion
if which pyenv > /dev/null; then eval "$(pyenv init -)"; fi
```

#### 4. GIT

https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

**Generate public/private key pair**

```
$ ssh-keygen -t rsa -b 4096 -C "pietro.tortorici@lightspeedhq.com
```

**Ensure ssh-agent is running**

```
$ eval "$(ssh-agent -s)"
$ touch ~/.ssh/config
```

**Append the following to ~/.ssh/config**

```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/ls_github
```

```
$ ssh-add -K ~/.ssh/ls_github
```

**GPG signing**

```
$ brew install gnupg
```

Follow instructions here: https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-gpg-key

#### 5. MISC

```
$ brew install wget curl tig
```
