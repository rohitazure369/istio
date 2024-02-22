# istio

git clone..

cd istio


## Create instio Gateway
kubectl apply -f gateway.yaml


## List Gateways

kubectl get gateways -n istio-system


 ## create Virtual service in Dev Namespace.

 kubectl apply -f virtual-service.yaml -n dev

 # get virtual service details
 kubectl get vs -n dev

 
