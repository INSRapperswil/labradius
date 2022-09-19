# docker-labradius
A preconfigured radius server based on [freeradius](https://hub.docker.com/r/freeradius/freeradius-server/).

> DO NOT USE IN PRODUCTION

## Build
```bash
$ docker build -t labradius .
```

## Run
```bash
$ docker run --rm -d -p 1812-1813:1812-1813/udp labradius
```
If you need more output (e.g. for debugging) add `-X` to the command

## Test
```bash
$ radtest alice radius_password_alice 127.0.0.1 0 radius_shared_secret
```
