# BSc Thesis (Vienna University of Technology) - AAL Sensor Data Cluster Analysis - Dzenan Hamzic - https://dzenanhamzic.com/

Data analysis experiments while writing my thesis.

check final work @ http://www.bitelligence.at/work/bthesis.pdf 
or
@http://www.grin.com/en/e-book/340200/aal-data-cluster-analysis-theory-and-implementation

For more work, feel free to check my blog @https://dzenanhamzic.com/

1. Introduction 



We are living in times of “smart-homes”. Sensors are registering our every movement. We can use these data on various ways like for preventing leakage, disasters, robbery and automating doors, lights etc. On the other hand, we can use these data to to support older people by finding out if they are behaving other than usual in order to trigger some help alarm like sending an emergency call or cutting the power-supply in order to prevent disaster. The e-Home project from the Vienna University of Technology [1] is an R&D project with goals of providing assistive technologies for private households of older people with the idea to give them possibilities for longer and independent living in their homes.  

Abstract


The e-Home project from the Vienna University of Technology [1] is an R&D project with goals of providing assistive technologies for private households of older people with idea to give them possibilities for longer and independent living in their homes.  The e-Home system consists of an adaptive intelligent network of wireless sensors for activity monitoring with a central context-aware embedded system [2].
The primary goal of this thesis is to investigate unsupervised prediction and clustering possibilities of user behaviour based on collected time-series data from infrared temperature sensors in the e-Home enviroment.
Three different prediction approaches are described. Hourly Based Event Binning approach is compared to two clustering algorithms, Hierarchical Clustering and Dirichlet Process GMM. Prediction rates are measured on data from three different test persons.

This thesis first examines two different approaches for event detection from infrared signal data.
In a second stage three different methods for unsupervised prediction analytics are discussed and tested on selected data-sets. Clustering algorithms parameter settings for time-series data have also been discussed and tested in detail. Finally the prediction performance results are compared and each method's advantages and disadvantages have been discussed.

The practical part of this thesis is implemented in IPython notebook. Python version was 2.7 on 64 bit Ubuntu linux 12.04 LTS. Data analysis has been implemented with Python’s Pandas library. Visualisations are made with Matplotlib and Seaborn libraries.

The results reveal that prediction accuracy depends on data quantity and spread of data points. The simplest method in prediction comparison, the Hourly Based Binning has however given the best prediction rates overall.
By contrast to the Hourly Based Binning the Dirichlet Process Gaussian Mixture Models clustering show best prediction performance on smaller training data sets and well spread data. By further parameter tuning on Dirichlet Process GMM clustering the prediction rates could be further improved coming very close or even over performing the Hourly Based Binning.
Due to the unknown distribution and well spread data, choosing the right threshold parameter for the Hierarchical Clustering was trickier than initially assumed. Despite the initial assumptions for Hierarchical Clustering, this method was at least applicable for unsupervised prediction analytics on used data sets.

The Goal
The goal is to have as reliable as possible solutions for detecting the typical times of a person’s behaviour like cooking without any supervised interventions. If the person usually cooks in intervals between 10 AM and 1 PM  and 3 PM and 5 PM it should be possible to find such time intervals. It should also be possible to have a probability of an event occurring in any given hour or time span.


