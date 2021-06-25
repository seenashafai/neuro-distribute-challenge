# neuro-distribute-challenge

Author: Seena Shafai
Language: Python 3.7.0
IDE: Jupyter Notebook

# Introduction

The Jupyter Notebook contains the set-up and execution of a Dask adaptive scheduling system.

# Solution

- The first box builds the adaptive scheduler, which allows the program to dynamically add and remove workers to maximise throughput at any given time, as required by the task.
- The second box contains the function, 'func'- the example given in the task brief, and the solution obtained via the distributive network is shown below it.
- The third box contains a series of equations designed for load testing. The function finds the sum of a large randomly allocated array after squaring it.

# Monitoring

- In a default configuration, running this program in Jupyter Notebook should result in a web-based dashboard based on port 8787 on the local machine: localhost:8787

- This dashboard, powered by visualisation library Bokeh, allows us to observe in real-time the workers being allocated, used, and destroyed as the distributed network attempts to solve the given equations.

# Conclusion

- The dashboard shows that the network successfully adds and removes workers depending on throughput at any given moment, maximising efficiency when dealing with larger datasets.
- However, with smaller datasets, I have observed that the overhead required to dynamically generate and destroy workers can result in a greater calculation time requirement. This is shown when testing the given test function 'func'
- When executing the load test functions, with a range of 0-20 workers, the calculation time was cut down by 40% when compared against a static network of 4 workers.
