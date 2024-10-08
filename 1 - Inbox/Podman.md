---
created: 2024-01-02
modified: 2024-09-03T17:07:55+02:00
---

[[1 - Inbox/Podman]] is a alternative container runtime to [[Docker]].

## Machine

To use it on [[1 - Inbox/Disable insecure SMB1 support on macOS]] or [[1 - Inbox/Windows]] we need to create a [[Linux]] [[VM]] that ships the podman environment. We can create this machine with

```
podman machine init
podman machine start
```

To log into this machine we can use `podman machine ssh`

We reboot the machine with

```
podman machine stop
podman machine start
```

## Rootless

One of the advantages of podman is the capability to run without a daemon that possesses root capabilities. We can switch between `rootful` and `rootless`

```
podman set --rootful=<true|false>
```

## Useful commands

```shell
# pull images
podman pull <image>
# show images
podman images
# show running containers
podman ps
# show all containers
podman ps -a

```
