
# Install Istio....

helm repo add istio https://istio-release.storage.googleapis.com/charts

helm repo update
#
helm install istio-base istio/base -n istio-system --create-namespace

#
helm install istiod istio/istiod -n istio-system 
#
helm install istio-ingress istio/gateway -n istio-system  --create-namespace



#Enable ISTIO Sidecar using below command to inject and enable ISTIO for namespace

kubectl label namespace dev istio-injection=enabled

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

 
