# Docker Sauce Labs Connect

This docker image runs [Sauce Labs Connect](https://docs.saucelabs.com/reference/sauce-connect/) 4.3 on Java 8.

## Versions

* 4.3, latest

## Usage

It sets the `sc` CLI as the entrypoint so it can be used as a replacement via
an shell alias:

```sh
$ alias sc="docker run --rm -it -p 8000:8000 ckloppers/sauce-connect"
$ sc -P 8000 -u $SAUCE_USERNAME -k SAUCE_ACCESS_KEY
```

Or just

```sh
$ docker run -rm -it \
             -p 0.0.0.0:8000:8000 \
             ckloppers/docker-sauce-connect -P 8000 \
                                        -u $SAUCE_USERNAME \
                                        -k $SAUCE_ACCESS_KEY \
                                        --tunnel-identifier foo
```


## Maintainers

* [Corne Kloppers](mailto:ckloppers@gmail.com)
