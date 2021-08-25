
# Deploy through CLI - JVM
aws lambda create-function --function-name QuarkusLambda --zip-file fileb://target/function.zip --handler io.quarkus.amazon.lambda.runtime.QuarkusStre
amHandler::handleRequest --runtime java11 --role arn:aws:iam::750895039924:role/lambda-ex --timeout 15 --memory-size 1024



# Deploy through CLI - Image
aws lambda create-function --function-name QuarkusLambda --zip-file fileb://target/function.zip --handler not.used.in.provided.runtime
 --runtime provided --role arn:aws:iam::750895039924:role/lambda-ex --timeout 15 --memory-size 1024