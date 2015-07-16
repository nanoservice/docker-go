# slim docker image for go

[on docker hub](https://registry.hub.docker.com/u/nanoservice/go/)

Part of nanoservice image library.

## Usage

Put `Dockerfile` inside of your service:

```dockerfile
FROM nanoservice/go

ADD . /go/src/github.com/username/app
WORKDIR /go/src/github.com/username/app

RUN go install
RUN go test

ENTRYPOINT ["app"]
```

Build it: `docker built -t my-app .`.

Run it: `docker run my-app`.

Enjoy!

## Contributing

1. Fork it ( https://github.com/nanoservice/docker-go/fork )
1. Create your feature branch (git checkout -b my-new-feature)
1. Commit your changes (git commit -am 'Add some feature')
1. Push to the branch (git push origin my-new-feature)
1. Create a new Pull Request

## Contributors

* [waterlink](https://github.com/waterlink) Oleksii Fedorov, creator, maintainer
