# Taking secrets from AWS secrets manager 
In this example: 
The workflow is triggered when a push event occurs on the main branch. 

The AWS region, access key ID, and secret access key are set as environment variables using GitHub Secrets. 

The workflow checks out the repository. 

The AWS credentials are configured using the aws-actions/configure-aws-credentials action. 

The aws secretsmanager get-secret-value command is used to retrieve the secrets from AWS Secrets Manager. Adjust the --secret-id parameter with the appropriate secret ID. 

The secrets are stored as output variables using ::set-output syntax. 

The retrieved secrets can be accessed using the steps.secrets.outputs syntax in subsequent steps. 



 
