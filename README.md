# CKAN

**Description**:  A simple vagrant box with provisioning scripts to stand up an out-of-the-box version of CKAN.  

Other things to include:

  - **Technology stack**: 
   - Python 2.7
   - Apache
   - Postgres
   - Solr
   - CKAN
  - **Status**:  1.0  Should be stable but we are still making refinements and looking for feedback

## Dependencies
- **Vagrant / Virtualbox** - creates the VM that is built by Ansible.  
Installation instructions can be found here: http://docs.vagrantup.com/v2/installation/
- **Ansible** - provisions the VM.  
    Installation: `pip install ansible` from your python virtual environment

## Installation

1. `vagrant up`
2. Once provisioning completes, open your browser to [localhost:8080](http://localhost:8080) and you should see CKAN

### Starting / Stopping the VM
To start the vagrant box: `vagrant up`  
To stop the vagrant box: `vagrant halt`  

## Getting Started
For information about how to use CKAN, please see the [official documentation](http://docs.ckan.org/en/latest/user-guide.html)

**Customizing Look and Feel**  
See the section on [Customizing Look and Feel](http://docs.ckan.org/en/latest/sysadmin-guide.html#customizing-look-and-feel) in the official documentation

## Developers

Check out the [Guide to Extending](http://docs.ckan.org/en/latest/extensions/tutorial.html) in the offical documentation

### Customizing this VM  
If you make any changes to the `provisioners/group_vars/local` or any of the default variables, you will need to re-provision the VM.  Simply run `vagrant provision` and the changes will be applied.  

## How to test the software

At the moment there are no tests for this codebase.  

## Known issues

None

## Getting help

If you have questions, concerns, bug reports, etc, please file an issue in this repository's Issue Tracker.

## Getting involved

Please see our [CONTRIBUTING](CONTRIBUTING.md) file for more information about contributing

## Troubleshooting  

### Solr 
If you can't seem to access solr in Vagrant (checking http://localhost:8983/solr), try stopping the iptables service:
`sudo service iptables stop`

----

## Open source licensing info
1. [TERMS](TERMS.md)
2. [LICENSE](LICENSE)
3. [CFPB Source Code Policy](https://github.com/cfpb/source-code-policy/)


----

