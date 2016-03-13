# Hadoop on OpenShift Demo

The demo is based on the Hadoop images of https://github.com/kiwenlau/hadoop-cluster-docker, many thanks to LIU's hard work.
What I have done is to to add a little bit of tricks to make it works with OpenShift and make it more automative while scaling the cluster.

##Seting up

###Clone the repository
  git clone https://github.com/nichochen/openshift3-demo-hadoop

###Bulid the Docker image
  cd openshift3-demo-hadoop/nic-hadoop-master/
  make
  
###Create templates in OpenShift
  cd openshift3-demo-hadoop/nic-hadoop-master/openshift
  oc create -f hadoop-master.json -n openshift
  oc create -f hadoop-slave.json -n openshift

Now you are all set, just process to create your own Hadoop cluster with the web console or command line tool oc.

Enjoy~

Thanks,
Nicholas
