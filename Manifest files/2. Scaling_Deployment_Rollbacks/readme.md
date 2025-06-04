### Dry run for YAML Generation
Generate pod YAML without creating it (client-side dry run):
kubectl run pod1 --image=nginx --dry-run=client -o yaml

### Basic Cluster and Resource Commands
eksctl get cluster
Lists all EKS clusters in your AWS account.

kubectl get nodes
Lists all nodes in the Kubernetes cluster.

kubectl delete po --all
Deletes all pods in the current namespace.

kubectl delete rs --all
Deletes all ReplicaSets in the current namespace.

kubectl delete all --all
Deletes all resources (pods, services, deployments, etc.) in the current namespace.

kubectl get all
Lists all resources in the current namespace.

kubectl cluster-info
Shows cluster endpoint and related info.

kubectl cluster-info dump
Dumps detailed cluster info and state.

Exploration and Documentation
kubectl explain pods
Shows documentation about Pod resource.

kubectl explain pods.spec
Explains Pod spec fields.

kubectl explain pods.metadata
Explains Pod metadata fields.

kubectl api-resources
Lists all available Kubernetes API resources.

kubectl api-resources | grep replicaset
Filters API resources for ReplicaSets.

kubectl get po -o wide
Shows pods with additional details (node, IP, etc).

### Node Management
kubectl cordon <node-ip>
Marks a node as unschedulable (no new pods scheduled).

kubectl uncordon <node-ip>
Marks a node as schedulable again.

kubectl drain <node-ip>
Safely evicts pods from the node for maintenance.

kubectl drain <node-ip> --force --ignore-daemonsets
Forces drain ignoring DaemonSets and certain pods.

### Scaling ReplicaSets
kubectl scale rs fb-rs --replicas 2
Scales ReplicaSet fb-rs to 2 replicas.

kubectl describe rs fb-rs
Shows detailed info about the ReplicaSet fb-rs.

Scaling Methods
Edit the manifest file and apply changes manually.

Scale using manifest file:

kubectl scale --replicas=5 -f replicaset.yaml
Scale directly by name:

kubectl scale replicaset fb-rs --replicas=3
Edit ReplicaSet interactively:

kubectl edit replicaset fb-rs
Rollout Management (Deployments)
kubectl rollout resume deploy fb-deploy
Resumes a paused rollout for deployment fb-deploy.

kubectl rollout history deploy fb-deploy
Shows rollout history for deployment fb-deploy.

kubectl describe deploy fb-deploy
Shows detailed info about deployment fb-deploy.