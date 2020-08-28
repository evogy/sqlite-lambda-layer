# SQLite Python Lambda Layer
Like many Python programmers, you've probably been disappointed when you tried to import `sqlite3`
in a Python3.6 AWS Lambda only to find out it doesn't work. This project remedies that by providing
a [Lambda Layer](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html) that contains the necessary compiled library
(`_sqlite3.so`).

## How to use
First you must clone the repo, build the file, and publish it to AWS:
```shell
git clone git@github.com:evogy/sqlite-lambda-layer.git
cd sqlite-lambda-layer
./build
sls deploy
```
Then see [the docs](https://serverless.com/framework/docs/providers/aws/guide/functions/#layers)
and configure your lambda to use the layer you just published.
