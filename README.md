Ansible module used by OSAS to create a swapfile.

## Usage

The module only serve for initial provisioning of a swap file, and cannot be used
to increase or decrease the size of the swap. 

To use it, just declare the role on a system like this:

```
$ cat deploy_server.yml
- hosts: server
  roles:
  - role: swap_file
    size: 10G
    path: /var/swap   
