# Vbox Deploy Ansible role
![Logo](logo.gif)

This role ...

## Role Variables

Below are the available varaibles you will need to supply to the role.

| Variable | Description | Var Type | Example |
| --- | --- | --- | --- |
| vbox_user | User used in the deploy | String | vbox_user: user | 
| vbox_dir_isos | Directory containing the isos | String | vbox_dir_isos: "/home/{{ vbox_user }}/ImagesISOs" | 
| vbox_dir_vms | Directory containing the VMs | String | vbox_dir_vms: "/home/{{ vbox_user }}/VMs" |
| vbox_images_isos | public key file (absolute path) to set into remote system | List containing dictionaries |  vbox_images_isos: List {} {}|
| vbox_custom_isos | SSH port to connect to | List containing dictionaries | vbox_custom_isos: - {name: ..., url: ..., path: ...} | 
| vbox_vms_options | SSH port to connect to | List containing dictionaries | vbox_vms_options: - {} {} | 

## Example Playbook

```yaml
---
- name: Vbox Deploy Role
  hosts: localhost

  roles:
    - role: vbox_deploy_role
      vars:
        
```

## License

GPLv3

## Author Information

Javier Sánchez Bracamonte
