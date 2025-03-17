# Build-Serverless-Chatbot-AmazonBedrock
Build a Serverless Chatbot using Amazon's Bedrock

--------------------------------------------------
### Introduction:
This project demonstrates building a serverless chatbot using Amazon's Bedrock service. We have used Bedrock's feature such as Retrieval Augmented Generation to retrieve the latest information about the company from the vector DB and augment with user prompt to send FM. This provides the model with the context it needs to produce accurate and useful output for the specific use case. We have used Bedrock Agents to automate the tasks such as create claim which agents will pertinent lambda to perform the business logic for various usecases. For Security and Responsible AI policies, we have used Guardrails to block the unwanted response from the Model.

--------------------------------------------------
### Architecture:

![KB](https://github.com/user-attachments/assets/4e8e94e6-95fc-41cb-b0d0-f23a926488fe)

--------------------------------------------------

![AGENTS](https://github.com/user-attachments/assets/2564f410-8d88-43e5-8b21-1b2ae16a792d)


### projects Highlights:
1. **CloudFormation Template :** Used CFT to provision the Resources such as VPC, RDS, S3
2. **Amazon Bedrock & Claude 3 Haiku:** Integrated Anthropic's Claude 3 Haiku, a cutting-edge AI model optimized for fast and efficient natural language processing, to generate intelligent response based on User Input. Amazon Bedrock provides a fully managed environment to deploy and scale foundation models with ease.
3. **Amazon Bedrock Titan Embedding Model:** It helps to convert the object to mathetical vectors and helps to store the vector to Vector DB(Opensearch Serverless)
4. **Knowledge Bases:** It is the External Datasource which will be augmented with the User prompt to get the accurate response from the Foundation Model (Claude 3 Haiku)
5. **Bedrock Agents:** : Used to automate multistep tasks by seamlessly connecting with company systems, APIs, and data sources
6. **Lambda:** Serverless Compute service which process the business logic and its high available, scalable.
7. **S3** : It is the Object Storage Service which helps to store the Company's PDF and Documents. It is high available and scalable.

--------------------------------------------------
### Understanding the Amazon's Bedrock Features:

1. Bedrock Knowledge bases : It is Managed RAG helps to store the Company's latest information in Vector DB
2. Bedrock Agents : Build agents  that use foundation models, make API calls, and (optionally) query knowledge bases in order to reason through and carry out tasks for your customers.
3. Bedrock Guardrails :  Used to implement safeguards customized to their application requirements and responsible AI  policies.

--------------------------------------------------
### Key Learning Outcomes: 
1. Provision the Resources such as VPC, RDS, S3 using CloudFormation Template
2. Created the Bedrock's Knowledge base by configuring the following steps
   •  Created the DataSource and Configured as S3 where Company's latest documents resides.
   •  Configured the Embedding Model [Amazon's Titan Embedding Model] to vectorize and Stores the data in Opensearch Serverless
   •  Interacted with the Knowledge base by selecting the FM.
3. Created and configued the Bedrock Agent by configuring the following steps
   •  Added the Action Group, by Define with API Schemas and for invokation selected the correct lambda function.
4. Created and configured the Bedrock Guardrails
   • Configure content filters
   • Enable harmful categories filter
   • Enable prompts attacks filter
   • Added Denied Topic


--------------------------------------------------
### Conclusion
This Project Highlights the Successful Implemenation of Serverless Chatbot GenAI Application  using various Bedrock's Features such as KB, Agents and Guardrails. By leveraging AWS's robust services and integrating best practices, the architecture delivers high scalability, resilience, and security while remaining cost-efficient.This hands-on experience reinforces the practical knowledge of designing, deploying, and managing GenAI applications, making it a significant step forward in mastering modern application hosting GenAI solutions.
