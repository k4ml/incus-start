
Launch incus container with:-

```
incus launch images:fedora/42/cloud container-name --config=user.user-data="$(cat fedora-42.yml)" --config security.nesting=true
```

When using fish, `cat filename.yml` doesn't work. Use:-

```
lxc init ubuntu:24.04 kamal-medan-02
lxc config set kamal-medan-02 cloud-init.user-data - < ubuntu-24.yml
lxc config set kamal-medan-02 security.nesting true
lxc start kamal-medan-02
```

Check cloud-init running:-

```
lxc exec kamal-medan-02 -- tail -f /var/log/cloud-init-output.log
```

## Todos
- [ ] Use https://github.com/Schniz/fnm
