+++
title = "Удаленный доступ через SSH"
menuTitle = "SSH / RCON"
weight = 3
+++

Vanilla Nox supported a telnet-based remote console (RCON) which allowed to control Nox server remotely.

OpenNox completely drops telnet support in favor of SSH-based remote console.

{{% notice info %}}
OpenNox only _emulates_ SSH protocol. It **does not** allow accessing the host machine via SSH.
{{% /notice %}}

To enable RCON, OpenNox must be started with an additional argument:

```shell
opennox --rcon=:18522 --rcon-pass=my-secret-password
```

This will allow SSH connections on port `18522` with a password `my-secret-password`:

```shell
ssh -p 18522 127.0.0.1
```

```

  /888888                                /88   /88           /88   /88
 /88__  88                              | 888 | 88          | 88  / 88
| 88  \ 88  /888888   /888888  /8888888 | 8888| 88  /888888 |  88/ 88/
| 88  | 88 /88__  88 /88__  88| 88__  88| 88 88 88 /88__  88 \  8888/
| 88  | 88| 88  \ 88| 88888888| 88  \ 88| 88  8888| 88  \ 88  >88  88
| 88  | 88| 88  | 88| 88_____/| 88  | 88| 88\  888| 88  | 88 /88/\  88
|  888888/| 8888888/|  8888888| 88  | 88| 88 \  88|  888888/| 88  \ 88
 \______/ | 88____/  \_______/|__/  |__/|__/  \__/ \______/ |__/  |__/
          | 88
          | 88        Version: v1.8.x (xxxxxxxxx)
          |__/

user@opennox:~$
```

From here, all [console commands]({{% relref "opennox/dev/console" %}}) will work the same way as via in-game console.
A good starting point is a `help` command.