# docker-pimatic
Dockerfile for pimatic with specific version of node.js

To build execute the following commands:
```bash
docker build -t wowthur/node:4.8.3 -f Dockerfile-wowthur-node-4.8.3
docker build -t wowthur/pimatic:0.9.42 -f Dockerfile-wowthur-pimatic-0.9.42
```

Then start a new docker container with:
```bash
docker run -p 80:80 -i -t wowthur/pimatic:0.9.42
```

This will start pimatic in foreground the first time so you can see if all plugins get downloaded and if there are any errors.

After first startup you can Ctrl-C out of container and start in background with:
```bash
docker run <container-id>
```
