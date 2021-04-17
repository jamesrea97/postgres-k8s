# Integration Test setup 

In order to simulate a test case closest to production, integration tests are used with the  help of Docker.
This document provides the reader with instructions to set up the containerized testing environment.

## Requirements
TODO

## Deployment
The following instructions set up of the testing environment:

```sh
cd ./test/integration
docker build -t accounts-db-test . # Builds from Dockerfile
docker run --name db-accounts-test-cont -it -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 accounts-db-test # Running Container
```