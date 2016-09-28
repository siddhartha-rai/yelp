## Pre-requisities
This code requires Python 3. 

* The following python3 modules should be installed - pandas, numpy, matplotlib, copy, and sklearn

* The Dockerfile which is part of this project ensures all necessary dependencies are available

* Instructions for running the notebook from Docker

Ensure your docker machine has at least 8 GB memory, for example on a MAC you need to run
```
docker-machine create -d virtualbox --virtualbox-memory 8192 machine_name

```
Now build and run your docker images, and start Jupyter Notebook

```
docker build  -t yelp-container yelp-container
docker run -d -p 8888:8888 yelp-container jupyter-notebook
```

# Jupyter Notebook

After running the above, the notebook will be available at port 8888 of yoru virtual machine. For examplem if your virual machine ip is
192.168.99.100,the notebook can be accessed at http://192.168.99.100:8888

The notebook name is yelp, to run the notebook navigate to http://192.168.99.100:8888/notebooks/yelp.ipynb

Click on Cell -> Run All, to run all instructions in the notebook.

##Data Preparation

Yelp data is available in JSON format, we need to convert this to JSON. 

For the experiments described in these slides, I have used the code available at https://github.com/Yelp/dataset-examples