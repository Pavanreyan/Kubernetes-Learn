# Kubernetes-Learn
What is Kubernetes and there components ?

Kubernetes, often abbreviated as K8s, is an open-source platform designed to automate deploying, scaling, and managing containerized applications. It abstracts away the underlying infrastructure and provides a framework for automating the deployment, scaling, and management of containerized applications.

The key components of Kubernetes include:

1. Master Node:

--> API Server: Acts as the front-end for Kubernetes. It's responsible for handling API requests, validating them, and executing them. Essentially, it's the entry point for all administrative tasks.

--> Scheduler: Assigns nodes for newly created pods (a group of one or more containers), based on resource requirements and other constraints.

--> Controller Manager: Enforces cluster state, constantly monitoring the cluster through the API server. It includes various controllers responsible for replication, endpoints, namespaces, and more.

--> etcd: A distributed key-value store that stores the cluster's configuration data, representing the single source of truth for the cluster.

2. Node (Minion):

--> Kubelet: An agent that runs on each node and is responsible for communicating with the Kubernetes master and managing the node's containers, ensuring they are running in a healthy state.

--> Container Runtime: The software responsible for running containers. Docker is the most common container runtime used with Kubernetes, but others like containerd, CRI-O, and rkt are also supported.

--> Kube Proxy: Maintains network rules on nodes, allowing network communication to your pods from network sessions inside or outside of your cluster.

3. Add-Ons:

--> DNS Service: Provides DNS-based service discovery for Kubernetes services.

--> Dashboard: A web-based user interface for Kubernetes clusters, allowing users to manage applications and resources visually.

--> Ingress Controller: Manages external access to services within a Kubernetes cluster, typically through HTTP/HTTPS routing.

--> Monitoring and Logging: Tools like Prometheus for monitoring and Fluentd/EFK (Elasticsearch, Fluentd, Kibana) or Loki for logging can be integrated to monitor the health and performance of the cluster and applications running on it.

4. Networking:

--> Pod Networking: Kubernetes requires a networking solution to enable communication between pods across nodes. Various networking plugins, like Calico, Flannel, Weave, Cilium, etc., provide networking capabilities to Kubernetes clusters.

--> Service Networking: Kubernetes Services abstract away the details of how pods are implemented, and the Kubernetes Service constructs expose a consistent networking interface to the consuming pods.

These components work together to provide a scalable, resilient platform for deploying and managing containerized applications in production environments.

Here's a simplified diagram illustrating the architecture of Kubernetes with master and worker nodes:

<p align="center">
  <img src="https://github.com/Pavanreyan/Kubernetes-Learn/assets/55541931/06a693c5-09f6-4242-b8b3-cea492f29870" width="350" title="Kubernetes Architecture">
</p>
