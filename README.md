
Launch incus container with:-

```
incus launch images:fedora/42/cloud container-name --config=user.user-data="$(cat fedora-42.yml)" --config security.nesting=true
```

## Todos
- [ ] Use https://github.com/Schniz/fnm
