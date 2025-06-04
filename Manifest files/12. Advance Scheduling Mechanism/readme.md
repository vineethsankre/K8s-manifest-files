
nodeName: <nodename> it is simplest way to choose a node 

nodeName: ip-192-168-24-160.ec2.internal

=============================================

node selector:
kubectl label nodes <nodename>  environment=prod
kubectl label nodes ip-192-168-39-84.ec2.internal env=prod


Limitations:
Limited to exact label matches (no complex logic like "OR," "NOT," or ranges).
No support for soft preferences (e.g., prefer a node but fall back to others if unavailable).
Less expressive for advanced scheduling requirements.
Use Case: When you need straightforward, mandatory scheduling on nodes with specific labels.

===============================================


affinity:
  nodeAffinity:
    requiredDuringSchedulingIgnoredDuringExecution:
      nodeSelectorTerms:
      - matchExpressions:
        - key: env
          operator: In
          values:
          - prod
          - staging

=============================
taint:

kubectl taint nodes <node-name> key=value:NoSchedule
kubectl taint nodes <node-name> critical=true:NoSchedule
spec:
  tolerations:
  - key: "critical"
    operator: "Equal"
    value: "true"
    effect: "NoSchedule"

====================================    


kubectl taint nodes ip-192-168-9-253.ec2.internal dedicated=payment:NoSchedule

kubectl taint nodes <node-name> gpu=true:NoSchedule
spec:
  tolerations:
  - key: "gpu"
    operator: "Equal"
    value: "true"
    effect: "NoSchedule"

====================================    