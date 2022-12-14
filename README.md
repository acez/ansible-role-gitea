ansible-role-gitea
=========

A very simple role to run gitea in a docker container

Requirements
------------

Docker and all dependencies to manage docker containers need to be installed on the target machine for this role to be working.

Role Variables
--------------

| Variable               | Description                                | Default            |
|------------------------|--------------------------------------------|--------------------|
| gitea_filesystem_root  | The filesystem root for gitea data         | /srv/volumes/gitea |
| gitea_container_name   | The container name for the gitea container | gitea              |
| gitea_image_name       | The image used for the gitea container     | gitea/gitea        |
| gitea_image_tag        | The tag used for the gitea container       | 1                  |
| gitea_config_sshd_port | The host port for sshd                     | 2222               |
| gitea_config_http_port | The host port for the web UI               | 3000               |


Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - gitea
```

License
-------

MIT
