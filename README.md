# Ansible-network_udld

Ansible role that configures udld global settings on network devices.  

The configuration of the role is done so that it shouldn't be necessary to modify the role for any configuration.
All settings can be configured by changing role parameters or by declaring new config as variable.

Please report any issues or send PR.

nxos specific: feature udld has to be enabled.

## Examples

```yaml
---
- name: Example of how to enable aggressive udld
  hosts: switches
  vars:
    udld:
        state: present
        aggressive: enabled
        msg_time: 15
      #  reset: true                     # when set to true, resets all ports shut down by udld. state cannot be 'absent' when this present
  roles:
    - Ansible-network_udld

```

## Role variables

```yaml
---
# Define the udld global settings to be configured (see README for examples)
udld: { }
```


## License

Apache


## Author

Dan Murarasu