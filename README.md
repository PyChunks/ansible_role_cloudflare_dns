Role Name
=========

Creates basic DNS records for a Cloudflare registered domain

Requirements
------------

This role is dependant on the `Ansible Community General collection` available from Ansible-galaxy.

```
ansible-galaxy collection install community.general
```

Role Variables
--------------

Variables that need to be set:
```yaml
domain: 
user_email: 
secret_token: 
remote_ip:
```

Where: 
`domain` is the domain you wish to create a record for (needs to be registered to your Cloudflare account).

`user_email` is the email associated to the Cloudflare account. 

`secret_token` is the api token associated to user.

`remote_ip` is the public ip of the webserver you wish to set the record to

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  vars:
    domain: example.com 
    user_email: yourEmail@example.com 
    secret_token: api_token 
    remote_ip: webserver_public_ip
  roles:
     - ansible_role_cloudflare_dns
```

License
-------

BSD

Author Information
------------------

Created by Vincent D-Gauthier
