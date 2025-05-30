# Tutorial 11 Reflection

## Abhiseka Susanto - 2306244942, Class A

### Reflection on Hello Minikube 1 

When the application has been exposed, the logs display requests coming into the Service. In this case, since the Service is accessed in the browser at the "/" endpoint, what appears in the logs are several GET requests requesting the "/" endpoint. Every time the application is opened in the browser or refreshed, the number of entries in the log also increases. This happens because each time the application is opened, the browser will make a GET request to the service. These requests are what get recorded in the service logs.

### Reflection on Hello Minikube 2

The -n option in the kubectl command allows you to specify which namespace to target. In Kubernetes, namespaces function as logical partitions that isolate resources within a cluster into separate groups. For example, when executing kubectl get pods,services -n kube-system, the command will only show pods and services within the kube-system namespace, which contains system components managed by Kubernetes itself. This explains why user-defined pods and services aren't displayed in this output - they don't belong to the system namespace. When the -n option is omitted, kubectl get defaults to showing only user-created resources in the default namespace.

---

### Reflection on Rolling Update & Kubernetes Manifest File 1

The Recreate deployment strategy terminates all existing pods before launching new ones. By contrast, Rolling Update progressively replaces pods without service interruption, achieving zero downtime deployment. Recreate offers advantages in speed and simplicity of implementation. However, it introduces service downtime and presents higher risks due to the simultaneous replacement of all instances. Rolling Update enhances service availability by eliminating downtime and reduces risk through incremental changes. The tradeoff is that Rolling Update implementations are more complex and require more time to complete compared to the Recreate approach.

### Reflection on Rolling Update & Kubernetes Manifest File 4

Kubernetes manifest files streamline the deployment process when compared to building configurations from scratch. These files allow developers to predefine critical deployment parameters—including replica counts, deployment strategies, and other configurations—before execution. Furthermore, manifest files integrate seamlessly with version control systems like Git, facilitating straightforward updates and rollbacks when needed. This approach ensures deployment consistency across team members, significantly reducing configuration-related errors that might otherwise occur. In essence, manifest-based deployments deliver three key benefits: reproducibility across environments, operational efficiency, and configuration consistency.