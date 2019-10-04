## Development in Kubernetes

**Highly recommended read:** https://github.com/jamiehannaford/what-happens-when-k8s

### Concepts

#### Kubernetes APIs

- K8s Objects (https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/)
- API Versioning
- API Groups
- Accessing K8s resource with REST API

References:
- https://kubernetes.io/docs/reference/using-api/api-overview/
- https://kubernetes.io/docs/concepts/overview/kubernetes-api/ 

#### Kubernetes Clients

There are several SDKs available for interacting with K8s API Service.

https://kubernetes.io/docs/reference/#api-client-libraries

https://kubernetes.io/docs/reference/using-api/client-libraries/

#### Controllers

- ReplicaSet and Deployments

References:
- https://engineering.bitnami.com/articles/a-deep-dive-into-kubernetes-controllers.html
- https://kubernetes.io/docs/concepts/architecture/controller 

#### Custom Resources

- Custom resources
- Custom controllers (for custom resources)
- Adding custom resources

References:
- https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources
