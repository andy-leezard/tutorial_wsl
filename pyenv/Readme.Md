# Install pyenv on Debian

Update : it works on Ubuntu too.

## Install dependencies
```
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev
```

## Install pyenv
```
curl https://pyenv.run | bash
```

## Configure environment variables

1. Open up ~/.bashrc or ~/.zshrc if you're using zsh.
2. At the moment of pyenv install, it gives an instruction in the shell. It basically tells you to copy and paste some commands as below.

```
# Load pyenv automatically by appending the following:
export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# Load pyenv-virtualenv automatically by adding the following:
eval "$(pyenv virtualenv-init -)"
```

## Reset the terminal

```
exec $SHELL
```

## Check out the pyenv version

```
pyenv -v
```

## Install Python versions

1. List available versions : **`pyenv install --list`**

- Example :

```
pyenv install 3.11.1
```

Set the installed version as the default local (to this terminal session) or global (entire system):

```
pyenv local 3.10.0
```

## Check Python and pip version

```
python3 -V
pip3 -V
```

## Install Django

```
pip3 install Django
django-admin --version
```