[![Build Status](
https://travis-ci.org/nickrusso42518/slt-netdevops.svg?branch=master)](
https://travis-ci.org/nickrusso42518/slt-netdevops)

# Safari Live Training - Network DevOps
Source code for the training course. Please contact me with any questions.
Before beginning, be sure you know how to use `git` at a basic level on
your computer. I teach `git` in the course so if you don't know how
to clone this repository yet, do not worry. For this course, only
Linux platforms should be used for the Ansible control/development machine.

> Contact information:\
> Email:    njrusmc@gmail.com\
> Twitter:  @nickrusso42518

  * [Download Instructions](#download-instructions)
  * [Usage](#usage)

## Download Instructions
The easiest way to consume this code is to clone it using SSH or HTTPS.

SSH: `git clone git@github.com:nickrusso42518/slt-netdevops`

or

HTTPS: `git clone https://github.com/nickrusso42518/slt-netdevops`

After cloning, you should see the following file system structure:

```
$ tree
.
├── ansible.cfg
├── hosts.yml
├── LICENSE
├── ntp_config.yml
├── README.md
├── requirements.txt
└── test.yml
```

Ensure you have Python 2.7 or Python 3.6 installed along with pip. Feel
free to use Python `virtualenv` if you'd like to test multiple versions.

> Visit https://www.python.org/downloads/ to download Python.

`sudo python -m ensurepip`

or

`sudo easy_install pip`

You can install the required packages (really just Ansible and a YAML linter)
using the following command:

`pip install -r requirements.txt`

You should have access to the `ansible` command on the correct version.

```
$ ansible --version | head -1
ansible 2.7.7
```

## Usage
This repository is kept minimal since the main point of this course is
teaching the fundamentals of Network DevOps, not Ansible as a specific tool.
  * To edit NTP server variables, open `hosts.yml` and update the
    `ntp_server` variables using valid IPv4 addresses.
  * To run the playbook, run `ansible-playbook ntp_config.yml` from the shell.
  * To test the playbook, run `ansible-playbook test.yml` from the shell. This
    mimics what Travis CI does each time code is committed to Github.
