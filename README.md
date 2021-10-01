# 1. Installing Nautobot on Red Hat Enterprise Linux - A Complete Walk Through

## 1.1. Table of Contents

<<<<<<< HEAD
- [Installing Nautobot on Red Hat Enterprise Linux - A Complete Walk Through](#installing-nautobot-on-red-hat-enterprise-linux---a-complete-walk-through)
  - [Table of Contents](#table-of-contents)
  - [Future Plans](#future-plans)
  - [Pre-requisites](#pre-requisites)

This is meant to assist users in installing Nautobot on Red Hat Enterprise Linux. I will go through the process of installation, hardening, and STIG implementation. This will be all done on a Virtual Machine. In addition, I will be using the ansible-playbook for the RHEL 8 STIG implementation. Please refer to the resources directory for the links to these repositories. Also, if you are not familiar with the dependencies of Nautobot, I highly recommend that you do some reading because nautobot consists of a rather diverse Application Stack.

## Future Plans
=======
- [1. Installing Nautobot on Red Hat Enterprise Linux - A Complete Walk Through](#1-installing-nautobot-on-red-hat-enterprise-linux---a-complete-walk-through)
  - [1.1. Table of Contents](#11-table-of-contents)
  - [1.2. Future Plans](#12-future-plans)
  - [1.3. Pre-requisites](#13-pre-requisites)
  - [1.4. Resources](#14-resources)

This is meant to assist users in installing Nautobot on Red Hat Enterprise Linux. I will go through the process of installation, hardening, and STIG implementation. This will be all done on a Virtual Machine. In addition, I will be using the ansible-playbook for the RHEL 8 STIG implementation. Please refer to the resources directory for the links to these repositories. Also, if you are not familiar with the dependencies of Nautobot, I highly recommend that you do some reading because nautobot consists of a rather diverse Application Stack.

## 1.2. Future Plans
>>>>>>> aeecf4cbe155b40f3c17bb08787b1eaf66f08a5f

- [X] Add Step by Step [LDAP](https://github.com/beholdenkey/Installing-Nautobot-on-RHEL-A-Complete-Walk-Through/tree/main/Configurations/LDAP) instructions for Nautobot and update nautobot_config.py template with changes
- [ ] Complete the [setup.sh](https://github.com/beholdenkey/Installing-Nautobot-on-RHEL-A-Complete-Walk-Through/blob/d6275765266b6b4ff4e1bfcdc989ecdc7662ecf4/SECURITY.md) script.
- [ ] Add compatibility Checks to [setup.sh](https://github.com/beholdenkey/Installing-Nautobot-on-RHEL-A-Complete-Walk-Through/blob/d6275765266b6b4ff4e1bfcdc989ecdc7662ecf4/SECURITY.md) script.
- [ ] Create a Table of Contents
- [ ] Create Installation/Upgrade Playbook
- [ ] Build RHEL Kickstart to support the STIG requirements for storage partitions.
- [ ] Create Red Hat Universal Basic Image Nautobot container images.
- [ ] Add STIG Partitioning Guide and Ratio's
- [X] Move development content from [Pandoras Box](https://github.com/beholdenkey/Pandoras-box) to this repository.
- [X] Create how to instructions for [RedHatGov STIG Playbook](https://github.com/RedHatGov/rhel8-stig-latest)

## 1.3. Pre-requisites

Minimum VM Resource Requirements:
>Note: These are the minimum requirements these are not the recommended requirements for a production environment.

- vCores - 4
- Memory - 8 GiB
- Storage - 125 GiB

Nautobot has the following minimum version requirements for its dependencies:

- Python: 3.6
- PostgreSQL: 9.6
- Redis: 4.0

Dependency versions I have successfully used on production Nautobot Server:

- Python: 3.9.6
- PostgreSQL: 13.3-4
- Redis 5.2

>Note if you are not using the latest version of python and would like to install the latest version from source please go to the following [Python](https://github.com/beholdenkey/Installing-Nautobot-on-RHEL-A-Complete-Walk-Through/blob/main/Resources/python_install.sh) However you can also install latest python available for that OS through the following commands

```bash
dnf -y install \
    python39 \
    python39-devel \
    python39-pip
```

## 1.4. [Resources](https://github.com/beholdenkey/Installing-Nautobot-on-RHEL-A-Complete-Walk-Through/tree/main/Resources)

The resources directory contains materials that can be useful when it comes to using this repository.
