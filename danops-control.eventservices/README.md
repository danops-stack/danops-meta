
# hostname-default

The `hostname-default` file points to the host that should be used be default, e.g.:
* `control`
* `test.control`
* `dev.control`

The content of this file will be changed manually to switch between different versions while testing and using various tools.

The value can be retrievd via public HTTPS as follows:

```bash
echo "HOSTNAME=`curl --silent https://raw.githubusercontent.com/danops-stack/danops-metadata/main/danops-control.eventservices/hostname-default`"
```


# hub.docker.com

Contains mappings of docker image tags. Details in hub.docker.com/README.md

