# Tutorial 11 Reflection

## Abhiseka Susanto - 2306244942, Class A

### 1. 

When the application has been exposed, the logs display requests coming into the Service. In this case, since the Service is accessed in the browser at the "/" endpoint, what appears in the logs are several GET requests requesting the "/" endpoint. Every time the application is opened in the browser or refreshed, the number of entries in the log also increases. This happens because each time the application is opened, the browser will make a GET request to the service. These requests are what get recorded in the service logs.

### 2. 

The -n option in the kubectl command allows you to specify which namespace to target. In Kubernetes, namespaces function as logical partitions that isolate resources within a cluster into separate groups. For example, when executing kubectl get pods,services -n kube-system, the command will only show pods and services within the kube-system namespace, which contains system components managed by Kubernetes itself. This explains why user-defined pods and services aren't displayed in this output - they don't belong to the system namespace. When the -n option is omitted, kubectl get defaults to showing only user-created resources in the default namespace.