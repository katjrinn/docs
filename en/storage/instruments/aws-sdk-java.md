# AWS SDK for Java

[The AWS SDK for Java](https://aws.amazon.com/sdk-for-java/) is a set of tools for developers working with AWS services.

## Before you start {#preparations}

{% include [storage-s3-http-api-preps](../_includes_service/storage-s3-http-api-preps.md) %}

## Installation {#installation}

To install the AWS SDK for JAVA, follow the [instructions](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/setup-install.html) on the manufacturer's website.

{% note info %}

Install SDK 1.11.336 or higher.

{% endnote %}

## Configuration {#setup}

{% include [storage-sdk-setup](../_includes_service/storage-sdk-setup.md) %}

## Code samples {#java-sdk-examples}

For a code sample, see `aws-java-sdk/samples/AmazonS3` in the archive with the SDK distribution package.

To connect to {{ objstorage-name }}, replace the code in the sample:

```cpp
AmazonS3 s3 = AmazonS3ClientBuilder.standard()
    .withCredentials(new AWSStaticCredentialsProvider(credentials))
    .withRegion("us-west-2")
    .build();
```

with

```cpp
AmazonS3 s3 = AmazonS3ClientBuilder.standard()
    .withCredentials(new AWSStaticCredentialsProvider(credentials))
    .withEndpointConfiguration(
        new AmazonS3ClientBuilder.EndpointConfiguration(
            "storage.yandexcloud.net","ru-central1"
        )
    )
    .build();
```

