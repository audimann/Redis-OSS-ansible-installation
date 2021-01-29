# Redis-OSS-ansible-installation
A simple playbook to install the Redis Opensource on Linux. 

## Requirements
Ansible must be installed on the server you want to deploy Redis on. This is typically done installing an existing package

```bash
apt-get install ansible
```

If the system package is unavailable or not available in a newer version, you can also install Ansible through the pip (or pip3) tool

```bash
pip install ansible
```

## Usage
```bash
ansible-playbook install_redis_oss.yaml
```
As the playbook requires sudo permissions for some tasks you might have to add the commandline flag "-K" to get prompted for the sudo privilege escalation (depending on your sudoers configuration).
You should set the variables in the vars.yaml file. Currently, the following variables can be set:
- **version** specifies the Redis version to download
- **build_directory** is the directory used to build the Redis executables
- **data_directory** is the directory where redis stores its data


## Platforms Tested
In its initial release, the playbook was only tested on:
- Ubuntu 18.04 with Ansible 2.5.1
- Ubuntu 16.04 with Ansible 2.10.5

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Authors and acknowledgment
Michael Ehrig (michael.ehrig@email.de)

## License
[MIT](https://choosealicense.com/licenses/mit/)
