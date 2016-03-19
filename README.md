# Mac OS X Provisioner

## Usage

### Prepare

```bash
$ brew update
$ brew install ansible
```

### Install

```bash
$ git clone https://github.com/kenjis/mac-os-x-setup-ansible.git
$ cd mac-os-x-setup-ansible/
$ cp vars.yml.placeholder vars.yml
```

### Execute

```bash
# e.g. execute all
$ ansible-playbook -vvv -i hosts localhost.yml

# e.g. only install brew packages
$ ansible-playbook -vvv -i hosts --tags=brew localhost.yml

# e.g. only install npm packages
$ ansible-playbook -vvv -i hosts --tags=npm  localhost.yml
```
