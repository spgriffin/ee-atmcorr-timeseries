## Introduction

Atmospherically corrected, cloud-free, time series of satellite imagery from [Google Earth Engine](https://earthengine.google.com/) using the [6S emulator](https://github.com/samsammurphy/6S_emulator/edit/master/README.md).

### Installation

#### Recommended: Docker

The following [Docker](https://www.docker.com/community-edition) container has all dependencies to run the code in this repository

`docker pull samsammurphy/ee-python3-jupyter-atmcorr-timeseries:v1.7`

#### Alternative: Conda 

Install [Anaconda](https://www.continuum.io/downloads).

Install the Earth Engine API:

```
pip install google-api-python-client
pip install earthengine-api 
```

### Usage

#### Recommended: Docker

Run the docker container with access to a web browser

`docker run -i -t -p 8888:8888 samsammurphy/ee-python3-jupyter-atmcorr-timeseries:v1.7`

Once inside the container, authenticate Earth Engine

`earthengine authenticate`

(tip: you can save your credentials, and avoid repeating this step, using [docker commits](https://github.com/samsammurphy/6S_emulator/wiki/docker-commits))

Run the example jupyter notebook

```
cd ee-atmcorr-timeseries/jupyter_notebooks/
jupyter-notebook ee-atmcorr-timeseries.ipynb --ip='*' --port=8888 --allow-root
```

this will print out a URL that you can copy/paste into your web browser to run the code.

#### Alternative: Conda

If necessary, create a python3 environment

`conda create -n my_python3_env`

and activate it..

`source activate my_python3_env`

.. if on Windows the command is a bit shorter:

`activate my_python3_env`

Authenticate the Earth Engine API.

`earthengine authenticate`

clone this repository

`git clone https://github.com/samsammurphy/ee-atmcorr-timeseries.git`

run the jupyter notebook

```
cd ee-atmcorr-timeseries/jupyter_notebooks
jupyter-notebook ee-atmcorr-timeseries.ipynb
```
