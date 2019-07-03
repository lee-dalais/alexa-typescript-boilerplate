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
AWS Account - Create an IAM User for the Serverless Framework that only has Programmatic access. I use `serverless.dev` with `dev` representing the specific environment. The full instructions can be found [here.](https://serverless.com/framework/docs/providers/aws/guide/credentials)

ASK CLI - To start using ask-cli, you need to initialize it: 
 ```
 ask init
 ```
 This allows ASK to connect to your Alexa Developer account for creating/updating the skill and use a predefined AWS profile. More details [here](https://developer.amazon.com/docs/smapi/manage-credentials-with-ask-cli.html#ask-init) 