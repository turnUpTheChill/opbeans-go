[![Build Status](https://apm-ci.elastic.co/buildStatus/icon?job=apm-agent-go%2Fopbeans-go-mbp%2Fmaster)](https://apm-ci.elastic.co/job/apm-agent-go/job/opbeans-go-mbp/job/master/)

# opbeans-go

This is a Go implementation of the Opbeans Demo app.

## Running locally

The simplest way to run this demo is by using the
provided docker-compose.yml:

```bash
docker-compose up
```

## Running with Elastic Cloud

0. Start Elastic Cloud [trial](https://www.elastic.co/cloud/elasticsearch-service/signup) (if you don't have it yet)
1. Add environmental variables `ELASTIC_APM_SERVER_URL`, `ELASTIC_APM_JS_SERVER_URL` and `ELASTIC_APM_SECRET_TOKEN` to the `.env` file. 
2. Run
```bash
docker-compose -f docker-compose-elastic-cloud.yml up
```

## Testing locally

The simplest way to test this demo is by running:

```bash
make test
```

Tests are written using [bats](https://github.com/sstephenson/bats) under the tests dir

## Publishing to dockerhub locally

Publish the docker image with

```bash
VERSION=1.2.3 make publish
```

NOTE: VERSION refers to the tag for the docker image which will be published in the registry
