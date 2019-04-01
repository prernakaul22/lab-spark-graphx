# Lab: Graphs with Spark using GraphFrames

## Start your cluster

Create an EMR cluster with **_Advanced Options_** and the following configuration:

* Select `emr-5.21.0` from the drop-down
* **Click check-boxes for these applications only**: Hadoop 2.8.5 and Spark 2.4.0
* Click Next
* Edit the instance types and set 1 master and 4 core of m4.xlarge 
* Click Next
* Give the cluster a name, and you can uncheck logging, debugging and termination protection enabled
* Click Next
* Select your key-pair
* Click "Create Cluster"

Once the cluster is in "Waiting" mode (should only take a few minutes), please `ssh` into the master. After you log-in to the master node, run the following commands in your terminal:

```

-------------- POST STARTUP SCRIPT COMPLETE --------------------
*** You are still logged into the master node of EMR cluster ***
To access Jupyter notebook, logoout from the master node as soon
as you see this message with the exit command.

Once you disconnect from the master node, ssh back in using
agent and port forwarding. Remember to type `ssh-add` before:

ssh -A -L8765:localhost:8765 hadoop@...
and then open a web browser and go to http://localhost:8765
----------------------------------------------------------------


```
Once this is done, please type `exit` to logoff and then log back on, making sure you enable both ssh-agent forwarding and port forwarding:


```
ssh-add
ssh -A -L8765:localhost:8765 hadoop@...
``` 

You can then open a browser and navigate to [http://localhost:8765](http://localhost:8765) to see your Jupyter Notebook environment, which got started within the lab directory you cloned. 

## Lab

Go to [graphx-lab.ipynb](graphx-lab.ipynb) to work on the lab.

