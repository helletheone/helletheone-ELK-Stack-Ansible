# Ansible Role: Metricbeat [![Build Status](https://travis-ci.org/jradtilbrook/ansible-role-metricbeat.svg?branch=master)](https://travis-ci.org/jradtilbrook/ansible-role-metricbeat)

This role installs and configures Metricbeat 5.x for the Elastic stack.

It has only been designed to work on Ubuntu 16.04, but other Debian flavours
should also work.


## Requirements

None.


## Role Variables

`metricbeat_modules` is a list containing the configuration for each module
Metricbeat should collect data on. See the Metricbeat documentation for the
structure of each list element.

`metricbeat_output` is a dictionary of outputs to send events to. See the
Metricbeat documentation for the structure and possible outputs.

`metricbeat_general_config` is the general global configuration of Metricbeat. Eg.
the name, extra fields or tags to apply to each event. More info can be found in
the Metricbeat documentation.

`metricbeat_install_state`: This is useful for updating Metricbeat to newer
versions after it has already been installed. Use `latest` to achieve this
functionality.


## Resources

Documentation related to Metricbeat can be found at the links below:

- [documentation](https://www.elastic.co/guide/en/beats/metricbeat/current/metricbeat-overview.html)


## Dependencies

None.

Check out my other roles on [Ansible Galaxy](https://galaxy.ansible.com/jradtilbrook)
if you are installing the entire Elastic Stack.


## Example Playbook

```yaml
- hosts: servers
  become: yes

  roles:
    - role: jradtilbrook.metricbeat
```


## License

MIT
