## docker-siege


[![Docker Automated build](https://img.shields.io/docker/automated/jean1989/docker-siege.svg)](https://hub.docker.com/r/jean1989/docker-siege) [![Docker Stars](https://img.shields.io/docker/stars/jean1989/docker-siege.svg)](https://hub.docker.com/r/jean1989/docker-siege/) [![Docker Pulls](https://img.shields.io/docker/pulls/jean1989/docker-siege.svg)](https://hub.docker.com/r/jean1989/docker-siege)


This image is used for building a given version of [Siege](https://github.com/JoeDog/siege) in Debian. 

The image uses the multi-stages build feature from Docker (version 17.05 and higher required). The final image weight 55.9MB.

### Usage

Create a container with all your Siege configuration (like urls file, siegerc...) as follow:

```dockerfile
FROM jean1989/docker-siege

COPY . /var/app

CMD ["siege", "-c 100", "google.com"]
```

Or directly from your terminal: `docker run -ti jean1989/docker-siege`

### Versions

For now, the image tags are created based on the branch. The master branch provides the latest version available. The other branches are based on the Siege releases.

### Contributing

If you find a bug or think about a way to improve the image, feel free to open an issue and/or a PR.
