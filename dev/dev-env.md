## Local Host

```sh
cd ~/.ssh

mv path/to/id_rsa ./
mv path/to/id_rsa.pub ./

chmod 400 id_rsa

# copy .pub file to remote host
# -p 36000
ssh-copy-id -i id_rsa.pub user@remote-host-ip

vim config
```

## Remote Host

### ssh

```sh
cd ~/.ssh

mv path/to/id_rsa ./

chmod 400 id_rsa

vim config
```

### zsh

```sh
# install oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# install plugins
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

vim .zshrc
```

```sh
# .zshrc

plugins=(zsh-autosuggestions zsh-syntax-highlighting nvm ssh-agent git gitignore)

# custom alias
```

### git

Update git

- [How To Install Git on CentOS 7](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-7)
- [yum install curl-devel](https://stackoverflow.com/questions/8329485/unable-to-find-remote-helper-for-https-during-git-clone)

```sh
git config --global user.name '[name]'
git config --global user.email '[email]'
git config --global color.ui auto
```

### vim

Update vim

- [How To Install Vim 8.2 On CentOS 7](https://phoenixnap.com/kb/how-to-install-vim-centos-7)

```sh
# YouCompleteMe require >= python2.7 and >=python3.6

# add python3
yum install ctags git tcl-devel \
ruby ruby-devel \
lua lua-devel \
luajit luajit-devel \
python python-devel \
python3 python3-devel \
perl perl-devel \
perl-ExtUtils-ParseXS \
perl-ExtUtils-XSpp \
perl-ExtUtils-CBuilder \
perl-ExtUtils-Embed

# add python3 interp
./configure --with-features=huge \
--enable-multibyte \
--enable-rubyinterp \
--enable-pythoninterp \
--enable-python3interp \
--with-python3-config-dir=/usr/lib/python3.6/config \
--enable-perlinterp \
--enable-luainterp
```

```sh
# .vimrc
:r $VIMRUNTIME/vimrc_example.vim
```

```sh
set number

set tabstop=2
set shiftwidth=2
set softtabstop=2
set expandtab
```

### node

```sh
# install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.36.0/install.sh | bash

# install lts node
nvm install --lts

# npm setting
npm config set registry https://registry.npm.taobao.org
# http://r.tnpm.oa.com
```

### docker

```sh
# Error response from daemon: could not find an available,
# non-overlapping IPv4 address pool among the defaults to
# assign to the network
# https://github.com/docker/for-linux/issues/599#issuecomment-466345951
docker network create 'localhost' --subnet='172.17.0.0/16'

# vim daemon.json
# change registry-mirrors

# install docker-compose (as a container)
# https://docs.docker.com/compose/install/#install-as-a-container
sudo curl -L --fail https://github.com/docker/compose/releases/download/1.27.4/run.sh -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```
