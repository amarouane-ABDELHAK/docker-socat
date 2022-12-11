# Minimal docker image for Socat

Images are built on top of alpine linux and tagged with alpine releases.
Not that alpine does not support `search` keyword in `/etc/resolv.conf`
so you should use FQDN instead of shortcuts.

## Usage

Instead of running socat, just run this image:

```
docker run --rm -it --net host bobrik/socat <your args>

docker run -d -v /var/run/docker.sock:/var/run/docker.sock -p 2375:2375 bobrik/socat TCP-LISTEN:2375,fork UNIX-CONNECT:/var/run/docker.sock
```
