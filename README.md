Task 1. Kjell's Python code
A. SAM & GitHub actions workflow

Hardcoded name of S3 bucket is removed. Modified the app.py file in the AWS SAM application to read the S3 bucket name from an environment variable BUCKET_NAME.
To enable an examiner (sensor) to run the GitHub Actions workflow in their own GitHub account after forking your repository, they will need to follow these steps:

Fork the Repository:

The sensor should fork your GitHub repository into their own account.
Set Up Environment Variables:

If your workflow relies on environment variables (like AWS credentials or specific configuration settings), the sensor will need to set these up in their forked repository. This is done under the repository's Settings -> Secrets.
Configure AWS Credentials:

If your workflow interacts with AWS (like deploying to AWS Lambda), the sensor must configure their AWS credentials as secrets in the GitHub repository. They will need AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY.
Modify Workflow File (if necessary):

If there are any hard-coded values or specific configurations tied to your account or resources, the sensor might need to modify the workflow file to align with their environment.
Trigger the Workflow:

Finally, they can trigger the workflow by performing an an action that the workflow is set to respond to, like pushing a commit to the main branch.
