# gve_devnet_dnac_fabric_automation
This is an example of how to create ansible playbooks to setup NVE's and VRFs for DNA Center's fabric.


## Contacts
* Charles Llewellyn

## Solution Components
* DNA Center
*  Ansible

## Related Sandbox Environment
This is as a template, project owner to update

This sample code can be tested using a Cisco dCloud demo instance that contains ** *Insert Required Sandbox Components Here* **



## Prerequisites
**DNA Center Credentials**: In order to use the DNA Center APIs, you need to make note of the IP address, username, and password of your instance of DNA Center. Note these values to add to the credentials_cpoc.yml file during the installation phase.

## Installation/Configuration
1. Clone this repository with `git clone [repository name]`
2. Add the IP address, username, and password that you collected in the Prerequisites section to the ansible/cpoc_credentials.yml file
```
dnac_host:
username:
password:

```
3. change the leaf and spine inventory files to point to your leaf and spine devices. Each inventory file points to only 1 device.
```
device_inventory:
- hostname:
  device_ip:
  device_id:
  version: 17.12.1
  device_family: Switches and Hubs
  role: ACCESS
  site:
  site_id:
```
5. Set up a Python virtual environment. Make sure Python 3 is installed in your environment, and if not, you may download Python [here](https://www.python.org/downloads/). Once Python 3 is installed in your environment, you can activate the virtual environment with the instructions found [here](https://docs.python.org/3/tutorial/venv.html).
6. Install ansible

## Usage
To run the code, use the command:
```
$ ansible-playbook configure_spine.yml
$ ansible-playbook configure_leaf.yml

# Verify Configurations
$ ansible-playbook configuration_validation_master_spine.yml
$ ansible-playbook configuration_validation_master_leaf.yml
```

# Screenshots

![/IMAGES/0image.png](/IMAGES/0image.png)

### LICENSE

Provided under Cisco Sample Code License, for details see [LICENSE](LICENSE.md)

### CODE_OF_CONDUCT

Our code of conduct is available [here](CODE_OF_CONDUCT.md)

### CONTRIBUTING

See our contributing guidelines [here](CONTRIBUTING.md)

#### DISCLAIMER:
<b>Please note:</b> This script is meant for demo purposes only. All tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss incurred with their use.
You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.
