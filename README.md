# serverless-framework-docker-image

This image was tested in [BitBucket](https://bitbucket.org) CI/CD service to builds and deploys serverless applications written in `Serverless Framework`.

## Why use it?

It has necessary dependencies baked in so it can speed up pipeline process and streamline your pipeline configuration.

## What's inside?
This image is based on official [node:12.20-alpine](https://hub.docker.com/_/node) and contains:

* `Node.js@12.20`
* `AWS CLI` v2
* and `Serverless Framework`

## Versioning
In your `bitbucket-pipelines.yml` or somewhere else if you're using other service define version of the image as follows:

```YAML
image: serverlesspolska/serverless-framework # it resolves `latest`
# or
image: serverlesspolska/serverless-framework:latest
```

If you need specific version just enter `tag number` (i.e. `2.16`) instead of `latest`:
```YAML
image: serverlesspolska/serverless-framework:2.16

```

# Available versions

Based on Serverless Framework [versions](https://github.com/serverless/serverless/releases):

* [Serverless Framework 2.17.0](https://github.com/serverlesspolska/serverless-framework-docker-image/releases/tag/2.17) - tag: `2.17` - 2020/12/30
* [Serverless Framework 2.16.0](https://github.com/serverlesspolska/serverless-framework-docker-image/releases/tag/2.16) - tag: `2.16` - 2020/12/22
* [Serverless Framework 2.4.0](https://github.com/serverlesspolska/serverless-framework-docker-image/releases/tag/2.4) - tag: `2.4` - 2020/12/17

You can view ready images on **Docker Hub** at https://hub.docker.com/r/serverlesspolska/serverless-framework.


# Side notes
## Compatibility with serverless-iam-roles-per-function

`Serverless Framework@2.4.0` is the last version of the framework that works with [serverless-iam-roles-per-function](https://github.com/functionalone/serverless-iam-roles-per-function) version 2.x.x. 

However, recently there was 3.x.x release that is compatible with `Serverless Framework` > `2.4.0`.

