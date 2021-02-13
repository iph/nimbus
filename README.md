# Nimbus
A load testing tool based on `rakyll/hey` but sigv4 sign's requests. 

Nimbus is latin for rain and it's about to be a downpour in your cloud!!

## Usage

There are two ways to use nimbus today:

1. Environment variables
2. Default location (~/.aws/credentials) credentials file

To specify your profile, use -p.

An example to test Lambda function invokes at a high TPS (remember to source your environment credentials):

```
./nimbus -c 100 -q 1000 -t 30s -d '{}' -m POST -r us-east-1 'https://lambda.us-east-1.amazonaws.com/2015-03-31/functions/<lambda_function_name>/invocations'
```

Have fun :)
