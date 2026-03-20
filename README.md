# COMP 4750 Class Survey

Starting point for the [Class Survey project](https://cs.harding.edu/gfoust/classes/comp4750/projects/survey).



## Project organization

- `template.yaml` — SAM template defining all AWS infrastructure: S3 bucket, API Gateway, DynamoDB
  table, and both Lambda functions.
- `frontend/` — Static HTML pages for the survey form (`index.html`) and the results page
  (`results.html`).  Put these in your front-end S3 bucket once it's created.
- `src/` — Lambda functions.
  - `submitHandler/` — Lambda function triggered by API Gateway; stores survey responses in
    DynamoDB.
  - `batchProcessor/` — Lambda function triggered by DynamoDB Streams; aggregates response
    statistics and writes them to S3.
- `events/` — Sample event payloads for each lambda.
