[![KhineWai710](https://circleci.com/gh/KhineWai710/project-ml-microservice-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/KhineWai710/project-ml-microservice-kubernetes)

## Project Overvivew
This project is simple project to operationalize a Machine Learning Microservice API. 
Application is a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, 
such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 

This project can easily run with Standalone, docker, Kubernetes.
It also integrate with CircleCI.

### Project Structure
This is project sturcture.
```
.
├── Dockerfile => setting of docker files
├── Makefile => setting of make files
├── README.md
├── app.py   => sklearn
├── get-pip.py
├── make_prediction.sh => prediction script
├── model_data
│   ├── boston_housing_prediction.joblib
│   └── housing.csv
├── output_txt_files => log output files
│   ├── docker_out.txt
│   └── kubernetes_out.txt
├── requirements.txt => necessaries installation
├── run_docker.sh  => script to run docker
├── run_kubernetes.sh => script to run kubernetes
└── upload_docker.sh => script to update application to kubernetes
```


## Setup the Environment
* Create a virtualenv and activate it
$make setup
$source ~/.devops/bin/activate

* Run `make install` to install the necessary dependencies
$make install
* Install docker
* Install Kubernetes

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
