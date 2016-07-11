A Docker image for SWI-Prolog Pengines
========

This docker image is based off the swi-prolog dev packages published on Ubuntu PPA, and creates a Pengines server running on port 3030 with the admin credentials of 'admin:admin' when run.

```
docker run -p 0.0.0.0:3030:3030 -t pengines
```

If you'd like to interact with the Pengines server, run it interactively:
```
docker run -p 0.0.0.0:3030:3030 -i -t pengines
```

You may also prefer to use `--rm` to ensure the container is removed when stopped, since it maps to the 3030 port on the host.

```
docker run --rm -p 0.0.0.0:3030:3030 -i -t pengines
```

By the way, if you are running it interactively, use `halt.` to stop the server.

```
?- halt.
```

If you experience any issues with this image or have any suggestions, please open an Issue or PR.
