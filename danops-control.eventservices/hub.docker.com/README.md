
# danops-control.eventservices-webapps--latest

The `danops-control.eventservices-webapps--latest` file contains an alternative but fixed Docker tags that points to the same Docker image.

Example content:
```
danops-control.eventservices-webapps--20201216-0000
```

The content of this file will be automatically written by the CI during Docker image build in https://app.circleci.com/pipelines/github/danops-stack/danops-control.eventservices-webapps configured by [danops-stack/danops-control.eventservices-webapps/.circleci/config.yml](https://github.com/danops-stack/danops-control.eventservices-webapps/blob/master/.circleci/config.yml).


The value can be retrievd via public HTTPS as follows:

```bash
echo "DOCKER_TAG_DEPLOYVERSION=`curl --silent https://raw.githubusercontent.com/danops-stack/danops-metadata/main/danops-control.eventservices/hub.docker.com/danops-control.eventservices-webapps--latest`"
```

