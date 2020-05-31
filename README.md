[![CircleCI](https://circleci.com/gh/mosaddek082751/udacityML.svg?style=svg)](https://circleci.com/gh/mosaddek082751/udacityML)

# STEPS:

### Create a virtualenv and activate it.

  - python3 -m venv ~/.devops
  - source ~/.devops/bin/activate
  - Install necessary dependencies with Makefile

### make install
  - Check the python app first. It should be working.
  - python3 app.py
  
### Run the Python app in Docker
  - chmod +x run_docker.sh
  - ./run_docker.sh

### Make prediction from a separate window
  - ./make_prediction.sh

### Run the app in Kubernetes
  - chmod +x run_kubernetes.sh
  - ./run_kubernetes.sh

### Make prediction:
  - chmod +x make_prediction_k8s.sh
  - ./make_prediction_k8s.sh

### Adding Circle CI

  - Open an account in Circle CI and include the github project.

# FILES:

1. **makefile** Setup instruction of python environment and lint.
2. **app.py** Python code which we will run.
3. **Dockerfile** Definition of the Docker container which will expose the service in port 80.
4. **run_docker.sh** Building docker container from Docker file and run it on port 8000
5. **make_prediction.sh** Tests the docker container connecting with port 8000
6. **upload_docker.sh** Uploads the image to dockerhub
7. **run_kubernates.sh** Pulls the docker image and creates deployment.
8. **make_prediction_k8s.sh** Tests kubernetes cluster connecting with port 8001
9. **docker_out.txt** Output of terminal while running docker
10.**kubernetes_out.txt** Output of terminal while running kubernetes
11. **.circleci/config.yml** Circle Ci configuration mentioning steps to lint and build the project

# DEPENDENCIES:

Did the project in AWS EC2. Used Amazon Linux 2.

1. Docker
2. Python3
3. pip3
4. Linuxbrew for simplified installation
5. Kubectl
6. Minikube
