# Ubuntu setup

## Checked OS

- Linux Mint 18.1 (Mate)

## Setup

### change default editor(visudo etc)

```bash
# choose best editor
sudo update-alternatives --config editor
```

### add sudo throw

```text
# TODO: not enable setting
USER_NAME ALL=NOPASSWD: ALL
```

### update system

```bash
sudo apt-get -y update && sudo apt-get -y upgrade
```

### install ansible

```bash
sudo apt-get -y install ansible
```

### get dotfiles and setup files

```bash
# use your dotfiles
git clone https://github.com/kaave/ubuntu_setup ~/ubuntu_setup
```

### run ansible

```bash
ansible-playbook -i ~/ubuntu_setup/hosts -vv ~/ubuntu_setup/ubuntu1604.yml
```

### after ansible

#### install other apps

- Web browsers
    - Google Chrome
    - Firefox developer edition
    - Vivaldi
    - Blisk
- Developments
    - Visual Studio Code
    - Jetbrains toolbox
    - GitKraken
    - Slack
    - rdm
    - robomongo
- Windows apps (dependency wine)
    - [1password](https://ry0.github.io/blog/2015/04/12/ubuntu-1password/)

#### create key

```bash
ssh-keygen
```

##### and add keys on web services

- GitHub
- Bitbucket
- Office tools

#### setting Terminal

```bash
# theme
git clone https://github.com/oz123/solarized-mate-terminal
cd solarized-mate-terminal && ./solarized-mate.sh
# font
```

#### setting Visual Studio Code

- install `Setting sync`
    - GistID: 9f4a74a7c814a9036fb1db5a5d70e04d

#### setting Jetbrains tools

#### Join Docker group development users

```bash
# Must log out and log back after exec command.
sudo usermod -aG docker $USER
```

