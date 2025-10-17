# VSC-AWS Toolkit Setup (Optional)

* In VSC, install AWS Toolkit from VSC Extensions

* Set credentials
    * https://rmit-research.awsapps.com/start/#/?tab=accounts
    * expand *stem-research-iar* (or appropriate other) account details
    * select *Access keys*
    * note ```SSO Start URL``` and ```SSO Region``` 
    * in VSC, select AWS Toolkit Explorer from left menu, enter SSO details
    * authenticate in browser

# Conda Environment Setup (Optional)

Create a new environment
* ```conda create --name bedrock```

Activate environment
* ```conda activate bedrock```

# AWS Environment Setup

Set environment credentials
1. ```aws configure```
   * Enter details from: https://rmit-research.awsapps.com/start/#/?tab=accounts (variables at bottom)
2. edit ~/.aws/credentials to add another line
    ```aws_session_token = <token>```
    * Note: the session token regularly expires so needs to be updated periodically

# Workshop setup
* (see https://catalog.workshops.aws/building-with-amazon-bedrock/en-US/prerequisites)
    ```
    cd environment/
    # the following zip archive is already included in the git repo
    # curl 'https://static.us-east-1.prod.workshops.aws/public/5dd5dc48-363d-4c69-9007-9e5528c5c31f/assets/workshop.zip' --output workshop.zip
    # unzip a local copy of the zip archive
    unzip workshop.zip
    pip3 install -r  workshop/setup/requirements.txt -U
    ```

* Verify setup
    ```
    python environment/workshop/completed/api/bedrock_api.py
    ```


