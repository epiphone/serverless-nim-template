# serverless-nim-template
Template for the Serverless Framework [Nim language plugin](https://github.com/epiphone/serverless-nim).

## Dependencies
- NodeJS
- [Serverless Framework](https://serverless.com/framework/docs/getting-started/)
- AWS account and IAM user (see [instructions](https://serverless.com/framework/docs/providers/aws/guide/credentials/))
- either a [Nim](https://nim-lang.org/install.html) or Docker installation

## Getting started

1. Create a new service using this template:
```bash
serverless create --template-url https://github.com/epiphone/serverless-nim-template --path my-service-path --name my-service
```

2. Install npm dependencies (basically just the `serveless-nim` plugin itself):
```bash
cd my-service-path
yarn install # or npm install
```

3. Deploy service:
```bash
serverless deploy
```

That's it! Now we can invoke functions, either on the cloud or locally:

```bash
serverless invoke -f hello
serverless invoke local -f hello --context {} --data {}
```

## Teardown

```bash
serverless remove
```

## Configuration

Check the [serverless-nim plugin docs](https://github.com/epiphone/serverless-nim) for more on Dockerized builds and other configuration matters.
