# Serverless-Web-Application
This repository provides a guide to building a serverless web application using AWS Lambda and API Gateway. It includes steps for creating IAM roles, Lambda functions, and REST API methods to enable seamless backend interactions.

## Project Overview

The project demonstrates how to build a serverless web application by leveraging AWS Lambda and API Gateway. The web ![webpage](https://github.com/user-attachments/assets/4e738a7c-15e9-4a00-9e77-2f80cd76c315)
application will allow users to interact with a backend system through RESTful API endpoints.


![Uploading webpage.png…]()

## Prerequisites

- AWS Account
- Basic understanding of AWS services such as IAM, Lambda, and API Gateway
- Python 3.8
- AWS CLI configured with appropriate permissions

## Steps to Create the Serverless Web Application

### Step 1: IAM (Identity and Access Management)

1. **Create IAM Role:**
   - Go to IAM Roles.
   - Use case: Lambda.
   - Attach the following policy:
     - Lambda basic execution role (to write logs)
   - Name the role.

### Step 2: Lambda Function

1. **Create Lambda Function:**
   - Go to Lambda and create a new function.
   - Give the function a name.
   - Select runtime as Python 3.8.
   - Choose the execution role created in Step 1.
   - Click "Create function".
   - Upload the code as a zip file.

### Step 3: API Gateway (REST API)

1. **Create API:**
   - Go to API Gateway and create a new REST API.
   - Give the API a name.
   - Choose the endpoint type as Regional.
   - Click "Create API".

2. **Create GET Method:**
   - Select the created API.
   - Create a new method with type GET.
   - Enable Lambda Proxy integration.
   - Select the region and the Lambda function created in Step 2.
   - Enable Default Timeout.
   - Click "Create Method".

3. **Create POST Method:**
   - Create a new method with type POST.
   - Enable Lambda Proxy integration.
   - Select the region and the Lambda function created in Step 2.
   - Enable Default Timeout.
   - Click "Create Method".

4. **Deploy API:**
   - Deploy the API by creating a new stage.
   - Give the stage a name.
   - Copy the generated URL to access the web application.

## Usage

- Access the web application using the URL provided after deploying the API.
- Interact with the API using the GET and POST methods.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes.
