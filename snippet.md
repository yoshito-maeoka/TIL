# _ _ S N I P P E T _ _

## how to login via ssh without password

generate ssh-key like that:
```
ssh-keygen -t rsa -b 4096
```

add generated public key into new server

define host_shortcut in ~/.ssh/config like:
```
Host host_shortcut
        HostName     (what ever ip address)
        Port         (port number if you need)
        User         (user name for ssh login)
        IdentityFile ~/.ssh/id_rsa

```

then call:

```bash
cat ~/.ssh/id_rsa.pub | ssh host_shortcut 'cat >> ~/.ssh/authorized_keys'
```

```bash
eval `ssh-agent -s`
ssh-add ~/.ssh/id_rsa
```
