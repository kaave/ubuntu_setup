# Ubuntu setup

## Checked OS

- Ubuntu Gnome 16.04 64bit

## Setup

### change default editor(visudo etc)

```bash
# choose best editor
sudo update-alternatives --config editor
```

### add sudo throw

```text
USER_NAME ALL=(ALL:ALL) NOPASSWD:ALL
```

### change mirror server

```bash
sudo sed -i.bak -e "s%http://[^ ]\+%http://ftp.jaist.ac.jp/pub/Linux/ubuntu/%g" /etc/apt/sources.list
```

### update system

```bash
sudo apt-get -y update && sudo apt-get -y upgrade
```

### install build tools

```bash
sudo apt-get -y install build-essential git
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
    - Firefox
    - Firefox developer edition
    - Vivaldi
- Developments
    - Atom
    - Visual Studio Code
    - Jetbrains toolbox
    - GitKraken
    - Slack
    - rdm
    - robomongo
- Utility
    - Dropbox
    - Enpass

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

