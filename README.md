# lumigo-cli-playground

learn [lumigo-CLI](https://github.com/lumigo-io/lumigo-cli), A collection of helpful commands for working with AWS Lambda.

## Example Usage

```sh
# display contents of gzipped cloudfront log file to stdout
# see S3 SQL reference @  https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-glacier-select-sql-reference-select.html
lumigo-cli s3-select-batch \
  --region="us-east-1" \
  --bucket="com.brianpfeil.cloudfront.logs" \
  --prefix="brianpfeil.com/E2IL5HY5XTHLNW.2019-09-17-21.66bbda6b.gz" \
  --expression="SELECT * FROM S3Object s" \
  --fileType="CSV" \
  --compressionType="GZIP"

# list Lambda functions in ALL regions
lumigo-cli list-lambda
```