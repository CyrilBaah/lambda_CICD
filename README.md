# How to configure the lambda function

1. Build the Dockerfile
```sh
$ docker build -t lambda_cicd:latest .
```
2. Run the Docker container
```sh
$ docker run -p 9000:8080 lambda_cicd:latest
```
3. Test the Docker container
```sh
$ curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{}'
```
4. Test the Docker container | Get all Countries
```sh
$ curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{"httpMethod": "GET", "path": "/countries"}'
```
5. Test the Docker container | Get all names
```sh
$ curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{"httpMethod": "GET", "path": "/names"}'
```
5. Test the Docker container | Get all todos
```sh
$ curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{"httpMethod": "GET", "path": "/todos"}'
```