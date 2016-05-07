## Docker image for Selenium Server with Chrome (adapted from lzhang/selenium)

* [selenium](http://docs.seleniumhq.org/)

### Installation

```sh
$ docker pull samber/docker-selenium-chrome
```

### Usage

Run the container:

```sh
$ SELENIUM_CONTAINER=$(docker run -p 8080:8080 -d samber/docker-selenium-chrome -port 8080)
```

Selenium server will be available on the host machine at port 4444. Web tests 
will run via headless chrome.

The privileged option is needed so that chrome can run (see
https://github.com/dotcloud/docker/issues/1079).

Shutting down the container:

```sh
$ docker kill $SELENIUM_CONTAINER
```
