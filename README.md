# Serverless sample project using express-http, aws-sdk and dynamodb
Reference: https://serverless.com/blog/serverless-express-rest-api/

This simple project use Express with serverless framework

It uses API-Gateway's {proxy+} feature to pass requests directly to Express



## Install packages
```
$ npm install --save express serverless-http
$ npm install --save aws-sdk body-parser
```

## Deploy
```
$ sls deploy
```

## Test
```
export BASE_DOMAIN=https://xxxxxxx.execute-api.us-east-1.amazonaws.com/dev

$ curl -H "Content-Type: application/json" -X POST ${BASE_DOMAIN}/users -d '{"userId": "alexdebrie1", "name": "Alex DeBrie"}'

$ curl -H "Content-Type: application/json" -X GET ${BASE_DOMAIN}/users/alexdebrie1

```
