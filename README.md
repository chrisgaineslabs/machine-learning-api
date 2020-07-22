[![CircleCI](https://circleci.com/gh/chrisgaineslabs/machine-learning-api.svg?style=svg)](https://circleci.com/gh/chrisgaineslabs/machine-learning-api)

## Project Overview

This project contains a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project exhibits an ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

---

## Setup the Environment

* These steps were verified with a Amazon Linux AMI 2018.03.0 (HVM), SSD Volume Type - ami-0e9089763828757e1 image in AWS EC2.

* Install host server dependencies

<code> sudo yum update -y </code>

<code> sudo yum install -y python37 python37-virtualenv python37-pip git </code>

* Create a virtualenv and activate it

<code> python3 -m venv .api </code> 

<code> source .api/bin/activate </code> 

* Clone Repo and cd into source code directory

<code> git clone https://github.com/chrisgaineslabs/machine-learning-api.git api && cd api</code>

* Run `make install` to install virtual env dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`


## Please Star and Watch this repo for updates including connecting to AWS, connecting to a custom machine learning algorithm, and using circleci to deploy to a production environment.