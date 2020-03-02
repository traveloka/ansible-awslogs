# shared/awslogs #

Installs and configures AWS CloudWatch Logs agent.

## Requirements ##

Ansible 2.0, pip

## Role Variables ##

These variables are not set in this role, but can be used:

   - name: awslogs_access_key_id
     desc: aws access_key_id to stream the log

   - name: awslogs_secret_access_key
     desc: aws secret_access_key to stream the log

   - name: virtualenv_version
     desc: version of virtualenv to be installed if `virtualenv_state` is set to `present`

### Defaults ##

See `defaults/main.yml`

## Dependencies ##

- shared/pip

## Example Playbook ##

    - hosts: servers
      vars:
        awslogs_access_key_id: "youraccesskey"
        awslogs_secret_access_key: "yoursecretkey"
      roles:
         - shared/awslogs

## License ##

MIT

## Author Information ##

https://github.com/sshvetsov
