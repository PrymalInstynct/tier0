# Tier 0

## Third Party Repos
### EPEL 7
`sudo rpm --import https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-7`

```
[epel]
name=Extra Packages for Enterprise Linux 7 - $basearch
# It is much more secure to use the metalink, but if you wish to use a local mirror
# place its address here.
#baseurl=http://download.example/pub/epel/7/$basearch
metalink=https://mirrors.fedoraproject.org/metalink?repo=epel-7&arch=$basearch&infra=$infra&content=$contentdir
failovermethod=priority
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7
```
### EPEL 8
`sudo rpm --import https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-8`

```
[epel]
name=Extra Packages for Enterprise Linux 8 - $basearch
# It is much more secure to use the metalink, but if you wish to use a local mirror
# place its address here.
#baseurl=https://download.example/pub/epel/8/Everything/$basearch
metalink=https://mirrors.fedoraproject.org/metalink?repo=epel-8&arch=$basearch&infra=$infra&content=$contentdir
enabled=1
gpgcheck=1
countme=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-8
```
### VSCode Repo

`sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc`

```
[code]
name=Visual Studio Code
baseurl=https://packages.microsoft.com/yumrepos/vscode
enabled=1
gpgcheck=1
gpgkey=https://packages.microsoft.com/keys/microsoft.asc
```

## Red Hat Enterprise Linux 7 (adm01/02)

### Required Repos
- rhel-7-workstation-rpms
- rhel-7-workstation-optional-rpms
- rhel-7-workstation-extras-rpms
- epel7
- vscode

### Required YUM Packages
- ansible
- code
- git
- nfs-utils
- python2
- python2-pip
- vim
- yum-utils

### Required Python2 Pip Packages
- setuptools-44.1.1-py2.py3-none-any.whl
- pip-20.3.4-py2.py3-none-any.whl
- wheel-0.37.1-py2.py3-none-any.whl
- certifi-2021.10.8-py2.py3-none-any.whl
- chardet-4.0.0-py2.py3-none-any.whl
- idna-2.10-py2.py3-none-any.whl
- ptyprocess-0.7.0-py2.py3-none-any.whl
- pexpect-4.8.0-py2.py3-none-any.whl
- urllib3-1.26.10-py2.py3-none-any.whl
- six-1.16.0-py2.py3-none-any.whl
- pyvmomi-7.0.3.tar.gz

### Ansible Roles
- provision01
- vcenter

### Ansible Collections
- ansible-posix-1.4.0.tar.gz
- ansible-utils-2.6.1.tar.gz
- community-general-5.3.0.tar.gz
- community-hashi_vault-3.1.0.tar.gz
- community-sops-1.2.3.tar.gz
- community-vmware-2.7.0.tar.gz
- kubernetes-core-2.3.2.tar.gz

## Red Hat Enterprise Linux 8 (adm01/02)

### Required Repos
- rhel-8-for-x86_64-baseos-rpms
- rhel-8-for-x86_64-appstream-rpms
- codeready-builder-for-rhel-8-x86_64-rpms
- epel8
- vscode

### Required DNF Packages
- ansible-core
- code
- git
- nfs-utils
- python38
- python38-pip
- vim
- yum-utils

### Required Python3.8 Pip Packages
- setuptools-63.2.0-py3-none-any.whl
- pip-22.1.2-py3-none-any.whl
- wheel-0.37.1-py2.py3-none-any.whl
- certifi-2022.6.15-py3-none-any.whl
- charset_normalizer-2.1.0-py3-none-any.whl
- idna-3.3-py3-none-any.whl
- ptyprocess-0.7.0-py2.py3-none-any.whl
- pexpect-4.8.0-py2.py3-none-any.whl
- urllib3-1.26.10-py2.py3-none-any.whl
- requests-2.28.1-py3-none-any.whl
- six-1.16.0-py2.py3-none-any.whl
- pyvmomi-7.0.3.tar.gz

### Ansible Roles
- provision01
- vcenter

### Ansible Collections
- ansible-posix-1.4.0.tar.gz
- ansible-utils-2.6.1.tar.gz
- community-general-5.3.0.tar.gz
- community-hashi_vault-3.1.0.tar.gz
- community-sops-1.2.3.tar.gz
- community-vmware-2.7.0.tar.gz
- kubernetes-core-2.3.2.tar.gz