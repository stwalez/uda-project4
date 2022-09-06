[![CircleCI](https://dl.circleci.com/status-badge/img/gh/stwalez/uda-project4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/stwalez/uda-project4/tree/main)

## Project Overview

This project operationalizes a Machine Learning Microservice API.

A pre-trained, `sklearn` model has been provided, it has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 
More information about this data can be found on Kaggle[the data source site](https://www.kaggle.com/c/boston-housing).
This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

---
## Project Tasks

The following tasks were performed:
* Test project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that the code has been tested

---

## Instructions
### Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl


---


## Short description of folders and files in the repo

* [.circleci](/.circleci): For the CircleCI build server
* [model_data](/model_data/) : this folder contains the pretrained `sklearn` model and housing csv files
* [output_txt_files](/output_txt_files): folder contains sample output logs from running `./run_docker.sh` and `./run_kubernetes.sh`
* [app.py](/app.py) : contains the flask app
* [Dockerfile](/Dockerfile): contains instructions to containerize the application
* [Makefile](/Makefile) : contains instructions for environment setup and lint tests
* [requirements.txt](/requirements.txt): list of required dependencies
* [run_docker.sh](/run_docker.sh): bash script to build Docker image and run the application in a Docker container
* [upload_docker.sh](/upload_docker.sh): bash script to upload the built Docker image to Dockerhub
* [run_kubernetes.sh](/run_kubernetes.sh): bash script to run the application in a Kubernetes cluster
* [make_prediction.sh](/make_prediction.sh): bash script to make predictions against the Docker container and k8s cluster
* [README.md](/README.md): this README file