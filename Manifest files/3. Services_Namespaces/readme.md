### Service Type Hierarchy
LoadBalancer:
Creates a LoadBalancer, NodePort, and ClusterIP.

External access via cloud provider’s load balancer.

NodePort:
Creates a NodePort and ClusterIP.

External access via <NodeIP>:<NodePort>.

ClusterIP:
Creates only a ClusterIP.

Internal access within the cluster.

This hierarchy ensures internal routing is always handled by ClusterIP.



### Kubernetes Namespaces
Purpose
Namespaces provide virtual isolation within a Kubernetes cluster.

Resources (pods, services, deployments) are scoped to a namespace.

Default namespaces:
default: Used for resources unless a namespace is specified.

kube-system: For Kubernetes system components.

kube-public, kube-node-lease, etc.
Commands:
List namespaces:
kubectl get ns

Create namespaces:
kubectl create ns lab
kubectl create ns uat

Apply resources to specific namespaces:
kubectl apply -f pod1.yaml -n lab
kubectl apply -f pod1.yaml -n uat

List pods across all namespaces:
kubectl get po --all-namespaces

Notes:
Your applications so far ran in the default namespace.
Namespaces are useful for separating environments (e.g., lab, uat, prod) or teams within the same cluster.


