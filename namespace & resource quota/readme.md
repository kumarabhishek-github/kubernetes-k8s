Namespaces:
Namespaces in Kubernetes are a way to organize cluster resources. They provide a scope for Kubernetes objects, such as pods, services, and replica sets. Namespaces are useful for different teams or projects within an organization to share a cluster without interfering with each other. They help in dividing cluster resources between multiple users or teams.

Example:
Suppose you have a Kubernetes cluster where you're running applications for different departments: marketing, sales, and engineering. You can create separate namespaces for each department. This way, resources for the marketing team's applications won't interfere with resources for the sales or engineering teams.


Resource Quotas:
Resource Quotas in k8s are used to limit the amount of compute resources that can be consumed within a namespace. They help in preventing resource exhaustion and ensure fair usage of cluster resources among different namespaces.

Resource Quotas can be defined for CPU, memory, and other resources like pods, services, persistent volume claims, etc.

Example:
when you want to limit the amount of CPU and memory that can be consumed in the marketing namespace to avoid one department monopolizing resources.


***
 kubectl config set-context $(kubectl config current-context) --namespace=dev:- to set  the namespace to dev
 
  kubectl config view | grep namespace:- to view namespace
***