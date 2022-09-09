# Noxx Micro Services

Micro Services built with a variety of languages (Java, Python, JavaScript, TypeScript) utilizing the [Serverless Framework](https://www.serverless.com/) compose the Noxx Platform.

These micro services automatically connect to the [central Noxx infrastructure built with AWS CDK](https://github.com/NoXX-Technologies/infrastructure).

Each service will include attitional documentation (if necessary) but this guide is to serve as global documentation, applicable to all Noxx services.

## Current Services
- [Card Recognition](https://github.com/NoXX-Technologies/card-recognition-service)
- [Java Sample](https://github.com/NoXX-Technologies/sample-java-service)
- [JavaScript Sample](https://github.com/NoXX-Technologies/sample-service)
## Setup

- [Install node and npm](https://nodejs.org/en/download/)
- [Install nvm](https://github.com/nvm-sh/nvm)
- [Install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- [Install Docker](https://docs.docker.com/engine/install/) (Python-based services, but good to have anyway)
- Install Serverless `$ npm install -g serverless`
- Install Oracle JDK and NOT Java JRE (Java-based services only)
- Install Maven: `$ brew install maven` (Java-based services only)
- Install depedencies: `$ npm install` or `$ yarn install`

You'll also need access to the corresponding AWS accounts.

Each stage cooresponds to an isolated AWS account which contains an infrastructure environment.

For example:

The stage `staging` will live in the `noxx-staging` infrastructure environment which is build in the noxx-staging AWS account.

You must add appropriate entries to your `~/.aws/credentials` and `~/.aws/config` files.

Example:

````
# ~/.aws/config
[profile noxx-staging]
role_arn=arn:aws:iam::602537455821:role/OrganizationAccountAccessRole
source_profile=default
region=us-east-1
````

````
# ~/.aws/credentials
[noxx-staging]
role_arn=arn:aws:iam::602537455821:role/OrganizationAccountAccessRole
source_profile=default
region=us-east-1
````

You may also have a Serverless Dashboard account (not required). If so, login with: `$ serverless login`

### Python Services Only

In order to package your dependencies locally with `serverless-python-requirements`, you need to have `Python3.8` installed locally. You can create and activate a dedicated virtual environment with the following command:

```bash
python3.8 -m venv ./venv
source ./venv/bin/activate
```

Alternatively, you can also use `dockerizePip` configuration from `serverless-python-requirements`. For details on that, please refer to corresponding [GitHub repository](https://github.com/UnitedIncome/serverless-python-requirements).

## Deploy

- `$ mvn clean install` # (Java-based services only)
- `$ sls deploy --stage <stage>`

Functions that have already been deployed as part of a full-deploy can be deployed without re-deploying the full stack with:

`$ sls deploy function -f <function-name>`

### CI/CD

The above is for manual deploys should you need to do it. That said, GitHub Actions will automatically deploy the appropriate stage on push.

For example, pushing to or opening a pull request to `staging` branch will trigger a deploy.

## Management

### Logs

`$ sls logs --function <function-name> --stage <stage>`

You can add `--tail` at the end to tail the logs

## Creating a new stage

Prior to creating a new stage, a new environment must be created using the [Infrastructure CDK](https://github.com/NoXX-Technologies/infrastructure).

For example, if you want to add a `demo` stage, you'll first need a `demo` environment created.

Once that is setup, simply add an entry in `env.yml` and add your corresponding AWS credentials entries as described in the Setup section.

### Setting up CI/CD

In order to setup CI/CD, you'll need access to the [Severless Dashboard](https://app.serverless.com/noxxtech) and the corresponding AWS Account.

First, click ["Org"](https://app.serverless.com/noxxtech/settings/team). Then ["Providers"](https://app.serverless.com/noxxtech/settings/providers).

Click "Add" > "Next"

Under "Simple" type the name of the stage (i.e. "dev", "staging", "production") and then "Connect AWS Provider".

This will open the AWS Console. **Make sure you are logged into the appropriate AWS Account**.

Follow the prompts until it's complete.

Once that's done click ["apps"](https://app.serverless.com/noxxtech) and find the app, service and stage you're setting up CI/CD for. Click the stage (i.e noxx > card-recognition > staging) and then click "Providers".

Click "add provider" and then select the Provider you added in the first step.

Finally, go back to Apps. Find your app stage (i.e. noxx > card-recognition) and click the three dots and then settings.

Select ci/cd.

If your GitHub account isn't connect already, do so.

Then in repository settings, select the repo that cooresponds with the service.

Finally, go down to "branch deploy" and select the branch and stage. These should be the same - i.e. branch (staging) should connect to stage (staging).

Now, whenever a pull request or push is made to that branch, serverless will trigger a deploy.

Optionally, jump down to "notifications" and add a notification to our Slack workplace.
## Creating a new service

Noxx has Java, Python, TypeScript and JavaScript services. 

The beauty of our approach is that developers are allowed to pick the right tool for the right job.

If you are creating a new service, run the command `$ serverless` to start a wizard to help set up a new service for you.

After the wizard is complete, select "n" for "deploy now?"

We then recommend you copy pieces from an existing service into your new service - specifically the serverless.yml and env.yml files.

These files conveniently mark YAML blocks as "Common" for pieces that should be used in every service.
