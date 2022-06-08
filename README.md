# Manage AWS S3 using aws-sdk in node.js

## Installation
Install the dependencies and devDependencies and start the server. ([aws-sdk])

```sh
npm install
```
## Configuring the SDK
Configure the SDK for JavaScript by creating a global configuration object then setting the Region for your code. In this example, the Region is set to us-west-2.
```sh
// Load the SDK for JavaScript
var AWS = require('aws-sdk');
// Set the Region 
AWS.config.update({region: 'us-west-2'});
```
## Run
### Creating and Using Amazon S3 Buckets
- Displaying a List of Amazon S3 Buckets
```sh
        node s3_listbuckets.js
```
- Creating an Amazon S3 Bucket
```sh
        node s3_createbucket.js BUCKET_NAME
```
- Uploading a File to an Amazon S3 Bucket
```sh
        node s3_upload.js BUCKET_NAME FILE_NAME
```
- Listing Objects in an Amazon S3 Bucket
```sh
        node s3_listobjects.js BUCKET_NAME
```
- Deleting an Amazon S3 Bucket
```sh
        node s3_deletebucket.js BUCKET_NAME
```
### Configuring Amazon S3 Buckets
- Retrieving a Bucket CORS Configuration
```sh
        node s3_getcors.js BUCKET_NAME
```
- Setting a Bucket CORS Configuration
```sh
        node s3_setcors.js BUCKET_NAME get put
```
### Managing Amazon S3 Bucket Access Permissions
- Retrieving the Current Bucket Access Control List
```sh
        node s3_getbucketacl.js BUCKET_NAME
```
### Working with Amazon S3 Bucket Policies
- Retrieving the Current Bucket Policy
```sh
        node s3_getbucketpolicy.js BUCKET_NAME
```
- Setting a Simple Bucket Policy
```sh
        node s3_setbucketpolicy.js BUCKET_NAME
```
- Deleting a Bucket Policy
```sh
        node s3_deletebucketpolicy.js BUCKET_NAME
```
### Using an Amazon S3 Bucket as a Static Web Host
- Retrieving the Current Bucket Website Configuration
```sh
        node s3_getbucketwebsite.js BUCKET_NAME
```
- Setting a Bucket Website Configuration
```sh
        node s3_setbucketwebsite.js BUCKET_NAME INDEX_PAGE ERROR_PAGE
```
- Deleting a Bucket Website Configuration
```sh
        node s3_deletebucketwebsite.js BUCKET_NAME
```

[aws-sdk]:https://www.npmjs.com/package/aws-sdk