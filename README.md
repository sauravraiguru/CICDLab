# Continuous Integration | Continuous Delivery - Workshop Lab
Creating a CI/CD Pipeline for deployment to IBM Cloud Kubernetes Cluster using Continuous Delivery Service.

### Overview

In this lab you will be connecting your Git repository having a sample NodeJs application to a Continuous Integration/Continuous Deployment pipeline using Continuous Delivery service that will deploy to a IBM Cloud Kubernetes Service cluster.

### Setup a Continuous Delivery Service

As a prerequisite we require a Continuous Delivery service on IBM Cloud, to create & run the pipeline
Note: Please check and note the region of your Kubernetes cluster, as we need to create a delivery pipeline

1. Lets go to [IBM Cloud Catalog](https://cloud.ibm.com/catalog) and search for ```Continuous Delivery``` OR directly go to [Continuous Delivery Service](https://cloud.ibm.com/catalog/services/continuous-delivery)
2. Select the region and create the service. Optionally, you can add any tag if required.
![CD](img/cd-create.png)



Note: service creation in the region of your Kubernetes cluster.




### Setup a Container Registry Service

As a prerequisite we require a Continuous Delivery service on IBM Cloud, to create & run the pipeline
Note: Please check and note the region of your Kubernetes cluster, as we need to create

1.  Lets go to [IBM Cloud Catalog](https://cloud.ibm.com/catalog) and search for ```Container Registry``` OR directly go to [Container Registry Service](https://cloud.ibm.com/kubernetes/catalog/registry)

2. Click on Create.
![CR](img/cr-create.png)
Note: Please choose the region on top left, same as your Kubernetes cluster.

3. Let us create a `namespace` for our lab today, which will help us to map our git repositories and container images.
Click on `Namespaces` tab and click on it.
![CR](img/cr-namespace.png)
On the lower right, we will have to click on `Create namespace`. for example `hello`
![CR](img/cr-namespace-create.png)


### Setup our Delivery Pipeline using IBM Toolchain Service.
