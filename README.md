# Build-Serverless-Chatbot-AmazonBedrock
Build a Serverless Chatbot using Amazon's Bedrock

### Introduction:
This project demonstrates building a serverless chatbot using Amazon's Bedrock service. We have used Bedrock's feature such as Retrieval Augmented Generation to retrieve the latest information about the company from the vector DB and augment with user prompt to send FM. This provides the model with the context it needs to produce accurate and useful output for the specific use case. We have used Bedrock Agents to automate the tasks such as create claim which agents will pertinent lambda to perform the business logic for various usecases. For Security and Responsible AI policies, we have used Guardrails to block the unwanted response from the Model.

### Architecture:
[Uploading AGENTS-BEROCK (1).drawio…]()

