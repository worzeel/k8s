# Linkerd

https://linkerd.io

## Installation

Installation done using the linkerd CLI

1. First install the CRDS into the cluster
   ```linkerd install -crds|kubectl apply -f -```
2. Next install linkerd itself into the cluster
   ```linkerd install|kubectl apply -f -```
3. Next install linkerd-viz for a nice UI
   ```linkerd install viz|kubectl apply -f -```
   
   Can now do a port forward to the web service within the linkerd-viz namespace to view the UI
   eg: ```kubectl port-forward svc/web 50084:8084 -n linkerd-viz```
