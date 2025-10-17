# VSC-AWS Toolkit Setup (Optional)

* \[First time only: Set credentials\]
    * In VSC, install AWS Toolkit from VSC Extensions
    * Visit https://rmit-research.awsapps.com/start/#/?tab=accounts
    * expand *stem-research-iar* (or appropriate other) account details
    * select *Access keys*
    * note ```SSO Start URL``` and ```SSO Region``` 

* In VSC, select AWS Toolkit Explorer from left menu
    * select Connected with IAM Identity Center (rmit-research)
    * select connection with number that matches "stem-research-iar", i.e. 536697255212
* authenticate in browser

# Conda Environment 

\[First time only: Create a new environment\]
* ```conda create --name bedrock```

Activate environment
* ```conda activate bedrock```

# AWS Environment Setup

\[First time only: Set environment credentials\]
* ```aws configure```
    * Enter details from: https://rmit-research.awsapps.com/start/#/?tab=accounts (variables at bottom)

Edit ~/.aws/credentials
* Visit https://rmit-research.awsapps.com/start/#/?tab=accounts
* Expand stem-research-iar, click Access Keys
* Copy content from "Option 2: Add a profile to your AWS credentials file"
* Rename first line from "\[\<some account number\>]\" to "\[default\]"
* Note: the session token regularly expires so needs to be updated periodically

# Workshop setup
* (see https://catalog.workshops.aws/building-with-amazon-bedrock/en-US/prerequisites)
    ```
    cd environment/
    # curl 'https://static.us-east-1.prod.workshops.aws/public/5dd5dc48-363d-4c69-9007-9e5528c5c31f/assets/workshop.zip' --output workshop.zip
    # unzip a local copy of the zip archive
    unzip workshop.zip
    pip3 install -r  workshop/setup/requirements.txt -U
    ```

* Verify setup
    ```
    python environment/workshop/completed/api/bedrock_api.py
    ```