# Overview of Openshift resources used in the workshops

## The big picture

![Overview of Openshit resources](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/ciber-openshift-workshop/doc/master/openshift-resources.puml)

## Resources

### Project
An Openshift _project_ is essentially a Kubernetes namespace, wtih security policies added. This is where you group together related resources, e.g. an application, and grants other people accees when needed. 

### DeploymentConfiguration
Describes how to deploy something to Openshift, such as definition of a ReplicationController, triggers for deployment, deployment strategy and life cycle hooks.

### ReplicationController
Controls that the desired number of pod replicas are up to date (low leve, has no concepts of scaling, although it effectuates config changes).

### Pod
The smallest compute unit in a Kubernetes cluster. Consists of one or more containers, which are instantiated from Docker images.
Containers in the same pod, share storage and networking on the same host.

## Container
Run-time instantiation of a Docker image, with configuration.

## Service
Internal load-balancer in front of pods. Pods are selected in the configuration through labels.

## Route
External load-balancer in front of services. Openshift allocates an externally accessible DNS name for the route, so we can 
invoke a service from the outside of an Openshift cluster.



