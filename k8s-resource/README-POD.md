## POD - LABEL - NAMESPACE
### Check list namespace
``
kubectl get ns
``
### Check pod with namespace
``
kubectl get pod --namespace kube-system
``
### Create namespace
``
kubectl create ns testing
``
-------------------------------------------
### Run Pod hello kube config YAML
``
kubectl apply -f pod-hello-kube.yaml
``
-------------------------------------------
### Show list pod with label
``
kubectl get pod --show-labels
``
### Show list pod with label enviroment
``
kubectl get pod -L enviroment
``
### Show and Filter pod by label
``
kubectl get pod -l enviroment=production
``
### Show pod with namespace testing
``
kubectl get pod -n testing
``
-------------------------------------------
### Forward port pod
``
kubectl port-forward pod/hello-kube 3000:3000
``
-------------------------------------------
### Delete pod
``
kubectl delete pod hello-kube
``
### Clear resource
``
kubectl delete -f pod-hello-kube.yaml
``
### Delete pod with namespace
``
kubectl delete pod hello-kube-testing -n testing
``
### Delete namespace with all resource
``
kubectl delete ns testing
``
