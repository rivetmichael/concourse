# Concourse commands:

## Add local resolution

```bash
$ echo '127.0.0.1    traefik.local\n127.0.0.1    concourse.local' | sudo tee -a /etc/hosts
```

## Start the app

```bash
$ docker-compose -p ci up -d
```

## Install the CLI fly

```bash
$ mv ~/Downloads/fly /usr/local/bin
$ chmod 0755 /usr/local/bin/fly
``` 

## Configure the CLI

```bash
$ fly --target tutorial login --concourse-url http://concourse.local -u admin -p admin
```
