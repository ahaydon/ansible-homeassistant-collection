Ansible Role: Home Assistant
=========

An Ansible role for deploying Home Assistant as a Podman container managed by systemd.

Requirements
------------

None.

Role Variables
--------------

```yaml
homeassistant_podman_version: stable
homeassistant_podman_user: hass
homeassistant_podman_group: "{{ homeassistant_podman_user }}"
homeassistant_podman_home: /home/hass/homeassistant
homeassistant_podman_network: homeassistant
```

Dependencies
------------

- [ahaydon.podman](https://github.com/ahaydon/ansible-podman-collection) is used by the `homeassistant_podman` role.

Example Playbook
----------------

```yaml
- name: Deploy Home Assistant
  hosts: all
  roles:
    - role: homeassistant_podman
      homeassistant_podman_user: "{{ homeassistant_user }}"
      homeassistant_podman_home: "{{ podman_user_home }}"
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon)
