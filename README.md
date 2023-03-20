# This is a terraform repository.

I will be uploading some terraform projects that I have worked on

TERRAFORM AND AWS CLI INSTALLATION:

A) Pre-requisites 

* Install AWS CLI
* Install terraform CLI
* Install vs code editor
* Install Hashicorp plugin for vs code

B) Install Terraform on Ubuntu/Debian

$ wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
$ echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
$ sudo apt update && sudo apt install terraform

# To install terraform on windows macOs follow officiak documentation on :
https://developer.hashicorp.com/terraform/downloads

C) Install AWS CLI on Linux

$ curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
$ sudo apt install unzip 
$ unzip awscliv2.zip
$ sudo ./aws/install
# Verify that AWS CLI is installed by running aws --version


# To install AWS cli on MacOs or Windows follow official recommendation on
 https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

D) CONFIGURE AWS CREDENTIALS IN COMMAND LINE 

$ aws configure
AWS Access Key ID [None]: REPLACEACCESSKEYID
AWS Secret Access Key [None]: REPLACEWITHYOUROWNSECRETACCESSKEY/
Default region name [None]: eu-west-1
Default output format [None]: json

# Verify if we are able to  list S3 buckets
aws s3 ls

# Command to reset your AWS credentials incase of a credentials error:

$ for var in AWS_ACCESS_KEY_ID AWS_SECRET_ACCESS_KEY AWS_SESSION_TOKEN AWS_SECURITY_TOKEN ; do eval unset $var ; done


