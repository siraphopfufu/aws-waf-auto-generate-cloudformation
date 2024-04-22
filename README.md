# aws-waf-auto-generate-cloudformation
### Disclaimer
This solution is a demonstration of how generative AI can be intregrated with cyber security. We as a developer of the solution do not recomend you to use this solution with out any understanding of the system, since doing so can cost a lot of money. 
### Solution Concept
This solution utilized amazon Bedrock which is a foundation model in order to generated aws WAF from Common Vulnerability and Exploit or CVE to create a virtual patching for your website or service. These solution is a prove of concept that Generative AI can be implement with cyber security fields to strengthen defense and reduce workload or overhead for cyber security team.
## Architect
![WAF Auto Generated Architecture](architect/Architect.jpg)

## Requirement

- [Python 3](https://www.python.org/downloads/), installed
- [AWS Command Line Interface (AWS CLI)](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) version 2, installed
- [AWS Serverless Application Model (SAM)](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-getting-started.html), installed

#### Installation

The CloudFormation stack must be deployed in the same AWS account and region where a GuardDuty detector has been configured and your EC2 instances are running.

```
git clone https://github.com/siraphopfufu/aws-waf-auto-generate-cloudformation.git
sam build
sam deploy --guided
```
After that input your Email and Owned Resource on system ie. application (not input anything will result in system recognize you have everythings) **AWS region that this solution currently work is us-east-1