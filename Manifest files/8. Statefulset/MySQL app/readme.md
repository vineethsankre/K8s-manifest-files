✅ Practice Steps:
kubectl apply -f storageclass.yaml

kubectl apply -f headless-service.yaml

kubectl apply -f statefulset.yaml

kubectl get pods → observe: mysql-0, mysql-1

kubectl get pvc → observe: data-mysql-0, data-mysql-1

Delete a pod and confirm:

Pod comes back as the same name

PVC is not deleted

Connect to MySQL: kubectl exec -it mysql-0 -- mysql -u root -p