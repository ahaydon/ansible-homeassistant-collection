# Ansible Collection for Home Assistant

This collection includes a role to deploy Home Assistant with Podman and systemd.

## Installation

The collection can be installed with `ansible-galaxy`:

```sh
ansible-galaxy collection install git+https://github.com/ahaydon/ansible-homeassistant-collection.git
```

## Usage

```yaml
- role: homeassistant_podman
  homeassistant_podman_user: hass
  homeassistant_podman_home: /home/hass/homeassistant
```

## License

This Ansible collection is [MIT licensed](LICENSE).
