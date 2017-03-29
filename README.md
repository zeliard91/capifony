Capistrano v3 + Capifony
========================

This container provides [Capistrano](https://github.com/capistrano/capistrano) command to deploy Symfony websites with [Capifony](https://github.com/capistrano/symfony)

## Usage

Type in your project directory :

```bash
docker run \
    -it \
    --rm \
    -v ${HOME}/.ssh:/root/.ssh \
    -v ${PWD}:/root/workdir \
    zeliard91/capifony
```

or if you prefer to forward your ssh agent : 
```bash
docker run \
    -it \
    --rm \
    -e SSH_AUTH_SOCK=${SSH_AUTH_SOCK} \
    -v $(dirname $SSH_AUTH_SOCK):$(dirname $SSH_AUTH_SOCK) \
    -v ${PWD}:/root/workdir \
    zeliard91/capifony
```

