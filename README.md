# Ansible biocomputinghub singularity install for RedHat Linux 

### tested versions
Rocky Linux 8.5

### Setup ansible in linux,  the ansible version in epel-release is an old version (2.9) but will still work and is the easiest method to install ansible.
```
sudo dnf update -y
sudo dnf install git -y
sudo dnf install epel-release -y
sudo dnf install ansible -y
```

### clone repo
```
git clone https://github.com/CarstenBaker/biocomputinghub_singularity.git
cd biocomputinghub_singularity/
```

### run playbook

#### -K option at end will prompt for sudo password, this is required for singularity install (if running as root user you can remove the -K)
```
ansible-playbook singularity.yml -K
```

# Ansible biocomputinghub singularity install for Ubuntu

```
sudo apt update -y
sudo apt install ansible
```

#### Singularity needs to be installed as root user, in ubuntu if you are not already root it's best to switch to root using something like this:
```
sudo /bin/bash
```

### clone repo
```
git clone https://github.com/CarstenBaker/biocoputinghub_singularity.git
cd biocomputinghub_singularity/
```

### run playbook

#### running as root user
```
ansible-playbook singularity.yml
```
