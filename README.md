# Mac OS X provisioner

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
$ ansible-playbook localhost.yml -i hosts

# e.g. only install brew packages
$ ansible-playbook localhost.yml -i hosts --tags=brew

# e.g. only install npm packages
$ ansible-playbook localhost.yml -i hosts --tags=npm
```
