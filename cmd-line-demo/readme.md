# Docker Technical Demo

Pull down ghost

```docker pull ghost```

Inspect the dockerfile:

From Kitematic, click [View on Dockerhub](https://hub.docker.com/_/ghost)

[Show docker cli documentation](https://docs.docker.com/engine/reference/commandline/cli/)

Check documentation of the container

```docker images```

```docker run -d -p 3001:2368 --name myghost ghost:latest```

Check it

```docker ps```

Inspect it

```docker inspect myghost```

Browse to it:

<http://localhost:3001>

Stop and delete it. Describe what happens to the contents of the container.

```docker stop myghost
docker ps -a
docker rm myghost
docker images
```

Adding the volume option to persist data! Note!! Tell Docker for Windows it has access to your drive.

```docker run -d -p 3001:2368 --name myghost -v c:\tmp\ghost:/var/lib/ghost/content ghost:latest```

Show contents of c:\tmp\ghost.

Clean up:

```docker system prune
docker image prune -a```
