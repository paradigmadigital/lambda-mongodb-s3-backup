# AWS Lambda MongoDB S3 Backup

This is simple `AWS Lambda` function that uses `mongodump` to backup MongoDB databases.

It *zips* the file and uploads it to an S3 bucket.

The following environment variables are required during the Lambda function setup:

```
MONGO_URL = mongodb://<user>:<password>@<host>:<port>/<database>
S3_PATH = <s3bucket>/<folder>/...
```

_____________________________
## Instructions for uploading

- Clone this repository. (`nodejs` is required)
- Run `npm install`.
- Create a ZIP with all the files¹.
- Upload the ZIP file to a new AWS Lambda function².

¹ If you are a *MAC OS X* user do not use the default compression tool.
Use `zip` from the command line instead

² The ZIP is far too large to be uploaded directly. First it must be uploaded to S3.
One it's there, copy the link and paste it to AWS Lambda.
