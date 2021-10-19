# HandsOn AWS

Command line script for install, setting and test.


## Step-by-step - INSTALL

### 1. Download Package AWS CLI


- [https://awscli.amazonaws.com/AWSCLIV2.pkg](https://awscli.amazonaws.com/AWSCLIV2.pkg)


### 2. Install Package AWS CLI

- On Finder run your package AWSCLIV2.pkg

### 3. Check Installation

```
aws --version
which aws
```

### 4. Configure


```
aws configure
```

**ATTENTION:** <b style="color:red;">ONLY SAMPLE</b>

```
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: us-west-2
Default output format [None]: json
```


### 4. AWS CLI - DynamoDB

#### 4. Create Table

```shell
aws dynamodb create-table \
    --table-name Music \
    --attribute-definitions \
        AttributeName=Artist,AttributeType=S \
        AttributeName=SongTitle,AttributeType=S \
    --key-schema \
        AttributeName=Artist,KeyType=HASH \
        AttributeName=SongTitle,KeyType=RANGE \
--provisioned-throughput \
        ReadCapacityUnits=10,WriteCapacityUnits=5
```

## References

[AWS CLI - User Guide](https://docs.aws.amazon.com/pt_br/cli/latest/userguide/cli-chap-welcome.html)

[AWS CLI - Configure](https://docs.aws.amazon.com/pt_br/cli/latest/userguide/cli-configure-quickstart.html)

[Amazon S3 Bucket Lifecycle Operations](https://github.com/awsdocs/aws-doc-sdk-examples/tree/main/aws-cli/bash-linux/s3/bucket-lifecycle-operations)

[Change Amazon EC2 Instance Type](https://github.com/awsdocs/aws-doc-sdk-examples/tree/main/aws-cli/bash-linux/ec2/change-ec2-instance-type)