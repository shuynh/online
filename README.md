# stevenhuynh.online

served from S3 through CloudFront at https://stevenhuynh.online.

## deploy

```
aws s3 sync . s3://stevenhuynh-online --delete --exclude ".*" --exclude "*/.*" --exclude "README.md"
aws cloudfront create-invalidation --distribution-id EQ23GFS1OSICN --paths "/*"
```
