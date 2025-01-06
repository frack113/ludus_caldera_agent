# Ansible Role: Caldera Agent

An Ansible Role that installs [Caldera Agent](https://caldera.mitre.org/) on windows .


## Requirements

- Caldera Server role
- windows host

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    # Name of the windows payload
    ludus_caldera_windows_agent_name: 'C:\Users\Public\splunkd.exe'


## Dependencies

Caldera Server

## Example Playbook


## Example Ludus Range Config

```yaml
ludus:
  - vm_name: "{{ range_id }}-win11-22h2-enterprise-x64-1"
    hostname: "{{ range_id }}-WIN11-22H2-1"
    template: win11-22h2-x64-enterprise-template
    vlan: 10
    ip_last_octet: 21
    ram_gb: 8
    cpus: 4
    windows:
      install_additional_tools: false
    roles:
      - frack113.ludus_caldera_agent
```

## License

[//]: # (If you change the License type, be sure to change the actual LICENSE file as well)
GPLv3

## Author Information

This role was created by [frack113](https://github.com/frack113), for [Ludus](https://ludus.cloud/).
