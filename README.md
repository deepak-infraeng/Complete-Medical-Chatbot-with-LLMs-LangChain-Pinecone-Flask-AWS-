Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask-AWS
How to run?
STEPS:
Clone the repository
git clonehttps://github.com/entbappy/Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask-AWS.git
STEP 01- Create a conda environment after opening the repository
conda create -n medibot python=3.10 -y
conda activate medibot
STEP 02- install the requirements
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
# run the following command to store embeddings to pinecone
python store_index.py
# Finally run the following command
python app.py
Now,
open up localhost:
Techstack Used:
Python
LangChain
Flask
GPT
Pinecone
AWS-CICD-Deployment-with-Github-Actions
Login to AWS console.
Create IAM user for deployment
#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
Create ECR repo to store/save docker image
- Save the URI: 315865595366.dkr.ecr.us-east-1.amazonaws.com/medicalbot
- Create EC2 machine (Ubuntu)
- Open EC2 and Install docker in EC2 Machine:
- #optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
Configure EC2 as self-hosted runner:
setting>actions>runner>new self hosted runner> choose os> then run command one by one
Setup github secrets:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
PINECONE_API_KEY
OPENAI_API_KEY


