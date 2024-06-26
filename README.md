# Text-Summarization Prozect

## STEPS:

Clone the repository

```bash
https://https://github.com/Kshitij-Nishant/Text-Summarization
```

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n summary python=3.8 -y
```

```bash
conda activate summary
```

### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

### STEP 03- run template.py to create required folders
```bash
python template.py
```

### STEP 04- Do research in notebooks and put those codes into respective folders based on Workflow

#### WORKFLOW followed for each stage:

1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. update the components
6. update the pipeline
7. update the main.py

8. Check the complete flow of code execution:

```bash
python  main.py
```

9. After each stage use below to push to Github:

```bash
git add .
git commit -m "<Put Caption here on the updates>"
git push origin main
```

### STEP 05- Make prediction pipeline in pipeline folder

Add the prediction pipeline and Update the app.py

check for complete flow of code execution in FastAPI:

```bash
# Finally run the following command
python  app.py
```

Now,
```bash
open up you local host and port
```

......Push to git after 




```bash
Author: Kshitij Nishant
Data Scientist Practitioner
Email: kshitijnishant09@gmail.com
```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

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

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/text-s

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app