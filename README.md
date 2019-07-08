# Alexa Skill Boilerplate with Typescript
The first revision of this starter-kit is intended for developers who want to deploy to AWS using AWS-CLI. A later revision will provide steps to automate via CodePipeline.  


## Getting Started

### Prerequisites
AWS Account

Alexa Developer Account

Node 8+

Typescript
```
$ npm install typescript -g
```

Serverless Framework
```
$ npm install serverless -g
```

AWS CLI
```
$ pip install awscli --upgrade --user
```

ASK CLI
```
npm install ask-cli -g
```

### Setup
AWS Account - Create an IAM User for the Serverless Framework that only has Programmatic access. The full instructions can be found [here.](https://serverless.com/framework/docs/providers/aws/guide/credentials)

ASK CLI - To start using ask-cli, you need to initialize it: 
 ```
 ask init
 ```
 This allows ASK to connect to your Alexa Developer account for creating/updating the skill and use a predefined AWS profile. More details [here](https://developer.amazon.com/docs/smapi/manage-credentials-with-ask-cli.html#ask-init)
  
### Alexa Skill
Deploy the Alexa boilerplate skill to create a Skill Id.

```
ask deploy
```

Copy the `Skill Id:` value from the terminal output or check the `.ask/config` file for the skill id.

### Serverless

Open `lambda\custom\serverless.yml` and replace the SKILL-ID with the copied Skill Id.

Provision the AWS resources:
```
sls deploy
```

Copy the function ARN from the Management Console and update the `.ask/config` file with 
```
"custom": {
    "endpoint": {
        "uri": "arn:aws:lambda:us-east-1:ABC:function:XYZ"
    }
}
```

Update the Alexa skill
```
ask deploy -t skill
```