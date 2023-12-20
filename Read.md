# Deploy AI model with FastAPI, Docker, and kubernetes
## Create imdb.py AI model
### From IMDB movie reviews data set create a model using sklearn library which predicts possitive or negative
### Create pkl file from the model
### From the imdb.py and pkl file create model.py, which is used to call in main.py
## Main.py
###  FastAPI web service with a health check endpoint and a prediction endpoint that uses the predict_pipeline ### function to provide predictions based on the input text.
## Dockerfile
### Sets up a Docker image for a FastAPI application, installing dependencies listed in requirements.txt, ### and copying the application code to the image.
### docker build -t image-name .
### docker run -d container-name -p 80:80 image-name
## Kuberenetes Deployment
### Register the container in azure container registery
### Deploy the kuberenetes Deployement using deployment.yaml with imdb-container, 3 replicas etc
## Expose the Fast API as a front end gui where user can do prediciton
### Similar sample was done in local host

curl -X 'POST' \
  'http://localhost/predict' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "text": "movie is great"    #enter text here
}'

	
Response body
Download
{
  "review": "positive"        #output
}

