# lumigo-cli-playground

learn [lumigo-CLI](https://github.com/lumigo-io/lumigo-cli), A collection of helpful commands for working with AWS Lambda.

## Examples

```sh

# display contents of gzipped cloudfront log file to stdout
lumigo-cli s3-select-batch \
  --region="us-east-1" \
  --bucket="com.brianpfeil.cloudfront.logs" \
  --prefix="brianpfeil.com/E2IL5HY5XTHLNW.2019-09-17-21.66bbda6b.gz" \
  --expression="SELECT s._1 FROM S3Object s" \
  --fileType="CSV" \
  --compressionType="GZIP"

# list Lambda functions in ALL regions
lumigo-cli list-lambda

```