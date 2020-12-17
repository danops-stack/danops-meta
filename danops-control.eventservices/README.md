
# hostname-default

The `hostname-default` file points to the host that should be used be default, e.g.

  control
  test.control
  dev.control
  
The value can be retrievd as follows:

```bash
echo "HOSTNAME=`curl --silent https://raw.githubusercontent.com/danops-stack/danops-metadata/main/danops-control.eventservices/hostname-default`"
```

