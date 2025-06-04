## Install Metrics server
HPA relies on the metrics server to collect pod metrics
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/high-availability-1.21+.yaml
kubectl get all -n kube-system

## Test HPA by increasing load
kubectl run -i --tty load-generator --rm --image=busybox:1.28 --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"

Monitor HPA:
kubectl get hpa --watch

