# Kubernetes-dev

### Contents
- [Kuberntes Dev](#kubernetes-dev)
    - [Getting Started](#getting-started)
    - [Kubernetes APIs](#kubernetes-apis)
    - [Kubernetes Clients](#kubernetes-clients)
    - [Introduction to client-go](#introduction-to-client-go)
    - [Informers](#informers)

## Getting started

Highly recommended read: https://github.com/jamiehannaford/what-happens-when-k8s

## Kubernetes APIs
- K8s Objects (https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/)
  - TypeMeta
  - ObjectMeta
  - Specs & Status
- API Versioning
- API Groups
- Accessing K8s resource with REST API

References:
- https://medium.com/programming-kubernetes/building-stuff-with-the-kubernetes-api-1-cc50a3642 
- https://kubernetes.io/docs/reference/using-api/api-overview/
- https://kubernetes.io/docs/concepts/overview/kubernetes-api/ 

## Kubernetes Clients
- Interacting K8s API Server with client

References:

- https://medium.com/programming-kubernetes/building-stuff-with-the-kubernetes-api-1-cc50a3642 
- https://kubernetes.io/docs/reference/#api-client-libraries
- https://kubernetes.io/docs/reference/using-api/client-libraries/

## Introduction to client-go

### Repositories
- kube client library (https://godoc.org/k8s.io/client-go)

  Contains HTTP client interfaces to call Get/List/Create/Patch/Delete methods on API Server (Client Set)

- API types (https://godoc.org/k8s.io/api)

  Contains Go types (structs) for K8s objects like - pods, services, deployment, etc

- API Machinery (https://godoc.org/k8s.io/apimachinery): 

  Contains helpers and miscellaneous types/methods

### Client Set
Client Set provides an interface to clients for multiple APIGroups and resources
e.g
ClientSet can be created from KUBECONFIG

```
clientset, err := kubernetes.NewForConfig(config)
```

Creating client to access Deployment resource in apps/v1 API Group

```
deploymentsClient := clientset.AppsV1().Deployments(apiv1.NamespaceDefault)
```

See https://github.com/kubernetes/client-go/tree/master/examples/create-update-delete-deployment for a complete example

Exercise:

Write a Go program using client-go to create, update and delete a Statefulset


## Informers
- Shared informers
- Event Handlers
- Work Queues

References:
- https://medium.com/@muhammet.arslan/write-your-own-kubernetes-controller-with-informers-9920e8ab6f84
- https://gianarb.it/blog/kubernetes-shared-informer 
- https://godoc.org/k8s.io/client-go/informers
