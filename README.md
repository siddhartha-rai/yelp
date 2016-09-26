This code requires Python 3. 

* The following python3 modules should be installed - pandas, numpy, matplotlib, copy, and sklearn

* The Dockerfile which is part of this project ensures all necessary dependencies are available

* Instructions for running the notebook from Docker


```
docker build yelp-container -t yelp-container
docker run -d -p 8889:8888 yelp-container jupyter-notebook
```

After running the above, the notebook will be available at port 8888 of yoru virtual machine. For examplem if your virual machine ip is
192.168.99.100, the notebook can be accessed at http://192.168.99.100:8888

Click on Cell -> Run All, to run all instructions in the notebook.
