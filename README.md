# ソフトウェア・クラウド開発プロジェクト実践III レポート課題

Run (at least two) programs on a native OS and a guest OS running on a virtualized CPU.  Compare their performance.

+ Choose programs you suppose that run with or without a performance penalty due to CPU virtualization.
+ You can choose any kinds of programs in any language.
+ Use your available environment.  On Windows, VMWare Player, Virtualbox Docker, and WSL2 (not 1) could be an environment.  However, you can change the problem settings if you don't have such a virtualized CPU.  In this case, mention what you compare for what purpose.
+ Submit a document in the PDF format.  One to two pages document is good enough.


# Requirements

## Python

Python 3.8.6

## Packages

```bash  
$ python3 -m venv .venv  
$ source .venv/bin/activate  
(.venv) $ pip install -r requirements.txt  
```


## Docker

[MacでDockerを使ってubuntu環境を構築する](https://qiita.com/yasuoka_dev/items/073f7e8c7dba75993323)

```bash  
$ docker pull ubuntu:18.04  
$ docker run -it -d --name ubuntu ubuntu:18.04  
$ docker exec -it ubuntu /bin/bash  
```

```bash  
$ adduser k-murakami  
$ gpasswd -a k-murakami sudo  
$ su k-murakami # switch from root to user  
```

### pyenv

See https://github.com/pyenv/pyenv#set-up-your-shell-environment-for-pyenv


```bash  
$ git clone https://github.com/pyenv/pyenv.git ~/.pyenv  
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc  
$ echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc  
$ echo 'eval "$(pyenv init -)"' >> ~/.bashrc  

$ pyenv install 3.8.6  
$ pyenv rehash # if needed  
```

I had to install followings.

```bash  
$ sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev  
$ sudo apt install gcc
```
