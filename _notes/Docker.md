## Bridge vs Host

Bridge means you need to use a reverse proxy to map to particular ports. Host means making it available on the same network stack as the host running Docker, so you need to use different ports

> If you want to deploy multiple containers connected between them with a private internal network use bridge networking. If you want to deploy a container connected to the same network stack as the host (and access the same networks as the host) use host networking.

> Host networking completely disables Docker's network isolation. It means containers see and use exactly the same network interfaces the host has available, without an intermediate NAT layer.