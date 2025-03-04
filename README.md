# 3.9-Monitor-Container

aws eks update-kubeconfig --name shared-eks-cluster --region ap-southeast-1

kubectl get namespaces

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm upgrade --install room3-prom prometheus-community/prometheus --version 27.5.1 --values prometheus-values.yaml --create-namespace --namespace room3-prom

kubectl get pods -n room3-prom
kubectl get svc -n room3--prom

http://room3-prom.sctp-sandbox.com/query
http://room3-prom-prometheus-server.room3-prom:80


Login to the grafana instance on with the following credentials
Username: admin
Password: prom-operator
admin-grafana.sctp-sandbox.com
