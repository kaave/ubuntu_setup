# Ubuntu setup

## Checked OS

- Linux Mint 18.1 (Mate)

## Setup

### change default editor(visudo etc)

```bash
sudo update-alternatives --config editor
```

### add sudo throw

```text
USER_NAME ALL=(ALL) NOPASSWD: ALL
```

### update system

```bash
sudo apt-get -y update && sudo apt-get upgrade
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

