# SAM Lambda Deploy With GitHub Pipeline and AWS Organizations

This project contains a exemple of AWS Lambda with framework AWS SAM with deploy Pipeline in multiple environments. 

## Requirements
To run this test, you need to have some configurations in place: 
- An AWS account with a CI/CD user configured. If you don't have a user, you can create one with the permissions found in the [SAM Permissions to Deploy](/sam_permissions_deploy.json) document. NOTE: This is a file with many permissions, if you want something leaner, feel free to limit the permissions, this was a user created to be used as a test;
- When generating your CI/CD user as mentioned in the previous topic, save the ACCESS_KEY_ID and SECRET_ACCESS_KEY as they will be needed later to perform the Deployment.
- It is optional to create an extra account on AWS to test versioning in different accounts, the idea of using Organizations is interesting to keep all control centralized and good practices.

## Deploy the application
- Fork this project to your account;
- In your repository, go to Settings > Secrets and Variables > Actions and register the two keys with the names below:
  - AWS_ACCESS_KEY_ID_DEV
  - AWS_SECRET_ACCESS_KEY_DEV
- If you have provisioned two environments, you can also configure the key to simulate a production environment:
  - AWS_ACCESS_KEY_ID_DEV
  - AWS_SECRET_ACCESS_KEY_DEV
- Once setup is complete, simply go to Actions and run the 'Deploy SAM With GitHub Actions' Action.

*If you have not provisioned, you can use the same key, but the deployment will be done in the same environment.

## Resources
This project was generated only using the AWS documentation in which you can find the entire SAM template generation process [here](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html) and an example deployment pipeline [here](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/deploying-using-github.html).