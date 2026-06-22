# ansible-role-btrbk
Ansible Role to install and configure btrbk.

> [!note] Note
> SSH Connection for remote volumes/targets to be ensured separately.

## Example

```yaml
- hosts: all
  tasks:
    - ansible.builtin.import_role:
        name: fizbee11.btrbk
      vars:

        btrbk_volumes:
            - path: '/mnt/test/' # volume path,
              snapshot_dir: _btrbk_snap
              target: 'ssh://my-user-host.com/mnt/btr_backup/home'
              subvolumes:
                - @
                - @home
                - @root
                - @srv
```


## Variables
For more configuration options, check `defaults/main.yml`. 

