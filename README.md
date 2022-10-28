##Project 4
This Readme file contains commands for succesfully executing the Project

##STEP1
##Docker login
docker login

##to build the Application
docker build -t techtrends .

##To test and Run the Application
docker run -dp 7111:3111 techtrends

##Docker run Output
1de025d17851750c84483760e34ea370051600685710441710b85f68cb0128ea

## Docker command to retrieve the logs 
docker logs 1de025d17851750c84483760e34ea370051600685710441710b85f68cb0128ea

## DOcker command to tag the image 
docker tag techtrends uchejen/techtrends:v1.0.0

## Docker command to push the images to dockerhub 
docker push uchejen/techtrends:v1.0.0

docker tag local-image:tagname new-repo:tagname
docker push new-repo:tagname


#STEP 2
##Github ACtions
1 Create a new repo 
2. push your codes to the new repo 
3. Add the docker token and GitHub encrypted secrets from the project directory Goto settings > secret > Actions > click New repository secret 
4. create the techtrends-dockerhub.yml in the .github/workflows/ Might be created automatically when creating the github action. 
5. Goto Github Actions and click on the create a new workflow yourself button

![Docker_secret](https://github.com/Uchejen/techtrend_project/blob/main/screenshots/Docker_secret.PNG?raw=true)

touch namespace.yaml
touch deploy.yaml
vim deploy.yaml
touch service.yaml
vim service.yaml

kubectl apply -f namespace.yaml
kubectl apply -f deploy.yaml
kubectl apply -f service.yaml
